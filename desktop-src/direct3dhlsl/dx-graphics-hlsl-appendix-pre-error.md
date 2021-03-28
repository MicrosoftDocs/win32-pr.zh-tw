---
title: " error 指示詞"
description: 產生編譯器時間錯誤訊息的預處理器指示詞。
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- error 指示詞 HLSL
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373034"
---
# <a name="error-directive"></a><span data-ttu-id="58175-104">\#error 指示詞</span><span class="sxs-lookup"><span data-stu-id="58175-104">\#error Directive</span></span>

<span data-ttu-id="58175-105">產生編譯器時間錯誤訊息的預處理器指示詞。</span><span class="sxs-lookup"><span data-stu-id="58175-105">Preprocessor directive that produces compiler-time error messages.</span></span>



| <span data-ttu-id="58175-106">\#錯誤 *標記-字串*</span><span class="sxs-lookup"><span data-stu-id="58175-106">\#error *token-string*</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="58175-107">參數</span><span class="sxs-lookup"><span data-stu-id="58175-107">Parameters</span></span>



| <span data-ttu-id="58175-108">項目</span><span class="sxs-lookup"><span data-stu-id="58175-108">Item</span></span>                                                                                    | <span data-ttu-id="58175-109">描述</span><span class="sxs-lookup"><span data-stu-id="58175-109">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58175-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-字串*</span><span class="sxs-lookup"><span data-stu-id="58175-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="58175-111">錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="58175-111">Error message.</span></span> <span data-ttu-id="58175-112">這個參數是由一系列的 token 所組成，例如關鍵字、常數或完整語句。</span><span class="sxs-lookup"><span data-stu-id="58175-112">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="58175-113">標記字串受限於宏展開。</span><span class="sxs-lookup"><span data-stu-id="58175-113">The token string is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="58175-114">備註</span><span class="sxs-lookup"><span data-stu-id="58175-114">Remarks</span></span>

<span data-ttu-id="58175-115">\#error 指示詞最適合用來偵測程式設計師不一致，並在前置處理期間違反條件約束。</span><span class="sxs-lookup"><span data-stu-id="58175-115">\#error directives are most useful for detecting programmer inconsistencies and violation of constraints during preprocessing.</span></span> <span data-ttu-id="58175-116">當遇到 error 指示詞時 \# ，編譯就會終止。</span><span class="sxs-lookup"><span data-stu-id="58175-116">When an \#error directive is encountered, compilation terminates.</span></span>

## <a name="examples"></a><span data-ttu-id="58175-117">範例</span><span class="sxs-lookup"><span data-stu-id="58175-117">Examples</span></span>

<span data-ttu-id="58175-118">下列範例示範前置處理期間的錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="58175-118">The following example demonstrates error processing during preprocessing.</span></span>


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a><span data-ttu-id="58175-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58175-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58175-120"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="58175-120">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





