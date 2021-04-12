---
title: 'INapCertRelyingParty GetSubscribedRelyingParties 方法 (NapCertRelyingParty .h) '
description: 取得已訂閱的信賴憑證者清單。
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- GetSubscribedRelyingParties 方法 NAP
- GetSubscribedRelyingParties 方法 NAP，INapCertRelyingParty 介面
- INapCertRelyingParty 介面 NAP，GetSubscribedRelyingParties 方法
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464489"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a>INapCertRelyingParty：： GetSubscribedRelyingParties 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**GetSubscribedRelyingParties** 方法會取得已訂閱的信賴憑證者清單。

## <a name="syntax"></a>語法


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* \[擴展\]
</dt> <dd>

[**EnforcementEntityCount**](nap-datatypes.md)的指標，其中包含已訂閱的信賴憑證者數目。

</dd> <dt>

*relyingParties* \[擴展\]
</dt> <dd>

指向 [**EnforcementEntityId**](nap-datatypes.md) 的指標，其中包含已訂閱之信賴憑證者的清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

呼叫端必須使用 **CoTaskMemFree** 釋放 *relyingParties* 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapCertRelyingParty。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCertRelyingParty .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





