---
title: 'EM_GETIMEOPTIONS 訊息 (Richedit .h) '
description: 抓取目前的輸入方法編輯器 (IME) 選項。
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104820"
---
# <a name="em_getimeoptions-message"></a><span data-ttu-id="fb469-104">EM \_ GETIMEOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="fb469-104">EM\_GETIMEOPTIONS message</span></span>

<span data-ttu-id="fb469-105">抓取目前的輸入方法編輯器 (IME) 選項。</span><span class="sxs-lookup"><span data-stu-id="fb469-105">Retrieves the current Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="fb469-106">只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="fb469-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="fb469-107">任何較新版本的 Rich Edit 都不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="fb469-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="fb469-108">參數</span><span class="sxs-lookup"><span data-stu-id="fb469-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb469-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb469-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb469-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="fb469-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fb469-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb469-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb469-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="fb469-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb469-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb469-113">Return value</span></span>

<span data-ttu-id="fb469-114">此訊息會傳回 [**EM \_ SETIMEOPTIONS**](em-setimeoptions.md) 訊息中所述的一或多個 IME 選項旗標值。</span><span class="sxs-lookup"><span data-stu-id="fb469-114">This message returns one or more of the IME option flag values described in the [**EM\_SETIMEOPTIONS**](em-setimeoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb469-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb469-115">Requirements</span></span>



| <span data-ttu-id="fb469-116">需求</span><span class="sxs-lookup"><span data-stu-id="fb469-116">Requirement</span></span> | <span data-ttu-id="fb469-117">值</span><span class="sxs-lookup"><span data-stu-id="fb469-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb469-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb469-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fb469-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb469-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb469-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb469-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fb469-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb469-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb469-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fb469-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb469-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb469-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb469-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb469-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb469-125">**EM \_ SETIMEOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="fb469-125">**EM\_SETIMEOPTIONS**</span></span>](em-setimeoptions.md)
</dt> </dl>

 

 





