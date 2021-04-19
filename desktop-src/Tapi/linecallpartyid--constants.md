---
description: LINECALLPARTYID \_ 位旗標常數描述有關呼叫中參與之合作物件的性質。
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: 'LINECALLPARTYID_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001860"
---
# <a name="linecallpartyid_-constants"></a>LINECALLPARTYID \_ 常數

**LINECALLPARTYID \_** 位旗標常數描述有關呼叫中參與之合作物件的性質。

<dl> <dt>

<span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID \_ 位址**
</dt> <dd> <dl> <dt>



合作物件識別碼資訊是以標準位址格式或可撥位址格式的合作物件位址所組成。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID 已 \_ 封鎖**
</dt> <dd> <dl> <dt>



無法使用合作物件識別碼資訊，因為它已被遠端方封鎖。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID \_ 名稱**
</dt> <dd> <dl> <dt>



合作物件識別碼資訊包含合作物件名稱 (例如，從保留在切換) 內的目錄。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID \_ OUTOFAREA**
</dt> <dd> <dl> <dt>



呼叫的呼叫端識別碼資訊無法使用，因為它不會傳播到網路的所有方法。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ 部分**
</dt> <dd> <dl> <dt>



合作物件識別碼資訊是有效的，但只限于部分資訊。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID \_ UNAVAIL**
</dt> <dd> <dl> <dt>



無法使用合作物件識別碼資訊，稍後將無法使用。 資訊可能因為未指定的原因而無法使用。 例如，資訊並非由網路傳遞、服務提供者已忽略，依此類推。


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ 不明**
</dt> <dd> <dl> <dt>



合作物件識別碼資訊目前未知，但稍後可能會變成已知。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

針對每個牽涉到呼叫的合作物件， **LINECALLPARTYID \_** 常數描述合作物件識別碼資訊的格式化方式。 這項資訊是在 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) 資料結構中提供。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




