---
title: 'EM_GETTHUMB 訊息 (Winuser .h) '
description: 取得在多行編輯控制項的垂直捲動條中，捲動方塊 (thumb) 的位置。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- EM_GETTHUMB message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105113"
---
# <a name="em_getthumb-message"></a><span data-ttu-id="51096-105">EM \_ GETTHUMB 訊息</span><span class="sxs-lookup"><span data-stu-id="51096-105">EM\_GETTHUMB message</span></span>

<span data-ttu-id="51096-106">取得在多行編輯控制項的垂直捲動條中，捲動方塊 (thumb) 的位置。</span><span class="sxs-lookup"><span data-stu-id="51096-106">Gets the position of the scroll box (thumb) in the vertical scroll bar of a multiline edit control.</span></span> <span data-ttu-id="51096-107">您可以將此訊息傳送至編輯控制項或 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="51096-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="51096-108">參數</span><span class="sxs-lookup"><span data-stu-id="51096-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51096-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51096-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51096-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="51096-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="51096-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51096-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51096-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="51096-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51096-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="51096-113">Return value</span></span>

<span data-ttu-id="51096-114">傳回值是捲動方塊的位置。</span><span class="sxs-lookup"><span data-stu-id="51096-114">The return value is the position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="51096-115">備註</span><span class="sxs-lookup"><span data-stu-id="51096-115">Remarks</span></span>

<span data-ttu-id="51096-116">**Rich Edit：** Microsoft Rich Edit 2.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="51096-116">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="51096-117">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="51096-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51096-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="51096-118">Requirements</span></span>



| <span data-ttu-id="51096-119">需求</span><span class="sxs-lookup"><span data-stu-id="51096-119">Requirement</span></span> | <span data-ttu-id="51096-120">值</span><span class="sxs-lookup"><span data-stu-id="51096-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51096-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51096-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51096-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51096-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51096-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51096-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51096-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51096-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51096-125">標頭</span><span class="sxs-lookup"><span data-stu-id="51096-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="51096-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="51096-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





