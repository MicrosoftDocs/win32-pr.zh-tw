---
title: " pragma 指示詞"
description: 預處理器指示詞，提供電腦特定或作業系統特有的功能，同時保留與 C 和 c + + 語言的整體相容性。
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022472"
---
# <a name="pragma-directive"></a><span data-ttu-id="9574a-104">\#pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="9574a-104">\#pragma Directive</span></span>

<span data-ttu-id="9574a-105">預處理器指示詞，提供電腦特定或作業系統特有的功能，同時保留與 C 和 c + + 語言的整體相容性。</span><span class="sxs-lookup"><span data-stu-id="9574a-105">Preprocessor directive that provides machine-specific or operating system-specific features while retaining overall compatibility with the C and C++ languages.</span></span>



| <span data-ttu-id="9574a-106">\#pragma *token-字串*</span><span class="sxs-lookup"><span data-stu-id="9574a-106">\#pragma *token-string*</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="9574a-107">參數</span><span class="sxs-lookup"><span data-stu-id="9574a-107">Parameters</span></span>



| <span data-ttu-id="9574a-108">項目</span><span class="sxs-lookup"><span data-stu-id="9574a-108">Item</span></span>                                                                                    | <span data-ttu-id="9574a-109">描述</span><span class="sxs-lookup"><span data-stu-id="9574a-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9574a-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-字串*</span><span class="sxs-lookup"><span data-stu-id="9574a-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="9574a-111">提供特定編譯器指令和引數的字元系列。</span><span class="sxs-lookup"><span data-stu-id="9574a-111">Series of characters that gives a specific compiler instruction and arguments.</span></span> <span data-ttu-id="9574a-112">此參數受限於宏展開。</span><span class="sxs-lookup"><span data-stu-id="9574a-112">This parameter is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="9574a-113">備註</span><span class="sxs-lookup"><span data-stu-id="9574a-113">Remarks</span></span>

<span data-ttu-id="9574a-114">如果編譯器發現無法辨識的 pragma，則會發出警告，但編譯會繼續進行。</span><span class="sxs-lookup"><span data-stu-id="9574a-114">If the compiler finds a pragma it does not recognize, it issues a warning, but compilation continues.</span></span>

<span data-ttu-id="9574a-115">HLSL 編譯器會辨識下列 pragma：</span><span class="sxs-lookup"><span data-stu-id="9574a-115">The HLSL compiler recognizes the following pragmas:</span></span>

-   [<span data-ttu-id="9574a-116">Def</span><span class="sxs-lookup"><span data-stu-id="9574a-116">def</span></span>](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [<span data-ttu-id="9574a-117">message</span><span class="sxs-lookup"><span data-stu-id="9574a-117">message</span></span>](message-pragma-directive--directx-hlsl-.md)
-   [<span data-ttu-id="9574a-118">套件 \_ 矩陣</span><span class="sxs-lookup"><span data-stu-id="9574a-118">pack\_matrix</span></span>](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [<span data-ttu-id="9574a-119">warning</span><span class="sxs-lookup"><span data-stu-id="9574a-119">warning</span></span>](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a><span data-ttu-id="9574a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9574a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9574a-121"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="9574a-121">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





