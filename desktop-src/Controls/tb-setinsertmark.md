---
title: 'TB_SETINSERTMARK 訊息 (Commctrl .h) '
description: 設定工具列的目前插入標記。
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- TB_SETINSERTMARK message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093816"
---
# <a name="tb_setinsertmark-message"></a><span data-ttu-id="95aa1-104">TB \_ SETINSERTMARK 訊息</span><span class="sxs-lookup"><span data-stu-id="95aa1-104">TB\_SETINSERTMARK message</span></span>

<span data-ttu-id="95aa1-105">設定工具列的目前插入標記。</span><span class="sxs-lookup"><span data-stu-id="95aa1-105">Sets the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="95aa1-106">參數</span><span class="sxs-lookup"><span data-stu-id="95aa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95aa1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95aa1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="95aa1-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="95aa1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="95aa1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95aa1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95aa1-110">包含插入標記之 [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="95aa1-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that contains the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95aa1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95aa1-111">Return value</span></span>

<span data-ttu-id="95aa1-112">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="95aa1-112">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="95aa1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="95aa1-113">Requirements</span></span>



| <span data-ttu-id="95aa1-114">需求</span><span class="sxs-lookup"><span data-stu-id="95aa1-114">Requirement</span></span> | <span data-ttu-id="95aa1-115">值</span><span class="sxs-lookup"><span data-stu-id="95aa1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95aa1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95aa1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95aa1-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95aa1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95aa1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95aa1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95aa1-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95aa1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95aa1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="95aa1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="95aa1-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="95aa1-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95aa1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95aa1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95aa1-123">**TB \_ GETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="95aa1-123">**TB\_GETINSERTMARK**</span></span>](tb-getinsertmark.md)
</dt> </dl>

 

 





