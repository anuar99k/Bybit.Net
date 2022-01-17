---
title: IBybitClientInversePerpetualApiTrading
has_children: false
parent: IBybitClientInversePerpetualApi
grand_parent: IBybitClient
---
*[generated documentation]*  
`BybitClient > InversePerpetualApi > Trading`  
*Bybit trading endpoints, placing and mananging orders.*
  

***

## CancelAllConditionalOrdersAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-cancelallcond](https://bybit-exchange.github.io/docs/inverse/#t-cancelallcond)  
<p>

```C#  
Task<WebCallResult<IEnumerable<BybitCanceledConditionalOrder>>> CancelAllConditionalOrdersAsync(string symbol, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Cancel all active conditional orders for a symbol*  

</p>

***

## CancelAllOrdersAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-cancelallactive](https://bybit-exchange.github.io/docs/inverse/#t-cancelallactive)  
<p>

```C#  
Task<WebCallResult<IEnumerable<BybitCanceledOrder>>> CancelAllOrdersAsync(string symbol, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Cancel all active orders for a symbol*  

</p>

***

## CancelConditionalOrderAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-cancelcond](https://bybit-exchange.github.io/docs/inverse/#t-cancelcond)  
<p>

```C#  
Task<WebCallResult<BybitStopOrderId>> CancelConditionalOrderAsync(string symbol, [Optional] string? stopOrderId, [Optional] string? clientOrderId, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`stopOrderId`|The id of the conditional order to cancel|
|`clientOrderId`|The client order id of the conditional order to cancel|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Cancel a conditional order, either stopOrderId or clientOrderId should be provided*  

</p>

***

## CancelOrderAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-cancelactive](https://bybit-exchange.github.io/docs/inverse/#t-cancelactive)  
<p>

```C#  
Task<WebCallResult<BybitOrder>> CancelOrderAsync(string symbol, [Optional] string? orderId, [Optional] string? clientOrderId, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`orderId`|The id of the order to cancel|
|`clientOrderId`|The client order id of the conditional order to cancel|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Cancel an order, either orderId or clientOrderId should be provided*  

</p>

***

## GetConditionalOrdersAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-getcond](https://bybit-exchange.github.io/docs/inverse/#t-getcond)  
<p>

```C#  
Task<WebCallResult<BybitCursorPage<IEnumerable<BybitConditionalOrder>>>> GetConditionalOrdersAsync(string symbol, [Optional] StopOrderStatus? status, [Optional] SearchDirection? direction, [Optional] int? limit, [Optional] string? cursor, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`status`|Filter by status|
|`direction`|Filter by direction|
|`limit`|Max number of results|
|`cursor`|Page cursor|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Get a list of conditional orders*  

</p>

***

## GetOpenConditionalOrderRealTimeAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-querycond](https://bybit-exchange.github.io/docs/inverse/#t-querycond)  
<p>

```C#  
Task<WebCallResult<BybitConditionalOrder>> GetOpenConditionalOrderRealTimeAsync(string symbol, [Optional] string? stopOrderId, [Optional] string? clientOrderId, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`stopOrderId`|The order id|
|`clientOrderId`|The client order id|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Get conditional order information. Either stopOrderId or clientOrderId should be provided*  

</p>

***

## GetOpenConditionalOrdersRealTimeAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-querycond](https://bybit-exchange.github.io/docs/inverse/#t-querycond)  
<p>

```C#  
Task<WebCallResult<IEnumerable<BybitConditionalOrder>>> GetOpenConditionalOrdersRealTimeAsync(string symbol, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Get order information for up to 10 conditional orders*  

</p>

***

## GetOpenOrderRealTimeAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-queryactive](https://bybit-exchange.github.io/docs/inverse/#t-queryactive)  
<p>

```C#  
Task<WebCallResult<BybitOrder>> GetOpenOrderRealTimeAsync(string symbol, [Optional] string? orderId, [Optional] string? clientOrderId, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`orderId`||
|`clientOrderId`||
|`receiveWindow`||
|`ct`||

*Get order information. Either orderId or clientOrderId should be provided*  

</p>

***

## GetOpenOrdersRealTimeAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-queryactive](https://bybit-exchange.github.io/docs/inverse/#t-queryactive)  
<p>

```C#  
Task<WebCallResult<IEnumerable<BybitOrder>>> GetOpenOrdersRealTimeAsync(string symbol, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Get order information for up to 500 orders*  

</p>

***

## GetOrdersAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-getactive](https://bybit-exchange.github.io/docs/inverse/#t-getactive)  
<p>

```C#  
Task<WebCallResult<BybitCursorPage<IEnumerable<BybitOrder>>>> GetOrdersAsync(string symbol, [Optional] OrderStatus? status, [Optional] SearchDirection? direction, [Optional] int? limit, [Optional] string? cursor, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`status`|Filter by status|
|`direction`|Filter by direction|
|`limit`|Max amount of results|
|`cursor`|Page cursor|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Get orders*  

</p>

***

## GetUserTradesAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-usertraderecords](https://bybit-exchange.github.io/docs/inverse/#t-usertraderecords)  
<p>

```C#  
Task<WebCallResult<IEnumerable<BybitUserTrade>>> GetUserTradesAsync(string symbol, [Optional] string? orderId, [Optional] DateTime? startTime, [Optional] int? page, [Optional] int? pageSize, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`orderId`|Filter by order id|
|`startTime`|Filter by start time|
|`page`|Page|
|`pageSize`|Page size|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Get executed user trades*  

</p>

***

## ModifyConditionalOrderAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-replacecond](https://bybit-exchange.github.io/docs/inverse/#t-replacecond)  
<p>

```C#  
Task<WebCallResult<BybitStopOrderId>> ModifyConditionalOrderAsync(string symbol, [Optional] string? stopOrderId, [Optional] string? clientOrderId, [Optional] decimal? newPrice, [Optional] decimal? newTriggerPrice, [Optional] decimal? newQuantity, [Optional] decimal? takeProfitPrice, [Optional] decimal? stopLossPrice, [Optional] TriggerType? takeProfitTriggerType, [Optional] TriggerType? stopLossTriggerType, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`stopOrderId`|Stop order id|
|`clientOrderId`|Client order id|
|`newPrice`|New price to set|
|`newTriggerPrice`|New trigger price to set|
|`newQuantity`|New quantity to set|
|`takeProfitPrice`|New take profit price|
|`stopLossPrice`|New stop loss price|
|`takeProfitTriggerType`|New take profit trigger type|
|`stopLossTriggerType`|New stop loss profit price|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Change an exising order. Either stopOrderId or clientOrderId should be provided*  

</p>

***

## ModifyOrderAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-replaceactive](https://bybit-exchange.github.io/docs/inverse/#t-replaceactive)  
<p>

```C#  
Task<WebCallResult<BybitOrderId>> ModifyOrderAsync(string symbol, [Optional] string? orderId, [Optional] string? clientOrderId, [Optional] decimal? newPrice, [Optional] decimal? newQuantity, [Optional] decimal? takeProfitPrice, [Optional] decimal? stopLossPrice, [Optional] TriggerType? takeProfitTriggerType, [Optional] TriggerType? stopLossTriggerType, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`orderId`|Stop order id|
|`clientOrderId`|Client order id|
|`newPrice`|New price to set|
|`newQuantity`|New quantity to set|
|`takeProfitPrice`|New take profit price|
|`stopLossPrice`|New stop loss price|
|`takeProfitTriggerType`|New take profit trigger type|
|`stopLossTriggerType`|New stop loss profit price|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Change an exising order. Either orderId or clientOrderId should be provided*  

</p>

***

## PlaceConditionalOrderAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-placecond](https://bybit-exchange.github.io/docs/inverse/#t-placecond)  
<p>

```C#  
Task<WebCallResult<BybitConditionalOrder>> PlaceConditionalOrderAsync(string symbol, OrderSide side, OrderType type, PositionMode positionMode, decimal quantity, decimal basePrice, decimal triggerPrice, TimeInForce timeInForce, [Optional] decimal? price, [Optional] TriggerType? triggerType, [Optional] bool? closeOnTrigger, [Optional] string? clientOrderId, [Optional] decimal? takeProfitPrice, [Optional] decimal? stopLossPrice, [Optional] TriggerType? takeProfitTriggerType, [Optional] TriggerType? stopLossTriggerType, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`side`|Order side|
|`type`|Order type|
|`positionMode`|Position mode|
|`quantity`|Quantity|
|`basePrice`|It will be used to compare with the value of trigger price, to decide whether your conditional order will be triggered by crossing trigger price from upper side or lower side. Mainly used to identify the expected direction of the current conditional order.|
|`triggerPrice`|Trigger price|
|`timeInForce`|Time in force|
|`price`|Price|
|`triggerType`|Trigger type|
|`closeOnTrigger`|For a closing order. It can only reduce your position, not increase it. If the account has insufficient available balance when the closing order is triggered, then other active orders of similar contracts will be cancelled or reduced. It can be used to ensure your stop loss reduces your position regardless of current available margin.|
|`clientOrderId`|Client order id|
|`takeProfitPrice`|Take profit price, only take effect upon opening the position|
|`stopLossPrice`|Stop loss price, only take effect upon opening the position|
|`takeProfitTriggerType`|Take profit trigger price type, default: LastPrice|
|`stopLossTriggerType`|Stop loss trigger price type, default: LastPrice|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Place a new conditional order*  

</p>

***

## PlaceOrderAsync  

[https://bybit-exchange.github.io/docs/inverse/#t-placeactive](https://bybit-exchange.github.io/docs/inverse/#t-placeactive)  
<p>

```C#  
Task<WebCallResult<BybitOrder>> PlaceOrderAsync(string symbol, OrderSide side, OrderType type, decimal quantity, TimeInForce timeInForce, [Optional] decimal? price, [Optional] bool? closeOnTrigger, [Optional] string? clientOrderId, [Optional] decimal? takeProfitPrice, [Optional] decimal? stopLossPrice, [Optional] TriggerType? takeProfitTriggerType, [Optional] TriggerType? stopLossTriggerType, [Optional] bool? reduceOnly, [Optional] long? receiveWindow, [Optional] CancellationToken ct);  
```  

|Parameter|Description|
|---|---|
|`symbol`|The symbol|
|`side`|Order side|
|`type`|Order type|
|`quantity`|Quantity|
|`timeInForce`|Time in force|
|`price`|Price|
|`closeOnTrigger`|For a closing order. It can only reduce your position, not increase it. If the account has insufficient available balance when the closing order is triggered, then other active orders of similar contracts will be cancelled or reduced. It can be used to ensure your stop loss reduces your position regardless of current available margin.|
|`clientOrderId`|Client order id|
|`takeProfitPrice`|Take profit price, only take effect upon opening the position|
|`stopLossPrice`|Stop loss price, only take effect upon opening the position|
|`takeProfitTriggerType`|Take profit trigger price type, default: LastPrice|
|`stopLossTriggerType`|Stop loss trigger price type, default: LastPrice|
|`reduceOnly`|True means your position can only reduce in size if this order is triggered|
|`receiveWindow`|The receive window for which this request is active. When the request takes longer than this to complete the server will reject the request|
|`ct`|Cancellation token|

*Place a new order*  

</p>