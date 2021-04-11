---
title: 'EM_GETCARETINDEX 訊息 (CommCtrl .h) '
description: 取得編輯控制項中插入號的位置之以零為基底的索引。
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETCARETINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6653e2ae0e2126941e3d8977a593300b86051800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934490"
---
# <a name="em_getcaretindex-message"></a><span data-ttu-id="976f1-104">EM \_ GETCARETINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="976f1-104">EM\_GETCARETINDEX message</span></span>

<span data-ttu-id="976f1-105">取得編輯控制項中插入號的位置之以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="976f1-105">Gets the zero-based index of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="976f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="976f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="976f1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="976f1-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="976f1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="976f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="976f1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="976f1-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="976f1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976f1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="976f1-111">Return value</span></span>

<span data-ttu-id="976f1-112">傳回值是以零為基底的索引值，即插入號的位置。</span><span class="sxs-lookup"><span data-stu-id="976f1-112">The return value is a zero-based index value of the position of the caret.</span></span>

## <a name="requirements"></a><span data-ttu-id="976f1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="976f1-113">Requirements</span></span>



| <span data-ttu-id="976f1-114">需求</span><span class="sxs-lookup"><span data-stu-id="976f1-114">Requirement</span></span> | <span data-ttu-id="976f1-115">值</span><span class="sxs-lookup"><span data-stu-id="976f1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="976f1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="976f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="976f1-117">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="976f1-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="976f1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="976f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="976f1-119">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="976f1-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="976f1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="976f1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="976f1-121"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="976f1-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="976f1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="976f1-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="976f1-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="976f1-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="976f1-124">**EM \_ SETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="976f1-124">**EM\_SETCARETINDEX**</span></span>](em-setcaretindex.md)
</dt> </dl>

 

 





