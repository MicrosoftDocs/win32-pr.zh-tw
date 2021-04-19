---
description: LINETRANSFERMODE \_ 位旗標常數描述解決呼叫傳輸要求的不同方式。
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: 'LINETRANSFERMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989709"
---
# <a name="linetransfermode_-constants"></a>LINETRANSFERMODE \_ 常數

**LINETRANSFERMODE \_** 位旗標常數描述解決呼叫傳輸要求的不同方式。

<dl> <dt>

<span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE \_ 會議**
</dt> <dd> <dl> <dt>



藉由在應用程式、連線至初始通話的合作物件，以及連線到諮詢通話的合作物件之間建立三向會議，即可解決此轉移。 選取此選項時，就會建立會議通話。


</dt> </dl> </dd> <dt>

<span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE \_ 傳輸**
</dt> <dd> <dl> <dt>



傳輸的解決方式是將初始呼叫傳送給諮詢通話。 這兩個呼叫都會變成閒置的應用程式。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




