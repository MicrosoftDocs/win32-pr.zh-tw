---
description: RealTimeStylus 物件是設計來提供從 tablet 畫筆即時存取資料流程的功能。
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: 外掛程式和 RealTimeStylus 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08177c5f4110897fa1887857788766f67ae38167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998547"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a><span data-ttu-id="5849d-103">外掛程式和 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="5849d-103">Plug-ins and the RealTimeStylus Class</span></span>

<span data-ttu-id="5849d-104">[**RealTimeStylus**](realtimestylus-class.md)物件是設計來提供從 tablet 畫筆即時存取資料流程的功能。</span><span class="sxs-lookup"><span data-stu-id="5849d-104">The [**RealTimeStylus**](realtimestylus-class.md) object is designed to provide real-time access to the data stream from the tablet pen.</span></span> <span data-ttu-id="5849d-105">外掛程式、可執行 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 或 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的物件，都可以新增至 **RealTimeStylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="5849d-105">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface, can be added to a **RealTimeStylus** object.</span></span> <span data-ttu-id="5849d-106">同步外掛程式通常會直接在高優先順序的執行緒上由 **RealTimeStylus** 物件呼叫，而非同步外掛程式通常會在應用程式的使用者介面上呼叫， (UI) 執行緒。</span><span class="sxs-lookup"><span data-stu-id="5849d-106">Synchronous plug-ins are generally called directly by the **RealTimeStylus** object on a high-priority thread, while asynchronous plug-ins are generally called on the application's user interface (UI) thread.</span></span> <span data-ttu-id="5849d-107">針對需要即時存取資料流程和 undemanding 的工作（例如封包篩選），建立或使用同步外掛程式。</span><span class="sxs-lookup"><span data-stu-id="5849d-107">Create or use synchronous plug-ins for tasks that require real-time access to the data stream and are computationally undemanding, such as packet filtering.</span></span> <span data-ttu-id="5849d-108">針對不需要即時存取資料流程的工作建立或使用非同步外掛程式，例如筆墨收集。</span><span class="sxs-lookup"><span data-stu-id="5849d-108">Create or use asynchronous plug-ins for tasks that do not require real-time access to the data stream, such as ink collection.</span></span>

<span data-ttu-id="5849d-109">某些工作可能會需要大量運算，但需要即時存取資料流程，例如 multistroke 手勢辨識。</span><span class="sxs-lookup"><span data-stu-id="5849d-109">Certain tasks may be computationally demanding yet require real-time access to the data stream, such as multistroke gesture recognition.</span></span> <span data-ttu-id="5849d-110">為了滿足這些需求，StylusInput Api 提供了串聯的 [**realtimestylus**](realtimestylus-class.md) 模型，可讓您使用兩個 **realtimestylus** 物件，每個都在自己的執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="5849d-110">To address these needs, the StylusInput APIs provide a cascaded [**RealTimeStylus**](realtimestylus-class.md) model that allows you to use two **RealTimeStylus** objects, each running on its own thread.</span></span> <span data-ttu-id="5849d-111">如需有關串聯的 **realtimestylus** 模型的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。</span><span class="sxs-lookup"><span data-stu-id="5849d-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

