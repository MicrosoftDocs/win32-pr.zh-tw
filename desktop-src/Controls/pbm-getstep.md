---
title: 'PBM_GETSTEP 訊息 (Commctrl .h) '
description: 從進度列抓取步驟增量。 步驟遞增是進度列在收到 PBM STEPIT 訊息時，增加其目前位置的數量 \_ 。 依預設，步驟遞增會設定為10。
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- PBM_GETSTEP message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934720"
---
# <a name="pbm_getstep-message"></a><span data-ttu-id="f9dcf-106">PBM \_ GETSTEP 訊息</span><span class="sxs-lookup"><span data-stu-id="f9dcf-106">PBM\_GETSTEP message</span></span>

<span data-ttu-id="f9dcf-107">從進度列抓取步驟增量。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-107">Retrieves the step increment from a progress bar.</span></span> <span data-ttu-id="f9dcf-108">步驟遞增是進度列在收到 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息時，增加其目前位置的數量。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="f9dcf-109">依預設，步驟遞增會設定為10。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9dcf-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9dcf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9dcf-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9dcf-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f9dcf-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f9dcf-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9dcf-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f9dcf-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9dcf-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9dcf-115">Return value</span></span>

<span data-ttu-id="f9dcf-116">傳回目前的步驟增量。</span><span class="sxs-lookup"><span data-stu-id="f9dcf-116">Returns the current step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9dcf-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9dcf-117">Requirements</span></span>



| <span data-ttu-id="f9dcf-118">需求</span><span class="sxs-lookup"><span data-stu-id="f9dcf-118">Requirement</span></span> | <span data-ttu-id="f9dcf-119">值</span><span class="sxs-lookup"><span data-stu-id="f9dcf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dcf-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9dcf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dcf-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9dcf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9dcf-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9dcf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dcf-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9dcf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9dcf-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f9dcf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9dcf-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9dcf-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





