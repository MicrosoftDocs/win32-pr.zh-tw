---
title: 'UDM_GETRANGE 訊息 (Commctrl .h) '
description: 抓取上下按鈕 (範圍) 的最小和最大位置。
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- UDM_GETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187319"
---
# <a name="udm_getrange-message"></a><span data-ttu-id="f051b-104">UDM \_ GETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="f051b-104">UDM\_GETRANGE message</span></span>

<span data-ttu-id="f051b-105">抓取上下按鈕 (範圍) 的最小和最大位置。</span><span class="sxs-lookup"><span data-stu-id="f051b-105">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f051b-106">參數</span><span class="sxs-lookup"><span data-stu-id="f051b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f051b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f051b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f051b-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f051b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f051b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f051b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f051b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f051b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f051b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f051b-111">Return value</span></span>

<span data-ttu-id="f051b-112">傳回值是包含最小和最大位置的32位值。</span><span class="sxs-lookup"><span data-stu-id="f051b-112">The return value is a 32-bit value that contains the minimum and maximum positions.</span></span> <span data-ttu-id="f051b-113">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是控制項的最大位置，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是最小位置。</span><span class="sxs-lookup"><span data-stu-id="f051b-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum position for the control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="f051b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f051b-114">Requirements</span></span>



| <span data-ttu-id="f051b-115">需求</span><span class="sxs-lookup"><span data-stu-id="f051b-115">Requirement</span></span> | <span data-ttu-id="f051b-116">值</span><span class="sxs-lookup"><span data-stu-id="f051b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f051b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f051b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f051b-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f051b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f051b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f051b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f051b-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f051b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f051b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f051b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f051b-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f051b-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

