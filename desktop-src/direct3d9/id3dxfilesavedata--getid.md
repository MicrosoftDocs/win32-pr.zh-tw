---
description: 抓取這個 ID3DXFileSaveData 檔資料節點的 GUID。
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'ID3DXFileSaveData：： GetId 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e6f502357510cc1c8fc51e9ada844a988a79b1571435639586380929b121c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748498"
---
# <a name="id3dxfilesavedatagetid-method"></a>ID3DXFileSaveData：： GetId 方法

抓取這個 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 檔資料節點的 GUID。

## <a name="syntax"></a>語法


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pId* \[擴展\]
</dt> <dd>

類型： **LPGUID**

用來接收此檔案資料節點識別碼之 GUID 的指標。 如果物件沒有識別碼，傳回的參數值將會是 GUID \_ Null。

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

 

 




