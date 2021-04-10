---
title: 'INapSystemHealthAgentCallback GetFixupInfo 方法 (NapSystemHealthAgent .h) '
description: 由 NapAgent 呼叫，以判斷系統健康狀態代理程式在處理 SoHResponse 時的狀態。
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- GetFixupInfo 方法 NAP
- GetFixupInfo 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，GetFixupInfo 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104141"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a>INapSystemHealthAgentCallback：： GetFixupInfo 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentCallback：： GetFixupInfo** 方法是由 NapAgent 呼叫，以判斷系統健康狀態代理程式在處理 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)時的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*資訊* \[擴展\]
</dt> <dd>

[**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)結構指標的指標，其中包含代理程式的修正狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                          | Description                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 表示成功。<br/> |



 

## <a name="remarks"></a>備註

此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。

系統健康狀態代理程式必須立即傳回 **\_ [確定]** ，而不會封鎖。

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

 

 





