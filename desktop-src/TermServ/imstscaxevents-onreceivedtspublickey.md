---
title: IMsTscAxEvents OnReceivedTSPublicKey 方法
description: 當用戶端從伺服器抓取公開金鑰時，在連接順序中呼叫。 只有當 NotifyTSPublicKey 屬性為 VARIANT TRUE 時，才會呼叫此事件 \_ 。
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- OnReceivedTSPublicKey 方法遠端桌面服務
- OnReceivedTSPublicKey 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnReceivedTSPublicKey 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73f2b12b59cbe8e6b7c5f8e614e2aed047d4f467117fa211839521fedc7f333b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009478"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a>IMsTscAxEvents：： OnReceivedTSPublicKey 方法

當用戶端從伺服器抓取公開金鑰時，在連接順序中呼叫。 只有當 **NotifyTSPublicKey** 屬性為 **VARIANT \_ TRUE** 時，才會呼叫此事件。 這是在 [**OnConnecting**](imstscaxevents-onconnecting.md)之後，但在 [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) 和 [**OnConnected**](imstscaxevents-onconnected.md)之前。

## <a name="syntax"></a>語法


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*publicKey* \[在\]
</dt> <dd>

包含遠端電腦的公開金鑰。

</dd> <dt>

*pfContinueLogon* \[擴展\]
</dt> <dd>

**VARIANT \_ BOOL** 變數的指標，此變數會接收登入進程是否應繼續。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windowsserver 2008、Windows server 2008 SP1<br/>                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





