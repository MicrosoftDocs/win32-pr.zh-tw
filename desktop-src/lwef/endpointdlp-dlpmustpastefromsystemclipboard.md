---
description: 判斷應用程式是否必須從系統剪貼簿提取資料，而不是從其內部快取中取得資料。
title: 'DlpMustPasteFromSystemClipboard 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e111cb85c6eada6f84f7bc10eb240e89447a173e741b26b316b232d742f8de48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888578"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>DlpMustPasteFromSystemClipboard 函式

判斷應用程式是否必須從系統剪貼簿提取資料，而不是從其內部快取中取得資料。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>傳回值

如果呼叫 OS 剪貼簿為必要，則為 TRUE。否則為 FALSE。

## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |