---
description: StylusInput Api 可讓您與 tablet 畫筆資料串流互動。 若要與資料流程互動，請將 RealTimeStylus 物件新增至您的應用程式，並將外掛程式加入至 RealTimeStylus 物件。
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: StylusInput Api 的架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeda6a6a0269e8306aed6a6b6de4c1bbe33bc46f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115781"
---
# <a name="architecture-of-the-stylusinput-apis"></a><span data-ttu-id="48674-104">StylusInput Api 的架構</span><span class="sxs-lookup"><span data-stu-id="48674-104">Architecture of the StylusInput APIs</span></span>

<span data-ttu-id="48674-105">StylusInput Api 可讓您與 tablet 畫筆資料串流互動。</span><span class="sxs-lookup"><span data-stu-id="48674-105">The StylusInput APIs allow you to interact with the tablet pen data stream.</span></span> <span data-ttu-id="48674-106">若要與資料流程互動，請將 [**RealTimeStylus**](realtimestylus-class.md) 物件新增至您的應用程式，並將外掛程式加入至 **RealTimeStylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="48674-106">To interact with the data stream add a [**RealTimeStylus**](realtimestylus-class.md) object to your application, and add plug-ins to the **RealTimeStylus** object.</span></span>

<span data-ttu-id="48674-107">StylusInput Api 中提供兩個外掛程式。</span><span class="sxs-lookup"><span data-stu-id="48674-107">Two plug-ins are provided in the StylusInput APIs.</span></span> <span data-ttu-id="48674-108">[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))物件會實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)介面。</span><span class="sxs-lookup"><span data-stu-id="48674-108">The [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) interface.</span></span> <span data-ttu-id="48674-109">**DynamicRenderer** 物件會在繪製時即時呈現筆墨。</span><span class="sxs-lookup"><span data-stu-id="48674-109">The **DynamicRenderer** object renders the ink in real time, as it is being drawn.</span></span> <span data-ttu-id="48674-110">[**GestureRecognizer**](gesturerecognizer-class.md)物件會實 **IStylusSyncPlugin** 和 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)介面。</span><span class="sxs-lookup"><span data-stu-id="48674-110">The [**GestureRecognizer**](gesturerecognizer-class.md) object implements the **IStylusSyncPlugin** and [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interfaces.</span></span> <span data-ttu-id="48674-111">**GestureRecognizer** 物件可識別應用程式手勢。</span><span class="sxs-lookup"><span data-stu-id="48674-111">The **GestureRecognizer** object recognizes application gestures.</span></span>

## <a name="definitions"></a><span data-ttu-id="48674-112">定義</span><span class="sxs-lookup"><span data-stu-id="48674-112">Definitions</span></span>

<span data-ttu-id="48674-113">描述 StylusInput Api 的章節中會使用下列詞彙：</span><span class="sxs-lookup"><span data-stu-id="48674-113">The following terms are used in the sections describing the StylusInput APIs:</span></span>

<span data-ttu-id="48674-114">同步外掛程式</span><span class="sxs-lookup"><span data-stu-id="48674-114">Synchronous plug-in</span></span>

<span data-ttu-id="48674-115">實 [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="48674-115">A class that implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) interface.</span></span> <span data-ttu-id="48674-116">同步外掛程式通常會直接由 [**RealTimeStylus**](realtimestylus-class.md) 物件呼叫。</span><span class="sxs-lookup"><span data-stu-id="48674-116">Synchronous plug-ins are generally called directly by the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span>

<span data-ttu-id="48674-117">非同步外掛程式</span><span class="sxs-lookup"><span data-stu-id="48674-117">Asynchronous plug-in</span></span>

<span data-ttu-id="48674-118">實 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="48674-118">A class that implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span> <span data-ttu-id="48674-119">非同步外掛程式通常會在應用程式的使用者介面上呼叫 (UI) 執行緒。</span><span class="sxs-lookup"><span data-stu-id="48674-119">Asynchronous plug-ins are generally called on the application's user interface (UI) thread.</span></span>

<span data-ttu-id="48674-120">同步外掛程式集合</span><span class="sxs-lookup"><span data-stu-id="48674-120">Synchronous plug-in collection</span></span>

<span data-ttu-id="48674-121">[StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10))集合，這是[IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))物件的已排序集合。</span><span class="sxs-lookup"><span data-stu-id="48674-121">A [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) collection, which is an ordered collection of [IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10)) objects.</span></span> <span data-ttu-id="48674-122">同步外掛程式集合通常是指指派給[RealTimeStylus](/previous-versions/ms824830(v=msdn.10))物件之[SyncPluginCollection](/previous-versions/ms824833(v=msdn.10))屬性的集合。</span><span class="sxs-lookup"><span data-stu-id="48674-122">A synchronous plug-in collection usually refers to the collection assigned to the [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) property of a [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) object.</span></span> <span data-ttu-id="48674-123">只有同步外掛程式才能新增至同步的外掛程式集合。</span><span class="sxs-lookup"><span data-stu-id="48674-123">Only synchronous plug-ins may be added to a synchronous plug-in collection.</span></span>

