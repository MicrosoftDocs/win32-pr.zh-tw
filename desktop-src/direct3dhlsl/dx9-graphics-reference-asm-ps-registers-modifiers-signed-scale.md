---
title: 來源註冊已簽署的調整
description: 從每個通道減去0.5，並依2.0 調整結果。 名稱 bx2 來自偏差和相應減少-二，也就是它所執行的作業。
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184194"
---
# <a name="source-register-signed-scaling"></a><span data-ttu-id="f2a4e-104">來源註冊已簽署的調整</span><span class="sxs-lookup"><span data-stu-id="f2a4e-104">Source Register Signed Scaling</span></span>

<span data-ttu-id="f2a4e-105">從每個通道減去0.5，並依2.0 調整結果。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-105">Subtracts 0.5 from each channel and scales the result by 2.0.</span></span> <span data-ttu-id="f2a4e-106">名稱 bx2 來自偏差和相應減少-二，也就是它所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-106">The name bx2 comes from bias and scale-times-two, which is the operation it performs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a4e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2a4e-107">Syntax</span></span>


```
source register_bx2
```



## <a name="register"></a><span data-ttu-id="f2a4e-108">註冊</span><span class="sxs-lookup"><span data-stu-id="f2a4e-108">Register</span></span>

<span data-ttu-id="f2a4e-109">來源註冊。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-109">Source Register.</span></span> <span data-ttu-id="f2a4e-110">如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-110">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2a4e-111">備註</span><span class="sxs-lookup"><span data-stu-id="f2a4e-111">Remarks</span></span>

<span data-ttu-id="f2a4e-112">這項作業通常用來將資料從 \[ 0.0 擴充至 \] 1.0 1.0 至 \[ 1.0 \] 。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-112">This operation is commonly used to expand data from \[0.0 to 1.0\] to \[-1.0 to 1.0\].</span></span> <span data-ttu-id="f2a4e-113">這個修飾詞是設計來搭配算術指令使用。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-113">This modifier is designed for use with the arithmetic instructions.</span></span> <span data-ttu-id="f2a4e-114">此修飾詞通常用於輸入點乘積指令 ([dp3-ps](dp3---ps.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-114">This modifier is commonly used on inputs to the dot product instruction ([dp3 - ps](dp3---ps.md)).</span></span> <span data-ttu-id="f2a4e-115">對 \_ 範圍0到1以外的資料使用 bx2 可能會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-115">Using \_bx2 on data outside the range 0 to 1 may produce undefined results.</span></span>

<span data-ttu-id="f2a4e-116">已簽署的調整作業會套用至下一個指令執行之前從註冊讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-116">The signed scaling operation is applied to the data read from the register before the next instruction is run.</span></span> <span data-ttu-id="f2a4e-117">此作業會套用至所有四色通道 (RGBA) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f2a4e-117">The operation is applied to all four color channels (RGBA) as follows:</span></span>


```
y = 2(x - 0.5)
```



<span data-ttu-id="f2a4e-118">註冊的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-118">The contents of the register are not changed.</span></span> <span data-ttu-id="f2a4e-119">修飾詞只會套用至從註冊讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-119">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="f2a4e-120">此修飾詞與 [來源](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) 暫存器有互斥，因此無法套用至相同的暫存器。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-120">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="f2a4e-121">版本資訊：</span><span class="sxs-lookup"><span data-stu-id="f2a4e-121">Version information:</span></span>

-   <span data-ttu-id="f2a4e-122">針對 ps \_ 1 \_ 0 和 ps \_ 1 \_ 1，您可以 \_ 在任何來源登錄上使用 bx2，以取得表單 texm3x2 \* 和 texm3x3 的材質指示 \* 。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-122">For ps\_1\_0 and ps\_1\_1, you can use \_bx2 on any source register for texture instructions of the form texm3x2\* and texm3x3\*.</span></span> <span data-ttu-id="f2a4e-123">\_bx2 不能用於任何其他的材質指示，例如 [texreg2ar-ps](texreg2ar---ps.md) 或 [texreg2gb](texreg2gb---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-123">\_bx2 cannot be used on any of the other texture instructions such as [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md).</span></span>
-   <span data-ttu-id="f2a4e-124">針對 ps \_ 1 \_ 2 和 ps \_ 1 \_ 3，您可以 \_ 在任何來源登錄上使用 bx2，以取得任何 tex \* 指令，但不包括： [texreg2ar-ps](texreg2ar---ps.md)、 [texreg2gb-ps](texreg2gb---ps.md)、 [texbem-ps](texbem---ps.md) 或 [texbeml-ps](texbeml---ps.md)。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-124">For ps\_1\_2 and ps\_1\_3, you can use \_bx2 on any source register for any tex\* instruction except: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) or [texbeml - ps](texbeml---ps.md).</span></span>

## <a name="example"></a><span data-ttu-id="f2a4e-125">範例</span><span class="sxs-lookup"><span data-stu-id="f2a4e-125">Example</span></span>

<span data-ttu-id="f2a4e-126">此範例會取樣材質、將資料轉換為-1 到 + 1 的範圍，並計算點乘積。</span><span class="sxs-lookup"><span data-stu-id="f2a4e-126">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a><span data-ttu-id="f2a4e-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2a4e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2a4e-128">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="f2a4e-128">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




