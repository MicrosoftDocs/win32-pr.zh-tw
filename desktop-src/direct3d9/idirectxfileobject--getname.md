---
description: 捕獲 DirectX 檔案物件名稱的指標。 已取代。
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'IDirectXFileObject：： GetName 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106979873"
---
# <a name="idirectxfileobjectgetname-method"></a>IDirectXFileObject：： GetName 方法

捕獲 DirectX 檔案物件名稱的指標。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pstrNameBuf* \[擴展\]
</dt> <dd>

類型： **[ **LPSTR**](../winprog/windows-data-types.md)**

緩衝區的指標，其中將複製 DirectX 檔案物件的名稱。 如果只需要緩衝區長度，則設定為 **Null** 。

</dd> <dt>

*pdwBufLen* \[in、out\]
</dt> <dd>

類型： **[ **LPDWORD**](../winprog/windows-data-types.md)**

DWORD 的指標，指定 pstrNameBuf 所指向的緩衝區長度。 即使 pstrNameBuf 為 **Null**，pdwBufLen 參數值仍會修改為保留物件名稱所需的緩衝區長度。 無論是哪一種情況， \_ 如果 pdwBufLen 的原始值不等於或大於保留物件名稱所需的長度，函數都會傳回 DXFILEERR BADVALUE。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 