<span data-ttu-id="48674-124">非同步外掛程式集合</span><span class="sxs-lookup"><span data-stu-id="48674-124">Asynchronous plug-in collection</span></span>

<span data-ttu-id="48674-125">[StylusAsyncPluginCollection](/previous-versions/ms824808(v=msdn.10))集合，這是[IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))物件的已排序集合。</span><span class="sxs-lookup"><span data-stu-id="48674-125">A [StylusAsyncPluginCollection](/previous-versions/ms824808(v=msdn.10)) collection, which is an ordered collection of [IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10)) objects.</span></span> <span data-ttu-id="48674-126">非同步外掛程式集合通常會參考指派給[RealTimeStylus](/previous-versions/ms824830(v=msdn.10))物件之[AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10))屬性的集合。</span><span class="sxs-lookup"><span data-stu-id="48674-126">An asynchronous plug-in collection usually refers to the collection assigned to the [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) property of a [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) object.</span></span> <span data-ttu-id="48674-127">只有非同步外掛程式可以加入至非同步外掛程式集合。</span><span class="sxs-lookup"><span data-stu-id="48674-127">Only asynchronous plug-ins may be added to an asynchronous plug-in collection.</span></span>

## <a name="synchronous-and-asynchronous-plug-ins"></a><span data-ttu-id="48674-128">同步和非同步外掛程式</span><span class="sxs-lookup"><span data-stu-id="48674-128">Synchronous and Asynchronous Plug-ins</span></span>

