---
description: 關於 Sequencer 來源
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: 關於 Sequencer 來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511736"
---
# <a name="about-the-sequencer-source"></a>關於 Sequencer 來源

Sequencer 來源可讓應用程式依序播放 [媒體來源](media-sources.md) 的集合，並在來源之間進行無縫轉換。 Sequencer 來源可以用於下列案例：

-   建立可順暢地從某個媒體來源切換至下一個媒體來源的播放清單。
-   同時播放多個來源的資料流程;例如，從另一個檔案中的影片播放音訊。
-   在連續播放清單專案中，于不同媒體來源的串流之間切換;例如，在每個專案都包含不同的音訊來源時，播放清單可以有共用相同影片來源的專案。

針對播放清單的每個元素，應用程式會建立個別的拓撲。 這些拓撲中的媒體來源稱為 *原生來源*，可區別它們與 sequencer 來源。 在播放期間，整個拓撲順序稱為 *簡報*，而序列內的每個拓撲都稱為 *區段*。

播放是由 [媒體會話](media-session.md)控制，提供傳輸控制項，例如播放、暫停和停止。 媒體會話也會管理展示時間，並將事件傳送至應用程式。 從 sequencer 來源 (事件會透過媒體會話轉送至應用程式。 ) 

若要建立播放清單，應用程式會建立一或多個播放拓撲，並以所需的播放順序將它們排入 sequencer 來源上。 就內部而言，sequencer 來源會修改拓撲，使來源節點指向 sequencer 來源，而不是原生來源。 應用程式會將這些修改過的拓撲（而不是原始的拓撲）傳送至媒體會話。 這可讓 sequencer 來源匯總原生來源，以及與媒體會話進行通訊。

若要在區段之間達成無縫轉換，sequencer 來源會 prerolls 每個區段。 當一個區段現正播放，而且在開始播放下列區段之前，sequencer 來源會引發包含展示描述項的 [MENewPresentation](menewpresentation.md) 事件。 應用程式會使用這個展示描述項來取得簡報中下一個區段的拓撲，並將拓撲排入媒體會話上的佇列。

下圖顯示透過 sequencer 來源的播放清單專案的資料流程。 應用程式會使用來源解析程式來建立原生來源、為每個區段建立拓撲，以及將拓撲排入 sequencer 來源上的佇列。

![顯示 imfmediasession、imfsequencersource 和播放清單區段之資料流程的圖表，這些區段會導致 imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何建立播放清單](how-to-create-a-playlist.md)
</dt> <dt>

[拓撲](topologies.md)
</dt> <dt>

[使用 Sequencer 來源](using-the-sequencer-source.md)
</dt> <dt>

[Sequencer 來源](sequencer-source.md)
</dt> </dl>

 

 



