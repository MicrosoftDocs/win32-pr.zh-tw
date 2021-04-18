---
title: 'SB_GETRECT 訊息 (Commctrl .h) '
description: 抓取狀態視窗中某部分的周框。
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- SB_GETRECT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48808b7bdf9c97fa6b9da53112e505e8cb8e66e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466232"
---
# <a name="sb_getrect-message"></a><span data-ttu-id="56a7e-104">SB \_ GETRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="56a7e-104">SB\_GETRECT message</span></span>

<span data-ttu-id="56a7e-105">抓取狀態視窗中某部分的周框。</span><span class="sxs-lookup"><span data-stu-id="56a7e-105">Retrieves the bounding rectangle of a part in a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="56a7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="56a7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a7e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56a7e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56a7e-108">以零為基底的索引，這是要抓取其周框矩形的部分。</span><span class="sxs-lookup"><span data-stu-id="56a7e-108">Zero-based index of the part whose bounding rectangle is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="56a7e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56a7e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56a7e-110">接收周框 [**的矩形結構指標**](/previous-versions//dd162897(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="56a7e-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56a7e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="56a7e-111">Return value</span></span>

<span data-ttu-id="56a7e-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="56a7e-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="56a7e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="56a7e-113">Requirements</span></span>



| <span data-ttu-id="56a7e-114">需求</span><span class="sxs-lookup"><span data-stu-id="56a7e-114">Requirement</span></span> | <span data-ttu-id="56a7e-115">值</span><span class="sxs-lookup"><span data-stu-id="56a7e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56a7e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56a7e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="56a7e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56a7e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56a7e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56a7e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="56a7e-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56a7e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56a7e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="56a7e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="56a7e-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="56a7e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

