---
description: 用來釋出安全通訊端層通訊協定 (SSL) 提供者函式所配置的記憶體。
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: 'SslFreeBuffer 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027530"
---
# <a name="sslfreebuffer-function"></a>SslFreeBuffer 函式

**SslFreeBuffer** 函式可用來釋出 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 提供者函式所配置的記憶體。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pvInput* \[在\]
</dt> <dd>

要釋放之記憶體緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PdwProviderCount* 或 *PpProviderList* 參數為 **Null**。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

