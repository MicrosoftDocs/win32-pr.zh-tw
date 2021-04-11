---
description: 檔案終端機可以用兩種方式來使用。
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: 使用檔案終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115809"
---
# <a name="using-file-terminals"></a>使用檔案終端機

檔案終端機可以用兩種方式來使用。 最簡單的方法是使用 [**ITBasicCallControl2：： SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) 來選取檔案終端機 (播放或記錄) 至 TAPI 呼叫物件。 在此情況下，TAPI 會負責將音訊串流連接至追蹤終端機。

第二種方法可讓應用程式更精確地控制要追蹤的音訊串流。 在此案例中，應用程式會列舉呼叫所提供的資料流程、挑選想要錄製的資料流程 (或用於播放) 、建立 (或尋找播放) 檔案終端機上的對應播放程式，並選取呼叫串流上的曲目。

如需詳細資訊，請參閱下列主題：

-   [簡單播放](simple-playback.md)
-   [追蹤控制播放](track-controlled-playback.md)
-   [簡單記錄](simple-record.md)
-   [追蹤控制記錄](track-controlled-record.md)

 

 



