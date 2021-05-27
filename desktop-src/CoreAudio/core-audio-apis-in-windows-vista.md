---
description: 核心音訊 Api
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: 核心音訊 Api
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 2cabb462d13786c874401394fa814484f79b0e3b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548953"
---
# <a name="core-audio-apis"></a><span data-ttu-id="b3d8c-103">核心音訊 Api</span><span class="sxs-lookup"><span data-stu-id="b3d8c-103">Core Audio APIs</span></span>

> [!NOTE]
> <span data-ttu-id="b3d8c-104">如需程式碼範例，請參閱 [使用核心音訊 api 的 SDK 範例](./sdk-samples-that-use-the-core-audio-apis.md)。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-104">For code examples, see [SDK samples that use the core audio APIs](./sdk-samples-that-use-the-core-audio-apis.md).</span></span>

<span data-ttu-id="b3d8c-105">本檔提供適用于 Microsoft Windows 系列作業系統的核心音訊應用程式開發介面 (Api) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-105">This documentation provides information about core audio application programming interfaces (APIs) for the Microsoft Windows family of operating systems.</span></span> <span data-ttu-id="b3d8c-106">它提供軟體發展人員在開發使用 Windows Vista 中核心音訊 Api 的應用程式時所遵循的指導方針。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-106">It provides guidelines for software developers to follow in developing applications that use the core audio APIs in Windows Vista.</span></span> <span data-ttu-id="b3d8c-107">這些 Api 是 Windows Vista 中的新功能，不適用於舊版的 Windows。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-107">These APIs were new in Windows Vista and are not available in earlier versions of Windows.</span></span>

<span data-ttu-id="b3d8c-108">核心音訊 Api 提供聲音應用程式存取音訊端點裝置的方法，例如耳機和麥克風。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-108">The core audio APIs provide the means for audio applications to access audio endpoint devices such as headphones and microphones.</span></span> <span data-ttu-id="b3d8c-109">核心音訊 Api 可作為較高層級音訊 Api 的基礎，例如 Microsoft DirectSound 和 Windows 多媒體 **waveXxx** 功能。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-109">The core audio APIs serve as the foundation for higher-level audio APIs such as Microsoft DirectSound and the Windows multimedia **waveXxx** functions.</span></span> <span data-ttu-id="b3d8c-110">大部分的應用程式都會與較高層級的 Api 通訊，但有些具有特殊需求的應用程式可能需要直接與核心音訊 Api 通訊。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-110">Most applications communicate with the higher-level APIs, but some applications with special requirements might need to communicate directly with the core audio APIs.</span></span>

<span data-ttu-id="b3d8c-111">從 Windows 7 開始，已改善現有的 Api，並新增了新的 Api 來支援新案例。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-111">Starting with Windows 7, the existing APIs have been improved and new APIs have been added to support new scenarios.</span></span> <span data-ttu-id="b3d8c-112">串流和會話管理 Api 已經過改良，因此應用程式現在可以對音訊會話進行列舉和擴充控制。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-112">The stream and session management APIs have been improved so that the application can now enumerate and get extended control over the audio session.</span></span> <span data-ttu-id="b3d8c-113">藉由使用新的 Api，應用程式可以執行自訂的串流衰減體驗。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-113">By using the new APIs, the application can implement a custom stream attenuation experience.</span></span> <span data-ttu-id="b3d8c-114">新裝置相關的 Api 可讓您存取端點裝置的驅動程式屬性。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-114">New device-related APIs provide access to the driver properties of the endpoint devices.</span></span>

<span data-ttu-id="b3d8c-115">本檔包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-115">This documentation includes the following sections.</span></span>

| <span data-ttu-id="b3d8c-116">區段</span><span class="sxs-lookup"><span data-stu-id="b3d8c-116">Section</span></span>                                                                    | <span data-ttu-id="b3d8c-117">描述</span><span class="sxs-lookup"><span data-stu-id="b3d8c-117">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b3d8c-118">關於 Windows Core 音訊 Api</span><span class="sxs-lookup"><span data-stu-id="b3d8c-118">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md) | <span data-ttu-id="b3d8c-119">提供 Windows core 音訊 Api 的總覽，並說明基本概念。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-119">Provides an overview of the Windows core audio APIs and describes basic concepts.</span></span> |
| [<span data-ttu-id="b3d8c-120">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="b3d8c-120">Programming Guide</span></span>](programming-guide.md)                                 | <span data-ttu-id="b3d8c-121">描述核心音訊 Api 的主要功能，以及如何使用它們。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-121">Describes the key features of the core audio APIs and how to use them.</span></span>            |
| [<span data-ttu-id="b3d8c-122">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="b3d8c-122">Programming Reference</span></span>](programming-reference.md)                         | <span data-ttu-id="b3d8c-123">提供核心音訊 Api 的 c + + 參考資訊。</span><span class="sxs-lookup"><span data-stu-id="b3d8c-123">Provides C++ reference information for the core audio APIs.</span></span>                       |

## <a name="related-topics"></a><span data-ttu-id="b3d8c-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3d8c-124">Related topics</span></span>

<span data-ttu-id="b3d8c-125">[適用于 Windows 的媒體技術](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b3d8c-125">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>

[<span data-ttu-id="b3d8c-126">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="b3d8c-126">SDK samples that use the core audio APIs</span></span>](./sdk-samples-that-use-the-core-audio-apis.md)