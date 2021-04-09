---
title: 'TB_GETINSERTMARK 訊息 (Commctrl .h) '
description: 抓取工具列目前的插入標記。
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- TB_GETINSERTMARK message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024720"
---
# <a name="tb_getinsertmark-message"></a><span data-ttu-id="1b031-104">TB \_ GETINSERTMARK 訊息</span><span class="sxs-lookup"><span data-stu-id="1b031-104">TB\_GETINSERTMARK message</span></span>

<span data-ttu-id="1b031-105">抓取工具列目前的插入標記。</span><span class="sxs-lookup"><span data-stu-id="1b031-105">Retrieves the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b031-106">參數</span><span class="sxs-lookup"><span data-stu-id="1b031-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b031-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b031-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b031-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1b031-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1b031-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b031-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b031-110">[**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)結構的指標，此結構會接收插入標記。</span><span class="sxs-lookup"><span data-stu-id="1b031-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b031-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b031-111">Return value</span></span>

<span data-ttu-id="1b031-112">一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="1b031-112">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b031-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b031-113">Requirements</span></span>



| <span data-ttu-id="1b031-114">需求</span><span class="sxs-lookup"><span data-stu-id="1b031-114">Requirement</span></span> | <span data-ttu-id="1b031-115">值</span><span class="sxs-lookup"><span data-stu-id="1b031-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b031-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b031-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1b031-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b031-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b031-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b031-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1b031-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b031-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b031-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1b031-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b031-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1b031-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b031-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b031-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b031-123">**TB \_ SETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="1b031-123">**TB\_SETINSERTMARK**</span></span>](tb-setinsertmark.md)
</dt> </dl>

 

 





