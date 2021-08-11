---
title: Status 屬性
description: Status 屬性
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edb1196e5ec41571c9c760b91a72b350b94f6b85f1f85af018691d3f25ecec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245822"
---
# <a name="status-property"></a>Status 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回音訊輸出通道的狀態。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 * * *。AudioOutput。狀態**



| 值 | 描述                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | 音訊輸出通道可用 () 不會忙碌。                                                                 |
| 1     | 不支援音訊輸出;例如，因為沒有音效卡。                                |
| 2     | 無法開啟音訊輸出通道 (忙碌中) ;例如，因為有些其他應用程式現正播放音訊。 |
| 3     | 音訊輸出通道忙碌中，因為伺服器正在處理使用者語音輸入。                              |
| 4     | 音訊輸出通道正在忙碌中，因為字元目前正在說話中。                                       |
| 5     | 音訊輸出通道不在忙碌中，但正在等候使用者語音輸入。                                    |
| 6     | 嘗試存取音訊輸出通道時發生一些其他 (未知的) 問題。                          |



 

</dd> </dl>

## <a name="remarks"></a>備註

這項設定可讓您的用戶端應用程式查詢音訊輸出通道，並傳回整數值以指出音訊輸出通道的狀態。 您可以使用此資訊來判斷是否適合讓您的字元說話，或是否適合嘗試使用 [**接聽**](listen-method.md) 方法) 來開啟接聽模式 (。

## <a name="see-also"></a>另請參閱

[**ListenComplete 事件**](listencomplete-event.md)


 

 




