---
title: 'DTM_GETMCFONT 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器 (DTP) 控制項的子月曆控制項目前使用的字型。 您可以明確地傳送此訊息，或使用 DateTime \_ GetMonthCalFont 宏。
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844140"
---
# <a name="dtm_getmcfont-message"></a><span data-ttu-id="b4560-105">DTM \_ GETMCFONT 訊息</span><span class="sxs-lookup"><span data-stu-id="b4560-105">DTM\_GETMCFONT message</span></span>

<span data-ttu-id="b4560-106">取得日期和時間選擇器 (DTP) 控制項的子月曆控制項目前使用的字型。</span><span class="sxs-lookup"><span data-stu-id="b4560-106">Gets the font that the date and time picker (DTP) control's child month calendar control is currently using.</span></span> <span data-ttu-id="b4560-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) 宏。</span><span class="sxs-lookup"><span data-stu-id="b4560-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4560-108">參數</span><span class="sxs-lookup"><span data-stu-id="b4560-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4560-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4560-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b4560-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b4560-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b4560-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4560-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b4560-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b4560-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4560-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4560-113">Return value</span></span>

<span data-ttu-id="b4560-114">傳回 HFONT 值，這個值是目前字型的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b4560-114">Returns an HFONT value that is the handle to the current font.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4560-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4560-115">Requirements</span></span>



| <span data-ttu-id="b4560-116">需求</span><span class="sxs-lookup"><span data-stu-id="b4560-116">Requirement</span></span> | <span data-ttu-id="b4560-117">值</span><span class="sxs-lookup"><span data-stu-id="b4560-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4560-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4560-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4560-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4560-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4560-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4560-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4560-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4560-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4560-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b4560-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4560-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4560-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





