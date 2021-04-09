---
title: 'LVM_ISITEMVISIBLE 訊息 (Commctrl .h) '
description: 指出是否可以看見清單視圖控制項中的專案。 明確地傳送此訊息，或使用 ListView \_ IsItemVisible 宏。
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844080"
---
# <a name="lvm_isitemvisible-message"></a><span data-ttu-id="89168-105">LVM \_ ISITEMVISIBLE 訊息</span><span class="sxs-lookup"><span data-stu-id="89168-105">LVM\_ISITEMVISIBLE message</span></span>

<span data-ttu-id="89168-106">指出是否可以看見清單視圖控制項中的專案。</span><span class="sxs-lookup"><span data-stu-id="89168-106">Indicates if an item in the list-view control is visible.</span></span> <span data-ttu-id="89168-107">明確地傳送此訊息，或使用 [**ListView \_ IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) 宏。</span><span class="sxs-lookup"><span data-stu-id="89168-107">Send this message explicitly or by using the [**ListView\_IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="89168-108">參數</span><span class="sxs-lookup"><span data-stu-id="89168-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89168-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89168-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89168-110">清單視圖控制項中專案的索引。</span><span class="sxs-lookup"><span data-stu-id="89168-110">An index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="89168-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89168-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="89168-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="89168-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89168-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="89168-113">Return value</span></span>

<span data-ttu-id="89168-114">如果 **為** 可見，則傳回 TRUE，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="89168-114">Returns **TRUE** if visible, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="89168-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="89168-115">Requirements</span></span>



| <span data-ttu-id="89168-116">需求</span><span class="sxs-lookup"><span data-stu-id="89168-116">Requirement</span></span> | <span data-ttu-id="89168-117">值</span><span class="sxs-lookup"><span data-stu-id="89168-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89168-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89168-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89168-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89168-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89168-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89168-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89168-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89168-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89168-122">標頭</span><span class="sxs-lookup"><span data-stu-id="89168-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89168-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="89168-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





