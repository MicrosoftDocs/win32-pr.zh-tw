---
description: 本主題提供執行播放軌之音訊串流錄製的程式。
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled 記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849576"
---
# <a name="track-controlled-record"></a><span data-ttu-id="ec8fb-103">Track-Controlled 記錄</span><span class="sxs-lookup"><span data-stu-id="ec8fb-103">Track-Controlled Record</span></span>

<span data-ttu-id="ec8fb-104">本主題提供執行播放軌之音訊串流錄製的程式。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-104">This topic provides a procedure for performing track-controlled recording of audio streams.</span></span>

<span data-ttu-id="ec8fb-105">**執行播放軌控制的音訊串流錄製**</span><span class="sxs-lookup"><span data-stu-id="ec8fb-105">**To perform track-controlled recording of audio streams**</span></span>

1.  <span data-ttu-id="ec8fb-106">選取 [檔案追蹤] 終端機至資料流程。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-106">Select File Track Terminals onto streams.</span></span>
2.  <span data-ttu-id="ec8fb-107">建立檔案記錄終端機。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-107">Create the File Record Terminal.</span></span>
3.  <span data-ttu-id="ec8fb-108">設定檔案名。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-108">Set the file name.</span></span>
4.  <span data-ttu-id="ec8fb-109">列舉 TAPI 呼叫上的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-109">Enumerate streams on the TAPI call.</span></span> <span data-ttu-id="ec8fb-110">如需這些步驟，請參閱下列程式。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-110">For these steps, see the following procedure.</span></span>
5.  <span data-ttu-id="ec8fb-111">在檔案記錄終端機上呼叫 [**start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) 方法，以啟動串流記錄。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Record Terminal to start stream recording.</span></span>

<span data-ttu-id="ec8fb-112">**列舉 TAPI 呼叫上的資料流程**</span><span class="sxs-lookup"><span data-stu-id="ec8fb-112">**To enumerate streams on the TAPI call**</span></span>

1.  <span data-ttu-id="ec8fb-113">建立與資料流程相同之音訊類型和方向的軌跡。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-113">Create a track of the same audio type and direction as the stream.</span></span>
2.  <span data-ttu-id="ec8fb-114">設定音訊格式的追蹤屬性。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-114">Set the track properties for audio format.</span></span> <span data-ttu-id="ec8fb-115">如果未設定，格式將會與資料流程格式相同。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-115">If not set, the format will be the same as the streams format.</span></span>
3.  <span data-ttu-id="ec8fb-116">選取資料流程上的曲目。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-116">Select the track on the stream.</span></span>

<span data-ttu-id="ec8fb-117">如果在多個資料流程上選取了一個追蹤，這表示混合的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ec8fb-117">If one track is selected on multiple streams, this implies mixing streams.</span></span>

 

 



