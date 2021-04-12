---
title: 'EDB_RSTMAP 結構 (Ntdsbcli .h) '
description: 搭配 DsRestoreRegister 函式使用，將已備份的資料庫對應至新的資料庫。
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP 結構 Active Directory
- PEDB_RSTMAP 結構指標 Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025213"
---
# <a name="edb_rstmap-structure"></a>EDB \_ RSTMAP 結構

**EDB \_ RSTMAP** 結構會搭配 [**DsRestoreRegister**](dsrestoreregister.md)函數使用，以將備份的資料庫對應至新的資料庫。

## <a name="syntax"></a>語法


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a>成員

<dl> <dt>

**szDatabaseName**
</dt> <dd>

以 null 結束的字串指標，其中包含備份時資料庫的名稱。

</dd> <dt>

**szNewDatabaseName**
</dt> <dd>

以 null 結束的字串指標，其中包含資料庫的新名稱（如果適用的話），包括新的位置。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **EDB \_RSTMAPW** (Unicode) 和 **EDB \_ RSTMAPA** (ANSI) <br/>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[目錄備份結構](directory-backup-structures.md)
</dt> </dl>

 

 





