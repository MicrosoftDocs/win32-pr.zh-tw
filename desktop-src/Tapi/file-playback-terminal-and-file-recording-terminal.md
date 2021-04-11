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
# <a name="file-playback-terminal-and-file-recording-terminal"></a><span data-ttu-id="d031f-104">檔案播放終端機和檔案記錄終端機</span><span class="sxs-lookup"><span data-stu-id="d031f-104">File Playback Terminal and File Recording Terminal</span></span>

<span data-ttu-id="d031f-105">檔案播放終端機和檔案記錄終端機會公開 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 和 [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) 介面。</span><span class="sxs-lookup"><span data-stu-id="d031f-105">The File Playback Terminal and File Recording Terminal expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) and [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interfaces.</span></span> <span data-ttu-id="d031f-106">這些物件也會公開 [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) 介面，以提供停止、啟動和媒體流覽的方法。</span><span class="sxs-lookup"><span data-stu-id="d031f-106">These objects also expose the [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) interface, which provides methods for stopping, starting, and media navigation.</span></span>

<span data-ttu-id="d031f-107">檔案播放終端機會公開具有播放特定方法的 [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) 介面。</span><span class="sxs-lookup"><span data-stu-id="d031f-107">The File Playback Terminal exposes the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface, which has playback-specific methods.</span></span>

<span data-ttu-id="d031f-108">檔案記錄終端機會公開 [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) 介面，以提供錄音特定的方法。</span><span class="sxs-lookup"><span data-stu-id="d031f-108">The File Recording Terminal exposes the [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) interface, which provides recording-specific methods.</span></span>

<span data-ttu-id="d031f-109">在 [multitrack 的終端](multitrack-terminals.md)機中，檔案記錄終端機和檔案播放終端機都會管理 [追蹤終端](track-terminals.md)機的集合。</span><span class="sxs-lookup"><span data-stu-id="d031f-109">As [multitrack terminals](multitrack-terminals.md), File Recording Terminal and File Playback Terminal each manage a collection of [track terminals](track-terminals.md).</span></span>

 

 
