---
description: RealTimeStylus 類別可讓您從 tablet 畫筆與資料流程進行互動。 若要與資料流程互動，請將 RealTimeStylus 物件新增至您的應用程式，並將外掛程式加入至 RealTimeStylus 物件。
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: 使用 StylusInput Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676752f242aa428b583390d7c3d38c952b4c0edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970596"
---
# <a name="working-with-the-stylusinput-apis"></a><span data-ttu-id="ee60b-104">使用 StylusInput Api</span><span class="sxs-lookup"><span data-stu-id="ee60b-104">Working with the StylusInput APIs</span></span>

<span data-ttu-id="ee60b-105">[**RealTimeStylus**](realtimestylus-class.md)類別可讓您從 tablet 畫筆與資料流程進行互動。</span><span class="sxs-lookup"><span data-stu-id="ee60b-105">The [**RealTimeStylus**](realtimestylus-class.md) class enables you to interact with the data stream from the tablet pen.</span></span> <span data-ttu-id="ee60b-106">若要與資料流程互動，請將 **RealTimeStylus** 物件新增至您的應用程式，並將外掛程式加入至 **RealTimeStylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="ee60b-106">To interact with the data stream, add a **RealTimeStylus** object to your application, and add plug-ins to the **RealTimeStylus** object.</span></span>

<span data-ttu-id="ee60b-107">外掛程式可以修改與空中封包、手寫筆向下、封包和手寫筆向上通知方法相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="ee60b-107">The plug-ins can modify the data associated with in-air packets, stylus down, packets, and stylus up notification methods.</span></span> <span data-ttu-id="ee60b-108">外掛程式可以取消無線封包和封包通知方法。</span><span class="sxs-lookup"><span data-stu-id="ee60b-108">The plug-ins can cancel the in-air packets and packets notification methods.</span></span> <span data-ttu-id="ee60b-109">外掛程式也可以將應用程式資料以 [CustomStylusData](/previous-versions/ms575208(v=vs.100)) 物件的形式新增至資料流程。</span><span class="sxs-lookup"><span data-stu-id="ee60b-109">The plug-ins can also add application data to the stream in the form of [CustomStylusData](/previous-versions/ms575208(v=vs.100)) objects.</span></span> <span data-ttu-id="ee60b-110">下列清單提供您可能想要使用或建立之常用外掛程式類別的概念。</span><span class="sxs-lookup"><span data-stu-id="ee60b-110">The following list offers ideas for common categories of plug-ins that you may want to use or create.</span></span>

-   <span data-ttu-id="ee60b-111">篩選外掛程式：選擇性地移除或取消 tablet 畫筆資料流程中資料的物件。</span><span class="sxs-lookup"><span data-stu-id="ee60b-111">Filter plug-in: An object that selectively removes or cancels data in the tablet pen data stream.</span></span>
-   <span data-ttu-id="ee60b-112">修飾詞外掛程式：選擇性地修改 tablet 畫筆資料串流中資料的物件。</span><span class="sxs-lookup"><span data-stu-id="ee60b-112">Modifier plug-in: An object that selectively modifies data in the tablet pen data stream.</span></span>
-   <span data-ttu-id="ee60b-113">動態轉譯器外掛程式：此物件會即時顯示 tablet 畫筆資料，因為它正由 [**RealTimeStylus**](realtimestylus-class.md) 物件處理。</span><span class="sxs-lookup"><span data-stu-id="ee60b-113">Dynamic-renderer plug-in: An object that displays the tablet pen data in real-time as it is being handled by the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="ee60b-114">之後，如果是表單重新整理之類的事件，動態轉譯器外掛程式或筆跡集合外掛程式可能會重繪筆墨。</span><span class="sxs-lookup"><span data-stu-id="ee60b-114">Later, for events such as a form refresh, the dynamic renderer plug-in or an ink collection plug-in might redraw the ink.</span></span>
-   <span data-ttu-id="ee60b-115">辨識器外掛程式：掃描 tablet 畫筆移動筆勢、手寫或其他字元的物件。</span><span class="sxs-lookup"><span data-stu-id="ee60b-115">Recognizer plug-in: An object that scans the movement of the tablet pen for gestures, handwriting, or other glyphs.</span></span>
-   <span data-ttu-id="ee60b-116">筆墨收集器外掛程式：來自 tablet 畫筆資料流程的物件會建立和儲存筆跡。</span><span class="sxs-lookup"><span data-stu-id="ee60b-116">Ink-collector plug-in: An object that from the tablet pen data stream creates and stores ink.</span></span>
-   <span data-ttu-id="ee60b-117">包裝函式外掛程式：一種外掛程式，可作為 [**RealTimeStylus**](realtimestylus-class.md) 物件與另一個外掛程式或物件之間的介面，以修改包裝物件的行為。</span><span class="sxs-lookup"><span data-stu-id="ee60b-117">Wrapper plug-in: A plug-in that acts as an interface between the [**RealTimeStylus**](realtimestylus-class.md) object and another plug-in or object as a way of modifying the behavior of the wrapped object.</span></span>

