---
title: 來源登錄反轉
description: 針對指定之註冊的每個通道，執行 (1 值) 計算。
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971456"
---
# <a name="source-register-invert"></a><span data-ttu-id="9f32b-103">來源登錄反轉</span><span class="sxs-lookup"><span data-stu-id="9f32b-103">Source Register Invert</span></span>

<span data-ttu-id="9f32b-104">針對指定之註冊的每個通道，執行 (1 值) 計算。</span><span class="sxs-lookup"><span data-stu-id="9f32b-104">Performs a (1 - value) calculation for each channel of the specified register.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f32b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f32b-105">Syntax</span></span>


```
1 - register
```



## <a name="registers"></a><span data-ttu-id="9f32b-106">暫存器</span><span class="sxs-lookup"><span data-stu-id="9f32b-106">Registers</span></span>

<span data-ttu-id="9f32b-107">來源註冊。</span><span class="sxs-lookup"><span data-stu-id="9f32b-107">Source Register.</span></span> <span data-ttu-id="9f32b-108">如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="9f32b-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f32b-109">備註</span><span class="sxs-lookup"><span data-stu-id="9f32b-109">Remarks</span></span>

<span data-ttu-id="9f32b-110">註冊的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="9f32b-110">The contents of the register are not changed.</span></span> <span data-ttu-id="9f32b-111">修飾詞只會套用至從註冊讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="9f32b-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="9f32b-112"> (RGBA) 的所有四色通道都會套用反向運算。</span><span class="sxs-lookup"><span data-stu-id="9f32b-112">The invert operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="9f32b-113">此修飾詞只能搭配算術指令使用。</span><span class="sxs-lookup"><span data-stu-id="9f32b-113">This modifier can be used only with arithmetic instructions.</span></span> <span data-ttu-id="9f32b-114">此外，此修飾詞不能與其他 [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)合併。</span><span class="sxs-lookup"><span data-stu-id="9f32b-114">In addition, this modifier cannot be combined with the other [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="example"></a><span data-ttu-id="9f32b-115">範例</span><span class="sxs-lookup"><span data-stu-id="9f32b-115">Example</span></span>

<span data-ttu-id="9f32b-116">此範例會使用反轉來產生 register r1 的補數。</span><span class="sxs-lookup"><span data-stu-id="9f32b-116">This example uses inversion to generate the complement of register r1.</span></span>


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a><span data-ttu-id="9f32b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f32b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f32b-118">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="9f32b-118">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




