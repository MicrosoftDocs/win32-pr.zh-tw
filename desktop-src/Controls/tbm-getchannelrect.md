---
title: 'TBM_GETCHANNELRECT 訊息 (Commctrl .h) '
description: 抓取的區域框之頻道的大小與位置。
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- TBM_GETCHANNELRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934090"
---
# <a name="tbm_getchannelrect-message"></a><span data-ttu-id="0003c-104">TBM \_ GETCHANNELRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="0003c-104">TBM\_GETCHANNELRECT message</span></span>

<span data-ttu-id="0003c-105">抓取的區域框之頻道的大小與位置。</span><span class="sxs-lookup"><span data-stu-id="0003c-105">Retrieves the size and position of the bounding rectangle for a trackbar's channel.</span></span> <span data-ttu-id="0003c-106"> (通道是滑杆移動的區域。</span><span class="sxs-lookup"><span data-stu-id="0003c-106">(The channel is the area over which the slider moves.</span></span> <span data-ttu-id="0003c-107">它包含選取範圍時的醒目提示。 ) </span><span class="sxs-lookup"><span data-stu-id="0003c-107">It contains the highlight when a range is selected.)</span></span>

## <a name="parameters"></a><span data-ttu-id="0003c-108">參數</span><span class="sxs-lookup"><span data-stu-id="0003c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0003c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0003c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0003c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0003c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0003c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0003c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0003c-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0003c-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="0003c-113">此訊息會以通道的周框為單位，在 [協調器] 視窗的用戶端座標中填滿此結構。</span><span class="sxs-lookup"><span data-stu-id="0003c-113">The message fills this structure with the channel's bounding rectangle, in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0003c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0003c-114">Return value</span></span>

<span data-ttu-id="0003c-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="0003c-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0003c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0003c-116">Requirements</span></span>



| <span data-ttu-id="0003c-117">需求</span><span class="sxs-lookup"><span data-stu-id="0003c-117">Requirement</span></span> | <span data-ttu-id="0003c-118">值</span><span class="sxs-lookup"><span data-stu-id="0003c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0003c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0003c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0003c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0003c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0003c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0003c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0003c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0003c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0003c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0003c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0003c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0003c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

