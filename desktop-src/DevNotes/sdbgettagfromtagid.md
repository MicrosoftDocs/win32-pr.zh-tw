---
description: 抓取與指定 TAGID 相關聯的標記。
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: SdbGetTagFromTagID 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a7e58343cf9a863f6b3cecc7f9b6414414387e2f2b33859de1eb015d65f1a78b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058468"
---
# <a name="sdbgettagfromtagid-function"></a>SdbGetTagFromTagID 函式

抓取與指定 **TAGID** 相關聯的標記。

## <a name="syntax"></a>語法


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
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

標記的 **TAGID** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回標記。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**標記**](tag.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




