---
description: ID3DXFileEnumObject：： System.windows.media.visualtreehelper.getchild 方法-抓取這個檔案資料物件中的子物件。
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'ID3DXFileEnumObject：： System.windows.media.visualtreehelper.getchild 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090356"
---
# <a name="id3dxfileenumobjectgetchild-method"></a>ID3DXFileEnumObject：： System.windows.media.visualtreehelper.getchild 方法

抓取這個檔案資料物件中的子物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

要取出之子物件的識別碼。

</dd> <dt>

*ppObj* \[擴展\]
</dt> <dd>

類型： **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

用來接收子物件介面指標之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE，D3DXFERR \_ NOMOREOBJECTS。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
