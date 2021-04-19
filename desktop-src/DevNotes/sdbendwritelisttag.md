---
description: 結束指定清單的寫入作業。
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: SdbEndWriteListTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971120"
---
# <a name="sdbendwritelisttag-function"></a>SdbEndWriteListTag 函式

結束指定清單的寫入作業。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[in、out\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> <dt>

*tiList* \[在\]
</dt> <dd>

清單的 [**TAGID**](tagid.md)

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="remarks"></a>備註

寫入所有清單專案之後，請呼叫此函式;它會標示清單的結尾。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
</dt> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




