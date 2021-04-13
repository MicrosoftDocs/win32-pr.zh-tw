---
title: 'EM_GETWORDWRAPMODE 訊息 (Richedit .h) '
description: 取得 rich edit 控制項的目前文字換行和斷詞選項。
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464541"
---
# <a name="em_getwordwrapmode-message"></a><span data-ttu-id="e8f8c-104">EM \_ GETWORDWRAPMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="e8f8c-104">EM\_GETWORDWRAPMODE message</span></span>

<span data-ttu-id="e8f8c-105">取得 rich edit 控制項的目前文字換行和斷詞選項。</span><span class="sxs-lookup"><span data-stu-id="e8f8c-105">Gets the current word wrap and word-break options for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="e8f8c-106">只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="e8f8c-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="e8f8c-107">任何較新版本的 Rich Edit 都不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="e8f8c-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="e8f8c-108">參數</span><span class="sxs-lookup"><span data-stu-id="e8f8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8f8c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8f8c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f8c-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="e8f8c-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e8f8c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8f8c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8f8c-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="e8f8c-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8f8c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8f8c-113">Return value</span></span>

<span data-ttu-id="e8f8c-114">訊息會傳回目前的自動換行和斷詞選項。</span><span class="sxs-lookup"><span data-stu-id="e8f8c-114">The message returns the current word wrap and word-break options.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8f8c-115">備註</span><span class="sxs-lookup"><span data-stu-id="e8f8c-115">Remarks</span></span>

<span data-ttu-id="e8f8c-116">此訊息不得由應用程式定義的斷詞程式傳送。</span><span class="sxs-lookup"><span data-stu-id="e8f8c-116">This message must not be sent by the application-defined, word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8f8c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8f8c-117">Requirements</span></span>



| <span data-ttu-id="e8f8c-118">需求</span><span class="sxs-lookup"><span data-stu-id="e8f8c-118">Requirement</span></span> | <span data-ttu-id="e8f8c-119">值</span><span class="sxs-lookup"><span data-stu-id="e8f8c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f8c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8f8c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e8f8c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8f8c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8f8c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8f8c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e8f8c-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8f8c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8f8c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e8f8c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8f8c-125"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8f8c-125"><dt>Richedit.h</dt></span></span> </dl> |



 

 





