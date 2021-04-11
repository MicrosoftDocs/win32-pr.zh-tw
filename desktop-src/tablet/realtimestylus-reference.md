---
description: 提供從畫筆或觸控數位板取得手寫筆事件的存取權。
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: RealTimeStylus 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193717"
---
# <a name="realtimestylus-reference"></a><span data-ttu-id="f2a97-103">RealTimeStylus 參考</span><span class="sxs-lookup"><span data-stu-id="f2a97-103">RealTimeStylus Reference</span></span>

<span data-ttu-id="f2a97-104">提供從畫筆或觸控數位板取得手寫筆事件的存取權。</span><span class="sxs-lookup"><span data-stu-id="f2a97-104">Provides access to the stylus events coming from pen or touch digitizers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f2a97-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f2a97-105">In This Section</span></span>

-   [<span data-ttu-id="f2a97-106">RealTimeStylus 類別和介面</span><span class="sxs-lookup"><span data-stu-id="f2a97-106">RealTimeStylus Classes and Interfaces</span></span>](realtimestylus-classes-and-interfaces.md)
-   [<span data-ttu-id="f2a97-107">RealTimeStylus 列舉</span><span class="sxs-lookup"><span data-stu-id="f2a97-107">RealTimeStylus Enumerations</span></span>](realtimestylus-enumerations.md)
-   [<span data-ttu-id="f2a97-108">RealTimeStylus 結構</span><span class="sxs-lookup"><span data-stu-id="f2a97-108">RealTimeStylus Structures</span></span>](realtimestylus-structures.md)

## <a name="remarks"></a><span data-ttu-id="f2a97-109">備註</span><span class="sxs-lookup"><span data-stu-id="f2a97-109">Remarks</span></span>

