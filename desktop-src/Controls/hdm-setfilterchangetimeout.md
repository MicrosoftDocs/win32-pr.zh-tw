---
title: 'HDM_SETFILTERCHANGETIMEOUT 訊息 (Commctrl .h) '
description: 設定篩選屬性中發生變更和張貼 HDN FILTERCHANGE 通知之間的逾時間隔 \_ 。 您可以明確地傳送此訊息，或使用標頭 \_ SetFilterChangeTimeout 宏。
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025345"
---
# <a name="hdm_setfilterchangetimeout-message"></a><span data-ttu-id="e71d7-105">HDM \_ SETFILTERCHANGETIMEOUT 訊息</span><span class="sxs-lookup"><span data-stu-id="e71d7-105">HDM\_SETFILTERCHANGETIMEOUT message</span></span>

<span data-ttu-id="e71d7-106">設定篩選屬性中發生變更和張貼 [HDN \_ FILTERCHANGE](hdn-filterchange.md) 通知之間的逾時間隔。</span><span class="sxs-lookup"><span data-stu-id="e71d7-106">Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification.</span></span> <span data-ttu-id="e71d7-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) 宏。</span><span class="sxs-lookup"><span data-stu-id="e71d7-107">You can send this message explicitly or use the [**Header\_SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e71d7-108">參數</span><span class="sxs-lookup"><span data-stu-id="e71d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e71d7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e71d7-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e71d7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e71d7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e71d7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e71d7-112">逾時值 (以毫秒為單位)。</span><span class="sxs-lookup"><span data-stu-id="e71d7-112">The timeout value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e71d7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e71d7-113">Return value</span></span>

<span data-ttu-id="e71d7-114">傳回要修改之篩選控制項的索引。</span><span class="sxs-lookup"><span data-stu-id="e71d7-114">Returns the index of the filter control being modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="e71d7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e71d7-115">Requirements</span></span>



| <span data-ttu-id="e71d7-116">需求</span><span class="sxs-lookup"><span data-stu-id="e71d7-116">Requirement</span></span> | <span data-ttu-id="e71d7-117">值</span><span class="sxs-lookup"><span data-stu-id="e71d7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e71d7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e71d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e71d7-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e71d7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e71d7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e71d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e71d7-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e71d7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e71d7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e71d7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e71d7-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e71d7-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e71d7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e71d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71d7-125">HDN \_ FILTERCHANGE</span><span class="sxs-lookup"><span data-stu-id="e71d7-125">HDN\_FILTERCHANGE</span></span>](hdn-filterchange.md)
</dt> </dl>

 

 





