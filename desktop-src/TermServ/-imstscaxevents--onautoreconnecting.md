---
title: IMsTscAxEvents OnAutoReconnecting 方法
description: 當用戶端正在自動重新連接具有遠端桌面工作階段主機 (RD 工作階段主機) server 的會話時呼叫。 |IMsTscAxEvents OnAutoReconnecting 方法
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting 方法遠端桌面服務
- OnAutoReconnecting 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAutoReconnecting 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a26bb57416cd73f6d838ab08167923c4900b7b923a6a6f411239bbacd3fdbac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309138"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a>IMsTscAxEvents：： OnAutoReconnecting 方法

當用戶端正在自動重新連接具有遠端桌面工作階段主機 (RD 工作階段主機) server 的會話時呼叫。

## <a name="syntax"></a>語法


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*disconnectReason* \[在\]
</dt> <dd>

描述上次會話中斷連接原因的程式碼。

</dd> <dt>

*了 attemptcount* \[在\]
</dt> <dd>

目前自動重新連接程式中所做的嘗試次數。 每次嘗試時，此計數都會增加一個。

</dd> <dt>

*pArcContinueStatus* \[擴展\]
</dt> <dd>

傳回的程式碼指標，指定自動重新連接程式的狀態。 您可以重設此程式碼，以變更目前自動重新連接程式的狀態。

如需重設此程式碼的詳細資訊，請參閱「備註」一節。

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic * * * (0) 


</dt> <dd>

重新連接程式會自動發生。 這是預設值。

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop * * * (1) 


</dt> <dd>

重新連接程式已停止。

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual * * * (2) 


</dt> <dd>

重新連接程式是以手動方式發生。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在事件接收中執行此方法，以接收控制項重新建立與 RD 工作階段主機伺服器之連接的通知。

如果透過將 *pArcContinueStatus* 參數的值設定為 **autoReconnectContinueAutomatic** 來變更自動重新連線程式的狀態，這個方法就會以純粹的諮詢模式來運作。 容器可以接聽此事件，以取得自動重新連接程式正在進行的通知。 控制項將會根據自己的內部時間和嘗試計數，自動繼續嘗試重新建立連接。 在每次自動重新連線嘗試期間都會呼叫這個方法，以便通知容器。

將 *pArcContinueStatus* 參數的值設定為 **autoReconnectContinueStop** 時，自動重新連接程式的狀態變更時，將會終止目前的自動重新連線嘗試，並將中斷連線通知傳送至容器，而不會再發出任何自動重新連線通知。

> [!Note]  
> 使用 [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) 屬性來啟用或停用自動重新連接。

 

透過將 *pArcContinueStatus* 參數的值設定為 **autoReconnectContinueManual** 來變更自動重新連線程式的狀態時，容器會藉由呼叫 [**連線**](imstscax-connect.md)來觸發連接嘗試或 [**中斷**](imstscax-disconnect.md)連線以取消自動重新連線程式，以手動方式控制自動重新連接程式。 一旦設定為此值，控制項就會停止進行自動重新連線嘗試，並且成為容器的原則，以進行 **連線** 呼叫，以觸發自動重新連線嘗試。 這是在容器提供自動重新連線的自訂 UI 行為時完成，例如在自動重新連線程式之前重新開機已中斷的 RAS 或 VPN 連線。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





