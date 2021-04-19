---
description: 此 API 僅供內部使用，不應在您的程式碼中使用。
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: 'ApiSetQueryApiSetPresence 函式 (Apiquery) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000495"
---
# <a name="apisetqueryapisetpresence-function"></a>ApiSetQueryApiSetPresence 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

此 API 僅供內部使用，不應在您的程式碼中使用。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*命名空間* \[在\]
</dt> <dd></dd> <dt>

*存在* \[擴展\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                                                                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                                                                                                                  |
| 標頭<br/>                   | <dl> <dt>Apiquery。h</dt> </dl>                                                                                                                 |
| 程式庫<br/>                  | <dl> <dt>Api-ms-win-core-apiquery-l1 .lib;</dt><dt>Api-ms-apiquery-l1-1 4.9.0-.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt> </dl>                                                                                        |



 

 




