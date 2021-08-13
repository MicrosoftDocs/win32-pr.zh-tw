---
description: 在指定的資料庫中宣告新的索引。
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: b428699641d5a18bad8a1869f59ab1bb5402e7b667526070c3dc0575e435fc38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666587"
---
# <a name="sdbdeclareindex-function"></a>SdbDeclareIndex 函式

在指定的資料庫中宣告新的索引。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[在\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> <dt>

*tWhich* \[在\]
</dt> <dd>

此參數必須是 **標記 \_ 類型 \_ 清單**。

</dd> <dt>

*tKey* \[在\]
</dt> <dd>

指定要做為索引鍵之類型的標記。 此參數不可以是 **標記 \_ 類型 \_ 清單**。

</dd> <dt>

*dwEntries* \[在\]
</dt> <dd>

要在索引中配置的專案數目。

</dd> <dt>

*bUniqueKey* \[在\]
</dt> <dd>

如果此參數為 **TRUE**，則索引是唯一索引鍵索引。

</dd> <dt>

*piiIndex* \[擴展\]
</dt> <dd>

新宣告索引的結果 **INDEXID** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="remarks"></a>備註

將標記寫入新的索引之前，請先呼叫此函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INDEXID**](indexid.md)
</dt> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




