---
description: 在指定的父系內搜尋下一個標記相符，並傳回相符的 TAGID。
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: SdbFindNextTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847178"
---
# <a name="sdbfindnexttag-function"></a>SdbFindNextTag 函式

在指定的父系內搜尋下一個標記相符，並傳回相符的 **TAGID** 。

## <a name="syntax"></a>語法


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
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

*tiPrev* \[在\]
</dt> <dd>

上一個相符項的 **TAGID** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

相符的 **TAGID** 。

## <a name="remarks"></a>備註

呼叫此函式之前，請先呼叫 [**SdbFindFirstTag**](sdbfindfirsttag.md) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




