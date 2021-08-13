---
description: 在指定的父系內搜尋標記相符，並傳回第一個相符項的 TAGID。
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: SdbFindFirstTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f6562589158e5c3a5e1b65273451f812802c1c73b76f52c47274c06b9639f5ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390228"
---
# <a name="sdbfindfirsttag-function"></a>SdbFindFirstTag 函式

在指定的父系內搜尋標記相符，並傳回第一個相符項的 **TAGID** 。

## <a name="syntax"></a>語法


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[在\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> <dt>

*tiParent* \[在\]
</dt> <dd>

搜尋的 **TAGID** 開始。 此參數可以是 **TAGID \_ 根** 或 **標記 \_ 類型 \_ 清單**。

</dd> <dt>

*tTag* \[在\]
</dt> <dd>

要比對的標記。 如需可能值的清單，請參閱 [標記](tag.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

第一個相符項的 **TAGID** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