<span data-ttu-id="5849d-112">[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)和 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)介面都會定義相同的方法。</span><span class="sxs-lookup"><span data-stu-id="5849d-112">Both the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) and [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interfaces define the same methods.</span></span> <span data-ttu-id="5849d-113">這些方法可讓 [**RealTimeStylus**](realtimestylus-class.md) 物件將畫筆資料傳遞至每個外掛程式，不論它是非同步或同步的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="5849d-113">These methods allow the [**RealTimeStylus**](realtimestylus-class.md) object to pass the pen data to each plug-in, regardless of whether it is an asynchronous or synchronous plug-in.</span></span> <span data-ttu-id="5849d-114">[StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10))和[StylusInput. IStylusAsyncPlugin](/previous-versions/ms824769(v=msdn.10))屬性可讓每個外掛程式訂閱 tablet 畫筆資料流程中的特定資料。</span><span class="sxs-lookup"><span data-stu-id="5849d-114">The [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) and [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) properties allow each plug-in to subscribe to specific data in the tablet pen data stream.</span></span> <span data-ttu-id="5849d-115">外掛程式只應訂閱執行其工作所需的資料，將效能需求降至最低。</span><span class="sxs-lookup"><span data-stu-id="5849d-115">A plug-in should only subscribe to the data necessary to perform its task, minimizing performance demands.</span></span> <span data-ttu-id="5849d-116">如需有關執行緒和 **RealTimeStylus** 類別的詳細資訊，請參閱 [StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)。</span><span class="sxs-lookup"><span data-stu-id="5849d-116">For more information about threading and the **RealTimeStylus** class, see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="5849d-117">[**RealTimeStylus**](realtimestylus-class.md)物件會使用 [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))命名空間中的物件，將畫筆資料傳遞給其外掛程式。**RealTimeStylus** 也會捕捉外掛程式擲回的例外狀況。當 **RealTimeStylus** 攔截到例外狀況時，它會呼叫 [IStylusSyncPlugin](/previous-versions/ms824754(v=msdn.10))或 [IStylusAsyncPlugin](/previous-versions/ms824771(v=msdn.10))方法來通知外掛程式。</span><span class="sxs-lookup"><span data-stu-id="5849d-117">The [**RealTimeStylus**](realtimestylus-class.md) object uses objects in the [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespace to pass the pen data to its plug-ins. The **RealTimeStylus** also catches exceptions thrown by plug-ins. When the **RealTimeStylus** catches exceptions, it notifies the plug-ins by calling the [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method.</span></span> <span data-ttu-id="5849d-118">如需使用外掛程式資料的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="5849d-118">For more information about using plug-in data, see [Plug-in Data and the RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) Class.</span></span> <span data-ttu-id="5849d-119">如需有關錯誤處理的詳細資訊，請參閱 [StylusInput api 的錯誤處理考慮](error-handling-considerations-for-the-stylusinput-apis.md) 和外掛程式資料和 RealTimeStylus 類別的錯誤資料區段。</span><span class="sxs-lookup"><span data-stu-id="5849d-119">For more information about error handling, see [Error Handling Considerations for the StylusInput APIs](error-handling-considerations-for-the-stylusinput-apis.md) and the Error Data section of Plug-in Data and the RealTimeStylus Class.</span></span>

> [!Note]  
> <span data-ttu-id="5849d-120">必須先將一個外掛程式附加到 [**realtimestylus**](realtimestylus-class.md) 物件，才能啟用 **realtimestylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="5849d-120">At least one plug-in must be attached to the [**RealTimeStylus**](realtimestylus-class.md) object before the **RealTimeStylus** object can be enabled.</span></span>

 

<span data-ttu-id="5849d-121">下列主題將說明一些常見的外掛程式類別。</span><span class="sxs-lookup"><span data-stu-id="5849d-121">The following topics describe some common categories of plug-ins.</span></span>

-   [<span data-ttu-id="5849d-122">筆墨-集合外掛程式</span><span class="sxs-lookup"><span data-stu-id="5849d-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
-   [<span data-ttu-id="5849d-123">動態轉譯器外掛程式</span><span class="sxs-lookup"><span data-stu-id="5849d-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
-   [<span data-ttu-id="5849d-124">辨識器外掛程式</span><span class="sxs-lookup"><span data-stu-id="5849d-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)

## <a name="special-considerations"></a><span data-ttu-id="5849d-125">特殊考慮</span><span class="sxs-lookup"><span data-stu-id="5849d-125">Special Considerations</span></span>

<span data-ttu-id="5849d-126">因為 [**RealTimeStylus**](realtimestylus-class.md) 物件的複雜本質，所以您應該注意下列事項。</span><span class="sxs-lookup"><span data-stu-id="5849d-126">Because of the complex nature of the [**RealTimeStylus**](realtimestylus-class.md) object, you should take note of the following.</span></span>

<span data-ttu-id="5849d-127">如果外掛程式修改附加的外掛程式集合，則 [**RealTimeStylus**](realtimestylus-class.md) 物件會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5849d-127">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in modifies the plug-in collection to which it is attached.</span></span> <span data-ttu-id="5849d-128">只有當外掛程式 **以該集合** 的成員身分呼叫它時，才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="5849d-128">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object as a member of that collection.</span></span>

<span data-ttu-id="5849d-129">下列 C \# 範例是導致 [**RealTimeStylus**](realtimestylus-class.md) 物件擲回例外狀況的程式碼。</span><span class="sxs-lookup"><span data-stu-id="5849d-129">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



<span data-ttu-id="5849d-130">如果外掛程式呼叫 **RealTimeStylus** 物件的 [Dispose](/previous-versions/ms825891(v=msdn.10))方法，則 [**RealTimeStylus**](realtimestylus-class.md)物件會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5849d-130">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in calls the **RealTimeStylus** object's [Dispose](/previous-versions/ms825891(v=msdn.10)) method.</span></span> <span data-ttu-id="5849d-131">只有當外掛程式在由 **RealTimeStylus** 物件呼叫時，才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="5849d-131">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object.</span></span>

<span data-ttu-id="5849d-132">下列 C \# 範例是導致 [**RealTimeStylus**](realtimestylus-class.md) 物件擲回例外狀況的程式碼。</span><span class="sxs-lookup"><span data-stu-id="5849d-132">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



<span data-ttu-id="5849d-133">啟用 [**RealTimeStylus**](realtimestylus-class.md) 物件時，可以修改外掛程式集合;不過，這可能會讓應用程式的行為難以預測。</span><span class="sxs-lookup"><span data-stu-id="5849d-133">Plug-in collections can be modified while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled; however, this can make the behavior of your application harder to predict.</span></span> <span data-ttu-id="5849d-134">當啟用了 **realtimestylus** 物件時，加入外掛程式時， **realtimestylus** 物件會呼叫外掛程式的 [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) 或 [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) 方法。</span><span class="sxs-lookup"><span data-stu-id="5849d-134">When a plug-in is added while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) method.</span></span> <span data-ttu-id="5849d-135">當啟用 **realtimestylus** 物件時移除外掛程式時， **realtimestylus** 物件會呼叫外掛程式的 [IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) 或 [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) 方法。</span><span class="sxs-lookup"><span data-stu-id="5849d-135">When a plug-in is removed while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) method.</span></span> <span data-ttu-id="5849d-136">這可讓外掛程式維持適當的狀態，而不需要檢查 **RealTimeStylus** 物件的 [Enabled](/previous-versions/ms824832(v=msdn.10))屬性。</span><span class="sxs-lookup"><span data-stu-id="5849d-136">This allows the plug-in to maintain its proper state without having to check the [Enabled](/previous-versions/ms824832(v=msdn.10)) property of the **RealTimeStylus** object.</span></span>

<span data-ttu-id="5849d-137">當您在啟用 [**RealTimeStylus**](realtimestylus-class.md) 物件時加入外掛程式時，外掛程式所接收的外掛程式資料可能不會包含足夠的資訊，以充分建立初始資料的內容。</span><span class="sxs-lookup"><span data-stu-id="5849d-137">When a plug-in is added while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled, the plug-in data that the plug-in receives may not contain enough information to adequately establish the context of the initial data.</span></span> <span data-ttu-id="5849d-138">例如，新加入的外掛程式可能會開始從中間筆劃的畫筆接收封包資料。</span><span class="sxs-lookup"><span data-stu-id="5849d-138">For example, the newly added plug-in could start receiving packet data from a pen that is mid-stroke.</span></span> <span data-ttu-id="5849d-139">同樣地，當啟用 **RealTimeStylus** 物件時移除外掛程式時，外掛程式所收到的外掛程式資料可能不足以完成處理資料。</span><span class="sxs-lookup"><span data-stu-id="5849d-139">Similarly, when a plug-in removed while the **RealTimeStylus** object is enabled, the plug-in data that the plug-in has received may be insufficient to finish processing the data.</span></span>

> [!Note]  
> <span data-ttu-id="5849d-140">若要取得整體穩定性，請在呼叫其 [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) 或 [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) 方法時重設外掛程式的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="5849d-140">For overall stability, reset a plug-in's internal state when either its [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) or [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) method is called.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5849d-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="5849d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5849d-142">串聯的 RealTimeStylus 模型</span><span class="sxs-lookup"><span data-stu-id="5849d-142">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[<span data-ttu-id="5849d-143">StylusInput Api 的錯誤處理考慮</span><span class="sxs-lookup"><span data-stu-id="5849d-143">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[<span data-ttu-id="5849d-144">外掛程式資料和 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="5849d-144">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="5849d-145">StylusInput Api 的執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="5849d-145">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
