---
description: 提供隱藏專案剪貼簿作業完成後的系統狀態資訊。
title: 'DlpNotifyPostStashClipboard 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495474"
---
# <a name="dlpnotifypoststashclipboard-function"></a>DlpNotifyPostStashClipboard 函式

提供隱藏專案剪貼簿作業完成後的系統狀態資訊。

## <a name="syntax"></a>語法


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>參數


<dl> <dt>

*OpStatus* \[在\]
</dt> <dd>

[DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md)結構的指標，其中包含隱藏專案剪貼簿作業的相關狀態資訊。

</dd> </dl>


## <a name="return-value"></a>傳回值

傳回 void。

## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |