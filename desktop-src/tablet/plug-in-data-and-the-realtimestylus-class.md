---
description: RealTimeStylus 類別的外掛程式必須執行 IStylusSyncPlugin 或 IStylusAsyncPlugin 介面，或兩者都是。
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: 外掛程式資料和 RealTimeStylus 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0540d90f291acfef27a09df08ffff645c280d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480964"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>外掛程式資料和 RealTimeStylus 類別

[**RealTimeStylus**](realtimestylus-class.md)類別的外掛程式必須執行 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)或 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)介面，或兩者都是。 當您必須執行所有外掛程式介面方法時，您的外掛程式只會在 [StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) 或 [StylusInput. IStylusAsyncPlugin](/previous-versions/ms574886(v=vs.100)) 屬性中標示的方法上接收呼叫。

在介面上定義的方法會使用 [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) 命名空間中的物件，將畫筆資料傳遞給外掛程式。下表描述的是通知方法中的參數資料物件，並列出與通知相關聯的 [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) 值。



| 外掛程式資料                                                                                          | DataInterestMask 值     | Description                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomStylusData](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | 外掛程式新增的自訂應用程式資料。<br/>                                                                                                                                                                                                 |
| [ErrorData](/previous-versions/ms824740(v=msdn.10))                                   | **錯誤**                  | [**RealTimeStylus**](realtimestylus-class.md)物件為了回應其中一個外掛程式的未處理例外狀況而加入的錯誤資訊。<br/>                                                                                          |
| [InAirPacketsData](/previous-versions/ms824592(v=msdn.10))                     | **InAirPackets**           | 手寫筆在數位板上的空氣上方時，手寫筆動作的封包資訊。<br/>                                                                                                                                                         |
| [PacketsData](/previous-versions/ms824590(v=msdn.10))                               | **封包**                | 手寫筆接觸數位板時，手寫筆動作的封包資訊。<br/>                                                                                                                                                             |
| [RealTimeStylusDisabledData](/previous-versions/ms824576(v=msdn.10)) | **RealTimeStylusDisabled** | 在停用 [**RealTimeStylus**](realtimestylus-class.md) 物件時所加入的資訊。<br/>                                                                                                                                        |
| [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | [**RealTimeStylus**](realtimestylus-class.md)物件在啟用時所加入的資訊。<br/>                                                                                                                                         |
| [StylusButtonDownData](/previous-versions/ms824181(v=msdn.10))             | **StylusButtonDown**       | 所按下之特定手寫筆按鈕的相關資訊。<br/>                                                                                                                                                                        |
| [StylusButtonUpData](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | 即將發行的特定手寫筆按鈕的相關資訊。<br/>                                                                                                                                                                       |
| [StylusDownData](/previous-versions/ms585582(v=vs.100))                                   | **StylusDown**             | 手寫筆的封包資訊會與數位板一起聯繫。<br/>                                                                                                                                                      |
| [StylusInRangeData](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | 輸入 [ [**realtimestylus**](realtimestylus-class.md) ] 物件輸入區域，或在 [ **realtimestylus** ] 物件的輸入區域上方輸入數位板偵測範圍之特定手寫筆的相關資訊。<br/> |
| [StylusOutOfRangeData](/previous-versions/ms824072(v=msdn.10))             | **StylusOutOfRange**       | 關於離開 [**realtimestylus**](realtimestylus-class.md) 物件輸入區域，或將數位板的偵測範圍保留在 [ **realtimestylus** ] 物件的輸入區域上方之特定手寫筆的資訊。<br/>   |
| [StylusUpData](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | 手寫筆的封包資訊是從數位板提起手寫筆。<br/>                                                                                                                                                                  |
| [SystemGestureData](/previous-versions/ms824019(v=msdn.10))                   | **SystemGesture**          | 當 [**RealTimeStylus**](realtimestylus-class.md) 物件偵測到系統手勢時，所新增的資訊。<br/>                                                                                                                                 |
| [TabletAddedData](/previous-versions/ms824010(v=msdn.10))                       | **TabletAdded**            | 正在加入的 [平板](/previous-versions/ms827783(v=msdn.10)) 電腦物件的相關資訊。<br/>                                                                                                                                                |
| [TabletRemovedData](/previous-versions/ms823997(v=msdn.10))                   | **TabletRemoved**          | 正在移除的 [平板](/previous-versions/ms827783(v=msdn.10)) 電腦物件的相關資訊。<br/>                                                                                                                                              |



 

如需有關 [**realtimestylus**](realtimestylus-class.md) 物件如何處理 tablet pen 資料流程的詳細資訊，請參閱使用 [realtimestylus 類別](working-with-the-realtimestylus-class.md)。

## <a name="data-interest"></a>資料興趣

當外掛程式加入至 **RealTimeStylus** 物件的同步或非同步外掛程式集合時， [**realtimestylus**](realtimestylus-class.md)物件會檢查外掛程式的 [StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100))或 [StylusInput. IStylusAsyncPlugin](/previous-versions/ms574886(v=vs.100))屬性，以供使用。 因此，您應該使用 DataInterest 屬性來訂閱這個外掛程式的實例所使用的所有通知，但不常使用，但不會使用此外掛程式的任何通知。 對於外掛程式只會使用的通知，偶爾會在通知方法中檢查外掛程式的狀態，並在您的外掛程式未在其目前的狀態中使用通知時傳回。

外掛程式只會收到外掛程式的 [StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) 或 [StylusInput. IStylusAsyncPlugin](/previous-versions/ms574886(v=vs.100)) 屬性中所標示之方法的呼叫。 如需外掛程式的 **DataInterest** 屬性可能值的詳細資訊，請參閱 [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) 列舉。

## <a name="timing"></a>計時

在將資料傳遞至非同步外掛程式集合中的外掛程式之前，資料會排入 [**RealTimeStylus**](realtimestylus-class.md) 物件中。 下列清單描述當您設計非同步外掛程式時，可能需要考慮的某些情況。

-   當已停用 [**RealTimeStylus**](realtimestylus-class.md) 物件時，非同步外掛程式可能會在呼叫 [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) 方法之前，接收其他已排入佇列的通知。 在這種情況下，從外掛程式對某些 **RealTimeStylus** 物件的方法和屬性進行的呼叫會擲回例外狀況。 當啟用 **RealTimeStylus** 物件時，應該快取與外掛程式相關的資訊。
-   [**RealTimeStylus**](realtimestylus-class.md)物件的 [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10))方法可能會從輸出佇列中移除資訊。 因此，非同步外掛程式無法依賴接收所有相關的通知。
-   當已移除可用於 [**RealTimeStylus**](realtimestylus-class.md)物件的 [平板](/previous-versions/ms827783(v=msdn.10))電腦物件時，非同步外掛程式可能會在呼叫 [TabletRemoved](/previous-versions/bb361092(v=vs.100))方法之前，收到 tablet 的佇列手寫筆通知。 在這種情況下，呼叫 **RealTimeStylus** 物件的 [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) 方法無法運作。 當啟用 **RealTimeStylus** 物件或加入新的平板電腦時，應該快取與外掛程式相關的資訊。

視您的應用程式而定，您可以在停用 [**RealTimeStylus**](realtimestylus-class.md) 物件時改善效能。 當 [ **RealTimeStylus** ] 物件的 [ [已啟用](/previous-versions/ms824832(v=msdn.10)) ] 屬性設定為 [ **FALSE**] 時，會處理輸入和輸出佇列上的資料，直到佇列空白為止。 您可以呼叫 **realtimestylus** 物件的 [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) 方法，在停用 **realtimestylus** 物件之前清除佇列。

## <a name="enabled-and-disabled-data"></a>啟用和停用的資料

啟用 [**RealTimeStylus**](realtimestylus-class.md) 物件之後，每個外掛程式都會收到對其 [StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) 或 [StylusInput. IStylusAsyncPlugin](/previous-versions/ms824775(v=msdn.10)) 方法的呼叫。 在通知中傳遞的 **RealTimeStylusEnabledData** 物件，會在啟用 **RealTimeStylus** 物件時，包含可用的平板電腦內容識別碼的集合。

> [!Note]  
> 因為 [**realtimestylus**](realtimestylus-class.md) 物件之非同步外掛程式集合的外掛程式資料已排入佇列，所以非同步外掛程式可能會在接收其 [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) 方法的呼叫之前接收資料，但在停用 **RealTimeStylus** 物件之後。 請注意，如果已停用 **realtimestylus** 物件，某些 **realtimestylus** 物件的方法和屬性會擲回例外狀況。

 

[**Realtimestylus**](realtimestylus-class.md)物件會在已啟用 **realtimestylus** 物件的執行緒上，或從中加入同步外掛程式的執行緒上，呼叫 [StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10))和 [StylusInput. IStylusSyncPlugin](/previous-versions/ms824757(v=msdn.10))方法。

一般而言，在停用 [**RealTimeStylus**](realtimestylus-class.md) 物件時新增或移除外掛程式。 如需有關新增和移除 **realtimestylus** 物件之外掛程式的詳細資訊，請參閱 [外掛程式和 realtimestylus 類別](plug-ins-and-the-realtimestylus-class.md)。

## <a name="tablet-data"></a>平板電腦資料

當您在啟用 **realtimestylus** 物件時，將 [**realtimestylus**](realtimestylus-class.md)物件可使用的平板電腦加入或移除 Tablet PC 時， **realtimestylus** 物件會通知其外掛程式已新增或移除 [tablet](/previous-versions/ms827783(v=msdn.10))物件。 每個 **RealTimeStylus** 物件都會維護可與其互動之 Tablet 物件的唯一識別碼清單。 **RealTimeStylus** 物件有兩種方法可以在唯一識別碼和平板電腦物件之間轉譯，也就是 [GetTabletCoNtextIdFromTablet](/previous-versions/ms825922(v=msdn.10))和 [GetTabletFromTabletCoNtextId](/previous-versions/ms825929(v=msdn.10))方法。

> [!Note]  
> 從 Tablet PC 移除平板電腦之後，將無法再從 [ [**RealTimeStylus**](realtimestylus-class.md) ] 物件使用 tablet 的相關資訊。

 

## <a name="tablet-pen-data"></a>Tablet 畫筆資料

在許多通知方法中， [**RealTimeStylus**](realtimestylus-class.md) 物件會將 tablet 畫筆的相關資訊傳遞到其外掛程式。 Tablet 畫筆的相關資訊會以 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件表示。 此物件是收集資料時 tablet 畫筆狀態的快照。 由於外掛程式會接收 tablet 畫筆資料作為 tablet 畫筆資料流程的一部分，因此外掛程式應使用手寫筆物件中的資訊，而不是透過 [Cursor](/previous-versions/ms839521(v=msdn.10)) 類別檢查特定 tablet 畫筆的目前狀態。

每個 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件都包含產生資料之平板電腦的 tablet 內容識別碼。

## <a name="system-gesture-data"></a>系統手勢資料

當 [**您在 TABLET**](realtimestylus-class.md) PC 辨識出系統手勢時，該物件會收到其相關資料。 下表描述在 tablet 畫筆資料串流中，與其他 tablet 畫筆資料相關的 [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) 物件發生順序。




| <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesture</a> | <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a>物件之前的物件 | 位於 <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> 物件之後的物件 | 
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <strong>點選</strong> | <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a>物件。<br /> | [StylusUpData](/previous-versions/ms824057(v=msdn.10))物件。<br /> | 
| <strong>DoubleTap</strong> | <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a>物件，用來點<strong>一下系統手勢</strong>和[StylusUpData](/previous-versions/ms824057(v=msdn.10))物件的<a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a>物件。<br /> | 第二個 <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> 物件。<br /> | 
| <strong>RightTap</strong> | <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesure</a>列舉之<strong>HoldEnter</strong>成員的<a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a>物件和<a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a>物件。<br /> | [StylusUpData](/previous-versions/ms824057(v=msdn.10))物件。<br /> | 
| <strong>拖曳</strong> | <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a>物件。<br /> | [StylusUpData](/previous-versions/ms824057(v=msdn.10))物件。<br /> | 
| <strong>RightDrag</strong> | <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a>物件。<br /> | [StylusUpData](/previous-versions/ms824057(v=msdn.10))物件。<br /> | 
| <strong>HoldEnter</strong> | <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a>物件。<br /> | [StylusUpData](/previous-versions/ms824057(v=msdn.10))物件。<br /><blockquote>[!Note]<br />如果使用者開始 <strong>拖曳</strong> 或 <strong>RightDrag</strong> 系統手勢，則無法辨識此系統手勢。</blockquote><br /> | 
| <strong>HoldLeave</strong> | 未實作。<br /> | 未實作。<br /> | 
| <strong>HoverEnter</strong> | 數個低平均速度的 <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> 物件。<br /> | <blockquote>[!Note]<br />在接收 <strong>HoverEnter</strong> 系統手勢之前，可能會有明顯的延遲。 如果已將<strong>realtimestylus</strong>物件附加至視窗或控制項，而該視窗或控制項在系統手勢時直接位於畫筆下，則<a href="realtimestylus-class.md"><strong>realtimestylus</strong></a>物件只會收到此資料。</blockquote><br /> | 
| <strong>HoverLeave</strong> | 適用于<strong>HoverEnter</strong>系統手勢的<a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a>物件，以及數個具有足夠平均速度的<a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a>物件。<br /> | <blockquote>[!Note]<br />在接收 <strong>HoverLeave</strong> 系統手勢之前，可能會有明顯的延遲。 如果已將<strong>realtimestylus</strong>物件附加至視窗或控制項，而該視窗或控制項在系統手勢時直接位於畫筆下，則<a href="realtimestylus-class.md"><strong>realtimestylus</strong></a>物件只會收到此資料。</blockquote><br /> | 




 

## <a name="custom-stylus-data"></a>自訂手寫筆資料

您可以藉由呼叫 [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10))方法，將自訂手寫筆資料新增至 [**RealTimeStylus**](realtimestylus-class.md)物件。 您可以在下列三個位置之一，將自訂手寫筆資料新增至 **RealTimeStylus** 物件的佇列。

-   當 *queue* 參數設定為 **Output** 時，自訂資料會在同步外掛程式集合目前處理的資料之後，加入至 [**RealTimeStylus**](realtimestylus-class.md) 物件的輸出佇列。
-   當 *queue* 參數設定為 **OutputImmediate** 時，自訂資料會先加入至 [**RealTimeStylus**](realtimestylus-class.md) 物件的輸出佇列，然後再由同步外掛程式集合處理目前的資料。
-   當 *queue* 參數設定為 **輸入** 時，自訂資料會新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件的輸入佇列，並在 tablet 畫筆的資料流程中的新資料之前，傳送至同步的外掛程式集合。

在上述每一種情況下，在同步外掛程式集合中後續外掛程式加入的資料，都會加入至上述外掛程式加入的資料之後。

> [!Note]  
> 如果從同步外掛程式呼叫 [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) 方法，以回應其中一個 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 方法的呼叫，則會以可預測的方式將自訂手寫筆資料新增至 tablet pen 資料流程;否則，它會與 [**RealTimeStylus**](realtimestylus-class.md) 物件正在處理的目前畫筆資料相關聯，而不是與非同步外掛程式正在處理的資料相對應。 如果已停用 **RealTimeStylus** 物件，AddCustomStylusDataToQueue 方法會擲回例外狀況。

 

自訂手寫筆資料會以 [CustomStylusData](/previous-versions/ms824747(v=msdn.10)) 物件的形式加入至佇列，而外掛程式會透過其 [StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) 或 StylusInput. IStylusAsyncPlugin [方法接收](/previous-versions/ms824770(v=msdn.10)) 這項資料。

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))和 [**GestureRecognizer**](gesturerecognizer-class.md)物件可能會將自訂手寫筆資料新增至佇列。 如需 **DynamicRenderer** 和 **GestureRecognizer** 物件的詳細資訊，請參閱動態轉譯器 [外掛程式](dynamic-renderer-plug-ins.md) 和辨識 [器外掛程式](recognizer-plug-ins.md)。

