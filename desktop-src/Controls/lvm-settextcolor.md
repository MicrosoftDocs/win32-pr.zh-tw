---
title: 'LVM_SETTEXTCOLOR 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的文字色彩。 您可以明確地傳送此訊息，或使用 ListView \_ SetTextColor 宏來傳送。
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- LVM_SETTEXTCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094304"
---
# <a name="lvm_settextcolor-message"></a><span data-ttu-id="8c536-105">LVM \_ SETTEXTCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="8c536-105">LVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="8c536-106">設定清單視圖控制項的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="8c536-106">Sets the text color of a list-view control.</span></span> <span data-ttu-id="8c536-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="8c536-107">You can send this message explicitly or by using the [**ListView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c536-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c536-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c536-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c536-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8c536-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8c536-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8c536-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c536-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c536-112">指定新文字色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 。</span><span class="sxs-lookup"><span data-stu-id="8c536-112">A [**COLORREF**](/windows/desktop/gdi/colorref) that specifies the new text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c536-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c536-113">Return value</span></span>

<span data-ttu-id="8c536-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8c536-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c536-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c536-115">Requirements</span></span>



| <span data-ttu-id="8c536-116">需求</span><span class="sxs-lookup"><span data-stu-id="8c536-116">Requirement</span></span> | <span data-ttu-id="8c536-117">值</span><span class="sxs-lookup"><span data-stu-id="8c536-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c536-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c536-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8c536-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c536-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c536-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c536-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8c536-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c536-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c536-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8c536-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c536-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c536-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

