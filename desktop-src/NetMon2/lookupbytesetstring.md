---
description: LookupByteSetString 函式會傳回對應至已加上標籤集合之指定值的字串。
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: 'LookupByteSetString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970201"
---
# <a name="lookupbytesetstring-function"></a>LookupByteSetString 函式

**LookupByteSetString** 函式會傳回對應至已加上標籤集合之指定值的字串。

## <a name="syntax"></a>語法


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpSet* 
</dt> <dd>

標記集合的指標，您可以從中解壓縮值的標籤。

</dd> <dt>

*值* 
</dt> <dd>

已加上標籤之集合的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是對應于所提供之值的字串。

如果函式不成功，則傳回值為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




