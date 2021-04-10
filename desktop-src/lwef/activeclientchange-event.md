---
title: ActiveClientChange 事件
description: ActiveClientChange 事件
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183500"
---
# <a name="activeclientchange-event"></a>ActiveClientChange 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當字元的作用中用戶端變更時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式。* ActiveClientChange (ByVal *CharacterID*，byval *主動* **)**



| 部分          | 描述                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | 傳回發生事件之字元的識別碼。                                                                                                                                                                                                      |
| *使用中*      | 指出用戶端是否為作用中或非作用中的布林值。 **True** 用戶端應用程式成為字元的作用中用戶端。 <br/> **False** 用戶端應用程式不再是字元的作用中用戶端。<br/> |



 

</dd> </dl>

### <a name="remarks"></a>備註

當多個用戶端應用程式共用相同的字元時，字元的作用中用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 。 同樣地，當顯示多個字元時，最上層字元的作用中用戶端 (也稱為輸入-主動用戶端) 接收 [命令](command-event.md) 事件。

當使用中用戶端的字元變更時，此事件會傳回該字元的識別碼，如果您的應用程式已成為字元的作用中用戶端， **則為 True** ; 如果不再是字元的作用中用戶端，則為 **False** 。

當使用者在字元的快顯功能表中選取用戶端應用程式的專案時，或在用戶端應用程式變更其作用中狀態，或當其他用戶端應用程式結束其代理程式的連接時，用戶端應用程式可能會收到此事件。 代理程式只會將此事件傳送給直接受影響的用戶端應用程式;這會成為作用中的用戶端，或停止成為作用中用戶端。

### <a name="see-also"></a>另請參閱

[* * * * ActivateInput * * event * *](activateinput-event.md)、* * * * [Active * * property * *](active-property.md)、 [* * * * DeactivateInput * * event * *](deactivateinput-event.md)、 [* * * * Activate * * 方法 *](activate-method.md) *


 

 





