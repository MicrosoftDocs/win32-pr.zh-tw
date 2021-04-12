---
title: 'MCM_GETCALID 訊息 (Commctrl .h) '
description: 取得指定月曆控制項的行事曆識別碼。 您可以使用 MonthCal GetCALID 宏明確地傳送此訊息 \_ 。
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- MCM_GETCALID message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104039"
---
# <a name="mcm_getcalid-message"></a><span data-ttu-id="ee1d8-105">MCM \_ GETCALID 訊息</span><span class="sxs-lookup"><span data-stu-id="ee1d8-105">MCM\_GETCALID message</span></span>

<span data-ttu-id="ee1d8-106">取得指定月曆控制項的行事曆識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee1d8-106">Gets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="ee1d8-107">您可以使用 [**MonthCal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ee1d8-107">You can send this message explicitly or by using the [**MonthCal\_GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee1d8-108">參數</span><span class="sxs-lookup"><span data-stu-id="ee1d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1d8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee1d8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee1d8-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ee1d8-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ee1d8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee1d8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee1d8-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ee1d8-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1d8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee1d8-113">Return value</span></span>

<span data-ttu-id="ee1d8-114">目前行事曆的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee1d8-114">ID of the current calendar.</span></span> <span data-ttu-id="ee1d8-115">其中一個行事 [曆識別碼](/windows/desktop/Intl/calendar-identifiers) 常數。</span><span class="sxs-lookup"><span data-stu-id="ee1d8-115">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee1d8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee1d8-116">Requirements</span></span>



| <span data-ttu-id="ee1d8-117">需求</span><span class="sxs-lookup"><span data-stu-id="ee1d8-117">Requirement</span></span> | <span data-ttu-id="ee1d8-118">值</span><span class="sxs-lookup"><span data-stu-id="ee1d8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1d8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee1d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee1d8-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee1d8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee1d8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee1d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee1d8-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee1d8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee1d8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ee1d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee1d8-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee1d8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

