---
description: 安裝指定的 ActiveX 物件。
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: IeAxiSystemInstaller：： InitializeSystemInstaller 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851696"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>IeAxiSystemInstaller：： InitializeSystemInstaller 方法

**InitializeSystemInstaller** 方法會安裝指定的 ActiveX 物件。

## <a name="syntax"></a>語法


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrUrl* \[在\]
</dt> <dd>

要安裝之 ActiveX 物件的 URL。

</dd> <dt>

*dwClientPID* \[在\]
</dt> <dd>

呼叫進程的處理序識別碼。

</dd> <dt>

*pCallback* \[在\]
</dt> <dd>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)介面實例的指標，該介面會驗證是否允許安裝 ActiveX 物件。

</dd> <dt>

*pbstrNonce* \[擴展\]
</dt> <dd>

可以用來在呼叫其他方法時，用來共用狀態資訊的內容，用來驗證及下載 ActiveX 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](/windows/desktop/SecCrypto/common-hresult-values)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller 定義為 a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

