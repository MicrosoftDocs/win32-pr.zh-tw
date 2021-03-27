---
title: message pragma 指示詞
description: 產生編譯器時間訊息的 Pragma 指示詞。
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- message pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f342f4a139320e4beb821f32662da72785ab751c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678816"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="a5331-104">message pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="a5331-104">message pragma Directive</span></span>

<span data-ttu-id="a5331-105">產生編譯器時間訊息的 Pragma 指示詞。</span><span class="sxs-lookup"><span data-stu-id="a5331-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="a5331-106">\#pragma 訊息 "*token-string*"</span><span class="sxs-lookup"><span data-stu-id="a5331-106">\#pragma message "*token-string*"</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="a5331-107">參數</span><span class="sxs-lookup"><span data-stu-id="a5331-107">Parameters</span></span>



| <span data-ttu-id="a5331-108">項目</span><span class="sxs-lookup"><span data-stu-id="a5331-108">Item</span></span>                                                                                    | <span data-ttu-id="a5331-109">描述</span><span class="sxs-lookup"><span data-stu-id="a5331-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="a5331-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-字串*</span><span class="sxs-lookup"><span data-stu-id="a5331-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="a5331-111">編譯器訊息。</span><span class="sxs-lookup"><span data-stu-id="a5331-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="a5331-112">範例</span><span class="sxs-lookup"><span data-stu-id="a5331-112">Examples</span></span>

<span data-ttu-id="a5331-113">下列範例示範在前置處理期間的訊息處理。</span><span class="sxs-lookup"><span data-stu-id="a5331-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="a5331-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5331-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5331-115"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="a5331-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="a5331-116">\# (DirectX HLSL) 的 pragma 指示詞 </span><span class="sxs-lookup"><span data-stu-id="a5331-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





