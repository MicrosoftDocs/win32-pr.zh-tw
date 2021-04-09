---
title: 'TB_INSERTMARKHITTEST 訊息 (Commctrl .h) '
description: 抓取工具列中某個點的插入標記資訊。
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024920"
---
# <a name="tb_insertmarkhittest-message"></a><span data-ttu-id="279e4-104">TB \_ INSERTMARKHITTEST 訊息</span><span class="sxs-lookup"><span data-stu-id="279e4-104">TB\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="279e4-105">抓取工具列中某個點的插入標記資訊。</span><span class="sxs-lookup"><span data-stu-id="279e4-105">Retrieves the insertion mark information for a point in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="279e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="279e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="279e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="279e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="279e4-108">[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，其中包含點擊測試座標（相對於工具列的工作區）。</span><span class="sxs-lookup"><span data-stu-id="279e4-108">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the hit test coordinates, relative to the client area of the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="279e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="279e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="279e4-110">[**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)結構的指標，此結構會接收插入標記資訊。</span><span class="sxs-lookup"><span data-stu-id="279e4-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="279e4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="279e4-111">Return value</span></span>

<span data-ttu-id="279e4-112">如果點是插入號，則會傳回非零，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="279e4-112">Returns nonzero if the point is an insertion mark, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="279e4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="279e4-113">Requirements</span></span>



| <span data-ttu-id="279e4-114">需求</span><span class="sxs-lookup"><span data-stu-id="279e4-114">Requirement</span></span> | <span data-ttu-id="279e4-115">值</span><span class="sxs-lookup"><span data-stu-id="279e4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="279e4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="279e4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="279e4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="279e4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="279e4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="279e4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="279e4-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="279e4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="279e4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="279e4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="279e4-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="279e4-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

