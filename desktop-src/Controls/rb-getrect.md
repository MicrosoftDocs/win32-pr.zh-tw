---
title: 'RB_GETRECT 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項中指定範圍的周框。
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- RB_GETRECT message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187290"
---
# <a name="rb_getrect-message"></a><span data-ttu-id="1d5c4-104">RB \_ GETRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="1d5c4-104">RB\_GETRECT message</span></span>

<span data-ttu-id="1d5c4-105">抓取 Rebar 控制項中指定範圍的周框。</span><span class="sxs-lookup"><span data-stu-id="1d5c4-105">Retrieves the bounding rectangle for a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d5c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d5c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d5c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d5c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d5c4-108">Rebar 控制項中的寬線索引（以零為基底）。</span><span class="sxs-lookup"><span data-stu-id="1d5c4-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="1d5c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d5c4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d5c4-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收 Rebar 區的範圍。</span><span class="sxs-lookup"><span data-stu-id="1d5c4-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounds of the rebar band.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d5c4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d5c4-111">Return value</span></span>

<span data-ttu-id="1d5c4-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="1d5c4-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5c4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d5c4-113">Requirements</span></span>



| <span data-ttu-id="1d5c4-114">需求</span><span class="sxs-lookup"><span data-stu-id="1d5c4-114">Requirement</span></span> | <span data-ttu-id="1d5c4-115">值</span><span class="sxs-lookup"><span data-stu-id="1d5c4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5c4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d5c4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1d5c4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d5c4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d5c4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d5c4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1d5c4-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d5c4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d5c4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1d5c4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d5c4-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d5c4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

