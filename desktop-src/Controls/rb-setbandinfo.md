---
title: 'RB_SETBANDINFO 訊息 (Commctrl .h) '
description: 在 Rebar 控制項中設定現有波段的特性。
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466073"
---
# <a name="rb_setbandinfo-message"></a><span data-ttu-id="cfc9b-104">RB \_ SETBANDINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="cfc9b-104">RB\_SETBANDINFO message</span></span>

<span data-ttu-id="cfc9b-105">在 Rebar 控制項中設定現有波段的特性。</span><span class="sxs-lookup"><span data-stu-id="cfc9b-105">Sets characteristics of an existing band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfc9b-106">參數</span><span class="sxs-lookup"><span data-stu-id="cfc9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc9b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfc9b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfc9b-108">以零為基底的索引，這是用來接收新設定的頻外索引。</span><span class="sxs-lookup"><span data-stu-id="cfc9b-108">Zero-based index of the band to receive the new settings.</span></span>

</dd> <dt>

<span data-ttu-id="cfc9b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfc9b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfc9b-110">[**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的指標，該結構定義要修改的頻外和新的設定。</span><span class="sxs-lookup"><span data-stu-id="cfc9b-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be modified and the new settings.</span></span> <span data-ttu-id="cfc9b-111">傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **sizeof** (REBARBANDINFO) 結構。</span><span class="sxs-lookup"><span data-stu-id="cfc9b-111">Before sending this message, you must set the **cbSize** member of this structure to the **sizeof**(REBARBANDINFO) structure.</span></span> <span data-ttu-id="cfc9b-112">此外，當指定 RBBIM 文字時，您必須將 **REBARBANDINFO** 結構的 **cch** 成員設定為 **lpText** 緩衝區的大小 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cfc9b-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc9b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfc9b-113">Return value</span></span>

<span data-ttu-id="cfc9b-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="cfc9b-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc9b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfc9b-115">Requirements</span></span>



| <span data-ttu-id="cfc9b-116">需求</span><span class="sxs-lookup"><span data-stu-id="cfc9b-116">Requirement</span></span> | <span data-ttu-id="cfc9b-117">值</span><span class="sxs-lookup"><span data-stu-id="cfc9b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc9b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfc9b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc9b-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfc9b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfc9b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfc9b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc9b-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfc9b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfc9b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="cfc9b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfc9b-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc9b-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cfc9b-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="cfc9b-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cfc9b-125">**RB \_SETBANDINFOW** (Unicode) 和 **RB \_ SETBANDINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="cfc9b-125">**RB\_SETBANDINFOW** (Unicode) and **RB\_SETBANDINFOA** (ANSI)</span></span><br/>             |



 

 





