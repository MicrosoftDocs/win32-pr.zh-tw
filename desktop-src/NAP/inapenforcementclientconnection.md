---
title: 'INapEnforcementClientConnection 介面 (NapEnforcementClient .h) '
description: '允許用戶端連接管理。 |INapEnforcementClientConnection 介面 (NapEnforcementClient .h) '
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- INapEnforcementClientConnection 介面 NAP
- INapEnforcementClientConnection 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195928"
---
# <a name="inapenforcementclientconnection-interface"></a>INapEnforcementClientConnection 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientConnection** 提供允許用戶端連接管理的方法。

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) 會繼承此介面的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapEnforcementClientConnection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapEnforcementClientConnection** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapEnforcementClientConnection** 介面具有這些方法。



| 方法                                                                                                                           | 描述                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection：： GetConnectionId**](inapenforcementclientconnection-getconnectionid-method.md)               | 取得用戶端的連接識別碼。<br/>                                                                                          |
| [**INapEnforcementClientConnection::GetCorrelationId**](inapenforcementclientconnection-getcorrelationid-method.md)             | 取得用來相互關聯 SoH 要求和 SoH 回應的識別碼。<br/>                                                                  |
| [**INapEnforcementClientConnection::GetEnforcerPrivateData**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | 供 enforcer 用來取得私用資料。<br/>                                                                                      |
| [**INapEnforcementClientConnection：： GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | 取得旗標的值，這個值會區分因為 enforcers 快取的 SoHRequests，而回應的第一次回應。<br/> |
| [**INapEnforcementClientConnection::GetIsolationInfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | 使用取得用戶端的隔離資訊。<br/>                                                                              |
| [**INapEnforcementClientConnection::GetMaxSize**](inapenforcementclientconnection-getmaxsize-method.md)                         | 取得此用戶端的 SoH 封包大小上限。<br/>                                                                       |
| [**INapEnforcementClientConnection::GetPrivateData**](inapenforcementclientconnection-getprivatedata-method.md)                 | 供 NapAgent 用來取得私用資料。<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetSoHRequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | 取得 SoH 要求。<br/>                                                                                                          |
| [**INapEnforcementClientConnection::GetSoHResponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | 取得強制用戶端接收的 SoH-Response。<br/>                                                                      |
| [**INapEnforcementClientConnection::GetStringCorrelationId**](inapenforcementclientconnection-getstringcorrelationid-method.md) | 取得 CorrelationId 的字串版本。 主要用於記錄用途。<br/>                                             |
| [**INapEnforcementClientConnection：： Initialize**](inapenforcementclientconnection-initialize-method.md)                         | 初始化連接。<br/>                                                                                                    |
| [**INapEnforcementClientConnection::SetConnectionId**](inapenforcementclientconnection-setconnectionid-method.md)               | 設定用戶端的連接識別碼。<br/>                                                                                          |
| [**INapEnforcementClientConnection::SetCorrelationId**](inapenforcementclientconnection-setcorrelationid-method.md)             | 設定用來相互關聯 SoH 要求和 SoH 回應的識別碼。<br/>                                                                  |
| [**INapEnforcementClientConnection::SetEnforcerPrivateData**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | 供 enforcer 用來設定私用資料。<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetFlags**](inapenforcementclientconnection-setflags-method.md)                             | 設定旗標，此旗標會根據 enforcers 快取的 SoHRequests，區分第一次回應與回應。<br/>                  |
| [**INapEnforcementClientConnection::SetIsolationInfo**](inapenforcementclientconnection-setisolationinfo-method.md)             | 供 NapAgent 用來設定用戶端的隔離資訊。<br/>                                                           |
| [**INapEnforcementClientConnection::SetMaxSize**](inapenforcementclientconnection-setmaxsize-method.md)                         | 設定此用戶端的 SoH 封包大小上限。<br/>                                                                       |
| [**INapEnforcementClientConnection::SetPrivateData**](inapenforcementclientconnection-setprivatedata-method.md)                 | 供 NapAgent 用來設定私用資料。<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetSoHRequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | 設定 SoH 要求。<br/>                                                                                                          |
| [**INapEnforcementClientConnection::SetSoHResponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | 設定 SoH-Response，並在接收封包時由強制用戶端使用。<br/>                                             |



 

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

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

