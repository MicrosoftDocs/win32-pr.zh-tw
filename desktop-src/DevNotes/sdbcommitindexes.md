---
description: 將新建立的索引認可至指定的資料庫。
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: SdbCommitIndexes 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110281"
---
# <a name="sdbcommitindexes-function"></a>SdbCommitIndexes 函式

將新建立的索引認可至指定的資料庫。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[in、out\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbDeclareIndex**](sdbdeclareindex.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




