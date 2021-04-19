---
description: 在 [另存新檔] 作業完成後，為系統提供檔的相關資訊。
title: 'DlpNotifyPostSaveAsDocument 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 564e7173cbfe72a020f1c7e12a60ceda25fd845c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495478"
---
# <a name="dlpnotifypostsaveasdocument-function"></a>DlpNotifyPostSaveAsDocument 函式

在 [另存新檔] 作業完成後，為系統提供檔的相關資訊。

## <a name="syntax"></a>語法


```C++
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a>參數

<dl> <dt>

*DocumentInfo* \[在\]
</dt> <dd>

[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含所儲存檔的相關資訊。

</dd> </dl>

<dl> <dt>

*目的地* \[在\]
</dt> <dd>

**LPCWSTR** ，其中包含所儲存檔的目的地路徑。

</dd> </dl>

<dl> <dt>

*OpStatus* \[在\]
</dt> <dd>

[DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md)結構的指標，其中包含有關「另存新檔」作業的狀態資訊。

</dd> </dl>


## <a name="return-value"></a>傳回值

傳回 void。

## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |