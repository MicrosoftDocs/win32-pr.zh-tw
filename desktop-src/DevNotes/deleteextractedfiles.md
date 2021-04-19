---
description: DeleteExtractedFiles 函式會刪除解壓縮函數所解壓縮的檔案。
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989584"
---
# <a name="deleteextractedfiles-function"></a><span data-ttu-id="f3432-103">DeleteExtractedFiles 函式</span><span class="sxs-lookup"><span data-stu-id="f3432-103">DeleteExtractedFiles function</span></span>

<span data-ttu-id="f3432-104">\[不再支援此函式，因此無法保證其行為。\]</span><span class="sxs-lookup"><span data-stu-id="f3432-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="f3432-105">**DeleteExtractedFiles** 函式會刪除 [**解壓縮**](extract.md)函數所解壓縮的檔案。</span><span class="sxs-lookup"><span data-stu-id="f3432-105">The **DeleteExtractedFiles** function deletes the files that were extracted by the [**Extract**](extract.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3432-106">語法</span><span class="sxs-lookup"><span data-stu-id="f3432-106">Syntax</span></span>


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a><span data-ttu-id="f3432-107">參數</span><span class="sxs-lookup"><span data-stu-id="f3432-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3432-108">*Ps*</span><span class="sxs-lookup"><span data-stu-id="f3432-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="f3432-109">[**會話**](session.md)結構的指標，其中包含目前會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3432-109">A pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

<span data-ttu-id="f3432-110">此函式會釋出此結構之 **pFileList** 成員中的記憶體，並將 **PFileList** 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3432-110">This function frees the memory in the **pFileList** member of this structure and sets **pFileList** to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3432-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3432-111">Return value</span></span>

<span data-ttu-id="f3432-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f3432-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3432-113">備註</span><span class="sxs-lookup"><span data-stu-id="f3432-113">Remarks</span></span>

<span data-ttu-id="f3432-114">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="f3432-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3432-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3432-115">Requirements</span></span>



| <span data-ttu-id="f3432-116">需求</span><span class="sxs-lookup"><span data-stu-id="f3432-116">Requirement</span></span> | <span data-ttu-id="f3432-117">值</span><span class="sxs-lookup"><span data-stu-id="f3432-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3432-118">DLL</span><span class="sxs-lookup"><span data-stu-id="f3432-118">DLL</span></span><br/> | <dl> <span data-ttu-id="f3432-119"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3432-119"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3432-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3432-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3432-121">**提取**</span><span class="sxs-lookup"><span data-stu-id="f3432-121">**Extract**</span></span>](extract.md)
</dt> <dt>

[<span data-ttu-id="f3432-122">**會話**</span><span class="sxs-lookup"><span data-stu-id="f3432-122">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
