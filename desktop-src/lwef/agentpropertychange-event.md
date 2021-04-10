---
title: AgentPropertyChange 事件
description: AgentPropertyChange 事件
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021230"
---
# <a name="agentpropertychange-event"></a>AgentPropertyChange 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

發生于使用者變更 [先進字元選項] 視窗中的屬性時。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式。 * * * AgentPropertyChange**

</dd> </dl>

### <a name="remarks"></a>備註

此事件表示使用者已變更並套用 [Advanced Character] 選項視窗中包含的任何屬性。

在處理此事件的程式碼中，您可以查詢 [AudioOutput](the-audiooutput-object.md) 或 [SpeechInput](the-speechinput-object.md) 物件的特定屬性設定。

### <a name="see-also"></a>另請參閱

[**DefaultCharacterChange 事件**](defaultcharacterchange-event.md)


 

 




