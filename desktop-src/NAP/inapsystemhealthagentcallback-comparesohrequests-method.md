---
title: 'INapSystemHealthAgentCallback CompareSoHRequests 方法 (NapSystemHealthAgent .h) '
description: SHA 用來比較 SoH 要求。
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- CompareSoHRequests 方法 NAP
- CompareSoHRequests 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，CompareSoHRequests 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af26786c8ef021794876d8876ae5d8faee65b8cbbfc39b434b000ff502c64c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939433"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>INapSystemHealthAgentCallback：： CompareSoHRequests 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

SHA 會使用 **INapSystemHealthAgentCallback：： CompareSoHRequests** 方法來比較 SoH 要求。

## <a name="syntax"></a>語法


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lhs* \[在\]
</dt> <dd>

比較作業左邊的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 指標。

</dd> <dt>

*rhs* \[在\]
</dt> <dd>

比較作業右邊 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 的指標。

</dd> <dt>

*isEqual* \[擴展\]
</dt> <dd>

**布林** 值的指標，如果 *lhs* 和 *rhs* 語義相等，則為 **TRUE** ，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                               | Description                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 表示成功。<br/>                         |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl> | 方法不是由 SHA 所執行。<br/> |



 

## <a name="remarks"></a>備註

此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。

SHA 應比較 Soh，如果 Soh 是語義相等，則傳回 **TRUE** 。 NapAgent 會使用此資訊來判斷是否因為用戶端電腦的狀態變更而應起始 SoH 交換。

如果 Sha 將遞增識別碼或時間戳記放入 SoH，則 Soh 可能會有語義相等 (亦即，它們可能會傳達相同的健康情況資訊) ，但它們可能是位元組的不相等。 Sha 應該會執行此函式來檢查 Soh 是否有語義相等。

如果 Sha 未在其 Soh 中放入任何時間戳記或識別碼，他們可能會選擇不執行此函式並傳回 **E \_ >notimpl**。 在此情況下，NapAgent 會對 [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh)執行位元組取向的比較。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





