---
title: 'INapSystemHealthAgentCallback GetSoHRequest 方法 (NapSystemHealthAgent .h) '
description: NapAgent 會呼叫，以查詢系統健康情況代理程式的 SoH 要求。
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384837"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>INapSystemHealthAgentCallback：： GetSoHRequest 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NapAgent 會呼叫 **INapSystemHealthAgentCallback：： GetSoHRequest** 方法，以查詢系統健康情況代理程式的 SoH 要求。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*要求* \[在\]
</dt> <dd>

識別要求物件之 [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) 物件的 COM 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值



| 傳回碼                                                                                                                      | Description                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                             | 表示成功。<br/>                                                                                                                      |
| <dl> <dt>**\_ \_ 無法使用 WIN32 (RPC \_ S \_ 伺服器的 HRESULT \_)**</dt> </dl> | 如果您的執行傳回此程式碼，則 NapAgent 會接著從系結-SHA 清單中移除 SHA，並清除其快取專案。<br/> |



 

當您的實 SoHRequest 傳回的任何傳回值 (不是 **\_ \_ WIN32 (RPC \_ S \_ 伺服器 \_)**) 時，NAP 系統會使用下列屬性類型和值，來將 [](/windows/win32/api/naptypes/ns-naptypes-soh)結構和傳回對應的 SHV：

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) = [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <錯誤-程式碼>

## <a name="remarks"></a>備註

此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。

這個方法必須處理要求並立即傳回。 延遲傳回這個方法會對系統效能和回應性造成負面影響，而且可能會導致作業系統的其他部分超時。

健全狀況狀態監視不應在此呼叫過程中完成，特別是在需要大量計算且需要很長的時間時。 健全狀況狀態監視和 SoH 計算應該在個別的執行緒或服務中執行。 這個方法的唯一功能應該是設定 SHA 的 SoH 並傳回。

如果 SHA 需要很長的時間才能產生 SoH，則應該將快取的 SoH 傳回給 NapAgent。 如果沒有快取的 SoH 要傳回，則 SHA 應該立即傳回具有下列屬性類型和值的 SoH：

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) = [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  = [ **NAP \_ E \_ 沒有 \_ \_** 快取的 SOH](nap-error-constants.md)

產生 SoH 時，SHA 必須呼叫 [**INapSystemHealthAgentBinding：： NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) ，以通知 NapAgent 系統健康狀態變更。

NapAgent 會呼叫這個方法來查詢系統健康情況代理程式的 SoHRequest。 SHA 可以查詢傳遞的 [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) 物件，以取得其所需的參數來計算 SoHRequest。 SHA 必須設定 request 物件的計算 SoHRequest。 此呼叫完成之後，SHA 不能保留要求物件的參考。

當呼叫這個方法時，如果 NapAgent 的快取中有 SoH，則會在要求物件上設定它。 SHA 可以使用 **GetSoHRequest** 來查詢它。 如果 SHA 沒有設定新的 SoH，則會使用快取的 SoH。

針對已向系統註冊的未系結 Sha，NAP 系統會使用下列屬性類型和值，來建立 SoHRequest 並將其傳送至對應的 SHV：

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) = [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  = [ **NAP \_ E \_ 未 \_ 初始化**](nap-error-constants.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





