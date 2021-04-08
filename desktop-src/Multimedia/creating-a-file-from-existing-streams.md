---
title: 從現有的資料流程建立檔案
description: 從現有的資料流程建立檔案
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- AVISave 函式
- AVISaveV 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc422d2170ccd49b8a9746666db7ebbcd7dff14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932135"
---
# <a name="creating-a-file-from-existing-streams"></a><span data-ttu-id="630c1-105">從現有的資料流程建立檔案</span><span class="sxs-lookup"><span data-stu-id="630c1-105">Creating a File from Existing Streams</span></span>

<span data-ttu-id="630c1-106">建立包含資料流程之檔案的其中一種方式，是將現有的資料流程合併成新的檔案。</span><span class="sxs-lookup"><span data-stu-id="630c1-106">One way to create a file that contains data streams is to combine existing streams into a new file.</span></span> <span data-ttu-id="630c1-107">提供新檔案之資料的資料流程可以位於記憶體或一或多個檔案中。</span><span class="sxs-lookup"><span data-stu-id="630c1-107">The streams that provide data for the new file can reside in memory or in one or more files.</span></span>

<span data-ttu-id="630c1-108">您可以使用 [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) 函數，從數個數據流建立檔案。</span><span class="sxs-lookup"><span data-stu-id="630c1-108">You can build a file from several streams by using the [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) function.</span></span> <span data-ttu-id="630c1-109">此函式會建立檔案，並將其呼叫順序中指定的資料流程寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="630c1-109">This function creates a file and writes the data streams specified in its calling sequence to the file.</span></span> <span data-ttu-id="630c1-110">**AVISave** 的呼叫序列會使用引數數目的引數，這些引數包含在新檔案中結合之資料流程的介面。</span><span class="sxs-lookup"><span data-stu-id="630c1-110">The calling sequence for **AVISave** uses a variable number of arguments that include interfaces for the streams combined in the new file.</span></span>

<span data-ttu-id="630c1-111">您也可以使用 [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) 函式，將資料流程合併在新的檔案中。</span><span class="sxs-lookup"><span data-stu-id="630c1-111">You can also combine data streams in a new file by using the [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) function.</span></span> <span data-ttu-id="630c1-112">此函式提供與 **AVISave** 相同的功能，但是當您使用 **AVISaveV** 時，您的應用程式會將資料流程指定為數組，而不是變數數目的引數。</span><span class="sxs-lookup"><span data-stu-id="630c1-112">This function provides the same functionality as **AVISave**, but when you use **AVISaveV**, your application specifies the data streams as an array, not as a variable number of arguments.</span></span>

<span data-ttu-id="630c1-113">您可以建立一個對話方塊，讓使用者可以使用 [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) 函數來選取新檔案的壓縮設定。</span><span class="sxs-lookup"><span data-stu-id="630c1-113">You can create a dialog box in which the user can select compression settings for the new file by using the [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) function.</span></span> <span data-ttu-id="630c1-114">對話方塊會顯示目前的壓縮設定，並讓使用者編輯這些設定。</span><span class="sxs-lookup"><span data-stu-id="630c1-114">The dialog box displays the current compression settings and lets the user edit them.</span></span> <span data-ttu-id="630c1-115">壓縮設定變更會儲存在 [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) 結構中。</span><span class="sxs-lookup"><span data-stu-id="630c1-115">Compression setting changes are stored in an [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) structure.</span></span>

<span data-ttu-id="630c1-116">您也可以加入具有 [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) 和 [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) 的回呼函式，讓您的應用程式用來顯示寫入檔案的進度，如有需要，可讓使用者取消儲存作業。</span><span class="sxs-lookup"><span data-stu-id="630c1-116">You can also include a callback function with [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) and [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) that your application can use to display the progress of writing the file and, if needed, let the user cancel the save operation.</span></span> <span data-ttu-id="630c1-117">您可以在 **AVISave** 或 **AVISaveV** 的呼叫順序中包含回呼函式的位址。</span><span class="sxs-lookup"><span data-stu-id="630c1-117">You can include the address of the callback function in the calling sequence of **AVISave** or **AVISaveV**.</span></span>

<span data-ttu-id="630c1-118">您可以讓使用者使用 [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) 函式來選取新檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="630c1-118">You can let the user select a filename for the new file by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function.</span></span> <span data-ttu-id="630c1-119">此函式會顯示 [另存新檔] 對話方塊，讓使用者可以在其中預覽 AVI 檔案的影片資料流程) 的第一個串流 (。</span><span class="sxs-lookup"><span data-stu-id="630c1-119">This function displays the Save As dialog box in which the user can preview the first stream (normally the video stream) of an AVI file.</span></span>

<span data-ttu-id="630c1-120">您可以使用 [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) 函式來建立檔案介面指標 (以及一組資料流程的虛擬檔案) 。</span><span class="sxs-lookup"><span data-stu-id="630c1-120">You can create a file interface pointer (and a virtual file) for a group of streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="630c1-121">其他 AVIFile 函式可以使用此函式所傳回的檔案介面指標，來存取虛擬檔案中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="630c1-121">Other AVIFile functions can use the file interface pointer returned by this function to access the streams in the virtual file.</span></span> <span data-ttu-id="630c1-122">當您使用完虛擬檔案之後，請使用 [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) 函數來刪除檔案介面指標。</span><span class="sxs-lookup"><span data-stu-id="630c1-122">After you finish using the virtual file, delete the file interface pointer by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span>

> [!Note]  
> <span data-ttu-id="630c1-123">若要將影像和音訊效能降至最低，請避免壓縮 AVI 檔案一次以上。</span><span class="sxs-lookup"><span data-stu-id="630c1-123">To minimize image and audio degradation, avoid compressing an AVI file more than once.</span></span> <span data-ttu-id="630c1-124">在編輯系統中結合未壓縮的部分影片，然後壓縮最終產品。</span><span class="sxs-lookup"><span data-stu-id="630c1-124">Combine uncompressed pieces of video in your editing system and then compress the final product.</span></span> <span data-ttu-id="630c1-125">如需壓縮選項的詳細資訊，請參閱 [影片壓縮管理員](video-compression-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="630c1-125">For information about compression options, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 

 




