---
title: 編輯資料流程
description: 編輯資料流程
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- CreateEditableStream 函式
- EditStreamCut 函式
- EditStreamCopy 函式
- EditStreamPaste 函式
- EditStreamClone 函式
- EditStreamSetInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462317"
---
# <a name="editing-streams"></a><span data-ttu-id="0b381-109">編輯資料流程</span><span class="sxs-lookup"><span data-stu-id="0b381-109">Editing Streams</span></span>

<span data-ttu-id="0b381-110">您可以使用 [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) 函式來建立可編輯的資料流程。</span><span class="sxs-lookup"><span data-stu-id="0b381-110">You can create a stream that you can edit by using the [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) function.</span></span> <span data-ttu-id="0b381-111">此函式會初始化用來編輯資料流程的環境。</span><span class="sxs-lookup"><span data-stu-id="0b381-111">This function initializes the environment for editing a stream.</span></span> <span data-ttu-id="0b381-112">這包括建立新資料流程的介面，以及追蹤對資料流程所做之變更的內部編輯資料表。</span><span class="sxs-lookup"><span data-stu-id="0b381-112">This includes creating an interface to the new stream, and internal edit tables that track changes made to the stream.</span></span> <span data-ttu-id="0b381-113">**CreateEditableStream** 會將資料流程指標傳回給其他資料流程編輯函數所需的可編輯資料流程。</span><span class="sxs-lookup"><span data-stu-id="0b381-113">**CreateEditableStream** returns a stream pointer to an editable stream that is required by other stream-editing functions.</span></span> <span data-ttu-id="0b381-114">可編輯的資料流程指標也可供接受資料流程指標的其他 AVIFile 函式使用。</span><span class="sxs-lookup"><span data-stu-id="0b381-114">The editable stream pointer can also be used by other AVIFile functions that accept stream pointers.</span></span>

<span data-ttu-id="0b381-115">您可以使用 [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) 函數，從可編輯的資料流程中剪下一或多個範例。</span><span class="sxs-lookup"><span data-stu-id="0b381-115">You can cut one or more samples from an editable stream by using the [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) function.</span></span> <span data-ttu-id="0b381-116">若要從可編輯的資料流程移除範例，此函式會將專案加入至編輯資料表。</span><span class="sxs-lookup"><span data-stu-id="0b381-116">To remove samples from the editable stream, this function adds an entry to the edit table.</span></span> <span data-ttu-id="0b381-117">然後，此函式會在新的暫存資料流程中放置剪下範例的複本，而此資料流程的介面指標會在變數中傳回。</span><span class="sxs-lookup"><span data-stu-id="0b381-117">The function then places a copy of the cut samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="0b381-118">您可以使用 [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) 函式，將一個或多個範例從可編輯的資料流程複製到暫存資料流程。</span><span class="sxs-lookup"><span data-stu-id="0b381-118">You can copy one or more samples from an editable stream into a temporary stream by using the [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) function.</span></span> <span data-ttu-id="0b381-119">**EditStreamCopy** 會將範例的複本放在新的暫存資料流程中，其介面指標會在變數中傳回。</span><span class="sxs-lookup"><span data-stu-id="0b381-119">**EditStreamCopy** places copies of the samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="0b381-120">您可以從資料流程複製一或多個範例，並使用 [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) 函式將它們貼到可編輯的資料流程中。</span><span class="sxs-lookup"><span data-stu-id="0b381-120">You can copy one or more samples from a stream and paste them into an editable stream by using the [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) function.</span></span> <span data-ttu-id="0b381-121">若要在指定的位置插入範例，此函式會在目標可編輯資料流程的編輯資料表中新增專案。</span><span class="sxs-lookup"><span data-stu-id="0b381-121">To insert the samples at the specified position, this function adds an entry in the edit table of the target editable stream.</span></span>

<span data-ttu-id="0b381-122">您可以使用 [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) 函數來複製可編輯的資料流程。</span><span class="sxs-lookup"><span data-stu-id="0b381-122">You can duplicate an editable stream by using the [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) function.</span></span> <span data-ttu-id="0b381-123">此函式會傳回新資料流程的資料流程介面指標。</span><span class="sxs-lookup"><span data-stu-id="0b381-123">This function returns a pointer to the stream interface of the new stream.</span></span> <span data-ttu-id="0b381-124">您可以將這些資料流程複製到剪貼簿，或使用它們來維護對資料流程所做的編輯記錄。</span><span class="sxs-lookup"><span data-stu-id="0b381-124">You can copy these streams to the clipboard or use them to maintain a trail of edits made to a stream.</span></span>

<span data-ttu-id="0b381-125">您可以使用 [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) 函數來變更可編輯資料流程的數個特性。</span><span class="sxs-lookup"><span data-stu-id="0b381-125">You can change several of the characteristics of an editable stream by using the [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) function.</span></span> <span data-ttu-id="0b381-126">此函式會更新優先權設定、語言、縮放和速率、開始時間、品質設定、目的地矩形維度和座標，以及資料流程的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0b381-126">This function updates the priority setting, language, scale and rate, starting time, quality setting, destination rectangle dimensions and coordinates, and the textual description of the stream.</span></span> <span data-ttu-id="0b381-127">這些專案會儲存在與可編輯資料流程相關聯的 [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) 結構中。</span><span class="sxs-lookup"><span data-stu-id="0b381-127">These items are stored in the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure associated with the editable stream.</span></span>

<span data-ttu-id="0b381-128">您也可以使用 [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) 函數來變更可編輯資料流程的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0b381-128">You can also change the textual description of an editable stream by using the [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) function.</span></span> <span data-ttu-id="0b381-129">此函數會更新與可編輯資料流程相關聯之 **AVISTREAMINFO** 結構的 **>szname** 成員。</span><span class="sxs-lookup"><span data-stu-id="0b381-129">This function updates the **szName** member of the **AVISTREAMINFO** structure associated with the editable stream.</span></span>

<span data-ttu-id="0b381-130">編輯函數可用於資料流程。</span><span class="sxs-lookup"><span data-stu-id="0b381-130">The editing functions work on streams.</span></span> <span data-ttu-id="0b381-131">您必須個別剪下並貼上每個資料流程，然後使用 [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) 函式來建立新的檔案指標。</span><span class="sxs-lookup"><span data-stu-id="0b381-131">You need to cut and paste each stream individually, and then use the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function to create a new file pointer.</span></span>

> [!Note]  
> <span data-ttu-id="0b381-132">可編輯資料流程中的編輯資料表會維護資料流程的所有變更。</span><span class="sxs-lookup"><span data-stu-id="0b381-132">The edit tables in an editable stream maintain all the changes for a stream.</span></span> <span data-ttu-id="0b381-133">來來源資料流永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="0b381-133">The source stream is never changed.</span></span>

 

 

 




