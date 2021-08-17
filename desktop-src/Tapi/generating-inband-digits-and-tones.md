---
description: 當通話處於已線上狀態之後，就可以將資訊傳送給它。
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: 產生 Inband 數位和音調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f144d4bc6b6273f71da37f6b9864146465c5ca29b91018a2e2ff097f6f19b44f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424878"
---
# <a name="generating-inband-digits-and-tones"></a>產生 Inband 數位和音調

當通話處於 *已連線* 狀態之後，就可以將資訊傳送給它。 提供了兩個函式，可允許應用程式與遠端工作站設備（例如，回應機器）之間的端對端 inband 信號。 其中一個函式是 [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)，它會在呼叫上產生 inband 位數，並透過語音通道來發出信號。 數位可以是旋轉/脈衝序列或 DTMF 聲。 另一個函式是 [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)，可讓應用程式透過媒體串流) 來產生各種 multifrequency 聲 inband (。 這會產生電話語音聲，例如回電、嗶聲和忙碌，以及任意 multifrequency、multicadenced 音。

在一次呼叫時，一次只能進行一個數位或語氣產生。 當數位或語氣產生完成時，會將 [**行 \_ 產生**](line-generate.md) 訊息傳送至要求產生的應用程式。 在產生多個數位的情況下，只會在產生所有數位之後傳回單一訊息。 在數位或語氣產生過程中呼叫 [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) 或 [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) ，將會中止目前進行中的產生作業，並將產生的行 \_ 產生訊息傳送至應用程式，而該應用程式的產生會以取消指示中止。

 

 



