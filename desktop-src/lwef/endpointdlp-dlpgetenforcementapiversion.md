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
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495536"
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