---
title: '已啟用屬性 (AudioOutput 物件) '
description: 瞭解已啟用的 AudioOutput 物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407341"
---
# <a name="enabled-property-audiooutput-object"></a>已啟用屬性 (AudioOutput 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回布林值，指出是否已啟用音訊 (讀出) 輸出。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 * * *。AudioOutput。已啟用**



| 值     | 描述                               |
|-----------|-------------------------------------------|
| **True**  | 已啟用 (預設) 的語音輸出。 |
| **False** | 語音音訊輸出已停用。          |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性會在 [代理程式] 屬性工作表的 [輸出] 頁面上反映 [播放音訊輸出] 選項， ([Advanced Character Options]) 。 當 [**Enabled**](enabled-property.md) 屬性傳回 **True** 時，如果已安裝相容的 TTS 引擎或您使用音效檔來進行語音輸出，則 [**說話**](speak-method.md) 方法會產生音訊輸出。 當它傳回 **False** 時，表示語音輸出未安裝或已由使用者停用。 屬性設定適用于所有代理程式字元，而且是唯讀的;只有使用者可以設定此屬性值。

## <a name="see-also"></a>另請參閱

[AgentPropertyChange 事件](agentpropertychange-event.md)


 

 




