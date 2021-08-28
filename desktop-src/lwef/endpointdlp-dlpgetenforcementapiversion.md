---
description: 在目前的裝置上，抓取端點資料遺失防止 (DLP) API 的版本。
title: 'DlpGetEnforcementApiVersion 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d126b720f1b6a0912598671c75240fb7f2a351098fc1fb00a748d873d1481905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725798"
---
# <a name="dlpgetenforcementapiversion-function"></a>DlpGetEnforcementApiVersion 函式

在目前的裝置上，抓取端點資料遺失防止 (DLP) API 的版本。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MajorVersion* \[在\]
</dt> <dd>

指定主要版本號碼的 **DWORD** 。

</dd> </dl>

<dl> <dt>

*MajorVersion* \[在\]
</dt> <dd>

指定次要版本號碼的 **DWORD** 。

</dd> </dl>


## <a name="return-value"></a>傳回值

傳回 HRESULT （包括但不限於下列值）。

| HRESULT | 描述 |
|---------|-------------|
| S_OK | 函數已順利完成 |




## <a name="remarks"></a>備註


## <a name="requirements"></a>需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |
| DLL<br/>                      | EndpointDlp.dll |