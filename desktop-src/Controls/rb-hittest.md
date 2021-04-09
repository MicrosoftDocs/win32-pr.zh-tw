---
title: 'RB_HITTEST 訊息 (Commctrl .h) '
description: 判斷如果在該點上存在 Rebar 帶，則在螢幕上的某個點上，Rebar 區的哪個部分是在指定的點上。
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024653"
---
# <a name="rb_hittest-message"></a><span data-ttu-id="ccc17-104">RB \_ system.windows.media.visualtreehelper.hittest 訊息</span><span class="sxs-lookup"><span data-stu-id="ccc17-104">RB\_HITTEST message</span></span>

<span data-ttu-id="ccc17-105">判斷如果在該點上存在 Rebar 帶，則在螢幕上的某個點上，Rebar 區的哪個部分是在指定的點上。</span><span class="sxs-lookup"><span data-stu-id="ccc17-105">Determines which portion of a rebar band is at a given point on the screen, if a rebar band exists at that point.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccc17-106">參數</span><span class="sxs-lookup"><span data-stu-id="ccc17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc17-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccc17-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ccc17-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ccc17-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ccc17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccc17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc17-110">[**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ccc17-110">Pointer to an [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) structure.</span></span> <span data-ttu-id="ccc17-111">傳送訊息之前，必須將此結構的 **pt** 成員初始化為在用戶端座標中進行點擊測試的時間點。</span><span class="sxs-lookup"><span data-stu-id="ccc17-111">Before sending the message, the **pt** member of this structure must be initialized to the point that will be hit tested, in client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc17-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccc17-112">Return value</span></span>

<span data-ttu-id="ccc17-113">傳回在指定點以零為基底的範圍索引，如果沒有 Rebar 波段，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="ccc17-113">Returns the zero-based index of the band at the given point, or -1 if no rebar band was at the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc17-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccc17-114">Requirements</span></span>



| <span data-ttu-id="ccc17-115">需求</span><span class="sxs-lookup"><span data-stu-id="ccc17-115">Requirement</span></span> | <span data-ttu-id="ccc17-116">值</span><span class="sxs-lookup"><span data-stu-id="ccc17-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc17-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccc17-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc17-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccc17-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ccc17-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccc17-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc17-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccc17-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccc17-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ccc17-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc17-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc17-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





