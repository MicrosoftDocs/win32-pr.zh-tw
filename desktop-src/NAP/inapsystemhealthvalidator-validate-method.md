---
title: 'INapSystemHealthValidator Validate 方法 (NapSystemHealthValidator .h) '
description: 驗證從用戶端接收之 SoHRequest 的 NAP 系統。
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- 驗證方法 NAP
- 驗證方法 NAP、INapSystemHealthValidator 介面
- INapSystemHealthValidator 介面 NAP，Validate 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c200e96024075d0c2880b294c197938a5ec0a6f3e1da4cb019d5ecd3ed32b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802768"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>INapSystemHealthValidator：： Validate 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidator：： Validate** 方法是由 SHV 開發人員定義，並由 NAP 系統呼叫來驗證從用戶端收到的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。

## <a name="syntax"></a>語法


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*要求* \[在\]
</dt> <dd>

識別驗證要求物件之 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) 物件的 COM 指標。

</dd> <dt>

*hintTimeOutInMsec* \[在\]
</dt> <dd>

通訊逾時間隔的持續時間（以毫秒為單位）。  (SHV) 的系統健全狀況驗證程式應在這段時間內回應;否則會捨棄回應。

> [!Note]  
> 所有 Shv 的預設超時值為2000毫秒。 使用預設值以外的值，將會變更所有已註冊之 Shv 的超時時間。

 

</dd> <dt>

*回呼* \[在\]
</dt> <dd>

回呼物件 [**INapServerCallback**](inapservercallback.md)的指標。 當 Shv 從呼叫 **INapSystemHealthValidator：： Validate** 傳回 **E \_ 暫** 止時，就會使用此回呼指標。 這可用於非同步驗證。 Shv 預期會在 *hintTimeOutInMsec* 時間內回應，否則將會捨棄回應。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果傳回任何其他錯誤碼，則系統會假設發生 serverComponent 失敗，而且會完成適當的對應以通過/失敗。



| 傳回碼                                                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 指出驗證程式已在 ' request ' 物件上設定 SoHResponse。<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ 暫止**</dt> </dl>                  | 指出將在個別的執行緒上呼叫 OnComplete () 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**RPC \_ S \_ 伺服器 \_ 無法使用**</dt> </dl> | 指出系統健全狀況驗證程式 (SHV) 進程終止，但 NapServer 實際上放開它的參考。 NapServer 會嘗試重新建立新的 SHV 參考，並且會重新叫用驗證呼叫一次。 如果建立物件或重新執行的驗證失敗，則會從已載入的 Shv 清單中移除 SHV。 現在可重載此 SHV 的唯一方法是再次取消註冊並重新註冊 SHV，或 NapServer 重新開機時<br/> |



 

## <a name="remarks"></a>備註

為了支援入侵偵測，系統會要求 Shv 驗證用戶端電腦，不論用戶端是否傳送了針對 SHV 的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。

SHV 必須執行下列動作：

-   藉由呼叫要求，從 *要求* 中取出 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) [**。GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md)。
-   如果 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包為 null：
    -   如果 SHV 是入侵偵測系統，請使用適當的 [**NAP 錯誤碼**](nap-error-constants.md)填入 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)封包，以因應用戶端電腦的惡意原因。
    -   所有其他 Shv 都應以 [**NAP \_ E \_ 缺少 \_ SOH**](nap-error-constants.md)的錯誤碼填入 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)封包。
-   如果 *napSystemGenerated* 為 **TRUE** ，則是來自 [**要求的呼叫。GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md)，SHV 應預期具有下列 3 TLVs 的 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包： [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)、 **sohAttributeTypeFailureCategory**、 **sohAttributeTypeErrorCodes**。 此 **SoHRequest** 是由 NapAgent 代表系統健康狀態代理程式產生， (sha) ，因為從 SHA 取出要求封包時發生錯誤。
-   驗證 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包。
    -   如果 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)的格式不正確，則請使用錯誤碼 [**NAP \_ E 不正確封 \_ \_ 包**](nap-error-constants.md)來建立 **SoHResponse** 封包。
    -   如果 SHV 只使用快取的資訊來驗證 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包 (也就是不會執行任何 i/o) ，它可以建立 **SoHResponse**，在 *要求* 中的物件上設定，並傳回「 **\_ 確定**」。
    -   如果 SHV 正在執行 i/o 以便與後端伺服器通訊以驗證用戶端的健康狀態，則它必須將 i/o 排入佇列，並將此函式傳回 **E \_ PENDING**。 在此情況下，SHV 必須呼叫 [**回呼。OnComplete**](inapservercallback-oncomplete-method.md) 在超時期間內的個別執行緒上進行 () *hintTimeOutInMsec*。 否則，將會捨棄 SHV 的回應。
-   請勿傳回上述任何其他錯誤。 如果 SHV 傳回任何其他錯誤碼 (例如 某些系統錯誤) ，將會捨棄封包。

SHV 必須在其 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)中傳回 **sohAttributeTypeComplianceResultCodes** 或 **sohAttributeTypeFailureCategory** TLV。

-   [**SOHATTRIBUTETYPECOMPLIANCERESULTCODES TLV**](sohattributetype-enum.md)：如果 SHV 可以驗證客戶 (端的健全狀況（例如狀況良好或狀況不良) ），則會傳回此 TLV。
-   [**SOHATTRIBUTETYPEFAILURECATEGORY TLV**](sohattributetype-enum.md)：如果用戶端或伺服器上有任何元件或通訊失敗，則必須由此 tlv 表示。 視 SHV 的設定而定，此 TLV 將進一步對應至狀況良好或狀況不良。 如需詳細資訊，請參閱 [**INapServerManagement**](inapservermanagement.md) 介面和 [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) 結構。

Asyncronous 呼叫完成後，SHV 不得持有 *要求* 或 *回呼* 的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





