---
title: DefaultCharacterChange 事件
description: DefaultCharacterChange 事件
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372384"
---
# <a name="defaultcharacterchange-event"></a>DefaultCharacterChange 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當使用者變更預設字元時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式。 * * * DefaultCharacterChange* *  **(ByVal** *GUID * * * )**



| 部分   | 描述                                      |
|--------|--------------------------------------------------|
| *GUID* | 傳回字元的唯一識別碼。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

此事件表示使用者已變更指派為使用者預設字元的字元。 伺服器只將此傳送給已載入預設字元的用戶端。

出現新的字元時，它會假設與任何已載入的字元實例或先前的預設字元相同的大小，) 的順序 (。

### <a name="see-also"></a>另請參閱

[**ShowDefaultCharacterProperties 方法**](showdefaultcharacterproperties-method.md)， [ **Load 方法**](load-method.md)


 

 




