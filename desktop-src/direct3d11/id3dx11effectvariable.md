---
title: 'ID3DX11EffectVariable 介面 (D3dx11effect .h) '
description: ID3DX11EffectVariable 介面是所有效果變數的基類。ID3DX11EffectVariable 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- ID3DX11EffectVariable 介面 Direct3D 11
- ID3DX11EffectVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696743"
---
# <a name="id3dx11effectvariable-interface"></a>ID3DX11EffectVariable 介面

**ID3DX11EffectVariable** 介面是所有效果變數的基類。

**ID3DX11EffectVariable** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11EffectVariable** 介面具有這些方法。



| 方法                                                                           | 描述                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**AsBlend**](id3dx11effectvariable-asblend.md)                                 | 取得效果 blend 變數。<br/>                |
| [**AsClassInstance**](id3dx11effectvariable-asclassinstance.md)                 | 取得類別執行個體變數。<br/>              |
| [**AsConstantBuffer**](id3dx11effectvariable-asconstantbuffer.md)               | 取得常數緩衝區。<br/>                      |
| [**AsDepthStencil**](id3dx11effectvariable-asdepthstencil.md)                   | 取得深度樣板變數。<br/>               |
| [**AsDepthStencilView**](id3dx11effectvariable-asdepthstencilview.md)           | 取得深度樣板視圖變數。<br/>          |
| [**AsInterface**](id3dx11effectvariable-asinterface.md)                         | 取得介面變數。<br/>                  |
| [**AsMatrix**](id3dx11effectvariable-asmatrix.md)                               | 取得矩陣變數。<br/>                      |
| [**AsRasterizer**](id3dx11effectvariable-asrasterizer.md)                       | 取得轉譯器變數。<br/>                  |
| [**AsRenderTargetView**](id3dx11effectvariable-asrendertargetview.md)           | 取得呈現目標視圖變數。<br/>          |
| [**AsSampler**](id3dx11effectvariable-assampler.md)                             | 取得取樣器變數。<br/>                     |
| [**AsScalar**](id3dx11effectvariable-asscalar.md)                               | 取得純量變數。<br/>                      |
| [**AsShader**](id3dx11effectvariable-asshader.md)                               | 取得著色器變數。<br/>                      |
| [**AsShaderResource**](id3dx11effectvariable-asshaderresource.md)               | 取得著色器的資源變數。<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | 取得字串變數。<br/>                      |
| [**AsUnorderedAccessView**](id3dx11effectvariable-asunorderedaccessview.md)     | 取得未排序的存取視圖變數。<br/>      |
| [**AsVector**](id3dx11effectvariable-asvector.md)                               | 取得向量變數。<br/>                      |
| [**GetAnnotationByIndex**](id3dx11effectvariable-getannotationbyindex.md)       | 依索引取得批註。<br/>                 |
| [**GetAnnotationByName**](id3dx11effectvariable-getannotationbyname.md)         | 依名稱取得批註。<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | 取得描述。<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | 取得陣列元素。<br/>                       |
| [**GetMemberByIndex**](id3dx11effectvariable-getmemberbyindex.md)               | 依索引取得結構成員。<br/>            |
| [**GetMemberByName**](id3dx11effectvariable-getmemberbyname.md)                 | 依名稱取得結構成員。<br/>             |
| [**GetMemberBySemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | 依語義取得結構成員。<br/>         |
| [**GetParentConstantBuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | 取得常數緩衝區。<br/>                      |
| [**GetRawValue**](id3dx11effectvariable-getrawvalue.md)                         | 取得資料。<br/>                                   |
| [**GetType**](id3dx11effectvariable-gettype.md)                                 | 取得型別資訊。<br/>                       |
| [**IsValid**](id3dx11effectvariable-isvalid.md)                                 | 比較資料類型與儲存的資料。<br/> |
| [**SetRawValue**](id3dx11effectvariable-setrawvalue.md)                         | 設定資料。<br/>                                   |



 

## <a name="remarks"></a>備註

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果11介面](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





