---
title: 'EM_SETTOUCHOPTIONS 訊息 (Richedit .h) '
description: 設定與 rich edit 控制項相關聯的觸控選項。
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465701"
---
# <a name="em_settouchoptions-message"></a><span data-ttu-id="90304-104">EM \_ SETTOUCHOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="90304-104">EM\_SETTOUCHOPTIONS message</span></span>

<span data-ttu-id="90304-105">設定與 rich edit 控制項相關聯的觸控選項。</span><span class="sxs-lookup"><span data-stu-id="90304-105">Sets the touch options associated with a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="90304-106">參數</span><span class="sxs-lookup"><span data-stu-id="90304-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90304-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90304-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90304-108">要設定的觸控選項。</span><span class="sxs-lookup"><span data-stu-id="90304-108">The touch option to set.</span></span> <span data-ttu-id="90304-109">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="90304-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="90304-110">值</span><span class="sxs-lookup"><span data-stu-id="90304-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="90304-111">意義</span><span class="sxs-lookup"><span data-stu-id="90304-111">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="90304-112"><dt>**RTO \_ SHOWHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="90304-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="90304-113">根據 *lParam* 的值，顯示或隱藏觸控控制手柄控點。</span><span class="sxs-lookup"><span data-stu-id="90304-113">Show or hide the touch gripper handles, depending on the value of *lParam*.</span></span><br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="90304-114"><dt>**RTO \_ DISABLEHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="90304-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="90304-115">根據 *lParam* 的值，啟用或停用觸控控制手柄控點。</span><span class="sxs-lookup"><span data-stu-id="90304-115">Enable or disable the touch gripper handles, depending on the value of *lParam*.</span></span> <span data-ttu-id="90304-116">當控制碼已停用時，如果已顯示並保持隱藏狀態，直到 **EM \_ SETTOUCHOPTIONS** 訊息變更其狀態時，就會隱藏處理常式。</span><span class="sxs-lookup"><span data-stu-id="90304-116">When handles are disabled, they are hidden if they are visible and remain hidden until an **EM\_SETTOUCHOPTIONS** message changes their status.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="90304-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90304-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90304-118">設定為 **TRUE** 以顯示/啟用觸控選取控點，或設定為 **FALSE** 以隱藏/停用觸控選取控點。</span><span class="sxs-lookup"><span data-stu-id="90304-118">Set to **TRUE** to show/enable the touch selection handles, or **FALSE** to hide/disable the touch selection handles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90304-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="90304-119">Return value</span></span>

<span data-ttu-id="90304-120">此訊息會傳回零。</span><span class="sxs-lookup"><span data-stu-id="90304-120">This message returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="90304-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="90304-121">Requirements</span></span>



| <span data-ttu-id="90304-122">需求</span><span class="sxs-lookup"><span data-stu-id="90304-122">Requirement</span></span> | <span data-ttu-id="90304-123">值</span><span class="sxs-lookup"><span data-stu-id="90304-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90304-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90304-124">Minimum supported client</span></span><br/> | <span data-ttu-id="90304-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90304-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="90304-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90304-126">Minimum supported server</span></span><br/> | <span data-ttu-id="90304-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90304-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90304-128">標頭</span><span class="sxs-lookup"><span data-stu-id="90304-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="90304-129"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="90304-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90304-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90304-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90304-131">**EM \_ GETTOUCHOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="90304-131">**EM\_GETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





