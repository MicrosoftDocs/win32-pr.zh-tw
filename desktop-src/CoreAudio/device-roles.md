---
description: 裝置角色
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: 裝置角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110785"
---
# <a name="device-roles"></a><span data-ttu-id="16387-103">裝置角色</span><span class="sxs-lookup"><span data-stu-id="16387-103">Device Roles</span></span>

<span data-ttu-id="16387-104">如果系統包含兩個以上的音訊轉譯端點裝置，則一部裝置最適合用來播放一種音訊內容，而另一部裝置可能最適合用來播放另一種類型的內容。</span><span class="sxs-lookup"><span data-stu-id="16387-104">If a system contains two or more audio-rendering endpoint devices, then one device might be best for playing one type of audio content, and another device might be best for playing another type of content.</span></span> <span data-ttu-id="16387-105">例如，如果系統有兩個轉譯裝置，則使用者可能會選擇在一部裝置上播放音樂，並在另一部裝置上播放系統通知聲音。</span><span class="sxs-lookup"><span data-stu-id="16387-105">For example, if a system has two rendering devices, the user might choose to play music on one device and to play system notification sounds on the other.</span></span>

<span data-ttu-id="16387-106">同樣地，如果系統包含兩個或多個音訊捕獲端點裝置，則一部裝置最適合用來捕捉一種類型的音訊內容，而另一部裝置可能最適合用來捕捉另一種類型的內容。</span><span class="sxs-lookup"><span data-stu-id="16387-106">Similarly, if a system contains two or more audio-capture endpoint devices, then one device might be best for capturing one type of audio content, and another device might be best for capturing another type of content.</span></span> <span data-ttu-id="16387-107">例如，如果系統有兩部捕獲裝置，則使用者可能會選擇在一部裝置上錄製即時音樂，以及使用其他裝置來進行語音命令。</span><span class="sxs-lookup"><span data-stu-id="16387-107">For example, if a system has two capture devices, the user might choose to record live music on one device and to use the other device for voice commands.</span></span>

<span data-ttu-id="16387-108">裝置可以有三個角色：主控台、通訊和多媒體。下表說明 [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) 列舉中的三個常數（EConsole、ECommunications 和 eMultimedia）所識別的裝置角色。</span><span class="sxs-lookup"><span data-stu-id="16387-108">Devices can have three roles: Console, Communications, and Multimedia.The following table describes the device roles identified by the three constants—eConsole, eCommunications, and eMultimedia—in the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>



| <span data-ttu-id="16387-109">ERole 常數</span><span class="sxs-lookup"><span data-stu-id="16387-109">ERole constant</span></span>  | <span data-ttu-id="16387-110">裝置角色</span><span class="sxs-lookup"><span data-stu-id="16387-110">Device role</span></span>                              | <span data-ttu-id="16387-111">轉譯範例</span><span class="sxs-lookup"><span data-stu-id="16387-111">Rendering examples</span></span>             | <span data-ttu-id="16387-112">Capture 範例</span><span class="sxs-lookup"><span data-stu-id="16387-112">Capture examples</span></span>                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| <span data-ttu-id="16387-113">eConsole</span><span class="sxs-lookup"><span data-stu-id="16387-113">eConsole</span></span>        | <span data-ttu-id="16387-114">與電腦的互動</span><span class="sxs-lookup"><span data-stu-id="16387-114">Interaction with the computer</span></span>            | <span data-ttu-id="16387-115">遊戲和系統通知</span><span class="sxs-lookup"><span data-stu-id="16387-115">Games and system notifications</span></span> | <span data-ttu-id="16387-116">語音命令</span><span class="sxs-lookup"><span data-stu-id="16387-116">Voice commands</span></span>                     |
| <span data-ttu-id="16387-117">eCommunications</span><span class="sxs-lookup"><span data-stu-id="16387-117">eCommunications</span></span> | <span data-ttu-id="16387-118">與其他人交流語音</span><span class="sxs-lookup"><span data-stu-id="16387-118">Voice communications with another person</span></span> | <span data-ttu-id="16387-119">聊天與 VoIP</span><span class="sxs-lookup"><span data-stu-id="16387-119">Chat and VoIP</span></span>                  | <span data-ttu-id="16387-120">聊天與 VoIP</span><span class="sxs-lookup"><span data-stu-id="16387-120">Chat and VoIP</span></span>                      |
| <span data-ttu-id="16387-121">eMultimedia</span><span class="sxs-lookup"><span data-stu-id="16387-121">eMultimedia</span></span>     | <span data-ttu-id="16387-122">播放或錄製音訊內容</span><span class="sxs-lookup"><span data-stu-id="16387-122">Playing or recording audio content</span></span>       | <span data-ttu-id="16387-123">音樂和電影</span><span class="sxs-lookup"><span data-stu-id="16387-123">Music and movies</span></span>               | <span data-ttu-id="16387-124">旁白和即時音樂錄製</span><span class="sxs-lookup"><span data-stu-id="16387-124">Narration and live music recording</span></span> |



 

<span data-ttu-id="16387-125">特定的轉譯或捕獲裝置可能指派給上表中的「無」、「一個」、「部分」或「所有」角色。</span><span class="sxs-lookup"><span data-stu-id="16387-125">A particular rendering or capture device might be assigned none, one, some, or all of the roles in the preceding table.</span></span> <span data-ttu-id="16387-126">在任何時候，資料表中的每個角色都會指派給一個 (，只有一個) 轉譯裝置和一個 (，而只有一個) capture 裝置。</span><span class="sxs-lookup"><span data-stu-id="16387-126">At any time, each role in the table is assigned to one (and only one) rendering device and to one (and only one) capture device.</span></span> <span data-ttu-id="16387-127">亦即，將角色指派給轉譯裝置的方式，與用來捕獲裝置的角色指派無關。</span><span class="sxs-lookup"><span data-stu-id="16387-127">That is, the assignment of roles to rendering devices is independent of the assignment of roles to capture devices.</span></span>

<span data-ttu-id="16387-128">應用程式可能會選擇透過單一轉譯端點裝置來播放其所有輸出資料流程，並從單一的捕獲端點裝置記錄其所有輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="16387-128">An application might choose to play all of its output streams through a single rendering endpoint device, and to record all of its input streams from a single capture endpoint device.</span></span> <span data-ttu-id="16387-129">或者，應用程式可能會選擇透過一個轉譯裝置來播放其輸出資料流程，並透過其他轉譯裝置播放其他輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="16387-129">Alternatively, an application might choose to play some of its output streams through one rendering device and to play other output streams through another rendering device.</span></span> <span data-ttu-id="16387-130">同樣地，它可能會選擇透過一個捕獲裝置來記錄部分輸入資料流程，並透過其他捕獲裝置來記錄其他輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="16387-130">Similarly, it might choose to record some of its input streams through one capture device and to record other input streams through another capture device.</span></span> <span data-ttu-id="16387-131">在所有情況下，應用程式可以將每個串流指派給其角色最適合該串流的裝置。</span><span class="sxs-lookup"><span data-stu-id="16387-131">In all cases, the application can assign each stream to the device whose role is most appropriate for that stream.</span></span>

<span data-ttu-id="16387-132">例如，VoIP 應用程式可能會將包含環形通知的輸出資料流程，指派給呈現端點裝置（具有 eConsole 角色）。</span><span class="sxs-lookup"><span data-stu-id="16387-132">For example, a VoIP application might assign the output stream that contains the ring-in notification to the rendering endpoint device with the eConsole role.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16387-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="16387-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16387-134">音訊端點裝置</span><span class="sxs-lookup"><span data-stu-id="16387-134">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="16387-135">使用裝置角色</span><span class="sxs-lookup"><span data-stu-id="16387-135">Working with Device Roles</span></span>](device-roles-in-windows-vista.md)
</dt> <dt>

[<span data-ttu-id="16387-136">與舊版音訊 Api 的互通性</span><span class="sxs-lookup"><span data-stu-id="16387-136">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



