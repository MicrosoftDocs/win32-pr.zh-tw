---
title: Echo 範例總覽
description: Echo 範例總覽
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Windows Media Player 外掛程式，Echo 範例總覽
- 外掛程式，Echo 範例總覽
- 數位信號處理外掛程式，Echo 範例總覽
- DSP 外掛程式，Echo 範例總覽
- Echo DSP 外掛程式範例，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976322"
---
# <a name="echo-sample-overview"></a>Echo 範例總覽

本指南建立 Windows Media Player 的 DSP 外掛程式，以在播放期間于 PCM 音訊中建立 echo 效果。 外掛程式的目標如下：

-   外掛程式只會處理8位或16位 PCM 音訊。
-   它支援介於10毫秒之間的延遲時間 (ms) 和2000毫秒 (2 秒的) 。 這代表大部分應用程式的實際範圍。
-   它支援混合原始信號與延遲信號。
-   它提供了屬性頁的執行，可讓使用者提供延遲時間的值，以及相對於整體音訊信號層級的延遲信號百分比值。
-   您可以藉由修改 Windows Media Player 外掛程式 Wizard 音訊 DSP 外掛程式範例來建立程式碼。

Echo 範例不包含在 Windows Media Player SDK 中;它是您所建立的範例。 若要建立 Echo 範例，您必須從 Windows Media Player 外掛程式 Wizard 中的預設專案開始。 您可以將專案命名為任何您喜歡的專案;本檔假設專案命名為 Echo。 如需使用 wizard 的詳細資訊，請參閱 [建立 DSP 外掛程式](building-a-dsp-plug-in.md)。

下一節將概述範例如何建立回應效果：

-   [Echo 範例的運作方式](how-the-echo-sample-works.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Echo 範例**](the-echo-sample.md)
</dt> </dl>

 

 




