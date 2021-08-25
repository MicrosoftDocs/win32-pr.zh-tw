---
description: 抓取這個 ID3DXFileSaveObject 檔資料節點的指標。
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'ID3DXFileSaveData：： GetSave 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 05b30c34f7e9d1383270c06ee70aca63d3f24b0f4f721d6859366794f2df361a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856638"
---
# <a name="id3dxfilesavedatagetsave-method"></a>ID3DXFileSaveData：： GetSave 方法

抓取這個 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 檔資料節點的指標。

## <a name="syntax"></a>語法


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppObj* \[擴展\]
</dt> <dd>

類型： **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

代表此檔案資料節點之 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 介面的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




