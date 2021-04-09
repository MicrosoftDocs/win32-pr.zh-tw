---
description: 未執行且無法使用。
ms.assetid: b41ba894-5cee-458d-935f-e89363925968
title: 'SslChangeNotify 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslChangeNotify
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 5539ef2529a4f3af86d34ae0e9d44cd31a8f4289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115177"
---
# <a name="sslchangenotify-function"></a>SslChangeNotify 函式

**SslChangeNotify** 函式不會執行，而且無法使用。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslChangeNotify(
  _In_ HANDLE hEvent,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hEvent* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **\_ 不 \_ 支援的上限**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




