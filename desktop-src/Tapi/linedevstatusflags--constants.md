---
description: LINEDEVSTATUSFLAGS \_ 位旗標常數描述布林線裝置狀態專案的集合。
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: 'LINEDEVSTATUSFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6649dc39c787be7c0b7f027637f12ff7f5d028add09b9f7d568149c6e9f76c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682004"
---
# <a name="linedevstatusflags_-constants"></a>LINEDEVSTATUSFLAGS \_ 常數

**LINEDEVSTATUSFLAGS \_** 位旗標常數描述布林線裝置狀態專案的集合。

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ 已連線**
</dt> <dd> <dl> <dt>



指定線路是否連接至 TAPI。 若 **為 TRUE**，表示線路已連線，且 TAPI 能夠線上路裝置上運作。 如果 **為 FALSE**，則表示該行已中斷連線，而且應用程式無法透過 TAPI 控制線路裝置。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INSERVICE**
</dt> <dd> <dl> <dt>



指出該行是否為服務。 若 **為 TRUE**，則為服務中的行;如果 **為 FALSE**，則表示該行不在服務中。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS 已 \_ 鎖定**
</dt> <dd> <dl> <dt>



指出行是否已鎖定或解除鎖定。 這位最常用於與行動電話相關聯的線路裝置。 許多行動電話都有一個安全性機制，需要輸入密碼才能讓電話撥打電話。 此位可用來向應用程式指出電話已鎖定，而且在手機的使用者介面上輸入密碼之前無法撥打電話，讓應用程式可以向使用者呈現適當的警示。


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**
</dt> <dd> <dl> <dt>



指出該行是否有等候中的訊息。 若 **為 TRUE**，則表示訊息正在等候;如果 **為 FALSE**，則表示沒有訊息正在等候。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

LINEDEVSTATUSFLAGS \_ 常數用於 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)資料結構的 **dwDevStatusFlags** 成員內。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




