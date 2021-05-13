---
description: 由檔案管理員延伸模組所傳送，可從 [active 檔案管理員] 視窗中取出所選檔案的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。
title: 'FM_GETFILESEL 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841419"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="31f2a-103">FM \_ GETFILESEL 訊息</span><span class="sxs-lookup"><span data-stu-id="31f2a-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="31f2a-104">由檔案管理員延伸模組所傳送，可從 [active 檔案管理員] 視窗中取出所選檔案的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。</span><span class="sxs-lookup"><span data-stu-id="31f2a-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="31f2a-105">參數</span><span class="sxs-lookup"><span data-stu-id="31f2a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31f2a-106">*index*</span><span class="sxs-lookup"><span data-stu-id="31f2a-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="31f2a-107">要抓取之所選取檔案的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="31f2a-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="31f2a-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="31f2a-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="31f2a-109">[**FMS \_ GETFILESEL**](fms-getfilesel.md)結構的位址，此結構會接收選取專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31f2a-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31f2a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="31f2a-110">Return value</span></span>

<span data-ttu-id="31f2a-111">傳回所選取檔案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="31f2a-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="31f2a-112">備註</span><span class="sxs-lookup"><span data-stu-id="31f2a-112">Remarks</span></span>

<span data-ttu-id="31f2a-113">延伸模組可以使用 [**FM \_ GETSELCOUNT**](fm-getselcount.md) 訊息來取出所選檔案的計數。</span><span class="sxs-lookup"><span data-stu-id="31f2a-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="31f2a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="31f2a-114">Requirements</span></span>



| <span data-ttu-id="31f2a-115">需求</span><span class="sxs-lookup"><span data-stu-id="31f2a-115">Requirement</span></span> | <span data-ttu-id="31f2a-116">值</span><span class="sxs-lookup"><span data-stu-id="31f2a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31f2a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31f2a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="31f2a-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31f2a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="31f2a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31f2a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="31f2a-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31f2a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="31f2a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="31f2a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="31f2a-122"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="31f2a-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f2a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31f2a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f2a-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="31f2a-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="31f2a-125">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="31f2a-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="31f2a-126">**FM \_ GETSELCOUNTLFN**</span><span class="sxs-lookup"><span data-stu-id="31f2a-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




