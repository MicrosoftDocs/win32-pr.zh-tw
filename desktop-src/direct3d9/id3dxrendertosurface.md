---
description: ID3DXRenderToSurface 介面可用來將轉譯的程式一般化至表面。
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: 'ID3DXRenderToSurface 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323307"
---
# <a name="id3dxrendertosurface-interface"></a>ID3DXRenderToSurface 介面

ID3DXRenderToSurface 介面可用來將轉譯的程式一般化至表面。

## <a name="members"></a>成員

**ID3DXRenderToSurface** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXRenderToSurface** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXRenderToSurface** 介面具有這些方法。



| 方法                                                       | 描述                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginScene**](id3dxrendertosurface--beginscene.md)       | 開始場景。<br/>                                                                                                                                                                      |
| [**EndScene**](id3dxrendertosurface--endscene.md)           | 結束場景。<br/>                                                                                                                                                                        |
| [**GetDesc**](id3dxrendertosurface--getdesc.md)             | 捕獲呈現介面的參數。<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | 抓取與呈現介面相關聯的 Direct3D 裝置。<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertosurface--onlostdevice.md)   | 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。<br/> |
| [**OnResetDevice**](id3dxrendertosurface--onresetdevice.md) | 您可以使用這個方法來重新取得資源，並儲存初始狀態。<br/>                                                                                                                      |



 

## <a name="remarks"></a>備註

您可以使用各種方式來使用介面，包括轉譯目標、螢幕轉譯或轉譯成紋理。

您可以使用 [**ID3DXRenderToSurface：： BeginScene**](id3dxrendertosurface--beginscene.md) 方法，透過不同的區隔圖來設定介面，以提供自訂呈現視圖。 如果介面不是轉譯目標，則會使用相容的呈現目標，並將結果複製到場景結尾的介面。

**ID3DXRenderToSurface** 介面是藉由呼叫 [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md)函數來取得。

LPD3DXRENDERTOSURFACE 型別定義為 **ID3DXRenderToSurface** 介面的指標。


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
