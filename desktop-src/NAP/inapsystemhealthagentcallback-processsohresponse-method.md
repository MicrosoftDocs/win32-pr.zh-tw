---
title: 'INapSystemHealthAgentCallback ProcessSoHResponse 方法 (NapSystemHealthAgent .h) '
description: 當 NapAgent 收到以這個健康情況代理程式為目標的 SoHResponse 時，會呼叫。
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- ProcessSoHResponse 方法 NAP
- ProcessSoHResponse 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，ProcessSoHResponse 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5aaca7833560dbb53422da08ced158bb172610c3bacef931866d74d416fcce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367753"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>INapSystemHealthAgentCallback：:P rocessSoHResponse 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentCallback：:P rocesssohresponse** 方法會在 NapAgent 收到以這個健康情況代理程式為目標的 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)時呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessSoHResponse(
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

這個方法可以傳回其中一個值。



| 傳回碼                                                                                            | Description                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 表示成功。<br/>                                                            |
| <dl> <dt>**NAP \_ E \_ 不正確封 \_ 包**</dt> </dl> | 如果回應的格式不正確，則會傳回此實作為。<br/> |



 

## <a name="remarks"></a>備註

此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。

當 NapAgent 收到以這個健康情況代理程式為目標的 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 時，它會叫用這個方法。 健康情況代理程式必須從要求物件查詢 SoHResponse。 一旦完成此呼叫，它就不能保存要求物件的參考。

**INapSystemHealthAgentCallback：:P rocesssohresponse** 方法不得封鎖。 如果需要進行任何修正程式，則任何 **ProcessSoHResponse** 的執行都必須啟動新的執行緒，以執行修正處理。 NapAgent 必須呼叫 [**INapSystemHealthAgentCallBack：： GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) ，以判斷 SHA 的修正狀態。

如果回應的格式不正確，此方法必須傳回 **NAP \_ E \_ 無效 \_** 的封包。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





