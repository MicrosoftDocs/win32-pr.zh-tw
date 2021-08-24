---
description: 抓取這個檔案資料物件中的列舉物件。
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'ID3DXFileData：： GetEnum 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79ee6272f6b685c5e80b7c7b76b39925a08bb67cc07ba7af23a5b276b414f194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748548"
---
# <a name="id3dxfiledatagetenum-method"></a>ID3DXFileData：： GetEnum 方法

抓取這個檔案資料物件中的列舉物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppObj* \[在\]
</dt> <dd>

類型： **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

在此檔案資料物件中接收列舉物件之指標的位址。

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

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




