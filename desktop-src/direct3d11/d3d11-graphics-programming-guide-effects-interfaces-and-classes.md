---
title: 作用中的介面和類別
description: 有許多方法可以在效果11中使用類別和介面。
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375724"
---
# <a name="interfaces-and-classes-in-effects"></a><span data-ttu-id="f0dcc-103">作用中的介面和類別</span><span class="sxs-lookup"><span data-stu-id="f0dcc-103">Interfaces and Classes in Effects</span></span>

<span data-ttu-id="f0dcc-104">有許多方法可以在效果11中使用類別和介面。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-104">There are many ways to use classes and interfaces in Effects 11.</span></span> <span data-ttu-id="f0dcc-105">如需介面和類別語法，請參閱 [介面和類別](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class)。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-105">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="f0dcc-106">下列各節將詳細說明如何指定類別實例至使用介面的著色器。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-106">The following sections detail how to specify class instances to a shader which uses interfaces.</span></span> <span data-ttu-id="f0dcc-107">我們將在範例中使用下列介面和類別：</span><span class="sxs-lookup"><span data-stu-id="f0dcc-107">We will use the following interface and classes in the examples:</span></span>


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



<span data-ttu-id="f0dcc-108">請注意，介面實例可以初始化為類別實例。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-108">Note that interface instances can be initialized to class instances.</span></span> <span data-ttu-id="f0dcc-109">也支援類別和介面實例的陣列，並可將其初始化，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="f0dcc-109">Arrays of class and interface instances are also supported and they can be initialized as in the following example:</span></span>


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a><span data-ttu-id="f0dcc-110">統一介面參數</span><span class="sxs-lookup"><span data-stu-id="f0dcc-110">Uniform Interface Parameters</span></span>

<span data-ttu-id="f0dcc-111">就像其他的統一資料類型一樣，必須在 CompileShader 呼叫中指定統一的介面參數。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-111">Just like other uniform data types, uniform interface parameters must be specified in the CompileShader call.</span></span> <span data-ttu-id="f0dcc-112">介面參數可以指派給全域介面實例或全域類別實例。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-112">Interface parameters can be assigned to global interface instances or global class instances.</span></span> <span data-ttu-id="f0dcc-113">當指派給全域介面實例時，著色器會相依于介面實例，這表示它必須設定為類別實例。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-113">When assigned to a global interface instance, the shader will have a dependency on the interface instance, which means that it must be set to a class instance.</span></span> <span data-ttu-id="f0dcc-114">當指派給全域類別實例時，編譯器會特製化著色器 (與其他統一資料類型) 使用該類別。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-114">When assigned to global class instances, the compiler specializes the shader (as with other uniform data types) to use that class.</span></span> <span data-ttu-id="f0dcc-115">這對兩個案例很重要：</span><span class="sxs-lookup"><span data-stu-id="f0dcc-115">This is important for two scenarios:</span></span>

1.  <span data-ttu-id="f0dcc-116">\_如果這些參數是統一的，且已指派給全域類別實例，則具有 4 x 目標的著色器可以使用介面參數 (因此) 不會使用動態連結。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-116">Shaders with a 4\_x target can use interface parameters if these parameters are uniform and assigned to global class instances (so no dynamic linkage is used).</span></span>
2.  <span data-ttu-id="f0dcc-117">使用者可以決定有許多已編譯、特製化的著色器，不含動態連結或少數具有動態連結的已編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-117">Users can decide to have many compiled, specialized shaders with no dynamic linkage or few compiled shaders with dynamic linkage.</span></span>


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



<span data-ttu-id="f0dcc-118">如果 pIColor2 透過 API 保持不變，則前兩個階段的功能相同，但第二個階段會使用 ps \_ 4 \_ 0 靜態著色器，而第二個會使用 \_ \_ 具有動態連結的 ps 5 0 著色器。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-118">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent, but the first uses a ps\_4\_0 static shader while the second uses a ps\_5\_0 shader with dynamic linkage.</span></span> <span data-ttu-id="f0dcc-119">如果透過效果 API 變更 pIColor2 (請參閱) 下方設定類別實例，則第二個階段中圖元著色器的行為可能會變更。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-119">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="non-uniform-interface-parameters"></a><span data-ttu-id="f0dcc-120">非統一介面參數</span><span class="sxs-lookup"><span data-stu-id="f0dcc-120">Non-Uniform Interface Parameters</span></span>

<span data-ttu-id="f0dcc-121">非統一介面參數會建立著色器的介面相依性。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-121">Non-uniform interface parameters create interface dependencies for the shaders.</span></span> <span data-ttu-id="f0dcc-122">使用介面參數套用著色器時，必須在中使用 BindInterfaces 呼叫來指派這些參數。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-122">When applying a shader with interface parameters, these parameters must be assigned in with the BindInterfaces call.</span></span> <span data-ttu-id="f0dcc-123">全域介面實例和全域類別實例可以在 BindInterfaces 呼叫中指定。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-123">Global interface instances and global class instances can be specified in the BindInterfaces call.</span></span>


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



<span data-ttu-id="f0dcc-124">如果 pIColor2 透過 API 保持不變，則前兩個階段的功能相同，而且兩者都會使用動態連結。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-124">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent and both use dynamic linkage.</span></span> <span data-ttu-id="f0dcc-125">如果透過效果 API 變更 pIColor2 (請參閱) 下方設定類別實例，則第二個階段中圖元著色器的行為可能會變更。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-125">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="setting-class-instances"></a><span data-ttu-id="f0dcc-126">設定類別實例</span><span class="sxs-lookup"><span data-stu-id="f0dcc-126">Setting Class Instances</span></span>

<span data-ttu-id="f0dcc-127">當您將具有動態著色器連結的著色器設定為 Direct3D 11 裝置時，也必須指定類別實例。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-127">When setting a shader with dynamic shader linkage to the Direct3D 11 device, class instances must also be specified.</span></span> <span data-ttu-id="f0dcc-128">使用 **Null** 類別實例來設定這類著色器是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-128">It is an error to set such a shader with a **NULL** class instance.</span></span> <span data-ttu-id="f0dcc-129">因此，著色器參考的所有介面實例都必須有相關聯的類別實例。</span><span class="sxs-lookup"><span data-stu-id="f0dcc-129">Therefore, all interface instances which a shader references must have an associated class instance.</span></span>

<span data-ttu-id="f0dcc-130">下列範例示範如何從效果中取得類別執行個體變數，並將它設定為介面變數：</span><span class="sxs-lookup"><span data-stu-id="f0dcc-130">The following example shows how to get a class instance variable from an effect and set it to an interface variable:</span></span>


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a><span data-ttu-id="f0dcc-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0dcc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0dcc-132"> (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="f0dcc-132">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 