<span data-ttu-id="48674-129">[**RealTimeStylus**](realtimestylus-class.md)物件是設計來提供從 tablet 畫筆即時存取資料流程的功能。</span><span class="sxs-lookup"><span data-stu-id="48674-129">The [**RealTimeStylus**](realtimestylus-class.md) object is designed to provide real-time access to the data stream from a tablet pen.</span></span> <span data-ttu-id="48674-130">針對需要即時存取資料流程和 undemanding 的工作（例如封包篩選），建立或使用同步外掛程式。</span><span class="sxs-lookup"><span data-stu-id="48674-130">Create or use synchronous plug-ins for tasks that require real-time access to the data stream and are computationally undemanding, such as for packet filtering.</span></span> <span data-ttu-id="48674-131">針對不需要即時存取資料流程的工作建立或使用非同步外掛程式，例如在 [**InkDisp**](inkdisp-class.md) 物件中建立和儲存筆觸。</span><span class="sxs-lookup"><span data-stu-id="48674-131">Create or use asynchronous plug-ins for tasks that do not require real-time access to the data stream, such as for creating and storing strokes in an [**InkDisp**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="48674-132">某些工作可能會需要大量運算，但需要即時存取資料流程，例如 multistroke 手勢辨識。</span><span class="sxs-lookup"><span data-stu-id="48674-132">Certain tasks may be computationally demanding yet require real-time access to the data stream, such as multistroke gesture recognition.</span></span> <span data-ttu-id="48674-133">為了滿足這些需求，StylusInput Api 提供了串聯的 [**realtimestylus**](realtimestylus-class.md) 模型，可讓您使用兩個 **realtimestylus** 物件，每個都在自己的執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="48674-133">To address these needs, the StylusInput APIs provide a cascaded [**RealTimeStylus**](realtimestylus-class.md) model that allows you to use two **RealTimeStylus** objects, each running on its own thread.</span></span> <span data-ttu-id="48674-134">如需有關串聯的 **realtimestylus** 模型的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。</span><span class="sxs-lookup"><span data-stu-id="48674-134">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

<span data-ttu-id="48674-135">如需使用和建立外掛程式的詳細資訊，請參閱使用 [StylusInput api](working-with-the-stylusinput-apis.md)。</span><span class="sxs-lookup"><span data-stu-id="48674-135">For more information about using and creating plug-ins, see [Working with the StylusInput APIs](working-with-the-stylusinput-apis.md).</span></span>

## <a name="the-tablet-pen-data-stream"></a><span data-ttu-id="48674-136">Tablet 畫筆資料串流</span><span class="sxs-lookup"><span data-stu-id="48674-136">The Tablet Pen Data Stream</span></span>

<span data-ttu-id="48674-137">[**RealTimeStylus**](realtimestylus-class.md)物件具有兩個包含 tablet 畫筆資料的內部佇列、輸入佇列和輸出佇列。</span><span class="sxs-lookup"><span data-stu-id="48674-137">The [**RealTimeStylus**](realtimestylus-class.md) object has two internal queues that carry the tablet pen data, the input queue and the output queue.</span></span> <span data-ttu-id="48674-138">畫筆資料會轉換成 [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) 命名空間中的類別實例。</span><span class="sxs-lookup"><span data-stu-id="48674-138">The pen data is converted into instances of the classes in the [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespace.</span></span> <span data-ttu-id="48674-139">下列清單說明 **RealTimeStylus** 物件如何處理 tablet 畫筆資料：</span><span class="sxs-lookup"><span data-stu-id="48674-139">The following list describes how the **RealTimeStylus** object handles the tablet pen data:</span></span>

<span data-ttu-id="48674-140">[**RealTimeStylus**](realtimestylus-class.md)物件會先在其輸入佇列中，然後從 tablet 畫筆資料流程檢查外掛程式資料物件。</span><span class="sxs-lookup"><span data-stu-id="48674-140">The [**RealTimeStylus**](realtimestylus-class.md) object checks for plug-in data objects first on its input queue and then from the tablet pen data stream.</span></span>

<span data-ttu-id="48674-141">[**RealTimeStylus**](realtimestylus-class.md)物件會將一個外掛程式資料物件傳送到其同步外掛程式集合中的物件。</span><span class="sxs-lookup"><span data-stu-id="48674-141">The [**RealTimeStylus**](realtimestylus-class.md) object sends one plug-in data object to the objects in its synchronous plug-in collection.</span></span> <span data-ttu-id="48674-142">每個同步外掛程式都可以將資料新增至輸入或輸出佇列。</span><span class="sxs-lookup"><span data-stu-id="48674-142">Each synchronous plug-in can add data to either the input or output queue.</span></span>

<span data-ttu-id="48674-143">將外掛程式資料物件傳送到同步外掛程式集合的所有成員之後，會將外掛程式資料物件放在 [**RealTimeStylus**](realtimestylus-class.md) 物件的輸出佇列。</span><span class="sxs-lookup"><span data-stu-id="48674-143">After the plug-in data object has been sent to all members of the synchronous plug-in collection, the plug-in data object is placed on the [**RealTimeStylus**](realtimestylus-class.md) object's output queue.</span></span>

<span data-ttu-id="48674-144">然後， [**RealTimeStylus**](realtimestylus-class.md) 物件會檢查下一個要處理的外掛程式資料物件。</span><span class="sxs-lookup"><span data-stu-id="48674-144">The [**RealTimeStylus**](realtimestylus-class.md) object then checks for the next plug-in data object to process.</span></span>

<span data-ttu-id="48674-145">當 [**realtimestylus**](realtimestylus-class.md) 物件的輸出佇列包含資料時， **realtimestylus** 物件會從其輸出佇列將一個外掛程式資料物件傳送到其非同步外掛程式集合中的物件。</span><span class="sxs-lookup"><span data-stu-id="48674-145">While the [**RealTimeStylus**](realtimestylus-class.md) object's output queue contains data, the **RealTimeStylus** object sends one plug-in data object from its output queue to the objects in its asynchronous plug-in collection.</span></span> <span data-ttu-id="48674-146">每個非同步外掛程式都可以將資料加入至輸入或輸出佇列。</span><span class="sxs-lookup"><span data-stu-id="48674-146">Each asynchronous plug-in can add data to either the input or output queue.</span></span> <span data-ttu-id="48674-147">不過，由於非同步外掛程式是在 UI 執行緒上執行，因此會將資料加入至佇列，以與 **RealTimeStylus** 物件正在處理的目前畫筆資料相關，而不是與非同步外掛程式正在處理的資料相關。</span><span class="sxs-lookup"><span data-stu-id="48674-147">However, because the asynchronous plug-ins run on the UI thread, the data is added to the queue in relation to the current pen data the **RealTimeStylus** object is processing, and not in relation to the data that the asynchronous plug-in is processing.</span></span>

<span data-ttu-id="48674-148">下圖說明透過 [**RealTimeStylus**](realtimestylus-class.md) 物件和其外掛程式集合進行 tablet 畫筆資料的流程。</span><span class="sxs-lookup"><span data-stu-id="48674-148">The following diagram illustrates the flow of tablet pen data through the [**RealTimeStylus**](realtimestylus-class.md) object and its plug-in collections.</span></span>

![透過 realtimestylus 物件和其外掛程式集合的 tablet 畫筆資料流程程](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

<span data-ttu-id="48674-150">在此圖中，標示為 "A" 和 "B" 的圓形代表已新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件輸出佇列且尚未傳送至非同步外掛程式集合的 tablet 畫筆資料。</span><span class="sxs-lookup"><span data-stu-id="48674-150">In this diagram, the circles labeled "A" and "B" represent tablet pen data that has already been added to the [**RealTimeStylus**](realtimestylus-class.md) object's output queue and that has not yet been sent to the asynchronous plug-in collection.</span></span> <span data-ttu-id="48674-151">標示為 "C" 的圓形代表 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。</span><span class="sxs-lookup"><span data-stu-id="48674-151">The circle labeled "C" represents the tablet pen data that the **RealTimeStylus** object is currently processing.</span></span> <span data-ttu-id="48674-152">它會傳送至同步的外掛程式集合，並放在輸出佇列中。</span><span class="sxs-lookup"><span data-stu-id="48674-152">It is sent to the synchronous plug-in collection and placed on the output queue.</span></span> <span data-ttu-id="48674-153">空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。</span><span class="sxs-lookup"><span data-stu-id="48674-153">The empty circle represents the position in the output queue where future tablet pen data is added.</span></span>

<span data-ttu-id="48674-154">如需有關如何將特定資料新增至佇列並加以處理的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。</span><span class="sxs-lookup"><span data-stu-id="48674-154">For more information about how specific data is added to the queue and processed, see [Plug-in Data and the RealTimeStylus Class](plug-in-data-and-the-realtimestylus-class.md).</span></span>

## <a name="the-stylusinput-apis"></a><span data-ttu-id="48674-155">StylusInput Api</span><span class="sxs-lookup"><span data-stu-id="48674-155">The StylusInput APIs</span></span>

<span data-ttu-id="48674-156">StylusInput Api 主要位於 [StylusInput](/previous-versions/ms824750(v=msdn.10)) 和 [StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="48674-156">The StylusInput APIs reside primarily in the [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces.</span></span> <span data-ttu-id="48674-157">不過，StylusInput Api 也會參考 [Microsoft Ink](/previous-versions/ms826516(v=msdn.10)) 命名空間中的某些類別，例如 [Tablet](/previous-versions/ms827783(v=msdn.10)) 類別、 [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) 集合，以及 [ApplicationGesture](/previous-versions/ms827547(v=msdn.10)) 和 [SystemGesture](/previous-versions/ms827134(v=msdn.10)) 列舉。</span><span class="sxs-lookup"><span data-stu-id="48674-157">However, the StylusInput APIs also reference some classes in the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace, such as the [Tablet](/previous-versions/ms827783(v=msdn.10)) class, the [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) collection, and the [ApplicationGesture](/previous-versions/ms827547(v=msdn.10)) and [SystemGesture](/previous-versions/ms827134(v=msdn.10)) enumerations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48674-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="48674-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="48674-159">[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48674-159">[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="48674-160">**GestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="48674-160">**GestureRecognizer**</span></span>](gesturerecognizer-class.md)
</dt> <dt>

[<span data-ttu-id="48674-161">**RealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="48674-161">**RealTimeStylus**</span></span>](realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="48674-162">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="48674-162">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[<span data-ttu-id="48674-163">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="48674-163">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[<span data-ttu-id="48674-164">使用 StylusInput Api</span><span class="sxs-lookup"><span data-stu-id="48674-164">Working with the StylusInput APIs</span></span>](working-with-the-stylusinput-apis.md)
</dt> <dt>

[<span data-ttu-id="48674-165">串聯的 RealTimeStylus 模型</span><span class="sxs-lookup"><span data-stu-id="48674-165">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
