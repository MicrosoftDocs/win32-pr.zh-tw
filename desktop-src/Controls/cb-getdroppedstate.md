---
title: 'CB_GETDROPPEDSTATE 訊息 (Winuser .h) '
description: 決定下拉式方塊的清單方塊是否已中斷。
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- CB_GETDROPPEDSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025510"
---
# <a name="cb_getdroppedstate-message"></a><span data-ttu-id="24fba-104">CB \_ GETDROPPEDSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="24fba-104">CB\_GETDROPPEDSTATE message</span></span>

<span data-ttu-id="24fba-105">決定下拉式方塊的清單方塊是否已中斷。</span><span class="sxs-lookup"><span data-stu-id="24fba-105">Determines whether the list box of a combo box is dropped down.</span></span>

## <a name="parameters"></a><span data-ttu-id="24fba-106">參數</span><span class="sxs-lookup"><span data-stu-id="24fba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24fba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24fba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24fba-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="24fba-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="24fba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24fba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24fba-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="24fba-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24fba-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="24fba-111">Return value</span></span>

<span data-ttu-id="24fba-112">如果清單方塊是可見的，則傳回值為 **TRUE**;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="24fba-112">If the list box is visible, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="24fba-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="24fba-113">Requirements</span></span>



| <span data-ttu-id="24fba-114">需求</span><span class="sxs-lookup"><span data-stu-id="24fba-114">Requirement</span></span> | <span data-ttu-id="24fba-115">值</span><span class="sxs-lookup"><span data-stu-id="24fba-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24fba-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24fba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="24fba-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24fba-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24fba-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24fba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="24fba-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24fba-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24fba-120">標頭</span><span class="sxs-lookup"><span data-stu-id="24fba-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="24fba-121"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="24fba-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24fba-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24fba-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24fba-123">**CB \_ SHOWDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="24fba-123">**CB\_SHOWDROPDOWN**</span></span>](cb-showdropdown.md)
</dt> </dl>

 

 