<span data-ttu-id="ee60b-118">您可以建立動態轉譯器和筆墨集合外掛程式，以轉譯成各種內容，例如檔案、資料流程或顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="ee60b-118">Both dynamic-renderer and ink-collection plug-ins can be created to render to various contexts—such as to a file, a stream, or to a display device.</span></span> <span data-ttu-id="ee60b-119">筆墨也可以不同的格式儲存，例如 [筆墨](/previous-versions/aa515768(v=msdn.10)) 物件、嚴加防禦圖形交換格式 (GIF) 檔、筆跡序列化格式 (ISF) 檔或其他格式。</span><span class="sxs-lookup"><span data-stu-id="ee60b-119">Ink can also be stored in various formats, such as an [Ink](/previous-versions/aa515768(v=msdn.10)) object, a fortified Graphics Interchange Format (GIF) file, an Ink Serialized Format (ISF) file, or other formats.</span></span>

<span data-ttu-id="ee60b-120">StylusInput Api 提供兩個外掛程式： [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) 類別和 [**GestureRecognizer**](gesturerecognizer-class.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="ee60b-120">Two plug-ins are provided with the StylusInput APIs: the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) class and the [**GestureRecognizer**](gesturerecognizer-class.md) class.</span></span> <span data-ttu-id="ee60b-121">**DynamicRenderer** 類別會即時提供筆跡資料的基本轉譯，並且經過簡化，以對效能造成最大的影響。</span><span class="sxs-lookup"><span data-stu-id="ee60b-121">The **DynamicRenderer** class provides basic rendering of the ink data in real time and is streamlined to have a minimal performance impact.</span></span> <span data-ttu-id="ee60b-122">**GestureRecognizer** 類別提供 [**RealTimeStylus**](realtimestylus-class.md)類別的手勢辨識。</span><span class="sxs-lookup"><span data-stu-id="ee60b-122">The **GestureRecognizer** class provides gesture recognition for the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ee60b-123">本節內容</span><span class="sxs-lookup"><span data-stu-id="ee60b-123">In This Section</span></span>

-   [<span data-ttu-id="ee60b-124">使用 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="ee60b-124">Working with the RealTimeStylus Class</span></span>](working-with-the-realtimestylus-class.md)
-   [<span data-ttu-id="ee60b-125">外掛程式和 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="ee60b-125">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
-   [<span data-ttu-id="ee60b-126">外掛程式資料和 RealTimeStylus 類別</span><span class="sxs-lookup"><span data-stu-id="ee60b-126">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
-   [<span data-ttu-id="ee60b-127">StylusInput Api 的執行注意事項</span><span class="sxs-lookup"><span data-stu-id="ee60b-127">Implementation Notes for the StylusInput APIs</span></span>](implementation-notes-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="ee60b-128">筆墨-集合外掛程式</span><span class="sxs-lookup"><span data-stu-id="ee60b-128">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
-   [<span data-ttu-id="ee60b-129">動態轉譯器外掛程式</span><span class="sxs-lookup"><span data-stu-id="ee60b-129">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
-   [<span data-ttu-id="ee60b-130">辨識器外掛程式</span><span class="sxs-lookup"><span data-stu-id="ee60b-130">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)

 

 
