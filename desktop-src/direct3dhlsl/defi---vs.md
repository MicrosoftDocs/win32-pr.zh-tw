---
title: defi-vs
description: 定義整數常數值，此值應該會在著色器設定為裝置時，隨時載入。
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508060"
---
# <a name="defi---vs"></a><span data-ttu-id="0dba9-103">defi-vs</span><span class="sxs-lookup"><span data-stu-id="0dba9-103">defi - vs</span></span>

<span data-ttu-id="0dba9-104">定義整數常數值，此值應該會在著色器設定為裝置時，隨時載入。</span><span class="sxs-lookup"><span data-stu-id="0dba9-104">Defines an integer constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dba9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dba9-105">Syntax</span></span>



| <span data-ttu-id="0dba9-106">defi dst、integerValue0、integerValue1、integerValue2、integerValue3</span><span class="sxs-lookup"><span data-stu-id="0dba9-106">defi dst, integerValue0, integerValue1, integerValue2, integerValue3</span></span> |
|----------------------------------------------------------------------|



 

-   <span data-ttu-id="0dba9-107">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="0dba9-107">dst is the destination register.</span></span>
-   <span data-ttu-id="0dba9-108">integerValue \# 是常數整數值。</span><span class="sxs-lookup"><span data-stu-id="0dba9-108">integerValue\# is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dba9-109">備註</span><span class="sxs-lookup"><span data-stu-id="0dba9-109">Remarks</span></span>



| <span data-ttu-id="0dba9-110">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="0dba9-110">Vertex shader versions</span></span> | <span data-ttu-id="0dba9-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="0dba9-111">1\_1</span></span> | <span data-ttu-id="0dba9-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0dba9-112">2\_0</span></span> | <span data-ttu-id="0dba9-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0dba9-113">2\_x</span></span> | <span data-ttu-id="0dba9-114">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="0dba9-114">2\_sw</span></span> | <span data-ttu-id="0dba9-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0dba9-115">3\_0</span></span> | <span data-ttu-id="0dba9-116">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="0dba9-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="0dba9-117">defi</span><span class="sxs-lookup"><span data-stu-id="0dba9-117">defi</span></span>                   |      | <span data-ttu-id="0dba9-118">x</span><span class="sxs-lookup"><span data-stu-id="0dba9-118">x</span></span>    | <span data-ttu-id="0dba9-119">x</span><span class="sxs-lookup"><span data-stu-id="0dba9-119">x</span></span>    | <span data-ttu-id="0dba9-120">x</span><span class="sxs-lookup"><span data-stu-id="0dba9-120">x</span></span>     | <span data-ttu-id="0dba9-121">x</span><span class="sxs-lookup"><span data-stu-id="0dba9-121">x</span></span>    | <span data-ttu-id="0dba9-122">x</span><span class="sxs-lookup"><span data-stu-id="0dba9-122">x</span></span>     |



 

<span data-ttu-id="0dba9-123">Defi 指令會定義整數著色器常數，其值會在著色器設定為裝置時載入。</span><span class="sxs-lookup"><span data-stu-id="0dba9-123">The defi instruction defines an integer shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="0dba9-124">這些都稱為立即常數。</span><span class="sxs-lookup"><span data-stu-id="0dba9-124">These are called immediate constants.</span></span> <span data-ttu-id="0dba9-125">立即的常數優先于 API 方法 SetVertexShaderConstantI 所設定的常數。</span><span class="sxs-lookup"><span data-stu-id="0dba9-125">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantI.</span></span>

<span data-ttu-id="0dba9-126">有兩種方式可以設定著色器中的整數常數。</span><span class="sxs-lookup"><span data-stu-id="0dba9-126">There are two ways to set an integer constant in a shader.</span></span>

1.  <span data-ttu-id="0dba9-127">您可以使用 defi 直接定義著色器內的整數常數向量。</span><span class="sxs-lookup"><span data-stu-id="0dba9-127">Use defi to define the integer constant vector directly inside a shader.</span></span>
2.  <span data-ttu-id="0dba9-128">使用 API 方法來設定常數。</span><span class="sxs-lookup"><span data-stu-id="0dba9-128">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="0dba9-129">使用 [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) 來設定整數常數。</span><span class="sxs-lookup"><span data-stu-id="0dba9-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0dba9-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="0dba9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dba9-131">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="0dba9-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="0dba9-132">def-vs</span><span class="sxs-lookup"><span data-stu-id="0dba9-132">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="0dba9-133">defb-vs</span><span class="sxs-lookup"><span data-stu-id="0dba9-133">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 