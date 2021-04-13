---
title: 'IConnectionBrokerRequest CheckStatus 方法 (Cbclient .h) '
description: 呼叫以判斷非同步要求的狀態。
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- CheckStatus 方法遠端桌面服務
- CheckStatus 方法遠端桌面服務，IConnectionBrokerRequest 介面
- IConnectionBrokerRequest 介面遠端桌面服務，CheckStatus 方法
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385178"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a>IConnectionBrokerRequest：： CheckStatus 方法

呼叫以判斷非同步要求的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pReqStatus* \[擴展\]
</dt> <dd>

變數的位址，此變數會接收 [**CB \_ 要求 \_ 狀態**](cb-request-status.md) 列舉值，指出要求的狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Cbclient。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Cbclient .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





