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
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495521"
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