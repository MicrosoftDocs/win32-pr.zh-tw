---
description: LINECALLTREATMENT \_ 常數會列出未接聽或保留的呼叫的進行中的操作。 除了基本參數驗證，呼叫處理是由 TAPI 直接傳遞給服務提供者。
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: 'LINECALLTREATMENT_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995483"
---
# <a name="linecalltreatment_-constants"></a>LINECALLTREATMENT \_ 常數

**LINECALLTREATMENT \_** 常數會列出未接聽或保留的呼叫的進行中的操作。 除了基本參數驗證，呼叫處理是由 TAPI 直接傳遞給服務提供者。

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ 忙碌**
</dt> <dd> <dl> <dt>



當呼叫未主動連線到裝置 (供應或舉 servicerequeststatusenum.onhold) 時，合作物件會聽到忙碌信號。


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT \_ 音樂**
</dt> <dd> <dl> <dt>



當呼叫未主動連線到裝置 (供應專案或舉 servicerequeststatusenum.onhold) 時，合作物件會聽到音樂。


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT \_ 回電**
</dt> <dd> <dl> <dt>



當呼叫未主動連線到裝置 (供應專案或舉 servicerequeststatusenum.onhold) 時，合作物件會聽到回電語氣。


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT \_ 無聲**
</dt> <dd> <dl> <dt>



當呼叫未主動連線到裝置 (供應專案或舉 servicerequeststatusenum.onhold) 時，合作物件會聽到無聲。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

保留值0x00000000 以表示服務提供者不支援呼叫處理。 範圍0x00000005 到0x000000FF 的值會保留供未來定義之用。 範圍0x00000100 到0xFFFFFFFF 的值會保留給服務提供者指派，而且可能包含特定的音樂選擇或記錄的宣告。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




