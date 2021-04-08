---
title: 'IConnectionBrokerRequest 介面 (Cbclient .h) '
description: 提供取得非同步 IConnectionBrokerClient GetTargetInfo 方法之結果所需的方法。
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- IConnectionBrokerRequest 介面遠端桌面服務
- IConnectionBrokerRequest 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686508"
---
# <a name="iconnectionbrokerrequest-interface"></a>IConnectionBrokerRequest 介面

提供取得非同步 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法之結果所需的方法。

此介面是由系統所執行。 使用 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法，將這個介面的實例提供給呼叫者。

## <a name="members"></a>成員

**IConnectionBrokerRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IConnectionBrokerRequest** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IConnectionBrokerRequest** 介面具有這些方法。



| 方法                                                      | 描述                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) | 呼叫以判斷非同步要求的狀態。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                        |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Cbclient。h</dt> </dl>       |
| 程式庫<br/>                  | <dl> <dt>Cbclient .lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IConnectionBrokerRequest 定義為 25114427-ED5D-46A6-AF53-C62D33A4108E<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