<span data-ttu-id="f2a97-110">這個物件會實 [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM 介面。</span><span class="sxs-lookup"><span data-stu-id="f2a97-110">This object implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM interface.</span></span>

<span data-ttu-id="f2a97-111">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="f2a97-111">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="f2a97-112">您可以完全控制、動態轉譯、修改，甚至刪除 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件的同步和非同步外掛程式內的封包資料流程中的資料。</span><span class="sxs-lookup"><span data-stu-id="f2a97-112">You can fully control, dynamically render, modify, and even delete data from the packet stream within the synchronous and asynchronous plug-ins of the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span>

<span data-ttu-id="f2a97-113">即時手寫筆會提供一種方法來建立 **InkCollecting** 物件，該物件為單一執行緒，且常駐于應用程式 UI 執行緒中。</span><span class="sxs-lookup"><span data-stu-id="f2a97-113">The real time stylus provides a way to create an **InkCollecting** object that is single-threaded and resident in the application UI thread.</span></span> <span data-ttu-id="f2a97-114">這個 **InkCollecting** 物件會從佇列存取即時手寫筆資料。</span><span class="sxs-lookup"><span data-stu-id="f2a97-114">This **InkCollecting** object accesses the real time stylus data from the queue.</span></span> <span data-ttu-id="f2a97-115">**InkCollecting** 物件與即時手寫筆搭配使用，可讓您即時選取編輯和即時編輯所收集的筆墨資料。</span><span class="sxs-lookup"><span data-stu-id="f2a97-115">An **InkCollecting** object in conjunction with real time stylus enables real-time selection editing and real-time editing of the collected ink data.</span></span> <span data-ttu-id="f2a97-116">如需詳細資訊，請參閱 [存取和操作手寫筆輸入](accessing-and-manipulating-stylus-input.md)。</span><span class="sxs-lookup"><span data-stu-id="f2a97-116">For more information, please see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span>

<span data-ttu-id="f2a97-117">使用 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件直接與 tablet 手寫筆資料流程互動，或封鎖即時手寫。</span><span class="sxs-lookup"><span data-stu-id="f2a97-117">Use the [**RealTimeStylus Class**](realtimestylus-class.md) object to interact directly with the tablet stylus data stream or to block real-time inking.</span></span> <span data-ttu-id="f2a97-118">當這些物件的預設行為提供您所需的行為時，請使用 [**InkCollector 類別**](inkcollector-class.md) 物件、 [**InkOverlay 類別**](inkoverlay-class.md) 物件、 [InkPicture 控制項](inkpicture-control-reference.md) 控制項或 [InkEdit 控制項](inkedit-control-reference.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="f2a97-118">Use the [**InkCollector Class**](inkcollector-class.md) object, [**InkOverlay Class**](inkoverlay-class.md) object, [InkPicture Control](inkpicture-control-reference.md) control, or [InkEdit Control](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

<span data-ttu-id="f2a97-119">即時手寫筆事件是在特定視窗輸入矩形內的特定視窗控制碼上。</span><span class="sxs-lookup"><span data-stu-id="f2a97-119">The real time stylus events are on a specific window handle within a specific window input rectangle.</span></span> <span data-ttu-id="f2a97-120">RealTimeStylusService 可將手寫筆資料傳送至多個 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f2a97-120">The RealTimeStylusService can send stylus data to multiple [**RealTimeStylus Class**](realtimestylus-class.md) objects.</span></span> <span data-ttu-id="f2a97-121">每個 **RealTimeStylus 類別** 物件都會根據該 **RealTimeStylus 類別** 物件的定義 [**IRealTimeStylus：： WindowInputRectangle 屬性**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle)，接收特定視窗區段的手寫筆資料。</span><span class="sxs-lookup"><span data-stu-id="f2a97-121">Each **RealTimeStylus Class** object receives stylus data for a specific section of a window based on the defined [**IRealTimeStylus::WindowInputRectangle Property**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) for that **RealTimeStylus Class** object.</span></span> <span data-ttu-id="f2a97-122">**RealTimeStylus 類別** 物件會取得手寫筆資料，然後透過同步和非同步外掛程式的清單進行處理。</span><span class="sxs-lookup"><span data-stu-id="f2a97-122">The **RealTimeStylus Class** object gets the stylus data and then processes this through a list of synchronous and asynchronous plug-ins.</span></span>

<span data-ttu-id="f2a97-123">同步外掛程式與非同步外掛程式之間的差異在於它們執行所在的執行緒和呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="f2a97-123">The difference between the synchronous plug-ins and the asynchronous plug-ins lies in the thread in which they execute and the calling sequence.</span></span> <span data-ttu-id="f2a97-124">同步外掛程式是由執行 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件的執行緒呼叫。</span><span class="sxs-lookup"><span data-stu-id="f2a97-124">Synchronous plug-ins are called by the thread in which the [**RealTimeStylus Class**](realtimestylus-class.md) object executes.</span></span> <span data-ttu-id="f2a97-125">每次具現化 **RealTimeStylus 類別** 物件時，都會具現化執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="f2a97-125">Every time **RealTimeStylus Class** object is instantiated, an execution thread is instantiated.</span></span> <span data-ttu-id="f2a97-126">同步外掛程式是在這個新的執行緒上執行，以針對 **RealTimeStylus 類別** 物件的實例來具現化。</span><span class="sxs-lookup"><span data-stu-id="f2a97-126">Synchronous plug-ins are executed on this new thread instantiated for the instance of the **RealTimeStylus Class** object.</span></span> <span data-ttu-id="f2a97-127">非同步外掛程式是在同步外掛程式處理封包資料流程之後，透過 UI 或應用程式執行緒呼叫，並且儲存在輸出佇列中。</span><span class="sxs-lookup"><span data-stu-id="f2a97-127">Asynchronous plug-ins are called through the UI or application thread after the packet stream has been processed by the synchronous plug-ins and stored in the output queue.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2a97-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2a97-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2a97-129">**IDynamicRenderer 介面**</span><span class="sxs-lookup"><span data-stu-id="f2a97-129">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[<span data-ttu-id="f2a97-130">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="f2a97-130">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[<span data-ttu-id="f2a97-131">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="f2a97-131">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[<span data-ttu-id="f2a97-132">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="f2a97-132">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
