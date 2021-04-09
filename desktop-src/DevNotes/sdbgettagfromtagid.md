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
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110649"
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
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**標記**](tag.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




