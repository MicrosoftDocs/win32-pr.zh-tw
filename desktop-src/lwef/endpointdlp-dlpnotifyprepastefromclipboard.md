---
description: 為系統提供檔的相關資訊，再開始貼上剪貼簿作業。
title: 'DlpNotifyPrePasteFromClipboard 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b490f4f5a258805c785822d815d9e341feb8bbd494e428eb7bf1be6da843d775
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778178"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a>DlpNotifyPrePasteFromClipboard 函式

為系統提供檔的相關資訊，再開始貼上剪貼簿作業。

## <a name="syntax"></a>語法


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DocumentInfo* \[在\]
</dt> <dd>

[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含要貼上內容之檔的相關資訊。

</dd> </dl>




## <a name="return-value"></a>傳回值

傳回 void。

## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |