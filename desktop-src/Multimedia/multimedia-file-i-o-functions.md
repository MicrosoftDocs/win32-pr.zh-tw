---
title: 多媒體檔案 i/o 函數
description: 多媒體檔案 i/o 函數
ms.assetid: a5d51906-881f-4fe0-a988-c10776a3b40d
keywords:
- Windows 多媒體，檔案 i/o 函數
- 多媒體，檔案 i/o 函數
- 多媒體輸入，file i/o 函數
- 多媒體檔案 i/o，函數
- 檔案 i/o，函數
- 輸入和輸出 (i/o) ，函數
- I/o (輸入和輸出) ，函數
- 多媒體檔案 i/o 的參考，函數
- 多媒體檔案 i/o 參考，函數
- 檔案 i/o 參考，函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62b8daf8e84953acebcca9106165f27b350ef2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507875"
---
# <a name="multimedia-file-io-functions"></a><span data-ttu-id="4f255-113">多媒體檔案 i/o 函數</span><span class="sxs-lookup"><span data-stu-id="4f255-113">Multimedia File I/O Functions</span></span>

<span data-ttu-id="4f255-114">下列函式用於多媒體檔案 i/o。</span><span class="sxs-lookup"><span data-stu-id="4f255-114">The following functions are used with multimedia file I/O.</span></span>

-   <span data-ttu-id="4f255-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f255-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="4f255-116">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="4f255-116">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="4f255-117">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="4f255-117">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="4f255-118">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="4f255-118">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="4f255-119">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="4f255-119">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="4f255-120">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="4f255-120">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="4f255-121">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="4f255-121">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="4f255-122">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="4f255-122">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [<span data-ttu-id="4f255-123">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="4f255-123">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="4f255-124">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="4f255-124">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="4f255-125">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="4f255-125">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="4f255-126">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="4f255-126">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="4f255-127">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="4f255-127">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="4f255-128">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="4f255-128">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)
-   [<span data-ttu-id="4f255-129">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="4f255-129">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="4f255-130">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="4f255-130">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)
-   [<span data-ttu-id="4f255-131">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="4f255-131">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)
-   [<span data-ttu-id="4f255-132">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="4f255-132">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="related-topics"></a><span data-ttu-id="4f255-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f255-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f255-134">多媒體檔案 i/o 參考</span><span class="sxs-lookup"><span data-stu-id="4f255-134">Multimedia File I/O Reference</span></span>](multimedia-file-i-o-reference.md)
</dt> </dl>

 

 