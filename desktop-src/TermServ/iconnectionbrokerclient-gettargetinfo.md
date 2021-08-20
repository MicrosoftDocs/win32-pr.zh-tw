---
title: 'IConnectionBrokerClient GetTargetInfo 方法 (Cbclient .h) '
description: 要求應重新導向連接之目的電腦的相關資訊。
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- GetTargetInfo 方法遠端桌面服務
- GetTargetInfo 方法遠端桌面服務，IConnectionBrokerClient 介面
- IConnectionBrokerClient 介面遠端桌面服務，GetTargetInfo 方法
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df214f23c09b7439843f0d7e8947d40cc32b2bf30eece887c921aac34306fbdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059186"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>IConnectionBrokerClient：： GetTargetInfo 方法

要求應重新導向連接之目的電腦的相關資訊。 重新導向器會使用這個方法來取得連入連線要求的重新導向資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pConnectionInfo* \[在\]
</dt> <dd>

[**CB \_ 連接 \_ 資訊**](cb-connection-info.md)結構的位址，其中包含連入連線要求的相關資訊。

</dd> <dt>

*保留* \[在\]
</dt> <dd>

此參數已保留供日後使用，且必須為零。

</dd> <dt>

*hStatusEvent* \[在\]
</dt> <dd>

每當要求的進度更新時，將會設定之事件的控制碼。 您必須負責建立和關閉此事件。

</dd> <dt>

*pTargetInfo* \[擴展\]
</dt> <dd>

[**CB \_ 目標 \_ 資訊**](cb-target-info.md)結構的位址，此結構會接收應重新導向連入連線之目的電腦的相關資訊。 因為這是非同步方法，所以在要求完成之前，此記憶體必須保持可用。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

*pResult* \[擴展\]
</dt> <dd>

接收結果碼的 **DWORD** 變數位址。 因為這是非同步方法，所以在要求完成之前，此記憶體必須保持可用。 如需詳細資訊，請參閱＜備註＞。

此結果碼將會是下列其中一個值。

<dt>

0
</dt> <dd>

成功。

</dd> <dt>

0x0000400
</dt> <dd>

找不到目的地電腦。

</dd> <dt>

0x0000401
</dt> <dd>

目的地電腦無法使用。

</dd> <dt>

0x0000402
</dt> <dd>

載入目的地電腦時發生錯誤。

</dd> <dt>

0x0000403
</dt> <dd>

將目的地電腦上線時發生錯誤。

</dd> <dt>

0x0000404
</dt> <dd>

重新導向至目的地電腦時發生錯誤。

</dd> <dt>

0x0000405
</dt> <dd>

喚醒虛擬機器時發生錯誤。

</dd> <dt>

0x0000406
</dt> <dd>

啟動虛擬機器時發生錯誤。

</dd> <dt>

0x0000407
</dt> <dd>

尋找虛擬機器的 IP 位址時發生錯誤。

</dd> <dt>

0x0000408
</dt> <dd>

Session broker 在集區中找不到任何可用的電腦。

</dd> <dt>

0x0000409
</dt> <dd>

會話代理人取消了連接。

</dd> <dt>

0x0000410
</dt> <dd>

Session broker 無法驗證連接設定。

</dd> </dl> </dd> <dt>

*ppCbReq* \[擴展\]
</dt> <dd>

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)介面指標的位址，您可用來取得非同步作業的狀態更新。 此介面會與 *hStatusEvent* 參數搭配使用，以等候並取得此非同步作業的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已建立異步要求，則傳回 **E \_ 暫** 止。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法是非同步方法。 *PTargetInfo* 和 *pResult* 參數必須維持有效，直到 [**IConnectionBrokerRequest：： CheckStatus**](iconnectionbrokerrequest-checkstatus.md)方法取得 **CB \_ 狀態 \_ 要求 \_ 已完成**。

如需如何使用此方法的詳細資訊，請參閱 [如何使用遠端桌面連線代理人用戶端 API](use-the-remote-desktop-connection-broker-client-api.md)。

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

[**IConnectionBrokerClient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





