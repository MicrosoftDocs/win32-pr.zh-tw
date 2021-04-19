---
title: 'INapEnforcementClientConnection2 SetIsolationInfoEx 方法 (NapEnforcementClient .h) '
description: NapAgent 會使用來設定用戶端的隔離資訊。
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- SetIsolationInfoEx 方法 NAP
- SetIsolationInfoEx 方法 NAP，INapEnforcementClientConnection2 介面
- INapEnforcementClientConnection2 介面 NAP，SetIsolationInfoEx 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711b4bfd27c3bd92d48a78f4767f5ed452b2d4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968390"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a>INapEnforcementClientConnection2：： SetIsolationInfoEx 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NapAgent 會使用 **INapEnforcementClientConnection2：： SetIsolationInfoEx** 方法來設定用戶端的隔離資訊。

## <a name="syntax"></a>語法


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*isolationInfo* \[在\]
</dt> <dd>

[**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構的指標，其中包含用戶端的連接狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

這項資訊是由 NapAgent 在處理 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 之後設定的，而且不得由 enforcer 設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





