---
description: 檔案播放終端機和檔案記錄終端機會公開 ITTerminal 和 ITMultiTrackTerminal 介面。 這些物件也會公開 ITMediaControl 介面，以提供停止、啟動和媒體流覽的方法。
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: 檔案播放終端機和檔案記錄終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944212"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>檔案播放終端機和檔案記錄終端機

檔案播放終端機和檔案記錄終端機會公開 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 和 [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) 介面。 這些物件也會公開 [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) 介面，以提供停止、啟動和媒體流覽的方法。

檔案播放終端機會公開具有播放特定方法的 [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) 介面。

檔案記錄終端機會公開 [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) 介面，以提供錄音特定的方法。

在 [multitrack 的終端](multitrack-terminals.md)機中，檔案記錄終端機和檔案播放終端機都會管理 [追蹤終端](track-terminals.md)機的集合。

 

 
