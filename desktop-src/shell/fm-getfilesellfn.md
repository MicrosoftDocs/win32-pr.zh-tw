---
description: 由檔案管理員延伸模組所傳送，可從 [active 檔案管理員] 視窗中取出所選檔案的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。 選取的檔案可以有較長的檔案名。
title: 'FM_GETFILESELLFN 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842389"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="21cbb-104">FM \_ GETFILESELLFN 訊息</span><span class="sxs-lookup"><span data-stu-id="21cbb-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="21cbb-105">由檔案管理員延伸模組所傳送，可從 [active 檔案管理員] 視窗中取出所選檔案的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。</span><span class="sxs-lookup"><span data-stu-id="21cbb-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="21cbb-106">選取的檔案可以有較長的檔案名。</span><span class="sxs-lookup"><span data-stu-id="21cbb-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="21cbb-107">參數</span><span class="sxs-lookup"><span data-stu-id="21cbb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21cbb-108">*index*</span><span class="sxs-lookup"><span data-stu-id="21cbb-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="21cbb-109">要抓取之所選取檔案的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="21cbb-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="21cbb-110">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="21cbb-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="21cbb-111">[**FMS \_ GETFILESEL**](fms-getfilesel.md)結構的位址，此結構會接收選取專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="21cbb-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21cbb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="21cbb-112">Return value</span></span>

<span data-ttu-id="21cbb-113">傳回所選取檔案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="21cbb-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="21cbb-114">備註</span><span class="sxs-lookup"><span data-stu-id="21cbb-114">Remarks</span></span>

<span data-ttu-id="21cbb-115">只有支援長檔名的延伸模組 (例如網路覺察的延伸模組) 應該使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="21cbb-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="21cbb-116">延伸模組可以使用 [**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) 訊息來取出所選檔案的計數。</span><span class="sxs-lookup"><span data-stu-id="21cbb-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="21cbb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="21cbb-117">Requirements</span></span>



| <span data-ttu-id="21cbb-118">需求</span><span class="sxs-lookup"><span data-stu-id="21cbb-118">Requirement</span></span> | <span data-ttu-id="21cbb-119">值</span><span class="sxs-lookup"><span data-stu-id="21cbb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21cbb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21cbb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="21cbb-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21cbb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="21cbb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21cbb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="21cbb-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21cbb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="21cbb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="21cbb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="21cbb-125"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="21cbb-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21cbb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21cbb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21cbb-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="21cbb-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="21cbb-128">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="21cbb-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="21cbb-129">**FM \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="21cbb-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




