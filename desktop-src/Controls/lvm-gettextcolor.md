---
title: 'LVM_GETTEXTCOLOR 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項的文字色彩。 您可以明確地傳送此訊息，或使用 ListView \_ GetTextColor 宏來傳送。
ms.assetid: 51685e61-dd0a-4c21-8c66-31cf72c2b3e4
keywords:
- LVM_GETTEXTCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7686e8f06f49dbfc14899f47ba52017daaf23c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968983"
---
# <a name="lvm_gettextcolor-message"></a><span data-ttu-id="fe11b-105">LVM \_ GETTEXTCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="fe11b-105">LVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="fe11b-106">抓取清單視圖控制項的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="fe11b-106">Retrieves the text color of a list-view control.</span></span> <span data-ttu-id="fe11b-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="fe11b-107">You can send this message explicitly or by using the [**ListView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe11b-108">參數</span><span class="sxs-lookup"><span data-stu-id="fe11b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe11b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe11b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe11b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fe11b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fe11b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe11b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fe11b-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fe11b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe11b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe11b-113">Return value</span></span>

<span data-ttu-id="fe11b-114">傳回文字色彩。</span><span class="sxs-lookup"><span data-stu-id="fe11b-114">Returns the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe11b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe11b-115">Requirements</span></span>



| <span data-ttu-id="fe11b-116">需求</span><span class="sxs-lookup"><span data-stu-id="fe11b-116">Requirement</span></span> | <span data-ttu-id="fe11b-117">值</span><span class="sxs-lookup"><span data-stu-id="fe11b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe11b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe11b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe11b-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe11b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe11b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe11b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe11b-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe11b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe11b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fe11b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe11b-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe11b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





