---
description: LINECALLSELECT \_ 位旗標常數描述要選取的呼叫。
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: 'LINECALLSELECT_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978497"
---
# <a name="linecallselect_-constants"></a>LINECALLSELECT \_ 常數

**LINECALLSELECT \_** 位旗標常數描述要選取的呼叫。

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT \_ 位址**
</dt> <dd> <dl> <dt>



選取指定位址上的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT \_ 呼叫**
</dt> <dd> <dl> <dt>



選取對指定之呼叫的相關呼叫。 例如，在會議通話中的合作物件。


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**
</dt> <dd> <dl> <dt>



選取對指定之呼叫識別碼的相關呼叫。 此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**
</dt> <dd> <dl> <dt>



選取指定裝置識別碼上的呼叫。 此旗標只會公開給協調 TAPI 2.1 版或更新版本的應用程式。 應用程式應該考慮使用 LINECALLSELECT \_ 行常數，而不是這一項。


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT \_ 行**
</dt> <dd> <dl> <dt>



選取指定線路裝置上的呼叫。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

這個常數會在 [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) 中使用，並指定所要求之呼叫 (範圍) 的選取範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




