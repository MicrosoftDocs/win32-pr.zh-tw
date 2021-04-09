---
description: 無法使用 [元件服務] 系統管理工具來設定暫時性訂閱。 您必須使用 COM + 系統管理介面來建立或更新暫時性訂用帳戶。
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: 註冊暫時性訂用帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110637"
---
# <a name="registering-a-transient-subscription"></a>註冊暫時性訂用帳戶

暫時性訂閱會要求已存在之特定訂閱者物件的事件。 暫時性訂閱會儲存在 COM + 目錄中，但如果事件系統或作業系統停止，就會刪除訂閱。 與持續性訂閱不同的是，暫時性訂閱會系結至特定的物件，而且只會儲存在事件系統中。 如果事件系統或作業系統發生問題，訂用帳戶將會消失。 暫時性訂用帳戶可比持續性訂閱更有效率，但您必須管理其物件生命週期。

無法使用 [元件服務] 系統管理工具來設定暫時性訂閱。 您必須使用 COM + 系統管理介面來建立或更新暫時性訂用帳戶。

## <a name="visual-basic"></a>Visual Basic

下列程式說明如何使用 Microsoft Visual Basic 建立暫時性訂用帳戶：

1.  將新專案加入至 [**TransientSubscriptions**](transientsubscriptions.md) 集合，並將 SubscriberInterface 屬性設定為訂閱者物件的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面，以將訂閱指定為暫時性。 當引發事件時，COM + 事件不會建立訂閱者物件的新實例，而是會使用您指定的實例。 COM + 事件會保存訂閱者物件的參考計數，直到從系統移除訂用帳戶為止。
2.  建立 COM + 伺服器應用程式 (.exe、.dll 或 .ocx 檔案，) 具有可執行您要訂閱之介面或方法的物件。
3.  使用下列程式碼建立您的暫時性訂閱，方法是傳遞 [事件類別](the-com--event-class-object.md) 物件的 CLSID 和訂閱者物件的實例。 您可以使用 [元件服務] 系統管理工具來取得 EventCLSID 屬性，方法是以滑鼠右鍵按一下 COM + 元件、選取 [ **屬性**]，然後選取 [ **一般** ] 索引標籤。

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

下列範例說明如何呼叫 CreateTransientSubscription 函式，以訂閱名為 IStockTicker 的介面，該介面具有稱為 UpdateStock 的方法。

1.  建立支援介面 IStockTicker 的事件類別，其中有一個方法 UpdateStock。
2.  在訂閱者專案中，加入可執行 IStockTicker 介面的類別。
3.  當您想要訂閱時，請執行下列程式碼：

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

CreateTransientSubscription 函式會傳回字串，此為 GUID，可做為控制碼或稍後用來撤銷訂閱的 cookie。 若要移除訂用帳戶，請在 [**TransientSubscriptions**](transientsubscriptions.md)集合上呼叫 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)的 [**remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，並在先前收到的 GUID 中傳入對應至訂用帳戶的索引。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊訂用帳戶](registering-a-subscription.md)
</dt> </dl>

 

 
