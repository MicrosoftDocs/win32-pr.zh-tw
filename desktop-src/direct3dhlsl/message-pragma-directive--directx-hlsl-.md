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
ms.openlocfilehash: 813483efb161a06db5ef7e40da99c391f53565bc
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153481"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="a80d1-104">message pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="a80d1-104">message pragma Directive</span></span>

<span data-ttu-id="a80d1-105">產生編譯器時間訊息的 Pragma 指示詞。</span><span class="sxs-lookup"><span data-stu-id="a80d1-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="a80d1-106">\#pragma message ( "*token-string*" ) </span><span class="sxs-lookup"><span data-stu-id="a80d1-106">\#pragma message("*token-string*")</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="a80d1-107">參數</span><span class="sxs-lookup"><span data-stu-id="a80d1-107">Parameters</span></span>



| <span data-ttu-id="a80d1-108">項目</span><span class="sxs-lookup"><span data-stu-id="a80d1-108">Item</span></span>                                                                                    | <span data-ttu-id="a80d1-109">描述</span><span class="sxs-lookup"><span data-stu-id="a80d1-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="a80d1-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-字串*</span><span class="sxs-lookup"><span data-stu-id="a80d1-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="a80d1-111">編譯器訊息。</span><span class="sxs-lookup"><span data-stu-id="a80d1-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="a80d1-112">範例</span><span class="sxs-lookup"><span data-stu-id="a80d1-112">Examples</span></span>

<span data-ttu-id="a80d1-113">下列範例示範在前置處理期間的訊息處理。</span><span class="sxs-lookup"><span data-stu-id="a80d1-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="a80d1-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a80d1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80d1-115"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="a80d1-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="a80d1-116">\# (DirectX HLSL) 的 pragma 指示詞 </span><span class="sxs-lookup"><span data-stu-id="a80d1-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





