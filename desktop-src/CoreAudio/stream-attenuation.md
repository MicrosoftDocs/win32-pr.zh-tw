---
description: 預設回避體驗
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: 預設回避體驗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688943"
---
# <a name="default-ducking-experience"></a><span data-ttu-id="67b37-103">預設回避體驗</span><span class="sxs-lookup"><span data-stu-id="67b37-103">Default Ducking Experience</span></span>

<span data-ttu-id="67b37-104">假設使用者在接聽電腦上的音樂時收到通話。</span><span class="sxs-lookup"><span data-stu-id="67b37-104">Consider a scenario where a user receives a phone call while listening to music on the computer.</span></span> <span data-ttu-id="67b37-105">在通話期間，使用者想要在接聽通話時減少音樂的音量等級，並在通話結束後繼續原始音量。</span><span class="sxs-lookup"><span data-stu-id="67b37-105">During the phone call, the user wants to reduce the volume level of the music while attending to the phone call, and resume the original volume after the phone call has ended.</span></span> <span data-ttu-id="67b37-106">視使用者 **在 [音效** ] 控制台中指定的選項而定，作業系統會自動透過 *回避* 或 *串流衰減* 來提供此功能—減少音訊串流的強度。</span><span class="sxs-lookup"><span data-stu-id="67b37-106">Depending on the options specified by the user in the **Sounds** control panel, the operating system automatically provides this functionality through *ducking* or *stream attenuation*—reduction in the intensity of an audio stream.</span></span>

<span data-ttu-id="67b37-107">預設衰減體驗取決於使用者的喜好設定，如 [控制台] 的 [ **音效** ] 選項中所指定。</span><span class="sxs-lookup"><span data-stu-id="67b37-107">The default attenuation experience depends on the user's preference, as specified in the control panel's **Sound** option.</span></span> <span data-ttu-id="67b37-108">在 [ **通訊** ] 索引標籤上，使用者可以選擇衰減層級 (預設值為 80% ) 、將所有非通訊串流靜音，或停用預設的串流衰減體驗。</span><span class="sxs-lookup"><span data-stu-id="67b37-108">On the **Communications** tab, the user can choose an attenuation level (default value is 80%), mute all non-communication streams, or disable the default stream attenuation experience.</span></span> <span data-ttu-id="67b37-109">系統允許新的非通訊資料流程 (但新的系統音效) 在通訊會話期間開啟，但不會自動衰減新的資料流程。</span><span class="sxs-lookup"><span data-stu-id="67b37-109">The system allows new non-communication streams (except for new system sounds) to be opened during the communication session but the new streams are not automatically attenuated.</span></span> <span data-ttu-id="67b37-110">當所有的通訊資料流程都關閉時，系統會結束通訊會話，並還原在通訊會話期間衰減的資料流量。</span><span class="sxs-lookup"><span data-stu-id="67b37-110">When all of the communication streams are closed, the system ends the communication session and restores the volume of the streams that were attenuated during the communication session.</span></span>

<span data-ttu-id="67b37-111">為了以視覺化方式指出資料流程衰減，系統會根據使用者的喜好設定來變更磁片區混音器設定。</span><span class="sxs-lookup"><span data-stu-id="67b37-111">To indicate stream attenuation visually, the system changes the volume mixer settings depending on the user's preference.</span></span> <span data-ttu-id="67b37-112">例如，如果使用者指定衰減層級，磁片區混音器會減少滑杆、顯示新的衰減磁片區，並顯示原始的音量層級。</span><span class="sxs-lookup"><span data-stu-id="67b37-112">For example, if the user specifies an attenuation level, the volume mixer lowers the slider, displays the new attenuated volume, and displays the original volume level.</span></span> <span data-ttu-id="67b37-113">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="67b37-113">The following image illustrates this process.</span></span>

![windows 7 中所提供之預設資料流程衰減行為的圖表](images/stream-aatenuation.jpg)

<span data-ttu-id="67b37-115">如果應用程式知道通訊會話的開始和結束時間，則應用程式可以覆寫資料流程衰減並執行自訂回避體驗。</span><span class="sxs-lookup"><span data-stu-id="67b37-115">An application can override stream attenuation and implement a custom ducking experience if it knows when the communication session starts and ends.</span></span> <span data-ttu-id="67b37-116">如需詳細資訊，請參閱 [提供自訂回避行為](providing-a-custom-ducking-experience.md)。</span><span class="sxs-lookup"><span data-stu-id="67b37-116">For more information, see [Providing a Custom Ducking Behavior](providing-a-custom-ducking-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67b37-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="67b37-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67b37-118">使用通訊裝置</span><span class="sxs-lookup"><span data-stu-id="67b37-118">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="67b37-119">停用預設的回避體驗</span><span class="sxs-lookup"><span data-stu-id="67b37-119">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="67b37-120">提供自訂回避行為</span><span class="sxs-lookup"><span data-stu-id="67b37-120">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="67b37-121">回避通知的執行考慮</span><span class="sxs-lookup"><span data-stu-id="67b37-121">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="67b37-122">取得回避事件</span><span class="sxs-lookup"><span data-stu-id="67b37-122">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



