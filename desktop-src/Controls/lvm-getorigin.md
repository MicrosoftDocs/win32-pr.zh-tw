---
title: 'LVM_GETORIGIN 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項的目前視圖原點。 您可以明確地傳送此訊息，或使用 ListView \_ GetOrigin 宏來傳送。
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- LVM_GETORIGIN message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105497"
---
# <a name="lvm_getorigin-message"></a><span data-ttu-id="f6e60-105">LVM \_ GETORIGIN 訊息</span><span class="sxs-lookup"><span data-stu-id="f6e60-105">LVM\_GETORIGIN message</span></span>

<span data-ttu-id="f6e60-106">抓取清單視圖控制項的目前視圖原點。</span><span class="sxs-lookup"><span data-stu-id="f6e60-106">Retrieves the current view origin for a list-view control.</span></span> <span data-ttu-id="f6e60-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="f6e60-107">You can send this message explicitly or by using the [**ListView\_GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6e60-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6e60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6e60-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6e60-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f6e60-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f6e60-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f6e60-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6e60-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e60-112">接收視圖來源的 [**點**](/previous-versions//dd162805(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="f6e60-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the view origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6e60-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6e60-113">Return value</span></span>

<span data-ttu-id="f6e60-114">如果成功，則傳回 **TRUE** ，如果目前 view 為清單或報表檢視，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f6e60-114">Returns **TRUE** if successful, or **FALSE** if the current view is list or report view.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e60-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6e60-115">Requirements</span></span>



| <span data-ttu-id="f6e60-116">需求</span><span class="sxs-lookup"><span data-stu-id="f6e60-116">Requirement</span></span> | <span data-ttu-id="f6e60-117">值</span><span class="sxs-lookup"><span data-stu-id="f6e60-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e60-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6e60-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e60-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6e60-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6e60-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6e60-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e60-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6e60-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6e60-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f6e60-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6e60-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6e60-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

