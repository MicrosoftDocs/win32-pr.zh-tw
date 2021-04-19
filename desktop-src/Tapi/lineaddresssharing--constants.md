---
description: LINEADDRESSSHARING \_ 位旗標常數描述可在各行之間共用位址的各種方式。
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: 'LINEADDRESSSHARING_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977730"
---
# <a name="lineaddresssharing_-constants"></a>LINEADDRESSSHARING \_ 常數

**LINEADDRESSSHARING \_** 位旗標常數描述可在各行之間共用位址的各種方式。

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ 私用**
</dt> <dd> <dl> <dt>



位址對使用者的行而言是私用的;它不會指派給任何其他工作站。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**
</dt> <dd> <dl> <dt>



位址會橋接于一或多個其他工作站。 在該行上啟用呼叫的第一行將可獨佔存取其上可能存在的位址和呼叫。 其他線條在使用時，將無法使用橋接位址。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**
</dt> <dd> <dl> <dt>



位址會與一或多個其他工作站橋接。 在該行上啟用呼叫的第一行，只會對對應的呼叫擁有獨佔存取權。 使用該位址的其他應用程式將會產生新的和不同的呼叫外觀。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**
</dt> <dd> <dl> <dt>



位址會橋接一或多個其他行。 所有橋接方都可以共用位址的呼叫，然後以會議的形式運作。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**\_受監視的 LINEADDRESSSHARING**
</dt> <dd> <dl> <dt>



這是將閒置/忙碌狀態設為可供這一行使用的位址。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

在各行之間共用位址的方式，可能會影響該位址的行為。 [**行 \_CALLSTATE**](line-callstate.md) 和 [**LINE \_ ADDRESSSTATE**](line-addressstate.md) 訊息會傳送至應用程式，以回應銜接站的活動。 透過這些訊息，應用程式可以追蹤位址的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**行 \_ CALLSTATE**](line-callstate.md)
</dt> </dl>

 

 




