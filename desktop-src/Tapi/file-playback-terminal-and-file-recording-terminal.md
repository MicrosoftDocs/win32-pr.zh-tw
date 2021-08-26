---
description: 檔案播放終端機和檔案記錄終端機會公開 ITTerminal 和 ITMultiTrackTerminal 介面。 這些物件也會公開 ITMediaControl 介面，以提供停止、啟動和媒體流覽的方法。
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: 檔案播放終端機和檔案記錄終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad07ea46e2abf13465ac3344e69f586673c3b29463eac8bdd324966fb838368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100588"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>檔案播放終端機和檔案記錄終端機

檔案播放終端機和檔案記錄終端機會公開 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 和 [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) 介面。 這些物件也會公開 [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) 介面，以提供停止、啟動和媒體流覽的方法。

檔案播放終端機會公開具有播放特定方法的 [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) 介面。

檔案記錄終端機會公開 [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) 介面，以提供錄音特定的方法。

在 [multitrack 的終端](multitrack-terminals.md)機中，檔案記錄終端機和檔案播放終端機都會管理 [追蹤終端](track-terminals.md)機的集合。

 

 
