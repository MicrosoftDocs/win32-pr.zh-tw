---
title: 執行 In-Place 啟用
description: 執行 In-Place 啟用
ms.assetid: 5fd67d1c-1dc5-4d83-a41e-b64d84cbf212
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c075f143c772fe34de0c494664227e892b998387
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968231"
---
# <a name="implementing-in-place-activation"></a><span data-ttu-id="0ddef-103">執行 In-Place 啟用</span><span class="sxs-lookup"><span data-stu-id="0ddef-103">Implementing In-Place Activation</span></span>

<span data-ttu-id="0ddef-104">就地啟用可讓使用者與内嵌物件互動，而不需要離開容器檔案。</span><span class="sxs-lookup"><span data-stu-id="0ddef-104">In-place activation enables a user to interact with an embedded object without leaving the container document.</span></span> <span data-ttu-id="0ddef-105">當使用者啟始物件時，由容器應用程式和伺服器應用程式功能表列中的元素組成的 *複合功能表列* ，會取代容器的主功能表列。</span><span class="sxs-lookup"><span data-stu-id="0ddef-105">When a user activates the object, a *composite menu bar* comprising elements from both the container application's and server application's menu bars replaces the container's main menu bar.</span></span> <span data-ttu-id="0ddef-106">這兩個應用程式的命令和功能，可供使用者使用，包括作用中物件的內容相關說明。</span><span class="sxs-lookup"><span data-stu-id="0ddef-106">Commands and features from both applications are thus available to the user, including context sensitive help for the active object.</span></span> <span data-ttu-id="0ddef-107">當使用者開始使用部分非物件部分的檔時，會停用該物件，使容器檔案的原始功能表取代複合功能表。</span><span class="sxs-lookup"><span data-stu-id="0ddef-107">When a user begins working with some non-object portion of the document, the object is deactivated, causing the container document's original menu to replace the composite menu.</span></span>

<span data-ttu-id="0ddef-108">這項功能最初是依 *就地編輯* 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ddef-108">This capability originally went by the name of *in-place editing*.</span></span> <span data-ttu-id="0ddef-109">名稱已變更，因為編輯只是使用者與執行中物件互動的一種方式。</span><span class="sxs-lookup"><span data-stu-id="0ddef-109">The name was changed because editing is only one way for a user to interact with a running object.</span></span> <span data-ttu-id="0ddef-110">例如，您可以聆聽音效片段，而不是編輯。</span><span class="sxs-lookup"><span data-stu-id="0ddef-110">Sound clips, for example, can be listened to instead of editing.</span></span> <span data-ttu-id="0ddef-111">影片剪輯可以用來流覽，而不是編輯。</span><span class="sxs-lookup"><span data-stu-id="0ddef-111">Video clips can be viewed instead of editing.</span></span> <span data-ttu-id="0ddef-112">在影片剪輯時，就地啟用特別 apt，因為它可讓它們就地執行，而不需要呼叫另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="0ddef-112">In-place activation is particularly apt in the case of video clips because it allows them to run in place, without calling up a separate window.</span></span> <span data-ttu-id="0ddef-113">如果影片是與容器檔案中的相鄰文字資料一起查看，這可能是很重要的。</span><span class="sxs-lookup"><span data-stu-id="0ddef-113">This could be critical if the video were to be viewed, say, in conjunction with adjacent text data in the container document.</span></span>

<span data-ttu-id="0ddef-114">容器和伺服器應用程式的就地啟用完全是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0ddef-114">Implementing in-place activation is strictly optional for both container and server applications.</span></span> <span data-ttu-id="0ddef-115">OLE 仍然支援模型，在此模型中啟始物件會導致伺服器應用程式開啟另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="0ddef-115">OLE still supports the model in which activating an object causes the server application to open a separate window.</span></span> <span data-ttu-id="0ddef-116">連結化物件一律會在個別的視窗中開啟，以強調它們位於不同的檔中。</span><span class="sxs-lookup"><span data-stu-id="0ddef-116">Linked objects always open in a separate window to emphasize that they reside in a separate document.</span></span>

