---
title: 輸入色彩暫存器
description: 包含頂點色彩的圖元著色器輸入暫存器。
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372674"
---
# <a name="input-color-register"></a><span data-ttu-id="a0494-103">輸入色彩暫存器</span><span class="sxs-lookup"><span data-stu-id="a0494-103">Input Color Register</span></span>

<span data-ttu-id="a0494-104">包含頂點色彩的圖元著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="a0494-104">Pixel shader input register containing vertex color.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0494-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0494-105">Syntax</span></span>


```
dcl v#.writeMask
```



<span data-ttu-id="a0494-106">其中：</span><span class="sxs-lookup"><span data-stu-id="a0494-106">where:</span></span>

-   <span data-ttu-id="a0494-107">[ (sm2，sm3-ps asm) ](dcl---ps.md) 是暫存器宣告指令。</span><span class="sxs-lookup"><span data-stu-id="a0494-107">[dcl - (sm2, sm3 - ps asm)](dcl---ps.md) is a register declaration instruction.</span></span>
-   <span data-ttu-id="a0494-108">v 是輸入暫存器，而 \# 是註冊編號。</span><span class="sxs-lookup"><span data-stu-id="a0494-108">v is an input register and \# is the register number.</span></span> <span data-ttu-id="a0494-109">允許的暫存器數目取決於著色器版本。</span><span class="sxs-lookup"><span data-stu-id="a0494-109">The number of registers allowed is determined by the shader version.</span></span>
-   <span data-ttu-id="a0494-110">writeMask 會判斷最多可 (四個) 寫入的元件。</span><span class="sxs-lookup"><span data-stu-id="a0494-110">writeMask determines which components (up to four) are written.</span></span> <span data-ttu-id="a0494-111">有效的元件包括： (x、y、z、w) 或 (r、g、b、) 。</span><span class="sxs-lookup"><span data-stu-id="a0494-111">Valid components are: (x,y,z,w) or (r,g,b,a).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0494-112">備註</span><span class="sxs-lookup"><span data-stu-id="a0494-112">Remarks</span></span>

<span data-ttu-id="a0494-113">色彩暫存器是唯讀的暫存器。</span><span class="sxs-lookup"><span data-stu-id="a0494-113">Color registers are read-only registers.</span></span> <span data-ttu-id="a0494-114">每個註冊包含四個元件的 RGBA 值，並從輸入頂點反復進行。</span><span class="sxs-lookup"><span data-stu-id="a0494-114">Each register contains four-component RGBA values iterated from input vertices.</span></span> <span data-ttu-id="a0494-115">它們的精確度比大部分的暫存器低，保證在範圍 (0、+ 1) 中有8位不帶正負號的資料。</span><span class="sxs-lookup"><span data-stu-id="a0494-115">They have lower precision than most registers, guaranteed to have 8 bits of unsigned data in the range (0, +1).</span></span> <span data-ttu-id="a0494-116">單一指令中不能使用一個以上的。</span><span class="sxs-lookup"><span data-stu-id="a0494-116">You cannot use more than one in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0494-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0494-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0494-118">寄存 器</span><span class="sxs-lookup"><span data-stu-id="a0494-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="a0494-119">ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊</span><span class="sxs-lookup"><span data-stu-id="a0494-119">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="a0494-120">ps \_ 2 \_ 0 註冊</span><span class="sxs-lookup"><span data-stu-id="a0494-120">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="a0494-121">ps \_ 2 \_ x 註冊</span><span class="sxs-lookup"><span data-stu-id="a0494-121">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="a0494-122">ps \_ 3 \_ 0 註冊</span><span class="sxs-lookup"><span data-stu-id="a0494-122">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




