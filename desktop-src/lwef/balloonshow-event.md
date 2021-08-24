---
title: BalloonShow 事件
description: BalloonShow 事件
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10aa8ab2c556fdf603a3972033a7440041fef6a45f828115c649a8a42810eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726138"
---
# <a name="balloonshow-event"></a>BalloonShow 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

發生于顯示字元的文字批註時。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**Sub** *agent* \_ **BalloonShow** **(ByVal** *CharacterID * * * )**



| 部分          | 描述                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | 傳回與文字提示字元相關聯之字元的識別碼。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

伺服器只會將此事件傳送給 (應用程式的用戶端，而這些應用程式已載入使用文字球的字元) 。

### <a name="see-also"></a>另請參閱

[**BalloonHide 事件**](balloonhide-event.md)


 

 




