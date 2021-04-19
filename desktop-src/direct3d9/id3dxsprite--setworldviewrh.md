---
description: 為 sprite 設定右手的世界視圖轉換。 在 billboarding 或排序 sprite 之前，需要呼叫此方法。
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: 'ID3DXSprite：： SetWorldViewRH 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7521f60f819829fc72ba907b57d4e4eb13682a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986525"
---
# <a name="id3dxspritesetworldviewrh-method"></a>ID3DXSprite：： SetWorldViewRH 方法

為 sprite 設定右手的世界視圖轉換。 在 billboarding 或排序 sprite 之前，需要呼叫此方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWorld* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

包含世界轉換之 [**D3DXMATRIX**](d3dxmatrix.md) 的指標。 如果是 **Null**，則會使用身分識別矩陣進行世界轉換。

</dd> <dt>

*pView* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

包含視圖轉換之 [**D3DXMATRIX**](d3dxmatrix.md) 的指標。 如果是 **Null**，則會使用標識矩陣進行視圖轉換。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

如果您要使用 [D3DXSprite \_ \_ 佈告欄](d3dxsprite.md)、D3DXSprite SORT depth [](id3dxsprite--setworldviewlh.md) \_ \_ \_ \_ FRONTTOBACK 或 D3DXSprite \_ \_ \_ \_ [**：： Begin**](id3dxsprite--begin.md)中的 BACKTOFRONT SORT Depth ID3DXSprite 旗標值來呈現 sprite，則需要呼叫此方法 (或 ID3DXSprite：： SetWorldViewLH) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




