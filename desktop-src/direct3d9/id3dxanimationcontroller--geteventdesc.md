---
description: 取得指定動畫事件的描述。
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'ID3DXAnimationController：： GetEventDesc 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc113788a8eb6b64accfcba8c58dd3a3512e17601ec02ce5dd33349628c69212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987938"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a>ID3DXAnimationController：： GetEventDesc 方法

取得指定動畫事件的描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hEvent* \[在\]
</dt> <dd>

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

要描述的動畫事件的事件控制碼。

</dd> <dt>

*pDesc* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**

[**D3DXEVENT \_ DESC**](d3dxevent-desc.md)結構的指標，其中包含動畫事件的描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




