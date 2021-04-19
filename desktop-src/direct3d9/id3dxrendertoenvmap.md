---
description: ID3DXRenderToEnvMap 介面可用來將轉譯的程式一般化至環境對應。
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: 'ID3DXRenderToEnvMap 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000627"
---
# <a name="id3dxrendertoenvmap-interface"></a>ID3DXRenderToEnvMap 介面

ID3DXRenderToEnvMap 介面可用來將轉譯的程式一般化至環境對應。

## <a name="members"></a>成員

**ID3DXRenderToEnvMap** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXRenderToEnvMap** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXRenderToEnvMap** 介面具有這些方法。



| 方法                                                          | 描述                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginCube**](id3dxrendertoenvmap--begincube.md)             | 起始三次環境對應的呈現。<br/>                                                                                                                                    |
| [**BeginHemisphere**](id3dxrendertoenvmap--beginhemisphere.md) | 起始 hemispheric 環境對應的呈現。<br/>                                                                                                                              |
| [**BeginParabolic**](id3dxrendertoenvmap--beginparabolic.md)   | 起始拋物線環境對應的呈現。<br/>                                                                                                                                |
| [**BeginSphere**](id3dxrendertoenvmap--beginsphere.md)         | 起始球形環境對應的呈現。<br/>                                                                                                                                |
| [**結束**](id3dxrendertoenvmap--end.md)                         | 還原所有呈現目標，並視需要將所有呈現的臉部組成環境地圖介面。<br/>                                                                           |
| [**臉部**](id3dxrendertoenvmap--face.md)                       | 起始每個環境圖臉部的繪圖。<br/>                                                                                                                              |
| [**GetDesc**](id3dxrendertoenvmap--getdesc.md)                 | 抓取呈現介面的描述。<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertoenvmap--getdevice.md)             | 捕獲與環境對應相關聯的 Direct3D 裝置。<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertoenvmap--onlostdevice.md)       | 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。<br/> |
| [**OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)     | 您可以使用這個方法來重新取得資源，並儲存初始狀態。<br/>                                                                                                                       |



 

## <a name="remarks"></a>備註

環境對應可用來紋理對應場景幾何，以提供更精密的場景，而不使用複雜的幾何。 此介面支援針對下列種類的幾何建立介面： cube、半球體或 hemispheric、拋物線或球體。

**ID3DXRenderToEnvMap** 介面是藉由呼叫 [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md)函數來取得。

LPD3DXRenderToEnvMap 型別定義為 **ID3DXRenderToEnvMap** 介面的指標。


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
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

 

 
