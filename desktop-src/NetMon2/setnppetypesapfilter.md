---
description: 設定 BLOB Etype/Sap 篩選器。
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: 'SetNPPEtypeSapFilter 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 30b2f6ffbefad955034f520162b6fdc44d80198d926f35443ce21fefd80ef5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363824"
---
# <a name="setnppetypesapfilter-function"></a>SetNPPEtypeSapFilter 函式

**SetNPPEtypeSapFilter** 函數會設定 BLOB Etype/Sap 篩選器。

## <a name="syntax"></a>語法


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

BLOB 的控制碼。

</dd> <dt>

*nSaps* \[在\]
</dt> <dd>

Sap 的數目。

</dd> <dt>

*nEtypes* \[在\]
</dt> <dd>

要設定之 Etype 資料表中的 Etypes 數目。

</dd> <dt>

*lpSapTable* \[在\]
</dt> <dd>

已設定的 SAP 資料表指標。

</dd> <dt>

*lpEtypeTable* \[在\]
</dt> <dd>

已設定之 Etype 資料表的指標。

</dd> <dt>

*FilterFlags* \[在\]
</dt> <dd>

已設定的篩選旗標。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，指定當發生任何) 時，原始 BLOB 中的錯誤 (。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[GetNPPEtypeSapFilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




