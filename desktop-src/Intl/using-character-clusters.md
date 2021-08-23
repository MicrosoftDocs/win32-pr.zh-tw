---
description: 字元叢集是無法在行之間分割的字元序列。
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: 使用字元叢集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7a48dc8ec1b6fa3ea28cd116f275b1f410b8abd7e232442cff430ab843765f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631818"
---
# <a name="using-character-clusters"></a>使用字元叢集

字元叢集是無法在行之間分割的字元序列。 某些語言（例如，泰文和印度）會限制在叢集之間放置插入點放置。 這種限制適用于使用鍵盤或滑鼠動作起始的插入號移動 (點擊測試) 。

Uniscribe 會在 [**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) 結構所包含的視覺屬性中提供叢集資訊，以及 [**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) 結構中所包含的邏輯屬性。 在應用程式呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)之後，會以 **腳本 \_ LOGATTR** 陣列中相同值的序列以及 **腳本 \_ VISATTR** 陣列中的 **fClusterStart** 成員來表示叢集資訊。

[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)也會抓取 [**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fCharStop** 成員，以識別叢集位置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



