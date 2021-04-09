---
title: 'EM_GETIMECOLOR 訊息 (Richedit .h) '
description: 抓取輸入方法編輯器 (IME) 組合色彩。
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- EM_GETIMECOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934734"
---
# <a name="em_getimecolor-message"></a><span data-ttu-id="64eba-104">EM \_ GETIMECOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="64eba-104">EM\_GETIMECOLOR message</span></span>

<span data-ttu-id="64eba-105">抓取輸入方法編輯器 (IME) 組合色彩。</span><span class="sxs-lookup"><span data-stu-id="64eba-105">Retrieves the Input Method Editor (IME) composition color.</span></span>

> [!Note]  
> <span data-ttu-id="64eba-106">只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="64eba-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="64eba-107">任何較新版本的 Rich Edit 都不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="64eba-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="64eba-108">參數</span><span class="sxs-lookup"><span data-stu-id="64eba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64eba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64eba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64eba-110">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="64eba-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="64eba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64eba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64eba-112">[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)結構的四個元素陣列，可接收組合色彩。</span><span class="sxs-lookup"><span data-stu-id="64eba-112">A four-element array of [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structures that receives the composition color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64eba-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="64eba-113">Return value</span></span>

<span data-ttu-id="64eba-114">如果作業成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="64eba-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="64eba-115">如果作業失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="64eba-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="64eba-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="64eba-116">Requirements</span></span>



| <span data-ttu-id="64eba-117">需求</span><span class="sxs-lookup"><span data-stu-id="64eba-117">Requirement</span></span> | <span data-ttu-id="64eba-118">值</span><span class="sxs-lookup"><span data-stu-id="64eba-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64eba-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64eba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="64eba-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64eba-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64eba-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64eba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="64eba-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64eba-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64eba-123">標頭</span><span class="sxs-lookup"><span data-stu-id="64eba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="64eba-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="64eba-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64eba-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64eba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64eba-126">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="64eba-126">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





