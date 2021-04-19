---
title: ListeningTip 屬性
description: ListeningTip 屬性
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966209"
---
# <a name="listeningtip-property"></a>ListeningTip 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回布林值，指出接聽提示目前的使用者設定。

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法** 
</dt> <dd>

*代理程式 * * *。SpeechInput. ListeningTip**



| 值     | 描述                    |
|-----------|--------------------------------|
| **True**  | 已啟用接聽提示。  |
| **False** | 接聽提示已停用。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**ListeningTip** 屬性會指出是否已啟用 Microsoft Agent 屬性工作表中的顯示接聽提示選項 ([Advanced Character Options]) 。 當 **ListeningTip** 傳回 **True** 且啟用語音輸入時，當使用者按下接聽鍵時，伺服器會顯示提示視窗。

## <a name="see-also"></a>另請參閱

[**AgentPropertyChange 事件**](agentpropertychange-event.md)


 

 




