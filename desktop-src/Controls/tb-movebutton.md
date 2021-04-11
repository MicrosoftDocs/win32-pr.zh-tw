---
title: 'TB_MOVEBUTTON 訊息 (Commctrl .h) '
description: 將按鈕從一個索引移至另一個索引。
ms.assetid: 030aedc5-2de5-4751-90b2-63794322f503
keywords:
- TB_MOVEBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_MOVEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac4cd303e895998b12e710910432ba2c38b230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105047"
---
# <a name="tb_movebutton-message"></a><span data-ttu-id="6a3c8-104">TB \_ MOVEBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="6a3c8-104">TB\_MOVEBUTTON message</span></span>

<span data-ttu-id="6a3c8-105">將按鈕從一個索引移至另一個索引。</span><span class="sxs-lookup"><span data-stu-id="6a3c8-105">Moves a button from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a3c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a3c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a3c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a3c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a3c8-108">要移動之按鈕的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="6a3c8-108">Zero-based index of the button to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="6a3c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a3c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a3c8-110">以零為基底的索引，將會在其中移動按鈕。</span><span class="sxs-lookup"><span data-stu-id="6a3c8-110">Zero-based index where the button will be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a3c8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a3c8-111">Return value</span></span>

<span data-ttu-id="6a3c8-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="6a3c8-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a3c8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a3c8-113">Requirements</span></span>



| <span data-ttu-id="6a3c8-114">需求</span><span class="sxs-lookup"><span data-stu-id="6a3c8-114">Requirement</span></span> | <span data-ttu-id="6a3c8-115">值</span><span class="sxs-lookup"><span data-stu-id="6a3c8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a3c8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a3c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a3c8-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a3c8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a3c8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a3c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a3c8-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a3c8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a3c8-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6a3c8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a3c8-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a3c8-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a3c8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a3c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a3c8-123">**TB \_ SETANCHORHIGHLIGHT**</span><span class="sxs-lookup"><span data-stu-id="6a3c8-123">**TB\_SETANCHORHIGHLIGHT**</span></span>](tb-setanchorhighlight.md)
</dt> </dl>

 

 





