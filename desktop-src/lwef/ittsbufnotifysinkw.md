---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de27451826a232092bc74e630a54621a004cc15e44ad4a9a7d3377509ff00ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476715"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

引擎必須透過 **書簽** 來呼叫。 在語音輸出的前置處理期間，Microsoft 代理程式程式碼會在「單字」之間插入書簽，並使用這些書簽的抵達來推動文字球中的文字步調。 雖然在語句結束之前，在一段時間內，不需要任何超過這些書簽的抵達，但必須以相當及時的方式傳回書簽，才能支援 Microsoft Agent。

請注意，某些語言（例如日文）沒有 "word" 的嚴格概念。 Microsoft 代理程式的「 [**說話**](speak-method.md) 」方法會將「單字」定義為已連接的符號字串，而這些符號的意義和發音都是隔離的。 Microsoft Agent 會使用相當簡單的剖析程式碼來判斷「單字」是什麼：它會尋找以空白字元分隔的符號。 因此，英文字串 "101 Dalmatians"： "a"、"101" 和 "Dalmatians" 中有三個「單字」。 Microsoft Agent Map 標記中包含的文字會被視為單一「單字」以供顯示之用。

 

 




