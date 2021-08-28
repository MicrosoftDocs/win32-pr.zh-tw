---
description: 針對指定的 TAGREF，抓取 TAGID 和填充碼資料庫的控制碼。
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: SdbTagRefToTagID 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: feeb622fd196ed20efb60d866d59b634fdcd9ecd955a97a1d7af0aef1347c8f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815317"
---
# <a name="sdbtagreftotagid-function"></a>SdbTagRefToTagID 函式

針對指定的 [**TAGREF**](tagref.md)，抓取 **TAGID** 和填充碼資料庫的控制碼。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSDB* \[在\]
</dt> <dd>

[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。

</dd> <dt>

*trWhich* \[在\]
</dt> <dd>

[**TAGREF**](tagref.md)。

</dd> <dt>

*ppdb* \[擴展\]
</dt> <dd>

填充碼資料庫產生的控制碼。

</dd> <dt>

*ptiWhich* \[擴展\]
</dt> <dd>

產生的 **TAGID**。

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

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




