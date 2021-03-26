---
title: 來源註冊級別 x 2
description: 將值乘以二，再于指令中使用。
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971453"
---
# <a name="source-register-scale-x-2"></a><span data-ttu-id="f80f4-103">來源註冊級別 x 2</span><span class="sxs-lookup"><span data-stu-id="f80f4-103">Source Register Scale x 2</span></span>

<span data-ttu-id="f80f4-104">將值乘以二，再于指令中使用。</span><span class="sxs-lookup"><span data-stu-id="f80f4-104">Multiply the value by two before using it in the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="f80f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f80f4-105">Syntax</span></span>


```
register_x2
```



## <a name="register"></a><span data-ttu-id="f80f4-106">註冊</span><span class="sxs-lookup"><span data-stu-id="f80f4-106">Register</span></span>

<span data-ttu-id="f80f4-107">來源註冊。</span><span class="sxs-lookup"><span data-stu-id="f80f4-107">Source register.</span></span> <span data-ttu-id="f80f4-108">如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="f80f4-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f80f4-109">備註</span><span class="sxs-lookup"><span data-stu-id="f80f4-109">Remarks</span></span>

<span data-ttu-id="f80f4-110">註冊的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="f80f4-110">The contents of the register are not changed.</span></span> <span data-ttu-id="f80f4-111">修飾詞只會套用至從註冊讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="f80f4-111">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="f80f4-112">此修飾詞與來源登錄 [反轉](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)互斥，因此無法套用至相同的暫存器。</span><span class="sxs-lookup"><span data-stu-id="f80f4-112">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

<span data-ttu-id="f80f4-113">此修飾詞僅適用于第1版中的算術指令 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f80f4-113">This modifier is only available to arithmetic instructions in version 1\_4.</span></span>

## <a name="example"></a><span data-ttu-id="f80f4-114">範例</span><span class="sxs-lookup"><span data-stu-id="f80f4-114">Example</span></span>

<span data-ttu-id="f80f4-115">此範例會取樣材質、將資料轉換為-1 到 + 1 的範圍，並計算點乘積。</span><span class="sxs-lookup"><span data-stu-id="f80f4-115">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a><span data-ttu-id="f80f4-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="f80f4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f80f4-117">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="f80f4-117">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




