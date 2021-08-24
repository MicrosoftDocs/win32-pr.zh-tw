---
description: LINEBUSYMODE \_ 位旗標常數描述交換器或網路可以產生的不同忙碌信號。 這些忙碌的信號通常表示進行呼叫所需的不同資源目前正在使用中。
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: 'LINEBUSYMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54563567944a2e5164717f7d64ff7026a0045ea735405a7bcad159969f07514a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681988"
---
# <a name="linebusymode_-constants"></a>LINEBUSYMODE \_ 常數

**LINEBUSYMODE \_** 位旗標常數描述交換器或網路可以產生的不同忙碌信號。 這些忙碌的信號通常表示進行呼叫所需的不同資源目前正在使用中。

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE \_ 站**
</dt> <dd> <dl> <dt>



忙碌信號表示被呼叫的合作物件的工作站忙碌中。 這通常會以 *正常* 忙碌的聲音來發出信號。


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE \_ 主幹**
</dt> <dd> <dl> <dt>



忙碌信號表示主幹或電路忙碌中。 這通常會以 *快速* 忙碌的聲音來發出信號。


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ 不明**
</dt> <dd> <dl> <dt>



忙碌信號的特定模式目前未知，但稍後可能會變成已知。


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



忙碌信號的特定模式無法使用，而且將不會變成已知。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

> [!Note]  
> 忙碌信號可能會以 inband 音或頻外訊息的形式傳送。 TAPI 不會假設特定的信號機制。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




