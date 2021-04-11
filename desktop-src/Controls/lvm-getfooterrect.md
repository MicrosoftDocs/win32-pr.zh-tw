---
title: 'LVM_GETFOOTERRECT 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項頁尾的座標。 明確地傳送此訊息，或使用 ListView \_ GetFooterRect 宏。
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093843"
---
# <a name="lvm_getfooterrect-message"></a><span data-ttu-id="4db6d-105">LVM \_ GETFOOTERRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="4db6d-105">LVM\_GETFOOTERRECT message</span></span>

<span data-ttu-id="4db6d-106">抓取清單視圖控制項頁尾的座標。</span><span class="sxs-lookup"><span data-stu-id="4db6d-106">Retrieves the coordinates of the footer for a list-view control.</span></span> <span data-ttu-id="4db6d-107">明確地傳送此訊息，或使用 [**ListView \_ GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) 宏。</span><span class="sxs-lookup"><span data-stu-id="4db6d-107">Send this message explicitly or by using the [**ListView\_GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4db6d-108">參數</span><span class="sxs-lookup"><span data-stu-id="4db6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db6d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4db6d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4db6d-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="4db6d-110">Not used.</span></span> <span data-ttu-id="4db6d-111">必須是 0。</span><span class="sxs-lookup"><span data-stu-id="4db6d-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="4db6d-112">*lParam* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4db6d-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4db6d-113">要接收座標的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="4db6d-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="4db6d-114">呼叫進程負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="4db6d-114">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="4db6d-115">收到的座標會以用戶端座標表示。</span><span class="sxs-lookup"><span data-stu-id="4db6d-115">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db6d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4db6d-116">Return value</span></span>

<span data-ttu-id="4db6d-117">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4db6d-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db6d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4db6d-118">Requirements</span></span>



| <span data-ttu-id="4db6d-119">需求</span><span class="sxs-lookup"><span data-stu-id="4db6d-119">Requirement</span></span> | <span data-ttu-id="4db6d-120">值</span><span class="sxs-lookup"><span data-stu-id="4db6d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4db6d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4db6d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4db6d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4db6d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4db6d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4db6d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4db6d-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4db6d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4db6d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4db6d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4db6d-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4db6d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