<span data-ttu-id="0ddef-117">就地啟用會從物件開始，以回應 IOleObject：從其容器 [**:D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0ddef-117">In-place activation begins with the object in response to an [**IOleObject::DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) call from its container.</span></span> <span data-ttu-id="0ddef-118">此呼叫通常是為了回應使用者按兩下物件，或是從容器應用程式的 [編輯] 功能表中選取命令 (動詞) 。</span><span class="sxs-lookup"><span data-stu-id="0ddef-118">This call usually happens in response to a user double-clicking the object or selecting a command (verb) from the container application's Edit menu.</span></span>

<span data-ttu-id="0ddef-119">當内嵌物件為使用中時，就地視窗會接收鍵盤和滑鼠輸入。</span><span class="sxs-lookup"><span data-stu-id="0ddef-119">The in-place window receives keyboard and mouse input while the embedded object is active.</span></span> <span data-ttu-id="0ddef-120">當使用者從複合功能表列選取命令時，會將命令和相關聯的功能表訊息傳送至容器或物件應用程式，這取決於所選取的特定下拉式功能表。</span><span class="sxs-lookup"><span data-stu-id="0ddef-120">When a user selects commands from the composite menu bar, the command and associated menu messages are sent to the container or object application, depending on which owns the particular drop-down menu selected.</span></span> <span data-ttu-id="0ddef-121">透過物件的尺規、工具列或框架裝飾的輸入，會直接移至擁有這些視窗的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="0ddef-121">Input by means of an object's rulers, toolbars, or frame adornments go directly to the embedded object, which owns these windows.</span></span>

<span data-ttu-id="0ddef-122">就地啟動的内嵌物件會保持作用中，直到容器將它停用以回應使用者輸入，或物件可主動達成作用中狀態時，例如影片剪輯可能會有作用。</span><span class="sxs-lookup"><span data-stu-id="0ddef-122">An in-place-activated embedded object remains active until either the container deactivates it in response to user input or the object voluntarily gives up the active state, as a video clip might do, for example.</span></span> <span data-ttu-id="0ddef-123">使用者可以在容器檔案內部按一下，但在物件的就地啟用視窗之外，或按一下其他物件來停用物件。</span><span class="sxs-lookup"><span data-stu-id="0ddef-123">A user can deactivate an object by clicking inside the container document but outside the object's in-place-activation window, or simply by clicking another object.</span></span> <span data-ttu-id="0ddef-124">但是，如果使用者按一下容器的標題列、捲軸或特別是功能表列，則就地啟動的物件會維持作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="0ddef-124">An in-place-activated object remains active, however, if the user clicks the container's title bar, scroll bar or, in particular, menu bar.</span></span>

<span data-ttu-id="0ddef-125">您可以將就地啟始物件伺服器視為同進程伺服器 (DLL) 或本機伺服器 (EXE) 。</span><span class="sxs-lookup"><span data-stu-id="0ddef-125">You can implement an in-place-activation-object server either as an in-process server (DLL) or a local server (EXE).</span></span> <span data-ttu-id="0ddef-126">在這兩種情況下，複合功能表列包含的專案 (通常是從伺服器和容器進程) 的下拉式功能表。</span><span class="sxs-lookup"><span data-stu-id="0ddef-126">In both cases, the composite menu bar contains items (typically drop-down menus) from both the server and container processes.</span></span> <span data-ttu-id="0ddef-127">在同進程伺服器的案例中，就地啟用視窗只是容器的視窗階層中的另一個子視窗，會透過容器應用程式的訊息提取接收其輸入。</span><span class="sxs-lookup"><span data-stu-id="0ddef-127">In the case of a in-process server, the in-place activation window is simply another child window in the container's window hierarchy, receiving its input through the container application's message pump.</span></span>

<span data-ttu-id="0ddef-128">在本機伺服器的案例中，就地啟用視窗屬於内嵌物件的伺服器應用程式進程，但其父視窗屬於容器。</span><span class="sxs-lookup"><span data-stu-id="0ddef-128">In the case of a local server, the in-place activation window belongs to the embedded object's server application process, but its parent window belongs to the container.</span></span> <span data-ttu-id="0ddef-129">就地啟動視窗的輸入會顯示在伺服器的訊息佇列中，並且由伺服器的訊息迴圈分派。</span><span class="sxs-lookup"><span data-stu-id="0ddef-129">Input for the in-place-activation window appears in the server's message queue and is dispatched by the server's message loop.</span></span> <span data-ttu-id="0ddef-130">OLE 程式庫會負責查看功能表命令和訊息是否已正確分派。</span><span class="sxs-lookup"><span data-stu-id="0ddef-130">The OLE libraries are responsible for seeing to it that menu commands and messages are dispatched correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ddef-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ddef-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ddef-132">複合檔案</span><span class="sxs-lookup"><span data-stu-id="0ddef-132">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




