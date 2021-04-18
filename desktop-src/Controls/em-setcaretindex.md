---
title: 'EM_SETCARETINDEX 訊息 (CommCtrl .h) '
description: 設定在編輯控制項中插入號的位置之以零為基底的索引值。
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETCARETINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466549"
---
# <a name="em_setcaretindex-message"></a><span data-ttu-id="7c1e3-104">EM \_ SETCARETINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="7c1e3-104">EM\_SETCARETINDEX message</span></span>

<span data-ttu-id="7c1e3-105">設定在編輯控制項中插入號的位置之以零為基底的索引值。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-105">Sets the zero-based index value of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c1e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c1e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c1e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c1e3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c1e3-108">插入號之位置的新索引值（以零為基底）。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-108">The new zero-based index value of the position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="7c1e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c1e3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7c1e3-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c1e3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c1e3-111">Return value</span></span>

<span data-ttu-id="7c1e3-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c1e3-113">備註</span><span class="sxs-lookup"><span data-stu-id="7c1e3-113">Remarks</span></span>

<span data-ttu-id="7c1e3-114">如果索引超出編輯控制項中的文字範圍，則會調整索引以容納在文字範圍內。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-114">If the index is out of the range of the text in an edit control, the index will be adjusted to fit inside the range of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1e3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c1e3-115">Requirements</span></span>



| <span data-ttu-id="7c1e3-116">需求</span><span class="sxs-lookup"><span data-stu-id="7c1e3-116">Requirement</span></span> | <span data-ttu-id="7c1e3-117">值</span><span class="sxs-lookup"><span data-stu-id="7c1e3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1e3-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c1e3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7c1e3-119">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c1e3-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c1e3-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c1e3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7c1e3-121">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c1e3-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c1e3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7c1e3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c1e3-123"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c1e3-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c1e3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c1e3-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c1e3-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="7c1e3-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c1e3-126">**EM \_ GETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="7c1e3-126">**EM\_GETCARETINDEX**</span></span>](em-getcaretindex.md)
</dt> </dl>

 

 





