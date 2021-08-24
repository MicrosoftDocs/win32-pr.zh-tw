---
description: 建立資料參考物件，並將其新增為子物件。 已取代。
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'IDirectXFileData：： AddDataReference 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 4c291e4f5754975f7e564c8c579b3651b29f0e6b684ad474f2f8436875dbf078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747258"
---
# <a name="idirectxfiledataadddatareference-method"></a>IDirectXFileData：： AddDataReference 方法

建立資料參考物件，並將其新增為子物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szRef* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

參考之資料物件名稱的指標。 如果 pguidRef 提供 GUID 的參考，則這個參數可以是 **Null** 。

</dd> <dt>

*pguidRef* \[在\]
</dt> <dd>

類型： **Const [**GUID**](guid.md) \***

代表資料之 GUID 的指標。 如果 szRef 提供名稱的參考，則這個參數可以是 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>備註

若要讓這個方法成功，szRef 或 pguidRef 參數都必須為非 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 
