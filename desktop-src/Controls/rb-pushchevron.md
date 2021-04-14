---
title: 'RB_PUSHCHEVRON 訊息 (Commctrl .h) '
description: 傳送至 Rebar 控制項以程式設計方式推送燕形。
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON message Windows 控制項
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508907"
---
# <a name="rb_pushchevron-message"></a><span data-ttu-id="903e2-104">RB \_ PUSHCHEVRON 訊息</span><span class="sxs-lookup"><span data-stu-id="903e2-104">RB\_PUSHCHEVRON message</span></span>

<span data-ttu-id="903e2-105">傳送至 Rebar 控制項以程式設計方式推送燕形。</span><span class="sxs-lookup"><span data-stu-id="903e2-105">Sent to a rebar control to programmatically push a chevron.</span></span>

## <a name="parameters"></a><span data-ttu-id="903e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="903e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="903e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="903e2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="903e2-108">以零為基底的範圍索引，其中的上推線會被推送。</span><span class="sxs-lookup"><span data-stu-id="903e2-108">Zero-based index of the band whose chevron is to be pushed.</span></span>

</dd> <dt>

<span data-ttu-id="903e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="903e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="903e2-110">應用程式定義的32位值。</span><span class="sxs-lookup"><span data-stu-id="903e2-110">An application defined 32-bit value.</span></span> <span data-ttu-id="903e2-111">它會傳回給應用程式，做為與 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)通知一起傳遞之 [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)結構的 **lParamNM** 成員。</span><span class="sxs-lookup"><span data-stu-id="903e2-111">It will be passed back to the application as the **lParamNM** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure that is passed with the [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="903e2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="903e2-112">Return value</span></span>

<span data-ttu-id="903e2-113">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="903e2-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="903e2-114">備註</span><span class="sxs-lookup"><span data-stu-id="903e2-114">Remarks</span></span>

<span data-ttu-id="903e2-115">傳送此訊息時，Rebar 控制項會將 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) 通知碼傳送給應用程式，提示它顯示箭號功能表。</span><span class="sxs-lookup"><span data-stu-id="903e2-115">When this message is sent, the rebar control will send the application an [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification code, prompting it to display the chevron menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="903e2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="903e2-116">Requirements</span></span>



| <span data-ttu-id="903e2-117">需求</span><span class="sxs-lookup"><span data-stu-id="903e2-117">Requirement</span></span> | <span data-ttu-id="903e2-118">值</span><span class="sxs-lookup"><span data-stu-id="903e2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="903e2-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="903e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="903e2-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="903e2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="903e2-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="903e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="903e2-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="903e2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="903e2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="903e2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="903e2-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="903e2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





