---
Description: 抓取指定之 TAGID 的二進位資料。
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: SdbReadBinaryTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 92d63182273c96707bb155071164a6b6838378615f603d8ef6d332d6c65be460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911568"
---
# <a name="sdbreadbinarytag-function"></a>SdbReadBinaryTag 函式

抓取指定之 **TAGID** 的二進位資料。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
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

*pBuffer* \[擴展\]
</dt> <dd>

接收二進位資料的緩衝區。 此參數不可以是 **Null**。

</dd> <dt>

*dwBufferSize* \[在\]
</dt> <dd>

*PBuffer* 緩衝區的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

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

 

 




