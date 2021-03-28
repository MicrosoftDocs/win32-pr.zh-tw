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
# <a name="interfaces-and-classes-in-effects"></a>作用中的介面和類別

有許多方法可以在效果11中使用類別和介面。 如需介面和類別語法，請參閱 [介面和類別](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class)。

下列各節將詳細說明如何指定類別實例至使用介面的著色器。 我們將在範例中使用下列介面和類別：


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



請注意，介面實例可以初始化為類別實例。 也支援類別和介面實例的陣列，並可將其初始化，如下列範例所示：


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a>統一介面參數

就像其他的統一資料類型一樣，必須在 CompileShader 呼叫中指定統一的介面參數。 介面參數可以指派給全域介面實例或全域類別實例。 當指派給全域介面實例時，著色器會相依于介面實例，這表示它必須設定為類別實例。 當指派給全域類別實例時，編譯器會特製化著色器 (與其他統一資料類型) 使用該類別。 這對兩個案例很重要：

1.  \_如果這些參數是統一的，且已指派給全域類別實例，則具有 4 x 目標的著色器可以使用介面參數 (因此) 不會使用動態連結。
2.  使用者可以決定有許多已編譯、特製化的著色器，不含動態連結或少數具有動態連結的已編譯著色器。


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



如果 pIColor2 透過 API 保持不變，則前兩個階段的功能相同，但第二個階段會使用 ps \_ 4 \_ 0 靜態著色器，而第二個會使用 \_ \_ 具有動態連結的 ps 5 0 著色器。 如果透過效果 API 變更 pIColor2 (請參閱) 下方設定類別實例，則第二個階段中圖元著色器的行為可能會變更。

## <a name="non-uniform-interface-parameters"></a>非統一介面參數

非統一介面參數會建立著色器的介面相依性。 使用介面參數套用著色器時，必須在中使用 BindInterfaces 呼叫來指派這些參數。 全域介面實例和全域類別實例可以在 BindInterfaces 呼叫中指定。


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



如果 pIColor2 透過 API 保持不變，則前兩個階段的功能相同，而且兩者都會使用動態連結。 如果透過效果 API 變更 pIColor2 (請參閱) 下方設定類別實例，則第二個階段中圖元著色器的行為可能會變更。

## <a name="setting-class-instances"></a>設定類別實例

當您將具有動態著色器連結的著色器設定為 Direct3D 11 裝置時，也必須指定類別實例。 使用 **Null** 類別實例來設定這類著色器是錯誤的。 因此，著色器參考的所有介面實例都必須有相關聯的類別實例。

下列範例示範如何從效果中取得類別執行個體變數，並將它設定為介面變數：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 