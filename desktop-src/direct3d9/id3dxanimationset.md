---
description: 這個介面會封裝動畫控制器所設定之動畫所需的最小功能。
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: 'ID3DXAnimationSet 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196441"
---
# <a name="id3dxanimationset-interface"></a>ID3DXAnimationSet 介面

這個介面會封裝動畫控制器所設定之動畫所需的最小功能。 Advanced users 可能會想要自行執行這個介面，以符合其特殊需求;不過，對於大多數的使用者而言，衍生的 [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) 和 [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) 介面應該已經足夠。

## <a name="members"></a>成員

**ID3DXAnimationSet** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXAnimationSet** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXAnimationSet** 介面具有這些方法。



| 方法                                                                        | 描述                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetAnimationIndexByName**](id3dxanimationset--getanimationindexbyname.md) | 取得動畫的索引，並指定其名稱。<br/>                        |
| [**GetAnimationNameByIndex**](id3dxanimationset--getanimationnamebyindex.md) | 取得動畫的名稱，指定其索引。<br/>                        |
| [**GetCallback**](id3dxanimationset--getcallback.md)                         | 取得動畫集中特定回呼的相關資訊。<br/>       |
| [**GetName**](id3dxanimationset--getname.md)                                 | 取得動畫集合的名稱。<br/>                                           |
| [**GetNumAnimations**](id3dxanimationset--getnumanimations.md)               | 取得動畫集中的動畫數目。<br/>                    |
| [**GetPeriod**](id3dxanimationset--getperiod.md)                             | 取得動畫集合的期間。<br/>                                  |
| [**GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)         | 傳回動畫集合的當地時間範圍內的時間位置。<br/>      |
| [**GetSRT**](id3dxanimationset--getsrt.md)                                   | 取得動畫集合的縮放、旋轉和轉譯值。<br/> |



 

## <a name="remarks"></a>備註

動畫組是由相同動畫的許多節點動畫所組成。

LPD3DXANIMATIONSET 型別定義為這個介面的指標。


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
