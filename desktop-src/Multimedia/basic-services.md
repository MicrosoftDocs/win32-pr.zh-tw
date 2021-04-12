---
title: 基本服務
description: 基本服務
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- 多媒體檔案 i/o，基本服務
- 檔案 i/o、基本服務
- 輸入和輸出 (i/o) ，基本服務
- I/o (輸入和輸出) 、基本服務
- 基本 i/o
- mmioOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375237"
---
# <a name="basic-services"></a><span data-ttu-id="2b7d9-109">基本服務</span><span class="sxs-lookup"><span data-stu-id="2b7d9-109">Basic Services</span></span>

<span data-ttu-id="2b7d9-110">使用基本的 i/o 服務，類似于使用 C 執行時間程式庫的執行時間檔案 i/o 服務。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-110">Using the basic I/O services is similar to using the run-time file I/O services of the C run-time library.</span></span> <span data-ttu-id="2b7d9-111">必須先開啟檔案，才能讀取或寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-111">Files must be opened before they can be read or written.</span></span> <span data-ttu-id="2b7d9-112">讀取或寫入之後，必須關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-112">After reading or writing, the file must be closed.</span></span> <span data-ttu-id="2b7d9-113">您也可以在開啟的檔案內變更目前的讀取或寫入位置。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-113">You can also change the current read or write location within an open file.</span></span>

<span data-ttu-id="2b7d9-114">在您開始對檔案進行任何 i/o 作業之前，必須先使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函式來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-114">Before you begin any I/O operations to a file, you must open the file by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="2b7d9-115">此函數會傳回 **HMMIO** 類型的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-115">This function returns a file handle of type **HMMIO**.</span></span> <span data-ttu-id="2b7d9-116">呼叫其他檔案 i/o 函式時，您可以使用此檔案控制代碼來識別開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-116">You can use this file handle to identify the open file when calling other file I/O functions.</span></span>

> [!Note]  
> <span data-ttu-id="2b7d9-117">**HMMIO** 檔案控制代碼不是標準檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-117">An **HMMIO** file handle is not a standard file handle.</span></span> <span data-ttu-id="2b7d9-118">請勿搭配 Win32 或 C 執行時間檔案 i/o 函數使用 **HMMIO** 檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-118">Do not use **HMMIO** file handles with Win32 or C run-time file I/O functions.</span></span>

 

<span data-ttu-id="2b7d9-119">當您使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 開啟檔案時，您可以使用旗標來指定是否要開啟它以進行讀取、寫入或兩者。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-119">When you use [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) to open a file, you use a flag to specify whether you are opening it for reading, writing, or both.</span></span> <span data-ttu-id="2b7d9-120">您也可以指定旗標，讓您建立或刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-120">You can also specify flags that enable you to create or delete a file.</span></span> <span data-ttu-id="2b7d9-121">當您完成讀取或寫入檔案時，請使用 [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) 函數來關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-121">Use the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to close a file when you are finished reading or writing to it.</span></span>

<span data-ttu-id="2b7d9-122">您可以分別使用 [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) 和 [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) 函數來讀取和寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-122">You can read and write files by using the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) and [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) functions respectively.</span></span> <span data-ttu-id="2b7d9-123">下一個讀取或寫入作業會發生在檔案中目前的檔案位置或檔案指標。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-123">The next read or write operation occurs at the current file position or file pointer in a file.</span></span> <span data-ttu-id="2b7d9-124">每次讀取或寫入檔案時，目前的檔案位置都是 advanced。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-124">The current file position is advanced each time a file is read or written.</span></span>

<span data-ttu-id="2b7d9-125">您也可以使用 [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) 函數來變更目前的檔案位置。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-125">You can also change the current file position by using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span> <span data-ttu-id="2b7d9-126">您應確定在檔案中指定有效的位置。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-126">You should ensure that you specify a valid location in a file.</span></span> <span data-ttu-id="2b7d9-127">如果您指定了不正確位置，例如超過檔案結尾， **mmioSeek** 可能不會傳回錯誤，但後續的 i/o 作業可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-127">If you specify an invalid location, such as past the end of the file, **mmioSeek** may not return an error, but subsequent I/O operations could fail.</span></span>

<span data-ttu-id="2b7d9-128">您可以針對基本檔案 i/o 以外的作業使用 **mmioOpen** 函式的旗標。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-128">There are flags you can use with the **mmioOpen** function for operations beyond basic file I/O.</span></span> <span data-ttu-id="2b7d9-129">例如，您可以藉由指定 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構來開啟記憶體檔案、指定自訂的 i/o 程式，或為緩衝的 i/o 提供緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2b7d9-129">By specifying an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure, for example, you can open memory files, specify a custom I/O procedure, or supply a buffer for buffered I/O.</span></span>

 

 