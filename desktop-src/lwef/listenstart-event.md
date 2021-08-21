---
title: ListenStart 事件
description: ListenStart 事件
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0017b628af3ca266058de74508d379bd665c94f94c64207f4d7bef5487a0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976108"
---
# <a name="listenstart-event"></a>ListenStart 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當接聽模式 (語音辨識) 開始時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式。 * * * ListenStart (ByVal* *  *CharacterID * * * )**



| 部分          | 描述                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | 以字串形式傳回接聽字元的識別碼。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

此事件會在接聽模式開始時傳送至所有用戶端，因為使用者按下接聽鍵或輸入主動用戶端，並以 **True** 呼叫 [**接聽**](listen-method.md)方法。 您可以使用此事件來避免在接聽模式開啟時，讓您的字元說話。

如果您使用 [**接聽**](listen-method.md) 方法開啟接聽模式，然後使用者按下接聽鍵，則接聽模式會重設並繼續進行，直到接聽的金鑰超時時間完成、接聽的金鑰已釋出或使用者已完成說話（以稍後的何者為准）。 在此情況下，當接聽模式已開啟時，當使用者按下接聽鍵時，您將不會收到額外的 **ListenStart** 事件。

此事件會將字元傳回給目前已載入此字元的用戶端。 所有其他用戶端都會收到 null 字元， (空的字串) 。

### <a name="see-also"></a>另請參閱

[**ListenComplete 事件**](listencomplete-event.md)， [**接聽方法**](listen-method.md)


 

 