[**RealTimeStylus**](realtimestylus-class.md)物件會在接收其 [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10))方法呼叫的執行緒上呼叫 [StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10))方法。

下圖說明如何將自訂手寫筆資料新增至輸出佇列，並將 *queue* 參數設定為 **output**。

![顯示自訂手寫筆資料流程至輸出佇列的圖例 ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

在此圖中，圓形 "A" 和 "B" 代表已新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件輸出佇列且尚未傳送至非同步外掛程式集合的 tablet 畫筆資料。 以字母 "C" 表示 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。 它會傳送至同步的外掛程式集合，並放在輸出佇列中。 編號為 "1"、"2" 和 "3" 的圓形代表自訂手寫筆資料，分別由第一個、第二個和第三個同步外掛程式新增至輸出佇列，以回應 "C" 所代表的 tablet 畫筆資料。 外掛程式已新增將 *queue* 參數設定為 **StylusQueues** 的自訂手寫筆資料。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。

下圖說明如何將自訂手寫筆資料新增至輸出佇列，並將 *queue* 參數設定為 **OutputImmediate**。

![顯示輸出佇列之自訂手寫筆資料流程的圖表。](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

在此圖中，圓形 "A" 和 "B" 代表已新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件輸出佇列且尚未傳送至非同步外掛程式集合的 tablet 畫筆資料。 以字母 "C" 表示 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。 它會傳送至同步的外掛程式集合，並放在輸出佇列中。 編號為 "1"、"2" 和 "3" 的圓形代表自訂手寫筆資料，分別由第一個、第二個和第三個同步外掛程式新增至輸出佇列，以回應 "C" 所代表的 tablet 畫筆資料。 外掛程式已新增將 *queue* 參數設定為 **OutputImmediate** 的自訂手寫筆資料。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。

下圖說明如何將自訂手寫筆資料新增至輸入佇列。

![顯示自訂手寫筆資料流程至輸出佇列的圖例](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

在此圖中，圓形 "A" 和 "B" 代表已新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件輸出佇列且尚未傳送至非同步外掛程式集合的 tablet 畫筆資料。 以字母 "C" 表示 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。 它會傳送至同步的外掛程式集合，並放在輸出佇列中。 編號為 "1"、"2" 和 "3" 的圓形代表自訂手寫筆資料，分別由第一個、第二個和第三個同步外掛程式新增至輸入佇列，以回應 "C" 所代表的 tablet 畫筆資料。 外掛程式已新增將 *queue* 參數設定為 **輸入** 的自訂手寫筆資料。 接著會將自訂手寫筆資料（編號為 "1"）傳遞至同步的外掛程式，然後傳遞至輸出佇列，然後再將自訂手寫筆資料編號為 "2" 和 "3"，這兩個數據會在下一次 tablet 畫筆資料處理之前處理。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。

## <a name="error-data"></a>錯誤資料

當外掛程式擲回例外狀況時，就會中斷正常的資料流程。 [**RealTimeStylus**](realtimestylus-class.md)物件會產生 [ErrorData](/previous-versions/ms824740(v=msdn.10))物件，並呼叫：

-   擲回例外狀況之外掛程式的 [StylusInput. IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) 或 [StylusInput. IStylusAsyncPlugin](/previous-versions/ms824771(v=msdn.10)) 方法。
-   該集合中其餘外掛程式的 [StylusInput. IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) 或 [StylusInput.. IStylusAsyncPlugin](/previous-versions/ms824771(v=msdn.10)) 方法。

如果擲回例外狀況的外掛程式是同步外掛程式，則會將 [ErrorData](/previous-versions/ms824740(v=msdn.10)) 物件新增至輸出佇列。 然後， [**RealTimeStylus**](realtimestylus-class.md) 物件會繼續正常處理原始資料。

下圖說明如何將錯誤資料新增至 tablet 畫筆資料。

![自訂手寫筆資料流程至輸出佇列，並新增錯誤資料](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

在此圖中，圓形 "A" 和 "B" 代表已新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件輸出佇列且尚未傳送至非同步外掛程式集合的 tablet 畫筆資料。 以字母 "C" 表示 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。 以字母 "e" 表示的圓形，代表當第二個同步外掛程式（同步外掛程式2）在處理 "C" 時擲回例外狀況時，由 **RealTimeStylus** 物件所產生的 [ErrorData](/previous-versions/ms824740(v=msdn.10))物件。 然後， **RealTimeStylus** 物件會暫停其對 "C" 的處理，並將 "e" 傳遞給產生例外狀況的外掛程式，以及所有後續的外掛程式。然後， **RealTimeStylus** 物件會將 "e" 放在輸出佇列，並繼續處理 "C"，這會傳遞給同步外掛程式集合中的其餘外掛程式，並放在 "e" 之後的輸出佇列。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。

如果外掛程式從其錯誤方法擲回例外狀況，則 [**RealTimeStylus**](realtimestylus-class.md) 物件會捕捉例外狀況，但不會產生新的 [ErrorData](/previous-versions/ms824740(v=msdn.10)) 物件。 這是為了防止遞迴。

在建立錯誤資料的例外狀況之前，于 **OutputImmediate** 位置加入的任何自訂手寫筆資料，以及在同步外掛程式集合中後續外掛程式加入 **OutputImmediate** 位置的任何自訂手寫筆資料之前，會將錯誤資料加入至輸出佇列。

下圖說明如何將錯誤資料加入至輸出佇列，相對於新增至 **OutputImmediate** 佇列的自訂資料。

![相對於新增至 outputimmediate 佇列的自訂資料，新增至輸出佇列的錯誤資料。](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

在此圖中，圓形 "A" 和 "B" 代表已新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件輸出佇列且尚未傳送至非同步外掛程式集合的 tablet 畫筆資料。 以字母 "C" 表示 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。 第一個、第二個和第三個同步外掛程式會分別將編號為 "1"、"2" 和 "3" 的圓形新增至 **OutputImmediate** 佇列，以回應以字母 "C" 表示的資料。 以字母 "e" 表示的圓圈表示在第二個外掛程式將自訂資料新增至 **OutputImmediate** 位置的輸出佇列後，第二個外掛程式所擲回的例外狀況所產生的錯誤資料。

如果任何同步外掛程式將自訂手寫筆資料新增至輸入佇列以回應錯誤資料，則會在錯誤資料之前立即加入資料。 如果有任何同步外掛程式在 **輸出** 位置將自訂手寫筆資料新增至輸出佇列以回應錯誤資料，則會在錯誤資料之後立即加入資料。

[**RealTimeStylus**](realtimestylus-class.md)物件會在擲回例外狀況的執行緒上呼叫 [StylusInput. IStylusSyncPlugin](/previous-versions/ms824754(v=msdn.10))方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft Ink 平板電腦](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[StylusInput](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[使用 RealTimeStylus 類別](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
