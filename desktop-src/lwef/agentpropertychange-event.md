---
title: AgentPropertyChange 事件
description: AgentPropertyChange 事件
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accafc89fbcd9f29dd7327cc4561c0375f773abe01077bab7cbfa24653f6106d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752689"
---
# <a name="agentpropertychange-event"></a>AgentPropertyChange 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




