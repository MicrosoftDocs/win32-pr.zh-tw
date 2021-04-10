---
title: 'DTM_GETMCSTYLE 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器 (DTP) 控制項的樣式。 請明確地傳送此訊息，或使用 DateTime \_ GetMonthCalStyle 宏。
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- DTM_GETMCSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934740"
---
# <a name="dtm_getmcstyle-message"></a><span data-ttu-id="f6d0c-105">DTM \_ GETMCSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="f6d0c-105">DTM\_GETMCSTYLE message</span></span>

<span data-ttu-id="f6d0c-106">取得日期和時間選擇器 (DTP) 控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="f6d0c-106">Gets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="f6d0c-107">請明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) 宏。</span><span class="sxs-lookup"><span data-stu-id="f6d0c-107">Send this message explicitly or by using the [**DateTime\_GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6d0c-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6d0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d0c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6d0c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6d0c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f6d0c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f6d0c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6d0c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f6d0c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f6d0c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6d0c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6d0c-113">Return value</span></span>

<span data-ttu-id="f6d0c-114">傳回控制項的樣式值。</span><span class="sxs-lookup"><span data-stu-id="f6d0c-114">Returns the style value of the control.</span></span> <span data-ttu-id="f6d0c-115">如需詳細資訊，請參閱 [月曆控制項樣式](month-calendar-control-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="f6d0c-115">For more information see [Month Calendar Control Styles](month-calendar-control-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6d0c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6d0c-116">Requirements</span></span>



| <span data-ttu-id="f6d0c-117">需求</span><span class="sxs-lookup"><span data-stu-id="f6d0c-117">Requirement</span></span> | <span data-ttu-id="f6d0c-118">值</span><span class="sxs-lookup"><span data-stu-id="f6d0c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d0c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6d0c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d0c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6d0c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6d0c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6d0c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d0c-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6d0c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6d0c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f6d0c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6d0c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6d0c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





