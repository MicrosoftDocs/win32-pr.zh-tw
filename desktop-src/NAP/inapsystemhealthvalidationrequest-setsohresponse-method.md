---
title: 'INapSystemHealthValidationRequest SetSoHResponse 方法 (NapSystemHealthValidator .h) '
description: 允許 (Shv) 的系統健康狀態驗證，將 SoHResponse 設定為要傳送到其系統健康情況代理程式 (用戶端上的 SHA) 對應。
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- SetSoHResponse 方法 NAP
- SetSoHResponse 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，SetSoHResponse 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af44bc3c4801a35ad311f184f3aa2763ccc401ee01dce8a96ef65a0e2496219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939136"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a>INapSystemHealthValidationRequest：： SetSoHResponse 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidationRequest：： SetSoHResponse** 方法可讓 (Shv 的系統健全狀況驗證程式) 將 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)設定為傳送至其系統健康情況代理程式 (用戶端上的 SHA) 對應。

## <a name="syntax"></a>語法


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sohResponse* \[在\]
</dt> <dd>

[**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





