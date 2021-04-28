---
description: ID3DXMATRIXStack 介面-應用程式會使用 ID3DXMATRIXStack 介面的方法來操作矩陣堆疊。
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: 'ID3DXMATRIXStack 介面 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62681c468fa7e78e6fd08c458798d98b467b992e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093316"
---
# <a name="id3dxmatrixstack-interface"></a>ID3DXMATRIXStack 介面

應用程式會使用 ID3DXMATRIXStack 介面的方法來操作矩陣堆疊。

## <a name="members"></a>成員

**ID3DXMATRIXStack** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXMATRIXStack** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXMATRIXStack** 介面具有這些方法。



| 方法                                                                       | 描述                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Vemap.gettop**](id3dxmatrixstack--gettop.md)                                   | 抓取堆疊頂端的目前矩陣。<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack--loadidentity.md)                       | 在目前的矩陣中載入識別。<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack--loadmatrix.md)                           | 將指定的矩陣載入至目前的矩陣。<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack--multmatrix.md)                           | 決定目前矩陣和指定矩陣的乘積。<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)                 | 決定給定矩陣和目前矩陣的乘積。<br/>                                                              |
| [**流行**](id3dxmatrixstack--pop.md)                                         | 從堆疊頂端移除目前的矩陣。<br/>                                                                           |
| [**推**](id3dxmatrixstack--push.md)                                       | 將矩陣加入至堆疊。<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack--rotateaxis.md)                           | 繞著任意軸的 (相對於全局座標空間) 旋轉。<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)                 | 在任意軸周圍) 旋轉 (相對於物件的區域座標空間。<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)           | 繞著任意軸的 (相對於全局座標空間) 旋轉。<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md) | 在任意軸周圍) 旋轉 (相對於物件的區域座標空間。<br/>                                             |
| [**調整**](id3dxmatrixstack--scale.md)                                     | 調整目前的矩陣與全球座標原點的大小。<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack--scalelocal.md)                           | 調整目前有關物件原點的矩陣。<br/>                                                                               |
| [**翻譯**](id3dxmatrixstack--translate.md)                             | 決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。<br/> |
| [**TranslateLocal**](id3dxmatrixstack--translatelocal.md)                   | 決定由給定因數決定的計算轉譯矩陣的乘積 (x、y 和 z) 和目前的矩陣。<br/> |



 

## <a name="remarks"></a>備註

**ID3DXMATRIXStack** 介面是藉由呼叫 [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md)函數來取得。

LPD3DXMATRIXSTACK 型別定義為 **ID3DXMATRIXStack** 介面的指標。


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
