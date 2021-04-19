---
description: 要求物件是使用 COM CoCreateInstance 建立的，而且會公開一個介面 ITRequest。
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: 要求物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982413"
---
# <a name="request-object"></a>要求物件

要求物件是使用 COM **CoCreateInstance** 建立的，而且會公開一個介面 [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)。 此介面會公開 [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) 方法，此方法可讓 TAPI 3 應用程式使用輔助電話語音。 輔助電話語音提供具備電話語音功能的應用程式，並使用簡單的機制來撥打電話，而不需要讓開發人員完全 >serilog.sinks.literate 電話語音。

例如，試算表應用程式可以使用輔助電話語音新增「打撥」按鈕，而不需要執行完整 TAPI 應用程式中更詳盡的控制項。

如需其他資訊，請參閱「 [輔助電話語音」總覽](assisted-telephony-overview.md) 。

 

 



