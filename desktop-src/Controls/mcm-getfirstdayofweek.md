---
title: 'MCM_GETFIRSTDAYOFWEEK 訊息 (Commctrl .h) '
description: 抓取月曆控制項的每週第一天。 您可以使用 MonthCal GetFirstDayOfWeek 宏明確地傳送此訊息 \_ 。
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966325"
---
# <a name="mcm_getfirstdayofweek-message"></a><span data-ttu-id="9ef85-105">MCM \_ GETFIRSTDAYOFWEEK 訊息</span><span class="sxs-lookup"><span data-stu-id="9ef85-105">MCM\_GETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="9ef85-106">抓取月曆控制項的每週第一天。</span><span class="sxs-lookup"><span data-stu-id="9ef85-106">Retrieves the first day of the week for a month calendar control.</span></span> <span data-ttu-id="9ef85-107">您可以使用 [**MonthCal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9ef85-107">You can send this message explicitly or by using the [**MonthCal\_GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ef85-108">參數</span><span class="sxs-lookup"><span data-stu-id="9ef85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef85-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ef85-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9ef85-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9ef85-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9ef85-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ef85-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9ef85-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9ef85-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef85-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ef85-113">Return value</span></span>

<span data-ttu-id="9ef85-114">傳回包含兩個值的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="9ef85-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="9ef85-115">如果一周的第一天設定為地區設定 IFIRSTDAYOFWEEK 以外 **的值** ，則最大的單字為非零值， \_ 否則為零。</span><span class="sxs-lookup"><span data-stu-id="9ef85-115">The high word is a **BOOL** value that is nonzero if the first day of the week is set to something other than LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="9ef85-116">低字組是代表一周第一天的 INT 值，其中0是星期一、1是星期二等等。</span><span class="sxs-lookup"><span data-stu-id="9ef85-116">The low word is an INT value that represents the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef85-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ef85-117">Requirements</span></span>



| <span data-ttu-id="9ef85-118">需求</span><span class="sxs-lookup"><span data-stu-id="9ef85-118">Requirement</span></span> | <span data-ttu-id="9ef85-119">值</span><span class="sxs-lookup"><span data-stu-id="9ef85-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef85-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ef85-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef85-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ef85-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ef85-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ef85-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef85-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ef85-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ef85-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9ef85-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef85-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ef85-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





