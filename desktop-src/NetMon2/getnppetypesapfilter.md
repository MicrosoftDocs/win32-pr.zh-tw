---
description: GetNPPEtypeSapFilter 函式會從指定的 BLOB 抓取 Etype/Sap 篩選器。
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: 'GetNPPEtypeSapFilter 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982115"
---
# <a name="getnppetypesapfilter-function"></a>GetNPPEtypeSapFilter 函式

**GetNPPEtypeSapFilter** 函式會從指定的 BLOB 抓取 Etype/Sap 篩選器。

## <a name="syntax"></a>語法


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

BLOB 的控制碼。

</dd> <dt>

*pnSaps* \[擴展\]
</dt> <dd>

SAP 資料表中傳回的通訊協定數目指標。

</dd> <dt>

*pnEtypes* \[擴展\]
</dt> <dd>

在 Etype 資料表中傳回之 Etypes 數目的指標。

</dd> <dt>

*ppSapTable* \[擴展\]
</dt> <dd>

傳回的 SAP 資料表指標。

</dd> <dt>

*ppEtypeTable* \[擴展\]
</dt> <dd>

傳回之 Etype 資料表的指標。

</dd> <dt>

*pFilterFlags* \[擴展\]
</dt> <dd>

傳回之篩選旗標的指標。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，指定發生錯誤時，發生錯誤)  (原始 BLOB 中的位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="remarks"></a>備註

Etype/Sap 資訊會儲存在 NPP **Owner** 區段的 **Config** 類別中。

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

[SetNPPEtypeSapFilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




