---
Description: 抓取指定之 TAGID 的 QWORD 值。
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: SdbReadQWORDTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4280c21983fa86312229930b7496625c594f0caac384f0dc6d130f673ce68509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815278"
---
# <a name="sdbreadqwordtag-function"></a>SdbReadQWORDTag 函式

抓取指定之 **TAGID** 的 **QWORD** 值。

## <a name="syntax"></a>語法


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[在\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> <dt>

*tiWhich* \[在\]
</dt> <dd>

對應至要抓取之資料的 **TAGID** 。

</dd> <dt>

*qwDefault* \[在\]
</dt> <dd>

失敗時要傳回的預設值。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會在失敗時傳回成功或 *qwDefault* 的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




