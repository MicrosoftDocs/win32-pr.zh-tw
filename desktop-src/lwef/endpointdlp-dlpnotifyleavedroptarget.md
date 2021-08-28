---
description: 當卸載目標結束時，為系統提供檔的相關資訊。
title: 'DlpNotifyLeaveDropTarget 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyLeaveDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: aac567843a88abb3355ab0b239c9ac0eca66bdfd240f2e6d82b3f8f91586c9a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976588"
---
# <a name="dlpnotifyleavedroptarget-function"></a>DlpNotifyLeaveDropTarget 函式

當卸載目標結束時，為系統提供檔的相關資訊。

## <a name="syntax"></a>語法


```C++
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DocumentInfo* \[在\]
</dt> <dd>

[PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md)結構的指標，其中包含與 drop 作業相關聯之檔的相關資訊。

</dd> </dl>

<dl> <dt>

*OpStatus* \[在\]
</dt> <dd>

[DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md)結構的指標，其中包含放置目標結束作業的狀態資訊。

</dd> </dl>


## <a name="return-value"></a>傳回值

傳回 void。

## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |