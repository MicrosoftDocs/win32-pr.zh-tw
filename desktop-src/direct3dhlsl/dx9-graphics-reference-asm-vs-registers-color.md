---
title: 色彩註冊
description: 這些頂點著色器輸出暫存器包含色彩值。
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104321324"
---
# <a name="color-register"></a><span data-ttu-id="34df0-103">色彩註冊</span><span class="sxs-lookup"><span data-stu-id="34df0-103">Color Register</span></span>

<span data-ttu-id="34df0-104">這些頂點著色器輸出暫存器包含色彩值。</span><span class="sxs-lookup"><span data-stu-id="34df0-104">These vertex shader output registers contain a color value.</span></span> 

| <span data-ttu-id="34df0-105">註冊</span><span class="sxs-lookup"><span data-stu-id="34df0-105">Register</span></span> | <span data-ttu-id="34df0-106">Description</span><span class="sxs-lookup"><span data-stu-id="34df0-106">Description</span></span>              |
|----------|--------------------------|
| <span data-ttu-id="34df0-107">oD0</span><span class="sxs-lookup"><span data-stu-id="34df0-107">oD0</span></span>      | <span data-ttu-id="34df0-108">擴散色彩註冊。</span><span class="sxs-lookup"><span data-stu-id="34df0-108">diffuse color register.</span></span>  |
| <span data-ttu-id="34df0-109">oD1</span><span class="sxs-lookup"><span data-stu-id="34df0-109">oD1</span></span>      | <span data-ttu-id="34df0-110">反射色彩註冊。</span><span class="sxs-lookup"><span data-stu-id="34df0-110">specular color register.</span></span> |



 

<span data-ttu-id="34df0-111">OD0 值會插入，並寫入至圖元著色器色彩 register 0 (v0) 。</span><span class="sxs-lookup"><span data-stu-id="34df0-111">The oD0 value is interpolated and is written to the pixel shader color register 0 (v0).</span></span> <span data-ttu-id="34df0-112">OD1 值會插入並寫入至圖元著色器色彩註冊 1 (v1) 。</span><span class="sxs-lookup"><span data-stu-id="34df0-112">The oD1 value is interpolated and written to the pixel shader color register 1 (v1).</span></span> <span data-ttu-id="34df0-113">如需圖元著色器色彩暫存器的詳細資訊，請參閱圖元著色器 [輸入色彩註冊](dx9-graphics-reference-asm-ps-registers-input-color.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="34df0-113">For more information about pixel shader color registers, see the pixel shader [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="34df0-114">備註</span><span class="sxs-lookup"><span data-stu-id="34df0-114">Remarks</span></span>

<span data-ttu-id="34df0-115">範例</span><span class="sxs-lookup"><span data-stu-id="34df0-115">Example</span></span>


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a><span data-ttu-id="34df0-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="34df0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34df0-117">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="34df0-117">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




