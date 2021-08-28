---
description: 捕獲此檔案資料物件中的子係數目。
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: 'ID3DXFileData：： GetChildren 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dca2197a321efea6cf86ee0f38b1778935e5f4cb336b55b5d662e49a4465162a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493838"
---
# <a name="id3dxfiledatagetchildren-method"></a>ID3DXFileData：： GetChildren 方法

捕獲此檔案資料物件中的子係數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*puiChildren* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***

用來接收此檔案資料物件中子係數目之指標的位址。

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

 

 
