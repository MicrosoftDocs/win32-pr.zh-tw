---
title: 'CBEM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 設定 ComboBoxEx 控制項中的延伸樣式。
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965116"
---
# <a name="cbem_setextendedstyle-message"></a><span data-ttu-id="fd124-104">CBEM \_ SETEXTENDEDSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="fd124-104">CBEM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="fd124-105">設定 ComboBoxEx 控制項中的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="fd124-105">Sets extended styles within a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd124-106">參數</span><span class="sxs-lookup"><span data-stu-id="fd124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd124-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd124-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd124-108">**DWORD** 值，指出要對 *lParam* 中的哪些樣式造成影響。</span><span class="sxs-lookup"><span data-stu-id="fd124-108">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="fd124-109">只有 *wParam* 中的擴充樣式會變更。</span><span class="sxs-lookup"><span data-stu-id="fd124-109">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="fd124-110">如果此參數為零，則 *lParam* 中的所有樣式都會受到影響。</span><span class="sxs-lookup"><span data-stu-id="fd124-110">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="fd124-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd124-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd124-112">**DWORD** 值，包含要為控制項設定的 [ComboBoxEx 控制項延伸樣式](comboboxex-control-extended-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="fd124-112">A **DWORD** value that contains the [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) to set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd124-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd124-113">Return value</span></span>

<span data-ttu-id="fd124-114">傳回 **DWORD** 值，包含先前用於控制項的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="fd124-114">Returns a **DWORD** value that contains the extended styles previously used for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd124-115">備註</span><span class="sxs-lookup"><span data-stu-id="fd124-115">Remarks</span></span>

<span data-ttu-id="fd124-116">*wParam* 可讓您修改一或多個擴充樣式，而不需要先取出現有的樣式。</span><span class="sxs-lookup"><span data-stu-id="fd124-116">*wParam* enables you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="fd124-117">例如，如果您傳遞 [**CBES 的 \_ \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* 和0（ *lParam*），將會清除 **CBES \_ EX \_ NOEDITIMAGE** 樣式，但所有其他樣式都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="fd124-117">For example, if you pass [**CBES\_EX\_NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **CBES\_EX\_NOEDITIMAGE** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="fd124-118">如果您嘗試為以 [**CBS \_ 簡單**](combo-box-styles.md) 樣式建立的 ComboBoxEx 控制項設定擴充樣式，則可能無法正確地重新繪製。</span><span class="sxs-lookup"><span data-stu-id="fd124-118">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it may not repaint properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd124-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd124-119">Requirements</span></span>



| <span data-ttu-id="fd124-120">需求</span><span class="sxs-lookup"><span data-stu-id="fd124-120">Requirement</span></span> | <span data-ttu-id="fd124-121">值</span><span class="sxs-lookup"><span data-stu-id="fd124-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd124-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd124-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd124-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd124-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd124-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd124-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd124-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd124-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd124-126">標頭</span><span class="sxs-lookup"><span data-stu-id="fd124-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd124-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd124-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





