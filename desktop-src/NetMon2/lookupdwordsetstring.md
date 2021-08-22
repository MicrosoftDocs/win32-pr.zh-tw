---
description: LookupDwordSetString 函式會傳回對應至已加上標籤集合之指定值的字串。
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: 'LookupDwordSetString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b72f21d47001e2060c3b27daa80a584dcad77b55fd1df289a5bdb5476549cf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677228"
---
# <a name="lookupdwordsetstring-function"></a>LookupDwordSetString 函式

**LookupDwordSetString** 函式會傳回對應至已加上標籤集合之指定值的字串。

## <a name="syntax"></a>語法


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpSet* 
</dt> <dd>

標示為 [設定]，您可以從中解壓縮值的標籤。

</dd> <dt>

*值* 
</dt> <dd>

已加上標籤之集合的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是對應至指定值的字串。

如果函式不成功，則指定的值不在集合中，傳回值為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>剖析器 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




