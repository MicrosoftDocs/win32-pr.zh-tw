---
description: 針對一組端點資料遺失防止 (DLP) 作業，通知系統所需的強制模式。
title: 'DlpInitializeEnforcementMode 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: be1e71782b258745e31d286a69ae76d3ecbcafb74c170f3b5baf5eb19bcc4b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610438"
---
# <a name="dlpinitializeenforcementmode-function"></a>DlpInitializeEnforcementMode 函式

針對一組端點資料遺失防止 (DLP) 作業，通知系統所需的強制模式。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* \[在\]
</dt> <dd>

**DWORD** ，指定包含在 *OperationEnforcement* 陣列中的作業數目。

</dd> </dl>

<dl> <dt>

*OperationEnforcement* \[在\]
</dt> <dd>

[DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md)結構的陣列，可指定端點 DLP 作業的強制等級。

</dd> </dl>


## <a name="return-value"></a>傳回值

傳回 HRESULT （包括但不限於下列值）。

| HRESULT | 描述 |
|---------|-------------|
| S_OK | 函數已順利完成 |
| E_INVALIDARG | 一或多個函數參數無效。 |
| E_OUTOFMEMORY | 作業的記憶體配置失敗。 |



## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |