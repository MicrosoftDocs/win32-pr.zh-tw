---
description: 搜尋指定父系內的下一個子標記，並傳回下一個子系的 TAGID。
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 210e0aab8cb5e43bfc649e8abb72cf565c4d4f892f651708286f7a3f87d11ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045306"
---
# <a name="sdbgetnextchild-function"></a>SdbGetNextChild 函式

搜尋指定父系內的下一個子標記，並傳回下一個子系的 **TAGID** 。

## <a name="syntax"></a>語法


```C++
TAGID WINAPI SdbGetNextChild(
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

上一個子系的 **TAGID** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果找不到子系，則為子系的 **TAGID** 或 **TAGID \_ Null** 。

## <a name="remarks"></a>備註

呼叫此函式之前，請先呼叫 [**SdbGetFirstChild**](sdbgetfirstchild.md) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




