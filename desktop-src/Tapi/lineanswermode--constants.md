---
description: LINEANSWERMODE \_ 位旗標常數描述如何藉由在同一行上接聽另一個供應專案呼叫，來影響線路裝置上現有的使用中呼叫。
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: 'LINEANSWERMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984439"
---
# <a name="lineanswermode_-constants"></a>LINEANSWERMODE \_ 常數

**LINEANSWERMODE \_** 位旗標常數描述如何藉由在同一行上接聽另一個供應專案呼叫，來影響線路裝置上現有的使用 *中呼叫。*

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ DROP**
</dt> <dd> <dl> <dt>



將會自動卸載目前作用中的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ 保存**
</dt> <dd> <dl> <dt>



目前作用中的呼叫會自動置於保留狀態。


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ 無**
</dt> <dd> <dl> <dt>



在同一行上回答另一個呼叫不會影響該行上的現有使用中呼叫。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

如果 (提供的呼叫會在另一個呼叫已在使用中時) ，則會叫用 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)，將新的呼叫連接至。 對現有使用中的呼叫所造成的影響，取決於該行的裝置功能。 第一個呼叫可能不受影響，可能會自動卸載，或可能會自動放置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




