---
title: 來源註冊偏差
description: 從所有元件減去0.5。
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932585"
---
# <a name="source-register-bias"></a><span data-ttu-id="e7d6a-103">來源註冊偏差</span><span class="sxs-lookup"><span data-stu-id="e7d6a-103">Source Register Bias</span></span>

<span data-ttu-id="e7d6a-104">從所有元件減去0.5。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-104">Subtract 0.5 from all components.</span></span>

## <a name="registers"></a><span data-ttu-id="e7d6a-105">暫存器</span><span class="sxs-lookup"><span data-stu-id="e7d6a-105">Registers</span></span>

<span data-ttu-id="e7d6a-106">來源註冊。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-106">Source register.</span></span> <span data-ttu-id="e7d6a-107">如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-107">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d6a-108">備註</span><span class="sxs-lookup"><span data-stu-id="e7d6a-108">Remarks</span></span>

<span data-ttu-id="e7d6a-109">註冊的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-109">The contents of the register are not changed.</span></span> <span data-ttu-id="e7d6a-110">修飾詞只會套用至從註冊讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-110">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="e7d6a-111">偏差會套用至所有四色通道 (RGBA) 如下所示：</span><span class="sxs-lookup"><span data-stu-id="e7d6a-111">The bias is applied to all four color channels (RGBA) as follows:</span></span>


```
output = (input - 0.5)
```



<span data-ttu-id="e7d6a-112">效果是修改範圍介於0到1之間的資料，範圍從-0.5 到0.5。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-112">The effect is to modify data that was in the range 0 to 1 to be in the range -0.5 to 0.5.</span></span> <span data-ttu-id="e7d6a-113">將偏差套用到此範圍以外的資料可能會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-113">Applying bias to data outside this range may produce undefined results.</span></span>

> [!Note]  
> <span data-ttu-id="e7d6a-114">此修飾詞與來源登錄 [反轉](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)互斥，因此無法套用至相同的暫存器。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

 

<span data-ttu-id="e7d6a-115">此修飾詞用於算術指令。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-115">This modifier is for use with the arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="e7d6a-116">範例</span><span class="sxs-lookup"><span data-stu-id="e7d6a-116">Example</span></span>

<span data-ttu-id="e7d6a-117">此範例會執行與 \_ DirectX 6.0 和7.0 多重紋理語法中的 D3DTOP ADDSIGNED 相同的作業。</span><span class="sxs-lookup"><span data-stu-id="e7d6a-117">This example performs the same operation as D3DTOP\_ADDSIGNED in DirectX 6.0 and 7.0 multiple texture syntax.</span></span>


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a><span data-ttu-id="e7d6a-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7d6a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7d6a-119">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="e7d6a-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




