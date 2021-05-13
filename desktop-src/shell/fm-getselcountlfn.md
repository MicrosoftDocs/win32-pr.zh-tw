---
description: 由檔案管理員延伸模組所傳送，可在 [active File Manager] 視窗中取出選取的檔案數目 (目錄視窗或 [搜尋結果] 視窗) 。 計數包括具有長檔名的檔案。
title: 'FM_GETSELCOUNTLFN 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 1ec06c08775836a94b9ada6520ea7c5ea46b62f3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841339"
---
# <a name="fm_getselcountlfn-message"></a><span data-ttu-id="29612-104">FM \_ GETSELCOUNTLFN 訊息</span><span class="sxs-lookup"><span data-stu-id="29612-104">FM\_GETSELCOUNTLFN message</span></span>

<span data-ttu-id="29612-105">由檔案管理員延伸模組所傳送，可在 [active File Manager] 視窗中取出選取的檔案數目 (目錄視窗或 [搜尋結果] 視窗) 。</span><span class="sxs-lookup"><span data-stu-id="29612-105">Sent by a File Manager extension to retrieve the number of selected files in the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="29612-106">計數包括具有長檔名的檔案。</span><span class="sxs-lookup"><span data-stu-id="29612-106">The count includes files that have long file names.</span></span>

## <a name="parameters"></a><span data-ttu-id="29612-107">參數</span><span class="sxs-lookup"><span data-stu-id="29612-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29612-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29612-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="29612-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="29612-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="29612-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29612-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="29612-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="29612-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29612-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="29612-112">Return value</span></span>

<span data-ttu-id="29612-113">傳回選取的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="29612-113">Returns the number of selected files.</span></span>

## <a name="remarks"></a><span data-ttu-id="29612-114">備註</span><span class="sxs-lookup"><span data-stu-id="29612-114">Remarks</span></span>

<span data-ttu-id="29612-115">只有支援長檔名的延伸模組 (例如網路覺察的延伸模組) 應該使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="29612-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="29612-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="29612-116">Requirements</span></span>



| <span data-ttu-id="29612-117">需求</span><span class="sxs-lookup"><span data-stu-id="29612-117">Requirement</span></span> | <span data-ttu-id="29612-118">值</span><span class="sxs-lookup"><span data-stu-id="29612-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29612-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29612-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29612-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29612-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="29612-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29612-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29612-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29612-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="29612-123">標頭</span><span class="sxs-lookup"><span data-stu-id="29612-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="29612-124"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="29612-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29612-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29612-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29612-126">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="29612-126">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="29612-127">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="29612-127">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="29612-128">**FM \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="29612-128">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




