---
title: 'INapSystemHealthValidationRequest GetSoHRequest 方法 (NapSystemHealthValidator .h) '
description: 允許 (Shv) 的系統健康狀態驗證，以取得並驗證其系統健康情況代理程式 (SHA) 用戶端上所傳送的 SoHRequest 資訊。
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9c140af202de263e99f0fa8ec72186da6e995ec
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882615"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>INapSystemHealthValidationRequest：： GetSoHRequest 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidationRequest：： GetSoHRequest** 方法可讓 (Shv 的系統健全狀況驗證程式) 抓取和驗證用戶端上的系統健康情況代理程式 (SHA) 對應項所傳送的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sohRequest* \[擴展\]
</dt> <dd>

指向 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 結構指標的指標。

</dd> <dt>

*napSystemGenerated* \[擴展\]
</dt> <dd>

如果 NapAgent 代表 SHA 建立 SoH，則 **布林****值為 TRUE** ，否則為 **FALSE** 。 它主要用來指出對 SHV 的 SHA 失敗。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 說明                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

如果用戶端未將 [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)傳送至 SHV， *sohRequest* 參數可能會傳回 **Null** 。 在該案例中，SHV 可以在 **SoHResponse** 中填入 [**NAP \_ E \_ 缺少 \_ SOH**](nap-error-constants.md)的錯誤碼。

如果 *napSystemGenerated* 參數為 **TRUE**，則 *SoHRequest* 的格式如下所示：

-   [](sohattributetype-enum.md) =  sohAttributeTypeSystemHealthId &lt;Id&gt;
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) = [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  = [ **&lt; sha-失敗-錯誤-代碼 &gt;**](nap-error-constants.md)

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

 

 





