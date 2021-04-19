---
description: TSP 會使用這些常數來識別 QoS (服務品質) 要求的結果。
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: 'LINEEQOSINFO_ 常數 (Tspi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993609"
---
# <a name="lineeqosinfo_-constants"></a>LINEEQOSINFO \_ 常數

TSP 會使用這些常數來識別 QoS (服務品質) 要求的結果。

<dl> <dt>

<span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO \_ NOQOS**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



無法使用 QoS。


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO \_ ADMISSIONFAILURE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



無法符合 QoS 要求。


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



不支援要求的 QoS 類型。


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ GENERICERROR**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



未指定的 QoS 錯誤。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



 

 




