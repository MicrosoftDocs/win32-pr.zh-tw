---
title: 'LVM_CREATEDRAGIMAGE 訊息 (Commctrl .h) '
description: 為指定的專案建立拖曳影像清單。 您可以明確地傳送此訊息，或使用 ListView \_ CreateDragImage 宏來傳送。
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093855"
---
# <a name="lvm_createdragimage-message"></a><span data-ttu-id="609eb-105">LVM \_ CREATEDRAGIMAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="609eb-105">LVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="609eb-106">為指定的專案建立拖曳影像清單。</span><span class="sxs-lookup"><span data-stu-id="609eb-106">Creates a drag image list for the specified item.</span></span> <span data-ttu-id="609eb-107">您可以明確地傳送此訊息，或使用 [**ListView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="609eb-107">You can send this message explicitly or by using the [**ListView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="609eb-108">參數</span><span class="sxs-lookup"><span data-stu-id="609eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="609eb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="609eb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="609eb-110">項目的索引。</span><span class="sxs-lookup"><span data-stu-id="609eb-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="609eb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="609eb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="609eb-112">[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，該結構會接收影像左上角的初始位置（以視圖座標表示）。</span><span class="sxs-lookup"><span data-stu-id="609eb-112">A pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the initial location of the upper-left corner of the image, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="609eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="609eb-113">Return value</span></span>

<span data-ttu-id="609eb-114">如果成功，則傳回拖曳影像清單的控制碼，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="609eb-114">Returns the handle to the drag image list if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="609eb-115">備註</span><span class="sxs-lookup"><span data-stu-id="609eb-115">Remarks</span></span>

<span data-ttu-id="609eb-116">當不再需要時，您的應用程式會負責終結影像清單。</span><span class="sxs-lookup"><span data-stu-id="609eb-116">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="609eb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="609eb-117">Requirements</span></span>



| <span data-ttu-id="609eb-118">需求</span><span class="sxs-lookup"><span data-stu-id="609eb-118">Requirement</span></span> | <span data-ttu-id="609eb-119">值</span><span class="sxs-lookup"><span data-stu-id="609eb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="609eb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="609eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="609eb-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="609eb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="609eb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="609eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="609eb-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="609eb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="609eb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="609eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="609eb-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="609eb-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

