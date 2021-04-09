---
title: 'RB_SHOWBAND 訊息 (Commctrl .h) '
description: 顯示或隱藏 Rebar 控制項中的指定頻。
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- RB_SHOWBAND message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106248"
---
# <a name="rb_showband-message"></a><span data-ttu-id="8a6cd-104">RB \_ SHOWBAND 訊息</span><span class="sxs-lookup"><span data-stu-id="8a6cd-104">RB\_SHOWBAND message</span></span>

<span data-ttu-id="8a6cd-105">顯示或隱藏 Rebar 控制項中的指定頻。</span><span class="sxs-lookup"><span data-stu-id="8a6cd-105">Shows or hides a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a6cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="8a6cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a6cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a6cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a6cd-108">Rebar 控制項中的寬線索引（以零為基底）。</span><span class="sxs-lookup"><span data-stu-id="8a6cd-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="8a6cd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a6cd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a6cd-110">**布林** 值，指出是否應該顯示或隱藏帶狀。</span><span class="sxs-lookup"><span data-stu-id="8a6cd-110">**BOOL** value that indicates if the band should be shown or hidden.</span></span> <span data-ttu-id="8a6cd-111">如果此值為非零值，則會顯示此波段。</span><span class="sxs-lookup"><span data-stu-id="8a6cd-111">If this value is nonzero, the band will be shown.</span></span> <span data-ttu-id="8a6cd-112">否則，將會隱藏此波段。</span><span class="sxs-lookup"><span data-stu-id="8a6cd-112">Otherwise, the band will be hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a6cd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a6cd-113">Return value</span></span>

<span data-ttu-id="8a6cd-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="8a6cd-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6cd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a6cd-115">Requirements</span></span>



| <span data-ttu-id="8a6cd-116">需求</span><span class="sxs-lookup"><span data-stu-id="8a6cd-116">Requirement</span></span> | <span data-ttu-id="8a6cd-117">值</span><span class="sxs-lookup"><span data-stu-id="8a6cd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6cd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a6cd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6cd-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a6cd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8a6cd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a6cd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6cd-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a6cd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a6cd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8a6cd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a6cd-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a6cd-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





