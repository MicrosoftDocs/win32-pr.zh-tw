---
description: 色調監視會監視指定色調的媒體串流。
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: 語氣監視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb811d91a70f439ae17123b35967800914bd6a04f1a30168754f602231f038e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034178"
---
# <a name="tone-monitoring"></a>語氣監視

色調監視會監視指定色調的媒體串流。 色調是依元件的頻率和步調來描述。 API 的執行可能會允許同時監視數個不同的色調。 應用程式可以標記每個色調，以便區分它要求偵測的不同聲音。

應用程式可以使用 [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)在指定的呼叫上啟用或停用語氣監視。 使用這個函式時，應用程式會指出要在指定的呼叫上偵測哪些色調。 啟用音調監視時，偵測到的數位會導致應用程式收到 [**行 \_ MONITORTONE**](line-monitortone.md) 訊息的通知。 此訊息提供偵測到其色調的呼叫控制碼，以及應用程式的音調標記。

語氣監視的範圍是由呼叫的存留期所限制。 當通話 *中斷* 連線或 *閒置* 時，呼叫上的色調監視就會結束。

> [!Note]  
> 聲音、數位或媒體類型的監視通常需要使用服務提供者只能有有限數量的資源。 如果無法使用資源，則可能會拒絕監視要求。 基於相同的理由，應用程式應該停用任何不必要的監視。

 

 

 



