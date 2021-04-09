---
title: 'CB_SETCUEBANNER 訊息 (Winuser .h) '
description: 設定為下拉式方塊編輯控制項顯示的提示橫幅文字。
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025082"
---
# <a name="cb_setcuebanner-message"></a><span data-ttu-id="4c38f-104">CB \_ SETCUEBANNER 訊息</span><span class="sxs-lookup"><span data-stu-id="4c38f-104">CB\_SETCUEBANNER message</span></span>

<span data-ttu-id="4c38f-105">設定為下拉式方塊編輯控制項顯示的提示橫幅文字。</span><span class="sxs-lookup"><span data-stu-id="4c38f-105">Sets the cue banner text that is displayed for the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c38f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c38f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c38f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c38f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c38f-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4c38f-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4c38f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c38f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c38f-110">包含文字之以 null 結束之 Unicode 字串緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="4c38f-110">A pointer to a null-terminated Unicode string buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c38f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c38f-111">Return value</span></span>

<span data-ttu-id="4c38f-112">如果成功，則傳回1，否則會傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="4c38f-112">Returns 1 if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c38f-113">備註</span><span class="sxs-lookup"><span data-stu-id="4c38f-113">Remarks</span></span>

<span data-ttu-id="4c38f-114">提示橫幅是在沒有選取專案時，顯示在下拉式方塊編輯控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="4c38f-114">The cue banner is text that is displayed in the edit control of a combo box when there is no selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c38f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c38f-115">Requirements</span></span>



| <span data-ttu-id="4c38f-116">需求</span><span class="sxs-lookup"><span data-stu-id="4c38f-116">Requirement</span></span> | <span data-ttu-id="4c38f-117">值</span><span class="sxs-lookup"><span data-stu-id="4c38f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c38f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c38f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4c38f-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c38f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4c38f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c38f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4c38f-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c38f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c38f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4c38f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c38f-123"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c38f-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c38f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c38f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c38f-125">下拉式列示方塊功能</span><span class="sxs-lookup"><span data-stu-id="4c38f-125">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





