---
title: BalloonHide 事件
description: BalloonHide 事件
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184030"
---
# <a name="balloonhide-event"></a>BalloonHide 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

發生于隱藏字元的文字批註時。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**Sub** *agent* \_ **BalloonHide** **(ByVal** *CharacterID * * * )**



| 部分          | 描述                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | 傳回與文字提示字元相關聯之字元的識別碼。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

伺服器只會將此事件傳送給 (應用程式的用戶端，而這些應用程式已載入使用文字球的字元) 。

### <a name="see-also"></a>另請參閱

[**BalloonShow 事件**](balloonshow-event.md)


 

 




