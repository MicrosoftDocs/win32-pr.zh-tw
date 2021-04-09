---
title: 'MCM_SETCALID 訊息 (Commctrl .h) '
description: 設定給定行事曆控制項的行事曆識別碼。 您可以使用 MonthCal SetCALID 宏明確地傳送此訊息 \_ 。
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024729"
---
# <a name="mcm_setcalid-message"></a><span data-ttu-id="f00fe-105">MCM \_ SETCALID 訊息</span><span class="sxs-lookup"><span data-stu-id="f00fe-105">MCM\_SETCALID message</span></span>

<span data-ttu-id="f00fe-106">設定給定行事曆控制項的行事曆識別碼。</span><span class="sxs-lookup"><span data-stu-id="f00fe-106">Sets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="f00fe-107">您可以使用 [**MonthCal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="f00fe-107">You can send this message explicitly or by using the [**MonthCal\_SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f00fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="f00fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f00fe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f00fe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f00fe-110">行事曆識別碼。</span><span class="sxs-lookup"><span data-stu-id="f00fe-110">The calendar ID.</span></span> <span data-ttu-id="f00fe-111">其中一個行事 [曆識別碼](/windows/desktop/Intl/calendar-identifiers) 常數。</span><span class="sxs-lookup"><span data-stu-id="f00fe-111">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

</dd> <dt>

<span data-ttu-id="f00fe-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f00fe-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f00fe-113">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f00fe-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f00fe-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f00fe-114">Return value</span></span>

<span data-ttu-id="f00fe-115">未使用的。</span><span class="sxs-lookup"><span data-stu-id="f00fe-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="f00fe-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f00fe-116">Requirements</span></span>



| <span data-ttu-id="f00fe-117">需求</span><span class="sxs-lookup"><span data-stu-id="f00fe-117">Requirement</span></span> | <span data-ttu-id="f00fe-118">值</span><span class="sxs-lookup"><span data-stu-id="f00fe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f00fe-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f00fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f00fe-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f00fe-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f00fe-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f00fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f00fe-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f00fe-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f00fe-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f00fe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f00fe-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f00fe-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

