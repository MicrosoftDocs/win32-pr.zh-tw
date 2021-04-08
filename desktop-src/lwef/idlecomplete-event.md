---
title: IdleComplete 事件
description: IdleComplete 事件
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020709"
---
# <a name="idlecomplete-event"></a>IdleComplete 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當伺服器結束字元的 **閒置** 狀態時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式 * * * \_ IdleComplete* *  **(ByVal** *CharacterID * * * )**



| 部分          | 描述                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | 以字串形式傳回閒置字元的識別碼。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

伺服器會將此事件傳送給該字元的所有用戶端。

### <a name="see-also"></a>另請參閱

[**IdleStart 事件**](idlestart-event.md)


 

 




