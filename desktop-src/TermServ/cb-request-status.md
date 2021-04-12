---
title: 'CB_REQUEST_STATUS 列舉 (Cbclient .h) '
description: 指定非同步要求的狀態。
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317191"
---
# <a name="cb_request_status-enumeration"></a>CB \_ 要求 \_ 狀態列舉

指定非同步要求的狀態。 此列舉會搭配 [**IConnectionBrokerRequest：： CheckStatus**](iconnectionbrokerrequest-checkstatus.md) 方法使用。

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB \_ 狀態 \_ 無效**
</dt> <dd>

要求物件未初始化。

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB \_ 狀態 \_ 起始 \_ 要求**
</dt> <dd>

未使用。

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB \_ 狀態 \_ 要求 \_ 已完成**
</dt> <dd>

要求已完成。

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB \_ 狀態 \_ 要求 \_ 失敗**
</dt> <dd>

要求失敗。

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB \_ 狀態 \_ 要求已 \_ 中止**
</dt> <dd>

要求已中止。

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB \_ 狀態 \_ 尋找 \_ 目的地**
</dt> <dd>

未使用。

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB \_ 狀態 \_ 載入 \_ 目的地**
</dt> <dd>

未使用。

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB \_ 狀態 \_ 將 \_ 會話 \_ 上線**
</dt> <dd>

未使用。

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB \_ 狀態重新導向 \_ \_ 至 \_ 目的地**
</dt> <dd>

未使用。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Cbclient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConnectionBrokerRequest：： CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





