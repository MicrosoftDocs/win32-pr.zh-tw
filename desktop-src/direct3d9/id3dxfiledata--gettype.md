---
description: 抓取此檔案資料物件中的範本識別碼。
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'ID3DXFileData：： GetType 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e386c27638ced2be41197bf5f0095a481365dd19bc39b69d5d13d1ac8ec8dc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748528"
---
# <a name="id3dxfiledatagettype-method"></a>ID3DXFileData：： GetType 方法

抓取此檔案資料物件中的範本識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pType* \[在\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \***

GUID 的指標，代表這個檔案資料物件中的範本。

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

 

 




