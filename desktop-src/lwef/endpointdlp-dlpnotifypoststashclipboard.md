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
ms.openlocfilehash: 97366a356b960fb8bea87bf552bf98576363663a6ca21de290d4035414fcb904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751657"
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