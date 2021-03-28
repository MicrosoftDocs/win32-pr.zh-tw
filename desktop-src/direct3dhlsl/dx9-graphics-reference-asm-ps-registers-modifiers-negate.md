---
title: 來源註冊否定
description: 在所有的暫存器元件上執行 (y x) 的否定。
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021338"
---
# <a name="source-register-negate"></a><span data-ttu-id="74344-103">來源註冊否定</span><span class="sxs-lookup"><span data-stu-id="74344-103">Source Register Negate</span></span>

<span data-ttu-id="74344-104">在所有的暫存器元件上執行 (y =-x) 的否定。</span><span class="sxs-lookup"><span data-stu-id="74344-104">Performs a negate (y = -x), on all register components.</span></span>

## <a name="syntax"></a><span data-ttu-id="74344-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74344-105">Syntax</span></span>


```
- register
```



## <a name="registers"></a><span data-ttu-id="74344-106">暫存器</span><span class="sxs-lookup"><span data-stu-id="74344-106">Registers</span></span>

<span data-ttu-id="74344-107">來源註冊。</span><span class="sxs-lookup"><span data-stu-id="74344-107">Source Register.</span></span> <span data-ttu-id="74344-108">如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="74344-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="74344-109">備註</span><span class="sxs-lookup"><span data-stu-id="74344-109">Remarks</span></span>

<span data-ttu-id="74344-110">註冊的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="74344-110">The contents of the register are not changed.</span></span> <span data-ttu-id="74344-111">修飾詞只會套用至從註冊讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="74344-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="74344-112">「否定」作業會套用至所有四色通道 (RGBA) 。</span><span class="sxs-lookup"><span data-stu-id="74344-112">The negate operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="74344-113">這項作業會在相同引數上出現的任何其他修飾詞之後執行。</span><span class="sxs-lookup"><span data-stu-id="74344-113">This operation is performed after any other modifiers present on the same argument.</span></span>

<span data-ttu-id="74344-114">此修飾詞與 [來源](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) 暫存器有互斥，因此無法套用至相同的暫存器。</span><span class="sxs-lookup"><span data-stu-id="74344-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="74344-115">此修飾詞僅用於算術指令。</span><span class="sxs-lookup"><span data-stu-id="74344-115">This modifier is for use only with arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="74344-116">範例</span><span class="sxs-lookup"><span data-stu-id="74344-116">Example</span></span>

<span data-ttu-id="74344-117">下列範例會示範如何使用這個修飾詞。</span><span class="sxs-lookup"><span data-stu-id="74344-117">The following example shows how to use this modifier.</span></span>


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a><span data-ttu-id="74344-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="74344-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74344-119">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="74344-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




