---
title: 'LVM_SETTEXTBKCOLOR 訊息 (Commctrl .h) '
description: 設定清單視圖控制項中文字的背景色彩。 您可以明確地傳送此訊息，或使用 ListView \_ SetTextBkColor 宏來傳送。
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024928"
---
# <a name="lvm_settextbkcolor-message"></a><span data-ttu-id="9746e-105">LVM \_ SETTEXTBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="9746e-105">LVM\_SETTEXTBKCOLOR message</span></span>

<span data-ttu-id="9746e-106">設定清單視圖控制項中文字的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="9746e-106">Sets the background color of text in a list-view control.</span></span> <span data-ttu-id="9746e-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="9746e-107">You can send this message explicitly or by using the [**ListView\_SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9746e-108">參數</span><span class="sxs-lookup"><span data-stu-id="9746e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9746e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9746e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9746e-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9746e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9746e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9746e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9746e-112">新的文字背景色彩。</span><span class="sxs-lookup"><span data-stu-id="9746e-112">New text background color.</span></span> <span data-ttu-id="9746e-113">這可以是 \_ 無背景色彩的 CLR 無。</span><span class="sxs-lookup"><span data-stu-id="9746e-113">This can be CLR\_NONE for no background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9746e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9746e-114">Return value</span></span>

<span data-ttu-id="9746e-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9746e-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9746e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9746e-116">Requirements</span></span>



| <span data-ttu-id="9746e-117">需求</span><span class="sxs-lookup"><span data-stu-id="9746e-117">Requirement</span></span> | <span data-ttu-id="9746e-118">值</span><span class="sxs-lookup"><span data-stu-id="9746e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9746e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9746e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9746e-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9746e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9746e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9746e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9746e-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9746e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9746e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9746e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9746e-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9746e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





