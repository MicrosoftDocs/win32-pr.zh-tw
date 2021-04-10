---
title: 'TB_GETPADDING 訊息 (Commctrl .h) '
description: 抓取工具列控制項的邊框距離。
ms.assetid: dde0f44d-5d22-4cab-a7f8-48d84b8995d3
keywords:
- TB_GETPADDING message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15babf2fd5d97377991d1827ea8947e9d794600
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025438"
---
# <a name="tb_getpadding-message"></a><span data-ttu-id="82071-104">TB \_ GETPADDING 訊息</span><span class="sxs-lookup"><span data-stu-id="82071-104">TB\_GETPADDING message</span></span>

<span data-ttu-id="82071-105">抓取工具列控制項的邊框距離。</span><span class="sxs-lookup"><span data-stu-id="82071-105">Retrieves the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="82071-106">參數</span><span class="sxs-lookup"><span data-stu-id="82071-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82071-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="82071-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="82071-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="82071-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="82071-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="82071-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="82071-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="82071-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82071-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="82071-111">Return value</span></span>

<span data-ttu-id="82071-112">傳回 **DWORD** 值，其中包含低字組中的水準填補，以及高單字中的垂直填補（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="82071-112">Returns a **DWORD** value that contains the horizontal padding in the low word and the vertical padding in the high word, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="82071-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="82071-113">Requirements</span></span>



| <span data-ttu-id="82071-114">需求</span><span class="sxs-lookup"><span data-stu-id="82071-114">Requirement</span></span> | <span data-ttu-id="82071-115">值</span><span class="sxs-lookup"><span data-stu-id="82071-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82071-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82071-116">Minimum supported client</span></span><br/> | <span data-ttu-id="82071-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82071-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82071-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82071-118">Minimum supported server</span></span><br/> | <span data-ttu-id="82071-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82071-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82071-120">標頭</span><span class="sxs-lookup"><span data-stu-id="82071-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="82071-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="82071-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82071-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82071-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82071-123">**TB \_ SETPADDING**</span><span class="sxs-lookup"><span data-stu-id="82071-123">**TB\_SETPADDING**</span></span>](tb-setpadding.md)
</dt> </dl>

 

 





