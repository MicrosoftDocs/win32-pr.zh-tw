---
title: 多媒體檔案 i/o 參考
description: 多媒體檔案 i/o 參考
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows 多媒體，檔案 i/o 參考
- 多媒體、檔案 i/o 參考
- 多媒體輸入，file i/o 參考
- 多媒體檔案 i/o，參考
- 檔案 i/o，參考
- 輸入和輸出 (i/o) ，參考
- I/o (輸入和輸出) ，參考
- 多媒體檔案 i/o 參考，關於
- 多媒體檔案 i/o 參考，關於
- 檔案 i/o 參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681737"
---
# <a name="multimedia-file-io-reference"></a><span data-ttu-id="d6390-113">多媒體檔案 i/o 參考</span><span class="sxs-lookup"><span data-stu-id="d6390-113">Multimedia File I/O Reference</span></span>

<span data-ttu-id="d6390-114">本節說明與多媒體檔案輸入和輸出相關聯的函式、宏、訊息和結構。</span><span class="sxs-lookup"><span data-stu-id="d6390-114">This section describes the functions, macros, messages, and structures associated with multimedia file input and output.</span></span> <span data-ttu-id="d6390-115">這些元素的分組方式如下。</span><span class="sxs-lookup"><span data-stu-id="d6390-115">These elements are grouped as follows.</span></span>

## <a name="basic-io"></a><span data-ttu-id="d6390-116">基本 i/o</span><span class="sxs-lookup"><span data-stu-id="d6390-116">Basic I/O</span></span>

-   [<span data-ttu-id="d6390-117">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="d6390-117">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="d6390-118">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="d6390-118">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="d6390-119">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="d6390-119">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="d6390-120">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="d6390-120">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="d6390-121">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="d6390-121">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="d6390-122">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="d6390-122">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a><span data-ttu-id="d6390-123">緩衝的 I/O</span><span class="sxs-lookup"><span data-stu-id="d6390-123">Buffered I/O</span></span>

-   [<span data-ttu-id="d6390-124">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="d6390-124">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="d6390-125">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="d6390-125">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="d6390-126">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="d6390-126">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   <span data-ttu-id="d6390-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6390-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span></span>
-   [<span data-ttu-id="d6390-128">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="d6390-128">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="d6390-129">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="d6390-129">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a><span data-ttu-id="d6390-130">RIFF I/O</span><span class="sxs-lookup"><span data-stu-id="d6390-130">RIFF I/O</span></span>

-   [<span data-ttu-id="d6390-131">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="d6390-131">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="d6390-132">**MMCKINFO**</span><span class="sxs-lookup"><span data-stu-id="d6390-132">**MMCKINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [<span data-ttu-id="d6390-133">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="d6390-133">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="d6390-134">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="d6390-134">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="d6390-135">**mmioFOURCC**</span><span class="sxs-lookup"><span data-stu-id="d6390-135">**mmioFOURCC**</span></span>](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [<span data-ttu-id="d6390-136">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="d6390-136">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a><span data-ttu-id="d6390-137">自訂 i/o 程式</span><span class="sxs-lookup"><span data-stu-id="d6390-137">Custom I/O Procedures</span></span>

-   <span data-ttu-id="d6390-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6390-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="d6390-139">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="d6390-139">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="d6390-140">**MMIOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="d6390-140">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="d6390-141">**MMIOM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="d6390-141">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="d6390-142">**MMIOM \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="d6390-142">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="d6390-143">**MMIOM \_ 重新命名**</span><span class="sxs-lookup"><span data-stu-id="d6390-143">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="d6390-144">**MMIOM \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="d6390-144">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="d6390-145">**MMIOM \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="d6390-145">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="d6390-146">**MMIOM \_ WRITEFLUSH**</span><span class="sxs-lookup"><span data-stu-id="d6390-146">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)
-   [<span data-ttu-id="d6390-147">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="d6390-147">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a><span data-ttu-id="d6390-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6390-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6390-149">多媒體檔案 i/o</span><span class="sxs-lookup"><span data-stu-id="d6390-149">Multimedia File I/O</span></span>](multimedia-file-i-o.md)
</dt> </dl>

 

 