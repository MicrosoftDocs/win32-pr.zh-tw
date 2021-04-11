---
title: 'MCM_SETMAXSELCOUNT 訊息 (Commctrl .h) '
description: 設定可在月曆控制項中選取的最大天數。 您可以使用 MonthCal SetMaxSelCount 宏明確地傳送此訊息 \_ 。
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- MCM_SETMAXSELCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844271"
---
# <a name="mcm_setmaxselcount-message"></a><span data-ttu-id="6cc45-105">MCM \_ SETMAXSELCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="6cc45-105">MCM\_SETMAXSELCOUNT message</span></span>

<span data-ttu-id="6cc45-106">設定可在月曆控制項中選取的最大天數。</span><span class="sxs-lookup"><span data-stu-id="6cc45-106">Sets the maximum number of days that can be selected in a month calendar control.</span></span> <span data-ttu-id="6cc45-107">您可以使用 [**MonthCal \_ SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="6cc45-107">You can send this message explicitly or by using the [**MonthCal\_SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cc45-108">參數</span><span class="sxs-lookup"><span data-stu-id="6cc45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cc45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc45-110">**Int** 類型的值，將設定為代表可選取的最大天數。</span><span class="sxs-lookup"><span data-stu-id="6cc45-110">Value of type **int** that will be set to represent the maximum number of days that can be selected.</span></span>

</dd> <dt>

<span data-ttu-id="6cc45-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cc45-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6cc45-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6cc45-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc45-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cc45-113">Return value</span></span>

<span data-ttu-id="6cc45-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="6cc45-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="6cc45-115">如果套用到不使用 [**MCS \_ 多重選**](month-calendar-control-styles.md) 樣式的月曆控制項，此訊息將會失敗。</span><span class="sxs-lookup"><span data-stu-id="6cc45-115">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc45-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cc45-116">Requirements</span></span>



| <span data-ttu-id="6cc45-117">需求</span><span class="sxs-lookup"><span data-stu-id="6cc45-117">Requirement</span></span> | <span data-ttu-id="6cc45-118">值</span><span class="sxs-lookup"><span data-stu-id="6cc45-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc45-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cc45-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc45-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cc45-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cc45-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cc45-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc45-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cc45-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cc45-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6cc45-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cc45-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6cc45-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





