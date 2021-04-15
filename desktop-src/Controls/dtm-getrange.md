---
title: 'DTM_GETRANGE 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以明確地傳送此訊息，或使用 DateTime \_ GetRange 宏。
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466120"
---
# <a name="dtm_getrange-message"></a><span data-ttu-id="2886e-105">DTM \_ GETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="2886e-105">DTM\_GETRANGE message</span></span>

<span data-ttu-id="2886e-106">取得日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。</span><span class="sxs-lookup"><span data-stu-id="2886e-106">Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="2886e-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) 宏。</span><span class="sxs-lookup"><span data-stu-id="2886e-107">You can send this message explicitly or use the [**DateTime\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2886e-108">參數</span><span class="sxs-lookup"><span data-stu-id="2886e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2886e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2886e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2886e-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2886e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2886e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2886e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2886e-112">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="2886e-112">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2886e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2886e-113">Return value</span></span>

<span data-ttu-id="2886e-114">傳回 GDTR  \_ MIN 或 GDTR MAX 組合的 DWORD 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2886e-114">Returns a **DWORD** value that is a combination of GDTR\_MIN or GDTR\_MAX.</span></span> <span data-ttu-id="2886e-115">如果設定 GDTR MIN， [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 陣列的第一個元素包含最小允許時間 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2886e-115">The first element of the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) array contains the minimum allowable time if GDTR\_MIN is set.</span></span> <span data-ttu-id="2886e-116">如果設定 GDTR MAX， **SYSTEMTIME** 陣列的第二個元素會包含最大允許時間 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2886e-116">The second element of the **SYSTEMTIME** array contains the maximum allowable time if GDTR\_MAX is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="2886e-117">備註</span><span class="sxs-lookup"><span data-stu-id="2886e-117">Remarks</span></span>

<span data-ttu-id="2886e-118">日期和時間選擇器只會顯示落在指定範圍內的日期/時間，防止使用者選取超出範圍的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="2886e-118">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="2886e-119">如果 [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) 訊息指定超出範圍的日期和時間，它將會失敗。</span><span class="sxs-lookup"><span data-stu-id="2886e-119">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="2886e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2886e-120">Requirements</span></span>



| <span data-ttu-id="2886e-121">需求</span><span class="sxs-lookup"><span data-stu-id="2886e-121">Requirement</span></span> | <span data-ttu-id="2886e-122">值</span><span class="sxs-lookup"><span data-stu-id="2886e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2886e-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2886e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2886e-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2886e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2886e-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2886e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2886e-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2886e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2886e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2886e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2886e-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2886e-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

