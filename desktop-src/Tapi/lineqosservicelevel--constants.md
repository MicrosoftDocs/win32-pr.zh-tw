---
description: TSP 會使用這些常數來識別 QoS (所需服務品質) 層級的類型。
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: 'LINEQOSSERVICELEVEL_ 常數 (Tspi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a74a4508b54a8b56e8e9cb359f966122c5c009f0e5ede0f1b8544cd1e46330c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003006"
---
# <a name="lineqosservicelevel_-constants"></a>LINEQOSSERVICELEVEL \_ 常數

TSP 會使用這些常數來識別 QoS (所需服務品質) 層級的類型。

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**\_需要 LINEQOSSERVICELEVEL**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



要求的服務層級品質是必要條件。


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



需要的服務層級品質（如果有的話）。


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



所需的服務等級品質是「最佳的努力」。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



 

 




