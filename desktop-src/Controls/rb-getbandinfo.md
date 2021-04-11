---
title: 'RB_GETBANDINFO 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項中指定之頻外的相關資訊。
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104790"
---
# <a name="rb_getbandinfo-message"></a><span data-ttu-id="9d898-104">RB \_ GETBANDINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="9d898-104">RB\_GETBANDINFO message</span></span>

<span data-ttu-id="9d898-105">抓取 Rebar 控制項中指定之頻外的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d898-105">Retrieves information about a specified band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d898-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d898-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d898-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d898-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d898-108">以零為起始的寬線索引，將會抓取資訊。</span><span class="sxs-lookup"><span data-stu-id="9d898-108">Zero-based index of the band for which the information will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="9d898-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d898-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d898-110">[**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的指標，此結構會接收要求的頻外資訊。</span><span class="sxs-lookup"><span data-stu-id="9d898-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that will receive the requested band information.</span></span> <span data-ttu-id="9d898-111">傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **REBARBANDINFO** 結構的大小，並將 **fMask** 成員設定為您想要取出的專案。</span><span class="sxs-lookup"><span data-stu-id="9d898-111">Before sending this message, you must set the **cbSize** member of this structure to the size of the **REBARBANDINFO** structure and set the **fMask** member to the items you want to retrieve.</span></span> <span data-ttu-id="9d898-112">此外，當指定 RBBIM 文字時，您必須將 **REBARBANDINFO** 結構的 **cch** 成員設定為 **lpText** 緩衝區的大小 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9d898-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d898-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d898-113">Return value</span></span>

<span data-ttu-id="9d898-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="9d898-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d898-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d898-115">Requirements</span></span>



| <span data-ttu-id="9d898-116">需求</span><span class="sxs-lookup"><span data-stu-id="9d898-116">Requirement</span></span> | <span data-ttu-id="9d898-117">值</span><span class="sxs-lookup"><span data-stu-id="9d898-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d898-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d898-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9d898-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d898-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d898-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d898-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9d898-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d898-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d898-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9d898-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d898-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d898-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9d898-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="9d898-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9d898-125">**RB \_GETBANDINFOW** (Unicode) 和 **RB \_ GETBANDINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="9d898-125">**RB\_GETBANDINFOW** (Unicode) and **RB\_GETBANDINFOA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="9d898-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d898-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d898-127">**RB \_ SETBANDINFO**</span><span class="sxs-lookup"><span data-stu-id="9d898-127">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





