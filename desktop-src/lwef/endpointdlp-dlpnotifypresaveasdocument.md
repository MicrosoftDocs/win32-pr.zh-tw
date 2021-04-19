---
description: 在起始「另存新檔」作業之前，為系統提供檔的相關資訊。
title: 'DlpNotifyPreSaveAsDocument 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495437"
---
# <a name="dlpnotifypresaveasdocument-function"></a>DlpNotifyPreSaveAsDocument 函式

在起始「另存新檔」作業之前，為系統提供檔的相關資訊。

## <a name="syntax"></a>語法


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DocumentInfo* \[在\]
</dt> <dd>

[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含要儲存之檔的相關資訊。

</dd> </dl>

<dl> <dt>

*目的地* \[在\]
</dt> <dd>

**LPCWSTR** ，其中包含要儲存之檔的目的地路徑。

</dd> </dl>


## <a name="return-value"></a>傳回值

傳回 void。

## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |