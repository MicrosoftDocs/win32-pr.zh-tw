---
title: defi-ps
description: 定義整數常數值，此值應該會在著色器設定為裝置時載入。
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093036"
---
# <a name="defi---ps"></a><span data-ttu-id="5c242-103">defi-ps</span><span class="sxs-lookup"><span data-stu-id="5c242-103">defi - ps</span></span>

<span data-ttu-id="5c242-104">定義整數常數值，此值應該會在著色器設定為裝置時載入。</span><span class="sxs-lookup"><span data-stu-id="5c242-104">Defines an integer constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c242-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c242-105">Syntax</span></span>



| <span data-ttu-id="5c242-106">defi dst，integerValue</span><span class="sxs-lookup"><span data-stu-id="5c242-106">defi dst, integerValue</span></span> |
|------------------------|



 

-   <span data-ttu-id="5c242-107">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="5c242-107">dst is the destination register.</span></span>
-   <span data-ttu-id="5c242-108">integerValue 是常數整數值。</span><span class="sxs-lookup"><span data-stu-id="5c242-108">integerValue is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c242-109">備註</span><span class="sxs-lookup"><span data-stu-id="5c242-109">Remarks</span></span>



| <span data-ttu-id="5c242-110">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="5c242-110">Pixel shader versions</span></span> | <span data-ttu-id="5c242-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="5c242-111">1\_1</span></span> | <span data-ttu-id="5c242-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="5c242-112">1\_2</span></span> | <span data-ttu-id="5c242-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5c242-113">1\_3</span></span> | <span data-ttu-id="5c242-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="5c242-114">1\_4</span></span> | <span data-ttu-id="5c242-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c242-115">2\_0</span></span> | <span data-ttu-id="5c242-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5c242-116">2\_x</span></span> | <span data-ttu-id="5c242-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5c242-117">2\_sw</span></span> | <span data-ttu-id="5c242-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c242-118">3\_0</span></span> | <span data-ttu-id="5c242-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5c242-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5c242-120">defi</span><span class="sxs-lookup"><span data-stu-id="5c242-120">defi</span></span>                  |      |      |      |      |      | <span data-ttu-id="5c242-121">x</span><span class="sxs-lookup"><span data-stu-id="5c242-121">x</span></span>    | <span data-ttu-id="5c242-122">x</span><span class="sxs-lookup"><span data-stu-id="5c242-122">x</span></span>     | <span data-ttu-id="5c242-123">x</span><span class="sxs-lookup"><span data-stu-id="5c242-123">x</span></span>    | <span data-ttu-id="5c242-124">x</span><span class="sxs-lookup"><span data-stu-id="5c242-124">x</span></span>     |



 

<span data-ttu-id="5c242-125">Defi 指令會定義著色器常數，其值會在著色器設定為裝置時載入。</span><span class="sxs-lookup"><span data-stu-id="5c242-125">The defi instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="5c242-126">這些都稱為立即常數。</span><span class="sxs-lookup"><span data-stu-id="5c242-126">These are called immediate constants.</span></span> <span data-ttu-id="5c242-127">立即的常數優先于 API 方法 SetPixelShaderConstantB 所設定的常數。</span><span class="sxs-lookup"><span data-stu-id="5c242-127">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="5c242-128">有兩種方式可以設定著色器中的常數。</span><span class="sxs-lookup"><span data-stu-id="5c242-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="5c242-129">您可以使用 defi，直接在著色器內定義常數。</span><span class="sxs-lookup"><span data-stu-id="5c242-129">Use defi to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="5c242-130">使用 API 方法來設定常數。</span><span class="sxs-lookup"><span data-stu-id="5c242-130">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="5c242-131">使用 [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) 設定布林值常數。</span><span class="sxs-lookup"><span data-stu-id="5c242-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>
    -   <span data-ttu-id="5c242-132">使用 [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) 設定浮點數常數。</span><span class="sxs-lookup"><span data-stu-id="5c242-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) to set a floating-point constant.</span></span>
    -   <span data-ttu-id="5c242-133">使用 [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) 來設定整數常數。</span><span class="sxs-lookup"><span data-stu-id="5c242-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c242-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c242-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c242-135">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="5c242-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 