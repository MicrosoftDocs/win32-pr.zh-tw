---
description: 在啟動開啟作業之前，為系統提供檔檔案的相關資訊。
title: 'DlpNotifyPreOpenDocumentFile 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: f2be797d0f4045f17e753031247797406f332afa2fcc47b3ca83973527d99216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778228"
---
# <a name="dlpnotifypreopendocumentfile-function"></a>DlpNotifyPreOpenDocumentFile 函式

在啟動開啟作業之前，為系統提供檔檔案的相關資訊。

## <a name="syntax"></a>語法


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DocumentInfo* \[在\]
</dt> <dd>

[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含要開啟之檔的相關資訊。

</dd> </dl>


## <a name="return-value"></a>傳回值

傳回 void。

## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |