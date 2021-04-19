---
description: Microsoft DVD 導覽器如何選取 DVD 區域
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Microsoft DVD 導覽器如何選取 DVD 區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000036"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a><span data-ttu-id="55956-103">Microsoft DVD 導覽器如何選取 DVD 區域</span><span class="sxs-lookup"><span data-stu-id="55956-103">How Microsoft DVD Navigator Selects the DVD Region</span></span>

<span data-ttu-id="55956-104">當您在電腦上播放 DVD 光碟時，Microsoft DVD 導覽器會使用下列演算法來判斷區域是否相符：</span><span class="sxs-lookup"><span data-stu-id="55956-104">The Microsoft DVD Navigator uses the following algorithm to determine region match while playing DVD discs on a PC:</span></span>

1.  <span data-ttu-id="55956-105">DVD 導覽器會取得光碟區域、磁片磁碟機區域和解碼器區域。</span><span class="sxs-lookup"><span data-stu-id="55956-105">The DVD Navigator gets the disc region, drive region, and decoder region.</span></span>
2.  <span data-ttu-id="55956-106">如果光碟區是「所有區域」，則 DVD 導覽器會播放光碟。</span><span class="sxs-lookup"><span data-stu-id="55956-106">If the disc region is "all regions," the DVD Navigator plays the disc.</span></span>
3.  <span data-ttu-id="55956-107">如果光碟未標示為所有區域，則 DVD 導覽器會檢查解碼器是否有預設的區域。</span><span class="sxs-lookup"><span data-stu-id="55956-107">If the disc is not marked for all regions, the DVD Navigator checks whether the decoder has a preset region.</span></span>
4.  <span data-ttu-id="55956-108">如果此解碼器具有預設的區域，而且不符合光碟區域，則 DVD 導覽器會傳回錯誤，指出無法在目前的 DVD 設定上播放光碟。</span><span class="sxs-lookup"><span data-stu-id="55956-108">If the decoder has a preset region and it does not match the disc region, the DVD Navigator returns an error indicating that it cannot play the disc on the current DVD configuration.</span></span> <span data-ttu-id="55956-109"> (Exit) </span><span class="sxs-lookup"><span data-stu-id="55956-109">(Exit)</span></span>
5.  <span data-ttu-id="55956-110">如果未設定解碼器區域，或與光碟區域相同，則 DVD 導覽器會檢查磁片磁碟機區域是否與光碟區域相同。</span><span class="sxs-lookup"><span data-stu-id="55956-110">If the decoder region is not set, or is the same as the disc region, the DVD Navigator checks whether the drive region is the same as the disc region.</span></span>
6.  <span data-ttu-id="55956-111">如果磁片磁碟機區域符合光碟區域，則 DVD 導覽器會播放標題。</span><span class="sxs-lookup"><span data-stu-id="55956-111">If the drive region matches the disc region, the DVD Navigator plays the title.</span></span>
7.  <span data-ttu-id="55956-112">否則，如果驅動程式區域不符合光碟區域，DVD 導覽器會叫用程式碼來變更磁片磁碟機的區域。</span><span class="sxs-lookup"><span data-stu-id="55956-112">Otherwise, if the driver region does not match the disc region, the DVD Navigator invokes the code to change the drive's region.</span></span> <span data-ttu-id="55956-113">如果允許的區域變更數目已用盡，區域變更嘗試就會失敗，而且無法在該系統上播放標題。</span><span class="sxs-lookup"><span data-stu-id="55956-113">If the allowed number of region changes has been exhausted, the region change attempt fails and the title cannot be played on that system.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55956-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="55956-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55956-115">Windows 中的 DVD 區域變更支援</span><span class="sxs-lookup"><span data-stu-id="55956-115">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



