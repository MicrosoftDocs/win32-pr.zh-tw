---
title: 'HDM_GETITEMRECT 訊息 (Commctrl .h) '
description: 取得標題控制項中指定專案的周框。 您可以明確地傳送此訊息，或使用標頭 \_ GetItemRect 宏。
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- HDM_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465885"
---
# <a name="hdm_getitemrect-message"></a><span data-ttu-id="bf7f7-105">HDM \_ GETITEMRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="bf7f7-105">HDM\_GETITEMRECT message</span></span>

<span data-ttu-id="bf7f7-106">取得標題控制項中指定專案的周框。</span><span class="sxs-lookup"><span data-stu-id="bf7f7-106">Gets the bounding rectangle for a given item in a header control.</span></span> <span data-ttu-id="bf7f7-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) 宏。</span><span class="sxs-lookup"><span data-stu-id="bf7f7-107">You can send this message explicitly or use the [**Header\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf7f7-108">參數</span><span class="sxs-lookup"><span data-stu-id="bf7f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf7f7-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf7f7-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7f7-110">以零為基底的標頭控制項專案索引，為其取得周框矩形。</span><span class="sxs-lookup"><span data-stu-id="bf7f7-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="bf7f7-111">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bf7f7-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf7f7-112">[**矩形**](/windows/win32/api/windef/ns-windef-rect)的指標，此結構會接收周框的資訊。</span><span class="sxs-lookup"><span data-stu-id="bf7f7-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="bf7f7-113">訊息寄件者負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="bf7f7-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="bf7f7-114">在矩形結構中傳回的座標會以相對於標題控制項父系的方式表示。</span><span class="sxs-lookup"><span data-stu-id="bf7f7-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf7f7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf7f7-115">Return value</span></span>

<span data-ttu-id="bf7f7-116">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="bf7f7-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7f7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf7f7-117">Requirements</span></span>



| <span data-ttu-id="bf7f7-118">需求</span><span class="sxs-lookup"><span data-stu-id="bf7f7-118">Requirement</span></span> | <span data-ttu-id="bf7f7-119">值</span><span class="sxs-lookup"><span data-stu-id="bf7f7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7f7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf7f7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7f7-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf7f7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf7f7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf7f7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7f7-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf7f7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf7f7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bf7f7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf7f7-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7f7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





