---
title: 複製效果
description: 複製效果會建立第二個與效果幾乎相同的複本。
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674003"
---
# <a name="cloning-an-effect"></a>複製效果

複製效果會建立第二個與效果幾乎相同的複本。 請參閱下列單一辨識符號，以取得為何不精確的說明。 當您想要在多個執行緒上使用效果架構時，效果的第二個複本會很有用，因為效果執行時間不會以安全線程的速度維持高效能。

由於裝置內容也是非安全線程，因此不同的執行緒應該將不同的裝置內容傳遞至 ID3DX11EffectPass：： Apply 方法。

您可以使用下列語法來複製效果：


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



在上述範例中，複製的複本將會封裝與原始效果相同的狀態，而不論原始效果的狀態為何。 尤其是：

1.  如果 pEffect 已優化，pCloned 效果就會優化
2.  如果 pEffect 有一些使用者管理的變數，pCloned 效果將會有相同的使用者管理變數 (請參閱下面的單一描述) 
3.  任何暫止的變數更新都會 (，直到 pEffect 中的 [套用呼叫更新裝置狀態]) 暫止于 pClonedEffect

下列 Direct3D 11 裝置物件是不可變的，或永遠不會被效果架構更新，因此複製的效果會指向與原始效果相同的物件：

1.  狀態欄塊物件 (ID3D11BlendState、ID3D11RasterizerState、ID3D11DepthStencilState、ID3D11SamplerState) 
2.  著色器
3.  類別實例
4.  材質 (不包括材質緩衝區) 
5.  未排序的存取權視圖

下列 Direct3D 11 裝置物件都是不可變的，且效果執行時間 (修改，除非在複製的效果中有使用者管理或單一的) ;當非單一時，會建立這些物件的新複本：

1.  常數緩衝區
2.  材質緩衝區

## <a name="single-constant-buffers-and-texture-buffers"></a>單一常數緩衝區和材質緩衝區

請注意，這項討論適用于常數緩衝區和紋理，但會假設常數緩衝區以方便閱讀。

在某些情況下，常數緩衝區只會由一個執行緒更新，但複製的效果所設定的裝置狀態將會使用此資料。 例如，主要效果可能會更新世界和視野矩陣，這些矩陣是在複製效果中從著色器參考，而不會變更世界和視野矩陣。 在這些情況下，複製的效果必須參考目前的常數緩衝區，而不是重新建立它。

有兩種方式可以達成此預期的結果：

1.  在複製的效果上使用 ID3DX11EffectConstantBuffer：： SetConstantBuffer，使其成為使用者管理的
2.  在 HLSL 程式碼中將常數緩衝區標示為「單一」，強制在複製之後，將作用中的執行時間視為使用者管理的

上述兩個方法之間有兩種差異。 首先，在方法1中，會先建立新的 ID3D11Buffer，然後再呼叫 SetConstantBuffer。 此外，在複製的效果中呼叫 UndoSetConstantBuffer 之後，方法1will 中的變數會指向新建立的緩衝區 (將會在套用) 時更新效果，而方法2中的變數將繼續指向原始緩衝區 (不會在套用) 時更新它。

請參閱 HLSL 中的下列範例：


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



在複製時，複製的效果會為 ObjectData 建立新的 ID3D11Buffer，並在套用時填入其內容，但參考 ViewData 的原始 ID3D11Buffer。 您可以藉由設定 D3DX11 \_ 效果 \_ 複製 \_ 強制 \_ NONSINGLE 旗標，在複製進程中忽略單一限定詞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




