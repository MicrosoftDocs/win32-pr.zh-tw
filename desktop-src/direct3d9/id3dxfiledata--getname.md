---
description: 抓取這個檔案資料物件的名稱。
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'ID3DXFileData：： GetName 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992126"
---
# <a name="id3dxfiledatagetname-method"></a>ID3DXFileData：： GetName 方法

抓取這個檔案資料物件的名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>szname* \[在\]
</dt> <dd>

類型： **[ **LPSTR**](../winprog/windows-data-types.md)**

用來接收此檔案資料物件名稱的指標位址。 如果此參數為 **Null**，則 puiSize 會傳回字串的大小。 如果 >szname 指向有效的記憶體，則會將這個檔案資料物件的名稱複製到 >szname 上，直到 puiSize 指定的字元數。

</dd> <dt>

*puiSize* \[in、out\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***

字串大小的指標，代表這個檔案資料物件的名稱。 如果 >szname 提供名稱的參考，則這個參數可以是 **Null** 。 如果 >szname 為 **Null**，此參數將會傳回字串的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。

## <a name="remarks"></a>備註

若要讓這個方法成功，>szname 或 *puiSize* 必須為非 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
