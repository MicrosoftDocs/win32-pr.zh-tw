---
title: 'TB_GETANCHORHIGHLIGHT 訊息 (Commctrl .h) '
description: 抓取工具列的錨點醒目提示設定。
ms.assetid: 167d481c-8684-40eb-9323-cfa238be3643
keywords:
- TB_GETANCHORHIGHLIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bfff5ef1853bbf5657604c673dcc6a9be43af83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844448"
---
# <a name="tb_getanchorhighlight-message"></a><span data-ttu-id="f7021-104">TB \_ GETANCHORHIGHLIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="f7021-104">TB\_GETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="f7021-105">抓取工具列的錨點醒目提示設定。</span><span class="sxs-lookup"><span data-stu-id="f7021-105">Retrieves the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7021-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7021-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7021-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7021-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f7021-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f7021-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f7021-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7021-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f7021-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f7021-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7021-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7021-111">Return value</span></span>

<span data-ttu-id="f7021-112">傳回布林值，指出是否已設定錨點反白顯示。</span><span class="sxs-lookup"><span data-stu-id="f7021-112">Returns a Boolean value that indicates if anchor highlighting is set.</span></span> <span data-ttu-id="f7021-113">如果此值為非零值，則會啟用錨點反白顯示。</span><span class="sxs-lookup"><span data-stu-id="f7021-113">If this value is nonzero, anchor highlighting is enabled.</span></span> <span data-ttu-id="f7021-114">如果這個值為零，則會停用。</span><span class="sxs-lookup"><span data-stu-id="f7021-114">If this value is zero, it is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7021-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7021-115">Requirements</span></span>



| <span data-ttu-id="f7021-116">需求</span><span class="sxs-lookup"><span data-stu-id="f7021-116">Requirement</span></span> | <span data-ttu-id="f7021-117">值</span><span class="sxs-lookup"><span data-stu-id="f7021-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7021-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7021-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f7021-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7021-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7021-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7021-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f7021-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7021-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7021-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f7021-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7021-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7021-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7021-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7021-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7021-125">**TB \_ SETANCHORHIGHLIGHT**</span><span class="sxs-lookup"><span data-stu-id="f7021-125">**TB\_SETANCHORHIGHLIGHT**</span></span>](tb-setanchorhighlight.md)
</dt> </dl>

 

 





