---
title: 'DTM_SETMCSTYLE 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的樣式。 請明確地傳送此訊息，或使用 DateTime \_ SetMonthCalStyle 宏。
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104838"
---
# <a name="dtm_setmcstyle-message"></a><span data-ttu-id="d904b-105">DTM \_ SETMCSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="d904b-105">DTM\_SETMCSTYLE message</span></span>

<span data-ttu-id="d904b-106">設定日期和時間選擇器 (DTP) 控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="d904b-106">Sets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="d904b-107">請明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) 宏。</span><span class="sxs-lookup"><span data-stu-id="d904b-107">Send this message explicitly or by using the [**DateTime\_SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d904b-108">參數</span><span class="sxs-lookup"><span data-stu-id="d904b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d904b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d904b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d904b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d904b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d904b-111">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d904b-111">*lParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="d904b-112">樣式值。</span><span class="sxs-lookup"><span data-stu-id="d904b-112">A style value.</span></span> <span data-ttu-id="d904b-113">如需詳細資訊，請參閱 <a href="month-calendar-control-styles.md">月曆控制項樣式</a>。</span><span class="sxs-lookup"><span data-stu-id="d904b-113">For more information see <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d904b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d904b-114">Return value</span></span>

<span data-ttu-id="d904b-115">傳回上一個樣式的值。</span><span class="sxs-lookup"><span data-stu-id="d904b-115">Returns the value of the previous style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d904b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d904b-116">Requirements</span></span>



| <span data-ttu-id="d904b-117">需求</span><span class="sxs-lookup"><span data-stu-id="d904b-117">Requirement</span></span> | <span data-ttu-id="d904b-118">值</span><span class="sxs-lookup"><span data-stu-id="d904b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d904b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d904b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d904b-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d904b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d904b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d904b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d904b-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d904b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d904b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d904b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d904b-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d904b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





