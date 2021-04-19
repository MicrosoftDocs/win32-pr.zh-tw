---
description: ID3DXBuffer 介面是用來做為資料緩衝區，在網格優化和載入作業期間儲存頂點、相鄰和材質資訊。
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: 'ID3DXBuffer 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975681"
---
# <a name="id3dxbuffer-interface"></a>ID3DXBuffer 介面

ID3DXBuffer 介面是用來做為資料緩衝區，在網格優化和載入作業期間儲存頂點、相鄰和材質資訊。 緩衝區物件是用來傳回任意長度的資料。 此外，也會使用緩衝區物件，在組合頂點和圖元著色器的方法中傳回物件程式碼和錯誤訊息。

## <a name="members"></a>成員

**ID3DXBuffer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXBuffer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXBuffer** 介面具有這些方法。



| 方法                                                    | 描述                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**GetBufferPointer**](id3dxbuffer--getbufferpointer.md) | 擷取緩衝區中資料的指標。<br/>      |
| [**GetBufferSize**](id3dxbuffer--getbuffersize.md)       | 抓取緩衝區中資料的總大小。<br/> |



 

## <a name="remarks"></a>備註

**ID3DXBuffer** 介面是藉由呼叫 [**D3DXCreateBuffer**](d3dxcreatebuffer.md)函數來取得。

LPD3DXBUFFER 型別定義為 **ID3DXBuffer** 介面的指標。


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
