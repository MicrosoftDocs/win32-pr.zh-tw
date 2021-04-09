---
description: 抓取多用途網際網路郵件延伸 (MIME) 類型的二進位資料。 已取代。
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'IDirectXFileBinary：： GetMimeType 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946084"
---
# <a name="idirectxfilebinarygetmimetype-method"></a>IDirectXFileBinary：： GetMimeType 方法

抓取多用途網際網路郵件延伸 (MIME) 類型的二進位資料。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszMimeType* \[擴展\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)\***

要接收 MIME 類型字串之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。

## <a name="remarks"></a>備註

當二進位物件的 DirectX 檔案中未指定 MIME 類型時，此函式會將 pszMimeType 設定為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
