---
description: RealTimeStylus 類別是 StylusInput 應用程式設計介面的一部分， (Api) 。 下列各節說明 RealTimeStylus 類別和 StylusInput Api 的主要元素。
ms.assetid: 6385c387-5b11-4719-a6ec-e0bebe875348
title: 使用 RealTimeStylus 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 919c4de38cb0835996928c877ca4c42faf6a5f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690892"
---
# <a name="working-with-the-realtimestylus-class"></a>使用 RealTimeStylus 類別

[**RealTimeStylus**](realtimestylus-class.md)類別是 StylusInput 應用程式設計介面的一部分， (api) 。 下列各節說明 **RealTimeStylus** 類別和 StylusInput api 的主要元素。

## <a name="instantiating-the-realtimestylus-class"></a>具現化 RealTimeStylus 類別

當您建立 [**RealTimeStylus**](realtimestylus-class.md) 物件時，可以選擇將它附加至視窗控制碼或控制項。 將 **RealTimeStylus** 物件附加至視窗控制碼需要額外的許可權。 如需這些許可權的詳細資訊，請參閱 [StylusInput api 的部分信任考慮](partial-trust-considerations-for-the-stylusinput-apis.md)。

> [!Note]  
> 您無法在不同的進程中將 [**RealTimeStylus**](realtimestylus-class.md) 物件附加至視窗或控制項。

 

如果您使用預設的函式，則會建立只能接受來自另一個 **realtimestylus** 物件之輸入的 [**realtimestylus**](realtimestylus-class.md)物件。 如需連接兩個 **realtimestylus** 物件的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。

[**RealTimeStylus**](realtimestylus-class.md)物件會實 [IDisposable](/dotnet/api/system.idisposable)介面。

## <a name="extending-the-realtimestylus-class"></a>擴充 RealTimeStylus 類別

為了讓您的外掛程式可以從 tablet 畫筆與資料流程互動， [**RealTimeStylus**](realtimestylus-class.md) 物件會維護兩個外掛程式集合，這些集合可由 [**GetStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylussyncplugin) 和 c + + 中的 [**GetStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylusasyncplugin) 方法和 managed 程式碼中的 [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) 和 [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) 屬性來存取。 您可以在適當的屬性中呼叫集合的 [**AddStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylussyncplugin) 或 [**AddStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylusasyncplugin) 方法，以加入外掛程式。 如需建立和使用外掛程式的詳細資訊，請參閱 [外掛程式和 RealTimeStylus 類別](plug-ins-and-the-realtimestylus-class.md)。 如需決定是否要針對特定工作建立同步或非同步外掛程式的詳細資訊，請參閱 [StylusInput api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md) 和 [StylusInput Api 的效能考慮](performance-considerations-for-the-stylusinput-apis.md)。

同步外掛程式必須執行 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 介面，而非同步外掛程式必須執行 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面。 每個外掛程式都有 [**IStylusSyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) 或 [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) 屬性。 [**RealTimeStylus**](realtimestylus-class.md)物件只會針對外掛程式已訂閱的方法，呼叫外掛程式的通知方法。 如需有關通知方法的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。

[**RealTimeStylus**](realtimestylus-class.md)物件會實 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)介面。 具現化可接受另一個 **realtimestylus** 物件輸入之 **realtimestylus** 物件的唯一方法是使用預設的函式，並執行串聯的 **RealTimeStylus** 模型。 如需連接兩個 **realtimestylus** 物件的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。

[**RealTimeStylus**](realtimestylus-class.md)物件具有兩個包含 tablet 畫筆資料的內部佇列、輸入佇列和輸出佇列。 畫筆資料會轉換成 [StylusInput. PluginData](/previous-versions/ms574862(v=vs.100)) 命名空間中的類別實例。 下列清單說明 **RealTimeStylus** 物件如何處理 tablet 畫筆資料。

1.  [**RealTimeStylus**](realtimestylus-class.md)物件會先在其輸入佇列中，然後從 tablet 畫筆資料流程檢查外掛程式資料物件。
2.  [**RealTimeStylus**](realtimestylus-class.md)物件會將一個外掛程式資料物件傳送到其同步外掛程式集合中的物件。 每個同步外掛程式都可以將資料新增至輸入或輸出佇列。
3.  將外掛程式資料物件傳送到同步外掛程式集合的所有成員之後，外掛程式資料物件就會放置在 [**RealTimeStylus**](realtimestylus-class.md) 物件的輸出佇列中。
4.  然後， [**RealTimeStylus**](realtimestylus-class.md) 物件會檢查下一個要處理的外掛程式資料物件。
5.  當 [**realtimestylus**](realtimestylus-class.md) 物件的輸出佇列包含資料時， **realtimestylus** 物件會從其輸出佇列將一個外掛程式資料物件傳送到其非同步外掛程式集合中的物件。 每個非同步外掛程式都可以將資料加入至輸入或輸出佇列，但由於非同步外掛程式是在使用者介面上執行 (UI) 執行緒，因此會將資料新增至佇列，而該資料會相對於 **RealTimeStylus** 物件正在處理的目前畫筆資料，而不是與非同步外掛程式所處理的資料相對。

下圖說明透過 [**RealTimeStylus**](realtimestylus-class.md) 物件和其外掛程式集合進行 tablet 畫筆資料的流程。

