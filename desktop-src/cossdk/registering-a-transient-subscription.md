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
# <a name="registering-a-transient-subscription"></a><span data-ttu-id="dd804-104">註冊暫時性訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="dd804-104">Registering a Transient Subscription</span></span>

<span data-ttu-id="dd804-105">暫時性訂閱會要求已存在之特定訂閱者物件的事件。</span><span class="sxs-lookup"><span data-stu-id="dd804-105">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="dd804-106">暫時性訂閱會儲存在 COM + 目錄中，但如果事件系統或作業系統停止，就會刪除訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd804-106">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="dd804-107">與持續性訂閱不同的是，暫時性訂閱會系結至特定的物件，而且只會儲存在事件系統中。</span><span class="sxs-lookup"><span data-stu-id="dd804-107">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="dd804-108">如果事件系統或作業系統發生問題，訂用帳戶將會消失。</span><span class="sxs-lookup"><span data-stu-id="dd804-108">If there is a problem with the event system or operating system, the subscription disappears.</span></span> <span data-ttu-id="dd804-109">暫時性訂用帳戶可比持續性訂閱更有效率，但您必須管理其物件生命週期。</span><span class="sxs-lookup"><span data-stu-id="dd804-109">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span>

<span data-ttu-id="dd804-110">無法使用 [元件服務] 系統管理工具來設定暫時性訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd804-110">Transient subscriptions cannot be set by using the Component Services administration tool.</span></span> <span data-ttu-id="dd804-111">您必須使用 COM + 系統管理介面來建立或更新暫時性訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="dd804-111">You must use the COM+ administrative interfaces to create or update a transient subscription.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="dd804-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dd804-112">Visual Basic</span></span>

<span data-ttu-id="dd804-113">下列程式說明如何使用 Microsoft Visual Basic 建立暫時性訂用帳戶：</span><span class="sxs-lookup"><span data-stu-id="dd804-113">The following procedure describes how to create a transient subscription using Microsoft Visual Basic:</span></span>

1.  <span data-ttu-id="dd804-114">將新專案加入至 [**TransientSubscriptions**](transientsubscriptions.md) 集合，並將 SubscriberInterface 屬性設定為訂閱者物件的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 介面，以將訂閱指定為暫時性。</span><span class="sxs-lookup"><span data-stu-id="dd804-114">Specify a subscription as transient by adding a new entry to the [**TransientSubscriptions**](transientsubscriptions.md) collection and setting the SubscriberInterface property to the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface of the subscriber object.</span></span> <span data-ttu-id="dd804-115">當引發事件時，COM + 事件不會建立訂閱者物件的新實例，而是會使用您指定的實例。</span><span class="sxs-lookup"><span data-stu-id="dd804-115">COM+ Events does not create a new instance of the subscriber object when firing an event but instead uses the instance you specify.</span></span> <span data-ttu-id="dd804-116">COM + 事件會保存訂閱者物件的參考計數，直到從系統移除訂用帳戶為止。</span><span class="sxs-lookup"><span data-stu-id="dd804-116">COM+ Events holds a reference count for the subscriber object until the subscription is removed from the system.</span></span>
2.  <span data-ttu-id="dd804-117">建立 COM + 伺服器應用程式 (.exe、.dll 或 .ocx 檔案，) 具有可執行您要訂閱之介面或方法的物件。</span><span class="sxs-lookup"><span data-stu-id="dd804-117">Create a COM+ server application (an .exe, a .dll, or an .ocx file) with an object that implements the interfaces or methods you want to subscribe to.</span></span>
3.  <span data-ttu-id="dd804-118">使用下列程式碼建立您的暫時性訂閱，方法是傳遞 [事件類別](the-com--event-class-object.md) 物件的 CLSID 和訂閱者物件的實例。</span><span class="sxs-lookup"><span data-stu-id="dd804-118">Create your transient subscription using the following code, by passing in the CLSID of the [event class](the-com--event-class-object.md) object and the instance of the subscriber object.</span></span> <span data-ttu-id="dd804-119">您可以使用 [元件服務] 系統管理工具來取得 EventCLSID 屬性，方法是以滑鼠右鍵按一下 COM + 元件、選取 [ **屬性**]，然後選取 [ **一般** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="dd804-119">Using the Component Services administrative tool, you can get the EventCLSID property by right-clicking the COM+ component, selecting **Properties**, and selecting the **General** tab.</span></span>

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

<span data-ttu-id="dd804-120">下列範例說明如何呼叫 CreateTransientSubscription 函式，以訂閱名為 IStockTicker 的介面，該介面具有稱為 UpdateStock 的方法。</span><span class="sxs-lookup"><span data-stu-id="dd804-120">The following example illustrates how to call the CreateTransientSubscription function to subscribe to an interface called IStockTicker, which has a method called UpdateStock.</span></span>

1.  <span data-ttu-id="dd804-121">建立支援介面 IStockTicker 的事件類別，其中有一個方法 UpdateStock。</span><span class="sxs-lookup"><span data-stu-id="dd804-121">Create an event class that supports the interface IStockTicker, which has one method, UpdateStock.</span></span>
2.  <span data-ttu-id="dd804-122">在訂閱者專案中，加入可執行 IStockTicker 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="dd804-122">In your subscriber project, add a class that implements the IStockTicker interface.</span></span>
3.  <span data-ttu-id="dd804-123">當您想要訂閱時，請執行下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="dd804-123">When you want to subscribe execute the following code:</span></span>

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

<span data-ttu-id="dd804-124">CreateTransientSubscription 函式會傳回字串，此為 GUID，可做為控制碼或稍後用來撤銷訂閱的 cookie。</span><span class="sxs-lookup"><span data-stu-id="dd804-124">The CreateTransientSubscription function returns a string, which is a GUID that can be used as a handle or a cookie to revoke the subscription later.</span></span> <span data-ttu-id="dd804-125">若要移除訂用帳戶，請在 [**TransientSubscriptions**](transientsubscriptions.md)集合上呼叫 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)的 [**remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，並在先前收到的 GUID 中傳入對應至訂用帳戶的索引。</span><span class="sxs-lookup"><span data-stu-id="dd804-125">To remove the subscription, call the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of [**COMAdminCatalogCollection**](comadmincatalogcollection.md) on the [**TransientSubscriptions**](transientsubscriptions.md) collection, passing in the index corresponding to the subscription with the GUID previously received.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd804-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd804-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd804-127">註冊訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="dd804-127">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 
