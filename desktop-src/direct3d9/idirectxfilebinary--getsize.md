---
description: 捕獲二進位資料的大小。 已取代。
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'IDirectXFileBinary：： GetSize 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514661"
---
# <a name="idirectxfilebinarygetsize-method"></a>IDirectXFileBinary：： GetSize 方法

捕獲二進位資料的大小。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcbSize* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

傳回之二進位資料大小的指標（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
