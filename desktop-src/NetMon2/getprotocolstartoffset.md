---
description: 傳回框架中指定之通訊協定的位移。
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: 'GetProtocolStartOffset 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973217"
---
# <a name="getprotocolstartoffset-function"></a>GetProtocolStartOffset 函式

**GetProtocolStartOffset** 函式會傳回框架中指定之通訊協定的位移。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* 
</dt> <dd>

框架的控制碼。

</dd> <dt>

*ProtocolName* 
</dt> <dd>

通訊協定名稱，例如 TCP。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是要搜尋的通訊協定開頭的 **DWORD** 位移，表示通訊協定是框架中的第一個通訊協定。

如果函式不成功，則此通訊協定不在框架中，傳回值為-1。

## <a name="remarks"></a>備註

當提供框架的控制碼時，此函式會傳回框架中指定之通訊協定的位移。 例如，若要判斷框架是否為 DNS 框架，DNS 剖析器需要 TCP 通訊協定的埠位址。 DNS 剖析器會以 TCP 作為 *ProtocolName* 值來呼叫此函數。 如果 TCP 通訊協定可以辨識框架，則會傳回從框架開頭到 TCP 框架開頭的 **單字** 位移。 如果沒有 TCP 通訊協定，則傳回值為零。

此函數會尋找框架中的通訊協定開頭。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




