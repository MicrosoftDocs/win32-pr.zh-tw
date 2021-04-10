---
title: 'TB_GETRECT 訊息 (Commctrl .h) '
description: 抓取指定之工具列按鈕的周框。
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- TB_GETRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844371"
---
# <a name="tb_getrect-message"></a><span data-ttu-id="5a3bc-104">TB \_ GETRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="5a3bc-104">TB\_GETRECT message</span></span>

<span data-ttu-id="5a3bc-105">抓取指定之工具列按鈕的周框。</span><span class="sxs-lookup"><span data-stu-id="5a3bc-105">Retrieves the bounding rectangle for a specified toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a3bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a3bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a3bc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3bc-108">按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a3bc-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="5a3bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a3bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a3bc-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收周框的矩形資訊。</span><span class="sxs-lookup"><span data-stu-id="5a3bc-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounding rectangle information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3bc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a3bc-111">Return value</span></span>

<span data-ttu-id="5a3bc-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="5a3bc-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a3bc-113">備註</span><span class="sxs-lookup"><span data-stu-id="5a3bc-113">Remarks</span></span>

<span data-ttu-id="5a3bc-114">此訊息不會針對其狀態設定為 [**TBSTATE \_ 隱藏**](toolbar-button-states.md) 值的按鈕，取得周框矩形。</span><span class="sxs-lookup"><span data-stu-id="5a3bc-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3bc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a3bc-115">Requirements</span></span>



| <span data-ttu-id="5a3bc-116">需求</span><span class="sxs-lookup"><span data-stu-id="5a3bc-116">Requirement</span></span> | <span data-ttu-id="5a3bc-117">值</span><span class="sxs-lookup"><span data-stu-id="5a3bc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3bc-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a3bc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3bc-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a3bc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a3bc-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a3bc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3bc-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a3bc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a3bc-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5a3bc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a3bc-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3bc-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

