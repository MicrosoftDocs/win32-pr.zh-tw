---
title: 'PBM_SETSTEP 訊息 (Commctrl .h) '
description: 指定進度列的步驟增量。 步驟遞增是進度列在收到 PBM STEPIT 訊息時，增加其目前位置的數量 \_ 。 依預設，步驟遞增會設定為10。
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984964"
---
# <a name="pbm_setstep-message"></a><span data-ttu-id="0de83-106">PBM \_ SETSTEP 訊息</span><span class="sxs-lookup"><span data-stu-id="0de83-106">PBM\_SETSTEP message</span></span>

<span data-ttu-id="0de83-107">指定進度列的步驟增量。</span><span class="sxs-lookup"><span data-stu-id="0de83-107">Specifies the step increment for a progress bar.</span></span> <span data-ttu-id="0de83-108">步驟遞增是進度列在收到 [**PBM \_ STEPIT**](pbm-stepit.md) 訊息時，增加其目前位置的數量。</span><span class="sxs-lookup"><span data-stu-id="0de83-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="0de83-109">依預設，步驟遞增會設定為10。</span><span class="sxs-lookup"><span data-stu-id="0de83-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="0de83-110">參數</span><span class="sxs-lookup"><span data-stu-id="0de83-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de83-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0de83-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0de83-112">新步驟增量。</span><span class="sxs-lookup"><span data-stu-id="0de83-112">New step increment.</span></span>

</dd> <dt>

<span data-ttu-id="0de83-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0de83-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0de83-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0de83-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de83-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0de83-115">Return value</span></span>

<span data-ttu-id="0de83-116">傳回上一個步驟增量。</span><span class="sxs-lookup"><span data-stu-id="0de83-116">Returns the previous step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="0de83-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0de83-117">Requirements</span></span>



| <span data-ttu-id="0de83-118">需求</span><span class="sxs-lookup"><span data-stu-id="0de83-118">Requirement</span></span> | <span data-ttu-id="0de83-119">值</span><span class="sxs-lookup"><span data-stu-id="0de83-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0de83-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0de83-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0de83-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0de83-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0de83-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0de83-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0de83-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0de83-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0de83-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0de83-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0de83-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0de83-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





