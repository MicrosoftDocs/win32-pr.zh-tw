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
# <a name="using-file-terminals"></a><span data-ttu-id="9cae2-103">使用檔案終端機</span><span class="sxs-lookup"><span data-stu-id="9cae2-103">Using File Terminals</span></span>

<span data-ttu-id="9cae2-104">檔案終端機可以用兩種方式來使用。</span><span class="sxs-lookup"><span data-stu-id="9cae2-104">The file terminals can be used in two ways.</span></span> <span data-ttu-id="9cae2-105">最簡單的方法是使用 [**ITBasicCallControl2：： SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) 來選取檔案終端機 (播放或記錄) 至 TAPI 呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="9cae2-105">The simplest method is to use [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) to select a file terminal (playback or record) onto a TAPI call object.</span></span> <span data-ttu-id="9cae2-106">在此情況下，TAPI 會負責將音訊串流連接至追蹤終端機。</span><span class="sxs-lookup"><span data-stu-id="9cae2-106">In this case TAPI takes care of connecting the audio streams to the track terminals.</span></span>

<span data-ttu-id="9cae2-107">第二種方法可讓應用程式更精確地控制要追蹤的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="9cae2-107">The second method allows an application to have finer control over the mapping of audio streams to tracks.</span></span> <span data-ttu-id="9cae2-108">在此案例中，應用程式會列舉呼叫所提供的資料流程、挑選想要錄製的資料流程 (或用於播放) 、建立 (或尋找播放) 檔案終端機上的對應播放程式，並選取呼叫串流上的曲目。</span><span class="sxs-lookup"><span data-stu-id="9cae2-108">In this scenario, the application enumerates the streams available on the call, picks the ones it wants to record (or use for playback), creates (or finds for playback) the corresponding tracks on the file terminal, and selects the tracks on call streams.</span></span>

<span data-ttu-id="9cae2-109">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9cae2-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9cae2-110">簡單播放</span><span class="sxs-lookup"><span data-stu-id="9cae2-110">Simple Playback</span></span>](simple-playback.md)
-   [<span data-ttu-id="9cae2-111">追蹤控制播放</span><span class="sxs-lookup"><span data-stu-id="9cae2-111">Track-Controlled Playback</span></span>](track-controlled-playback.md)
-   [<span data-ttu-id="9cae2-112">簡單記錄</span><span class="sxs-lookup"><span data-stu-id="9cae2-112">Simple Record</span></span>](simple-record.md)
-   [<span data-ttu-id="9cae2-113">追蹤控制記錄</span><span class="sxs-lookup"><span data-stu-id="9cae2-113">Track-Controlled Record</span></span>](track-controlled-record.md)

 

 



