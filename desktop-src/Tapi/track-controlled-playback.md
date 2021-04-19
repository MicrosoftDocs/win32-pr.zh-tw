---
description: 以下是針對追蹤控制播放執行的步驟。
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Track-Controlled 播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc657f0d301097edd280c358a34daafa83ef356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988849"
---
# <a name="track-controlled-playback"></a><span data-ttu-id="2a379-103">Track-Controlled 播放</span><span class="sxs-lookup"><span data-stu-id="2a379-103">Track-Controlled Playback</span></span>

<span data-ttu-id="2a379-104">若要執行追蹤控制播放，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="2a379-104">To perform track-controlled playback, do the following:</span></span>

-   <span data-ttu-id="2a379-105">選取 [追蹤終端機到資料流程]。</span><span class="sxs-lookup"><span data-stu-id="2a379-105">Select the Track Terminals onto streams.</span></span>
-   <span data-ttu-id="2a379-106">建立檔案播放終端機。</span><span class="sxs-lookup"><span data-stu-id="2a379-106">Create the File Playback Terminal.</span></span>
-   <span data-ttu-id="2a379-107">設定屬性：儲存的檔案名和類型。</span><span class="sxs-lookup"><span data-stu-id="2a379-107">Set properties—file name and type of storage.</span></span>
-   <span data-ttu-id="2a379-108">在檔案播放終端機上使用方法，以列舉檔案追蹤終端機。</span><span class="sxs-lookup"><span data-stu-id="2a379-108">Using a method on the File Playback Terminal, enumerate File Track Terminals.</span></span>
-   <span data-ttu-id="2a379-109">列舉 TAPI 呼叫上的資料流程。</span><span class="sxs-lookup"><span data-stu-id="2a379-109">Enumerate streams on the TAPI call.</span></span>
-   <span data-ttu-id="2a379-110">選取串流上的檔案追蹤終端機。</span><span class="sxs-lookup"><span data-stu-id="2a379-110">Select the File Track Terminal on the stream.</span></span>
-   <span data-ttu-id="2a379-111">在檔案播放終端機上呼叫 [**start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) 方法，開始將記錄的資料播放至 TAPI 串流。</span><span class="sxs-lookup"><span data-stu-id="2a379-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of recorded data to the TAPI streams.</span></span>

 

 



