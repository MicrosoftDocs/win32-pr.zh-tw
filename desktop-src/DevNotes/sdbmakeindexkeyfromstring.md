---
description: 從字串建立索引鍵。
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: SdbMakeIndexKeyFromString 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936027"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>SdbMakeIndexKeyFromString 函式

從字串建立索引鍵。

## <a name="syntax"></a>語法


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszKey* \[在\]
</dt> <dd>

字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，函式會傳回索引鍵或0。

## <a name="remarks"></a>備註

標準索引鍵是字串的前八個字元，轉換成大寫，然後轉換成 **ULONGLONG** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




