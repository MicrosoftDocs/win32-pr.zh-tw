---
description: 下圖顯示用於事件的 WMI 安全性常數。 它們是用來在用於事件或接收的安全描述項)  (Ace 設定存取控制專案。
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: '事件安全性常數 (Wbemcli .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ae26364c7edf6daaf9b70dcf769675c0a39966286b3b8f725fefe0af73ff8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244288"
---
# <a name="event-security-constants"></a>事件安全性常數

下圖顯示用於事件的 WMI 安全性常數。 它們是用來在用於事件或接收的安全描述項)  (Ace 設定存取控制專案。

<dl> <dt>

<span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM \_ 正確 \_ 發佈**
</dt> <dd> <dl> <dt>

128 (0x80) 
</dt> <dt>



指定帳戶可以將事件發佈至定義永久性取用者之事件篩選器的 [**\_ \_ >eventfilter**](--eventfilter.md)實例。 可在 wbemcli 中取得。


</dt> </dl> </dd> <dt>

<span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM \_ 正確 \_ 訂閱**
</dt> <dd> <dl> <dt>

64 (0x40) 
</dt> <dt>



指定取用者可以訂閱傳遞給接收的事件。 用於 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)。 可在 wbemcli 中取得。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ \_ 受限於 \_ \_ SDS**
</dt> <dd> <dl> <dt>

274435 (0x43003) 
</dt> <dt>



事件提供者指出 WMI 會檢查每個事件中的 **安全 \_ 描述項** 屬性 (繼承自 [**\_ \_ 事件**](--event.md)) ，而且只會將事件傳送給具有適當存取權限的取用者。 可在 wbemprov 中取得。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                         |
| 標頭<br/>                   | <dl> <dt>Wbemcli .h;</dt><dt>Wbemprov .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[維護 WMI 安全性](maintaining-wmi-security.md)
</dt> <dt>

[保護 WMI 事件](securing-wmi-events.md)
</dt> </dl>

 

 