![顯示 tablet pc 畫筆資料流程的 illustratiom](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

在此圖中，圓形 "A" 和 "B" 代表已新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件輸出佇列且尚未傳送至非同步外掛程式集合的 tablet 畫筆資料。 以字母 "C" 表示 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。 它會傳送至同步的外掛程式集合，並放在輸出佇列中。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。

如需有關如何將特定資料新增至佇列並加以處理的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。

以下是在收集筆墨的表單上使用 [**RealTimeStylus**](realtimestylus-class.md) 物件的最基本案例。

1.  建立可執行 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的表單。
2.  建立附加至表單上控制項的 [**RealTimeStylus**](realtimestylus-class.md) 物件。
3.  在表單的 [**IStylusAsyncPlugin DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) 屬性中，設定 StylusDown、封包和 StylusUp 通知的興趣。
4.  在表單的 [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown)、封 [**包**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)和 [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) 方法中，新增程式碼以處理從表單之 [**RealTimeStylus**](realtimestylus-class.md) 物件傳送的手寫筆向下、封包和手寫筆的通知。

如需這類應用程式的範例，請參閱 [RealTimeStylus 筆墨集合範例](realtimestylus-ink-collection-sample.md)。

## <a name="working-with-tablet-objects"></a>使用平板電腦物件

每個啟用的 [**RealTimeStylus**](realtimestylus-class.md) 物件都會維護可與其互動之 [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 物件的唯一識別碼清單。 **RealTimeStylus** 物件會公開兩種方法來轉譯唯一識別碼和 **平板** 電腦物件： [**GetTabletCoNtextIdFromTablet**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet)和 [**GetTabletFromTabletCoNtextId**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid)方法。

Managed 程式碼中的 [TabletPropertyDescription](/previous-versions/ms827769(v=msdn.10)) 物件 () 包含 [PacketPropertyId](/previous-versions/ms827780(v=msdn.10)) 屬性和 [TabletPropertyMetrics](/previous-versions/ms827781(v=msdn.10)) 結構，可描述特定 [**平板**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 電腦物件之屬性的範圍、解析度和單位。 [**Realtimestylus**](realtimestylus-class.md)物件的 [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription)方法會傳回全域唯一識別碼的陣列 (Guid) 適用于 **RealTimeStylus** 物件在有這些封包屬性時轉送到其外掛程式的封包屬性。 若要修改 **realtimestylus** 物件傳遞給其外掛程式的封包屬性集合，請呼叫 **Realtimestylus** 物件的 [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) 方法。 **RealTimeStylus** 物件的 managed 程式碼) 中 (的 [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10))方法會接受唯一的平板電腦識別碼，並傳回 [TabletPropertyDescription](/previous-versions/ms827760(v=msdn.10))物件的集合。 這些封包屬性代表 **GetDesiredPacketDescription** 方法所傳回的 tablet 所支援的屬性子集。

如需標準的封包屬性 Guid 清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md) 類別。

## <a name="special-considerations"></a>特殊考慮

下列清單描述搭配 [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)物件使用 [**RealTimeStylus**](realtimestylus-class.md)物件時，要考慮的其他重點。

-   只有當 [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)物件停用時，才能呼叫 [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription)方法。 [**RealTimeStylus**](realtimestylus-class.md)物件可修改所需的封包屬性清單;因此，呼叫 **SetDesiredPacketDescription** 方法之後，請呼叫 [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription)方法來判斷 **RealTimeStylus** 物件可以轉寄至其外掛程式的封包屬性。只保證平板電腦支援 [PacketProperty](packetproperty-guids.md)的 **X**、 **Y** 和 **PacketStatus** 值。 因此，您的外掛程式設計可能需要考慮接收的封包屬性數少於預期。
-   Managed 程式碼) 的 [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) 方法 (只能在啟用 [**RealTimeStylus**](realtimestylus-class.md) 物件時呼叫。 因為在停用 **RealTimeStylus** 物件之後，可以將通知傳送至非同步外掛程式，所以您可能需要快取每個 [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 物件的資訊。 GetTabletPropertyDescriptionCollection 方法會傳回指定的平板電腦所支援之所需的封包屬性清單。
-   啟用 [**RealTimeStylus**](realtimestylus-class.md) 物件之後，每個外掛程式都會收到其 [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) 方法的呼叫。 在通知中傳遞的 [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10)) 物件，會在啟用 **RealTimeStylus** 物件時，包含可用的平板電腦內容識別碼的集合。
-   當您在啟用 **realtimestylus** 物件時，將 [**realtimestylus**](realtimestylus-class.md)物件可使用的平板電腦加入或移除 Tablet PC 時， **realtimestylus** 物件會通知其外掛程式已新增或移除 [**tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)物件。 如需詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。

## <a name="working-with-tablet-pens"></a>使用 Tablet 畫筆

在許多通知方法中， [**RealTimeStylus**](realtimestylus-class.md) 物件會將 tablet 畫筆的相關資訊傳遞到其外掛程式。 Tablet 畫筆的相關資訊會由 [手寫筆](/previous-versions/ms824824(v=msdn.10)) 物件（透過 [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) 方法取得）來表示。 此物件是資料收集時的 tablet 畫筆標記法。 由於外掛程式會接收 tablet 畫筆資料作為 tablet 畫筆資料流程的一部分，因此外掛程式應使用手寫筆物件中的資訊，而不是透過 [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 類別檢查特定 tablet 畫筆的目前狀態。 如需 tablet 畫筆和 tablet 畫筆按鈕資料如何傳遞至外掛程式的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。

若要取得 [**realtimestylus**](realtimestylus-class.md)物件自上一次啟用以來遇到的 [手寫筆](/previous-versions/ms824824(v=msdn.10))物件陣列，請使用 **realtimestylus** 物件的 [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses)方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft Ink 平板電腦](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[StylusInput](/previous-versions/ms585724(v=vs.100))
</dt> <dt>

[串聯的 RealTimeStylus 模型](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[StylusInput Api 的部分信任考慮](partial-trust-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
