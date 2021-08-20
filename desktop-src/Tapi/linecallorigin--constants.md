---
description: LINECALLORIGIN \_ 常數描述呼叫的來源。
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: 'LINECALLORIGIN_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 296bcc27f3f238e20608279a14ab00c0ab04060faef458fade3f222c7fa35fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117944909"
---
# <a name="linecallorigin_-constants"></a>LINECALLORIGIN \_ 常數

**LINECALLORIGIN \_** 常數描述呼叫的來源。

<dl> <dt>

<span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN \_ 會議**
</dt> <dd> <dl> <dt>



通話控制碼適用于會議電話，也就是應用程式與交換器中的會議橋接器的連接。


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ 外部**
</dt> <dd> <dl> <dt>



呼叫是以外部線路上的撥入電話來產生。


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN \_ 輸入**
</dt> <dd> <dl> <dt>



呼叫是以來電的形式產生，但服務提供者無法判斷它是否來自相同交換器上的另一個站，或從外部線路。 只有在已協商 TAPI 1.4 版或更新版本時，服務提供者才能使用此常數。 否則，服務提供者可以替代 LINECALLORIGIN \_ UNAVAIL。


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ 內部**
</dt> <dd> <dl> <dt>



呼叫是源自相同切換環境內部之站上的撥入電話。


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN \_ 輸出**
</dt> <dd> <dl> <dt>



由此站發出的呼叫會被撥出呼叫。


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN \_ UNAVAIL**
</dt> <dd> <dl> <dt>



呼叫來源無法使用，而且永遠不會成為此呼叫的已知。


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ 不明**
</dt> <dd> <dl> <dt>



呼叫來源目前未知，但稍後可能會變成已知。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

呼叫的來源會儲存在呼叫之 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)結構的 **>dworigin** 成員中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




