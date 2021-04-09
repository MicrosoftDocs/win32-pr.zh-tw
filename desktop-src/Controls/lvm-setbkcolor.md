---
title: 'LVM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的背景色彩。 您可以明確地傳送此訊息，或使用 ListView \_ SetBkColor 宏來傳送。
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934628"
---
# <a name="lvm_setbkcolor-message"></a><span data-ttu-id="8916f-105">LVM \_ SETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="8916f-105">LVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="8916f-106">設定清單視圖控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="8916f-106">Sets the background color of a list-view control.</span></span> <span data-ttu-id="8916f-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="8916f-107">You can send this message explicitly or by using the [**ListView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8916f-108">參數</span><span class="sxs-lookup"><span data-stu-id="8916f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8916f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8916f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8916f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8916f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8916f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8916f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8916f-112">要設定的背景色彩，或 \_ 無背景色彩的 CLR 無值。</span><span class="sxs-lookup"><span data-stu-id="8916f-112">Background color to set or the CLR\_NONE value for no background color.</span></span> <span data-ttu-id="8916f-113">具有背景色彩的清單視圖控制項，其重繪速度會比沒有背景色彩的控制項更快。</span><span class="sxs-lookup"><span data-stu-id="8916f-113">List-view controls with background colors redraw themselves significantly faster than those without background colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8916f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8916f-114">Return value</span></span>

<span data-ttu-id="8916f-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8916f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8916f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8916f-116">Requirements</span></span>



| <span data-ttu-id="8916f-117">需求</span><span class="sxs-lookup"><span data-stu-id="8916f-117">Requirement</span></span> | <span data-ttu-id="8916f-118">值</span><span class="sxs-lookup"><span data-stu-id="8916f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8916f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8916f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8916f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8916f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8916f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8916f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8916f-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8916f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8916f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8916f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8916f-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8916f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





