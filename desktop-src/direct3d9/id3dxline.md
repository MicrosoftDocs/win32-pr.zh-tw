---
description: ID3DXLine 介面會使用紋理三角形來實行繪圖。
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: 'ID3DXLine 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9677ca802a800624b374212c6942ab6676423f8d63e62cbf136a8b9e69c533d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951368"
---
# <a name="id3dxline-interface"></a>ID3DXLine 介面

ID3DXLine 介面會使用紋理三角形來實行繪圖。

## <a name="members"></a>成員

**ID3DXLine** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXLine** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXLine** 介面具有這些方法。



| 方法                                                | 描述                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**開始**](id3dxline--begin.md)                     | 準備裝置來繪製線條。<br/>                                                                                                                                                  |
| [**Draw**](id3dxline--draw.md)                       | 在螢幕空間中繪製帶狀線。 輸入的格式為數組，可定義 [**D3DXVECTOR2**](d3dxvector2.md)) 在行條紋 (的點。<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | 使用指定的輸入轉換矩陣，在螢幕空間中繪製行帶狀。<br/>                                                                                                      |
| [**結束**](id3dxline--end.md)                         | 將裝置狀態還原為呼叫 [**ID3DXLine：： Begin**](id3dxline--begin.md) 時的狀態。<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | 取得線條消除鋸齒狀態。<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | 抓取與 line 物件相關聯的 Direct3D 裝置。<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | 取得 OpenGL 樣式的線條繪圖模式。<br/>                                                                                                                                              |
| [**System.windows.automation.peers.uielementautomationpeer.getpattern**](id3dxline--getpattern.md)           | 取得行 stipple 模式。<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | 取得 stipple 模式比例值。<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | 取得線條的粗細。<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | 您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。 只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | 您可以使用這個方法來重新取得資源，並儲存初始狀態。<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | 切換線條消除鋸齒。<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | 切換模式以繪製 OpenGL 樣式的線條。<br/>                                                                                                                                          |
| [**SetPattern**](id3dxline--setpattern.md)           | 將 stipple 模式套用至線條。<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | 沿著線條方向伸展 stipple 模式。<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | 指定線條的粗細。<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>備註

使用 [**D3DXCreateLine**](d3dxcreateline.md)建立線條繪圖物件。

LPD3DXLINE 型別定義為 **ID3DXLine** 介面的指標。


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
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

 

 
