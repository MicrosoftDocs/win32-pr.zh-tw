---
title: 'TBM_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取指派給的提示（如果有的話）之工具提示控制項的控制碼。
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843600"
---
# <a name="tbm_gettooltips-message"></a><span data-ttu-id="65adb-104">TBM \_ GETTOOLTIPS 訊息</span><span class="sxs-lookup"><span data-stu-id="65adb-104">TBM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="65adb-105">抓取指派給的提示（如果有的話）之工具提示控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="65adb-105">Retrieves the handle to the tooltip control assigned to the trackbar, if any.</span></span>

## <a name="parameters"></a><span data-ttu-id="65adb-106">參數</span><span class="sxs-lookup"><span data-stu-id="65adb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65adb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65adb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65adb-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="65adb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="65adb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65adb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="65adb-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="65adb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65adb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="65adb-111">Return value</span></span>

<span data-ttu-id="65adb-112">傳回指派給的提示之工具提示控制項的控制碼，如果工具提示不在使用中，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="65adb-112">Returns the handle to the tooltip control assigned to the trackbar, or **NULL** if tooltips are not in use.</span></span> <span data-ttu-id="65adb-113">如果 [執行程式] 控制項未使用 [ [**tb] \_ 工具提示**](trackbar-control-styles.md) 樣式，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="65adb-113">If the trackbar control does not use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65adb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="65adb-114">Requirements</span></span>



| <span data-ttu-id="65adb-115">需求</span><span class="sxs-lookup"><span data-stu-id="65adb-115">Requirement</span></span> | <span data-ttu-id="65adb-116">值</span><span class="sxs-lookup"><span data-stu-id="65adb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65adb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65adb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65adb-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65adb-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65adb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65adb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65adb-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65adb-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65adb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="65adb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="65adb-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="65adb-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





