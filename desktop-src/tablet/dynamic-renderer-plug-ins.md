---
description: 動態轉譯器外掛程式是一種物件，會即時顯示 tablet 畫筆資料，因為它正由 RealTimeStylus 物件處理。
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Dynamic-Renderer 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c3f1a33c3cd7faef2e899bcb198ea64aa5bd76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553832"
---
# <a name="dynamic-renderer-plug-ins"></a>Dynamic-Renderer 外掛程式

動態轉譯器外掛程式是一種物件，會即時顯示 tablet 畫筆資料，因為它正由 [**RealTimeStylus**](realtimestylus-class.md) 物件處理。 之後，如果是表單重新整理之類的事件，動態轉譯器外掛程式或筆墨收集器外掛程式可能會重繪筆墨。

## <a name="the-dynamicrenderer-object"></a>DynamicRenderer 物件

[**RealTimeStylus**](realtimestylus-class.md)物件會實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)介面。 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件會在繪製時即時呈現筆墨。 在啟用 **DynamicRenderer** 物件時呼叫 [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh)方法時， **DynamicRenderer** 物件會重新繪製目前正在收集的筆劃。 **DynamicRenderer** 物件的 [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled)屬性一開始會設為 **FALSE**。

> [!Note]  
> 從 managed 程式碼中的 [繪製](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1)事件處理常式內呼叫 [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10))物件的 [**Refresh**](/previous-versions/ms826370(v=msdn.10))方法時，請將 **DynamicRenderer** 物件的 [**ClipRectangle**](/previous-versions/ms826346(v=msdn.10))屬性設定為 [PaintEventArgs](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1)物件的 [ClipRectangle](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1)屬性。

 

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件可以暫時快取筆墨資料。 若要在 managed 程式碼中使用這項功能，請將 [EnableDataCache](/previous-versions/ms826349(v=msdn.10)) 屬性設定為 **TRUE**。 當 [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) 物件收到 [**IStylusSyncPlugin. StylusUp**](/previous-versions/ms826366(v=msdn.10)) 方法的呼叫時，它會快取筆劃資料，並將自訂手寫筆資料新增至輸入佇列，以回應筆劃的 [**StylusUpData**](/previous-versions/ms824057(v=msdn.10)) 物件。 [**CustomStylusData**](/previous-versions/ms824747(v=msdn.10))物件的 [CustomDataId](/previous-versions/ms824749(v=msdn.10))屬性設定為 [DynamicRendererCachedDataGuid](/previous-versions/ms824744(v=msdn.10))值，而 **CustomStylusData** 物件的 Data 屬性包含 DynamicRendererCachedData 物件。 一旦已收集筆劃，並且可以靜態呈現，請呼叫 **DynamicRenderer** 物件的 [ReleaseCachedData](/previous-versions/ms826371(v=msdn.10)) 方法。 在啟用 **DynamicRenderer** 物件時呼叫 [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh)方法時， **DynamicRenderer** 物件會重新繪製所有已快取的筆劃。 當 [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) 屬性設定為 **false** 時，就會刪除快取的筆劃資料。

下圖說明當設定 **DynamicRenderer** 物件的 [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled)屬性時， [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件如何將資料新增至 tablet 畫筆資料。

![顯示 dynamicrenderer 資料流程的圖例](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

在此圖中，"SD" 的圓形表示 [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown)物件，而圓形 "P" 表示已新增至 [**RealTimeStylus**](realtimestylus-class.md)物件輸出佇列且尚未傳送至非同步外掛程式集合的封 [**包**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)物件。 以字母 "SU" 表示 [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) 物件，此物件目前正在 **處理的物件** 。 它會傳送至同步的外掛程式集合，然後放在輸出佇列中。 圓圈表示「DR」表示自訂手寫筆資料，由 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 外掛程式新增至輸入佇列，以回應與「SU」相關聯的手寫筆上傳通知。 自訂手寫筆資料會以字母「DR」的形式傳遞至同步的外掛程式，然後再傳遞至輸出佇列，然後再處理下一個 tablet 畫筆資料。 空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。 此外，圖表上也會顯示筆墨收集器外掛程式，呼叫 **DynamicRenderer** 物件的 [**ReleaseCachedData**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) 方法，以便在筆墨收集外掛程式處理筆劃之後釋放快取的筆劃資料。

### <a name="special-considerations"></a>特殊考慮

下列清單描述使用 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 物件時應考慮的其他重點。

-   您不應該將 [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 物件附加至一個以上的 [**RealTimeStylus**](realtimestylus-class.md) 物件。 一旦已啟用 **DynamicRenderer** 物件附加的兩個 **RealTimeStylus** 物件，就會發生下列情況。

    -   [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件會擲回例外狀況，以回應其 [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled)方法的第二次呼叫。
    -   已啟用的第二個 [**RealTimeStylus**](realtimestylus-class.md) 物件會產生 [**error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) 物件，並在該錯誤的外掛程式集合中通知其餘的外掛程式。
    -   [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件會停止呈現 tablet 畫筆資料。

-   當使用設定為 DynamicRendererCachedDataGuid 全域唯一識別碼 (GUID) 的 *guid* 參數呼叫 [**AddCustomStylusDataToQueue**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue)方法 [**時，會**](realtimestylus-class.md)擲回例外狀況。
-   [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件會實作為元件物件模型 (COM) 包裝函式，而且您無法直接呼叫其 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)介面方法。 如需有關 COM 操作和 [**RealTimeStylus**](realtimestylus-class.md) 物件的詳細資訊，請參閱 [StylusInput Api 的執行附注](implementation-notes-for-the-stylusinput-apis.md)。

## <a name="custom-rendering"></a>自訂轉譯

您可以建立訂閱 [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown)、封 [**包**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)和 [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) 通知的同步外掛程式，以建立自己的動態轉譯器外掛程式。 然後，您的外掛程式可以在繪製時轉譯筆劃。 例如，這可能是一種執行選擇工具的方式，使用自由格式選取或選取方塊。

 

 
