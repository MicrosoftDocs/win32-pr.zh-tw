---
title: 'TTM_GETBUBBLESIZE 訊息 (Commctrl .h) '
description: 傳回工具提示控制項的寬度和高度。
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103751"
---
# <a name="ttm_getbubblesize-message"></a><span data-ttu-id="c31a6-104">TTM \_ GETBUBBLESIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="c31a6-104">TTM\_GETBUBBLESIZE message</span></span>

<span data-ttu-id="c31a6-105">傳回工具提示控制項的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="c31a6-105">Returns the width and height of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c31a6-106">參數</span><span class="sxs-lookup"><span data-stu-id="c31a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c31a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c31a6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c31a6-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c31a6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c31a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c31a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c31a6-110">工具提示 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c31a6-110">Pointer to the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c31a6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c31a6-111">Return value</span></span>

<span data-ttu-id="c31a6-112">如果成功，則傳回低字組中的工具提示寬度和高單字中的高度。</span><span class="sxs-lookup"><span data-stu-id="c31a6-112">Returns the width of the tooltip in the low word and the height in the high word if successful.</span></span> <span data-ttu-id="c31a6-113">否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c31a6-113">Otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c31a6-114">備註</span><span class="sxs-lookup"><span data-stu-id="c31a6-114">Remarks</span></span>

<span data-ttu-id="c31a6-115">如果 TTF \_ TRACK 和 TTF \_ 絕對旗標是在工具提示 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中設定，則可以使用此訊息來協助正確定位工具提示。</span><span class="sxs-lookup"><span data-stu-id="c31a6-115">If the TTF\_TRACK and TTF\_ABSOLUTE flags are set in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, this message can be used to help position the tooltip accurately.</span></span>

## <a name="requirements"></a><span data-ttu-id="c31a6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c31a6-116">Requirements</span></span>



| <span data-ttu-id="c31a6-117">需求</span><span class="sxs-lookup"><span data-stu-id="c31a6-117">Requirement</span></span> | <span data-ttu-id="c31a6-118">值</span><span class="sxs-lookup"><span data-stu-id="c31a6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c31a6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c31a6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c31a6-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c31a6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c31a6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c31a6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c31a6-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c31a6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c31a6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c31a6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c31a6-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c31a6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





