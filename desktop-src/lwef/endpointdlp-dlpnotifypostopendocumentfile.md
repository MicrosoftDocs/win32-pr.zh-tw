---
description: 在開啟作業完成後，為系統提供檔檔案的相關資訊。
title: 'DlpNotifyPostOpenDocumentFile 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2957b09282fe64e41805f09a1761ca75aa3551ca70e9d4aa5b52517374fd9ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976598"
---
# <a name="dlpnotifypostopendocumentfile-function"></a>DlpNotifyPostOpenDocumentFile 函式

在開啟作業完成後，為系統提供檔檔案的相關資訊。

## <a name="syntax"></a>語法


```C++
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus 
```

## <a name="parameters"></a>參數

<dl> <dt>

*DocumentInfo* \[在\]
</dt> <dd>

[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含已開啟檔的相關資訊。

</dd> </dl>

<dl> <dt>

*OpStatus* \[在\]
</dt> <dd>

[DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md)結構的指標，其中包含有關開啟檔作業的狀態資訊。

</dd> </dl>


## <a name="return-value"></a>傳回值

傳回 void。

## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |