---
description: 程式設計手冊
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: 核心音訊程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb99369058983ebac7205053efdf967bbb8c36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191008"
---
# <a name="core-audio-programming-guide"></a><span data-ttu-id="e745d-103">核心音訊程式設計指南</span><span class="sxs-lookup"><span data-stu-id="e745d-103">Core Audio Programming Guide</span></span>

<span data-ttu-id="e745d-104">本指南一節將說明 Windows Vista 核心音訊 Api 的概念和功能，並說明如何在應用程式設計中使用它們。</span><span class="sxs-lookup"><span data-stu-id="e745d-104">This guide section explains the concepts and features of the core audio APIs of Windows Vista, and describes how to use them in application programming.</span></span>

<span data-ttu-id="e745d-105">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="e745d-105">This section contains the following topics.</span></span>



| <span data-ttu-id="e745d-106">主題</span><span class="sxs-lookup"><span data-stu-id="e745d-106">Topic</span></span>                                                                                                                      | <span data-ttu-id="e745d-107">描述</span><span class="sxs-lookup"><span data-stu-id="e745d-107">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e745d-108">使用者模式音訊元件</span><span class="sxs-lookup"><span data-stu-id="e745d-108">User-Mode Audio Components</span></span>](user-mode-audio-components.md)                                                               | <span data-ttu-id="e745d-109">透過核心音訊 Api 中的低層級介面，用戶端可以存取管理和混合音訊串流的系統元件。</span><span class="sxs-lookup"><span data-stu-id="e745d-109">Through the low-level interfaces in the core audio APIs, a client can access the system components that manage and mix audio streams.</span></span>                                                                        |
| [<span data-ttu-id="e745d-110">受保護的使用者模式音訊 (PUMA) </span><span class="sxs-lookup"><span data-stu-id="e745d-110">Protected User Mode Audio (PUMA)</span></span>](protected-user-mode-audio--puma-.md)                                                   | <span data-ttu-id="e745d-111">描述受保護使用者模式音訊 (PUMA) 的更新，此為受保護環境中的使用者模式音訊引擎 (PE) ，可提供更安全的音訊處理和轉譯環境。</span><span class="sxs-lookup"><span data-stu-id="e745d-111">Describes the updates to Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE), which provides a safer environment for audio processing and rendering.</span></span>              |
| [<span data-ttu-id="e745d-112">音訊端點裝置</span><span class="sxs-lookup"><span data-stu-id="e745d-112">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)                                                                       | <span data-ttu-id="e745d-113">音訊端點裝置是一種軟體抽象概念，可讓使用者輕鬆地與音訊裝置（例如麥克風和喇叭）互動。</span><span class="sxs-lookup"><span data-stu-id="e745d-113">An audio endpoint device is a software abstraction that enables user-friendly interactions with audio devices such as microphones and speakers.</span></span>                                                              |
| [<span data-ttu-id="e745d-114">音訊會話</span><span class="sxs-lookup"><span data-stu-id="e745d-114">Audio Sessions</span></span>](audio-sessions.md)                                                                                       | <span data-ttu-id="e745d-115">音訊會話是一種軟體抽象概念，可讓用戶端將相關音訊串流的集合當作單一單位來管理。</span><span class="sxs-lookup"><span data-stu-id="e745d-115">An audio session is a software abstraction that enables a client to manage a collection of related audio streams as a single unit.</span></span>                                                                           |
| [<span data-ttu-id="e745d-116">音量控制項</span><span class="sxs-lookup"><span data-stu-id="e745d-116">Volume Controls</span></span>](volume-controls.md)                                                                                     | <span data-ttu-id="e745d-117">系統會以邏輯一致的方式，將其以原則為基礎的磁片區設定與使用者的磁片區設定整合。</span><span class="sxs-lookup"><span data-stu-id="e745d-117">The system integrates its policy-based volume settings with the user's volume settings in a logical and consistent way.</span></span>                                                                                      |
| [<span data-ttu-id="e745d-118">串流管理</span><span class="sxs-lookup"><span data-stu-id="e745d-118">Stream Management</span></span>](stream-management.md)                                                                                 | <span data-ttu-id="e745d-119">Windows 音訊會話 API (WASAPI) 提供用戶端一組完整的方法來建立和管理音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e745d-119">The Windows Audio Session API (WASAPI) provides a client with a complete set of methods for creating and managing audio streams.</span></span>                                                                             |
| [<span data-ttu-id="e745d-120">裝置拓撲</span><span class="sxs-lookup"><span data-stu-id="e745d-120">Device Topologies</span></span>](device-topologies.md)                                                                                 | <span data-ttu-id="e745d-121">DeviceTopology API 可讓用戶端探索音訊硬體中不同資料路徑的音訊控制項。</span><span class="sxs-lookup"><span data-stu-id="e745d-121">The DeviceTopology API enables a client to discover the audio controls that lie along the various data paths in the audio hardware.</span></span>                                                                          |
| [<span data-ttu-id="e745d-122">使用 IKsControl 介面存取音訊屬性</span><span class="sxs-lookup"><span data-stu-id="e745d-122">Using the IKsControl Interface to Access Audio Properties</span></span>](using-the-ikscontrol-interface-to-access-audio-properties.md) | <span data-ttu-id="e745d-123">特製化的音訊應用程式可能需要使用 IKsControl 介面來存取音訊介面卡的屬性。</span><span class="sxs-lookup"><span data-stu-id="e745d-123">A specialized audio application might need to use the IKsControl interface to access the properties of an audio adapter.</span></span>                                                                                     |
| [<span data-ttu-id="e745d-124">與舊版音訊 Api 的互通性</span><span class="sxs-lookup"><span data-stu-id="e745d-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)                                     | <span data-ttu-id="e745d-125">Windows Vista 中核心音訊 Api 的主要功能，可以併入使用 DirectSound、DirectShow 和 Windows 多媒體 **waveOutXxx** 和 **waveInXxx** 功能的現有應用程式中。</span><span class="sxs-lookup"><span data-stu-id="e745d-125">Key features of the core audio APIs in Windows Vista can be incorporated into existing applications that use DirectSound, DirectShow, and the Windows multimedia **waveOutXxx** and **waveInXxx** functions.</span></span> |
| [<span data-ttu-id="e745d-126">空間音效</span><span class="sxs-lookup"><span data-stu-id="e745d-126">Spatial Sound</span></span>](spatial-sound.md)                                                                                         | <span data-ttu-id="e745d-127">針對 Xbox 和 Windows 上的空間音效支援，提供使用 Windows Sonic （Microsoft 的平台層級解決方案）的指導方針，在接聽程式) 音訊提示的上方或下方啟用環繞和提高許可權 (。</span><span class="sxs-lookup"><span data-stu-id="e745d-127">Provides guidance for using Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, enabling both surround and elevation (above or below the listener) audio cues.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e745d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="e745d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e745d-129">核心音訊 Api</span><span class="sxs-lookup"><span data-stu-id="e745d-129">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



