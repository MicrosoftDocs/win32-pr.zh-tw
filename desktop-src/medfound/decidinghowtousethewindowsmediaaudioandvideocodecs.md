---
description: 使用編解碼器和 DSP 物件
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: 使用編解碼器和 DSP 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981741"
---
# <a name="using-the-codec-and-dsp-objects"></a><span data-ttu-id="a705d-103">使用編解碼器和 DSP 物件</span><span class="sxs-lookup"><span data-stu-id="a705d-103">Using the Codec and DSP Objects</span></span>

<span data-ttu-id="a705d-104">有幾種方式可使用 Windows Media 音訊和影片編解碼器和 Dsp 來編碼、解碼或轉換您的數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="a705d-104">There are several ways to use the Windows Media Audio and Video codecs and DSPs to encode, decode, or transform your digital media content.</span></span> <span data-ttu-id="a705d-105">Windows Media 音訊和影片編解碼器和 DSP API 適用于需要手動設定編解碼器和 DSP 物件的使用者，或在 Windows Media Sdk （例如 Windows Media Format SDK 或媒體基礎 SDK）之外的內容之外使用它們。</span><span class="sxs-lookup"><span data-stu-id="a705d-105">The Windows Media Audio and Video Codec and DSP API is intended for those users who need to configure codec and DSP objects manually or use them outside of the context one of the Windows Media SDKs, such as the Windows Media Format SDK or Media Foundation SDK.</span></span>

<span data-ttu-id="a705d-106">內容建立者和終端使用者可以使用各種工具和應用程式來編碼 Windows Media 音訊或 Windows Media 視訊串流中的內容。</span><span class="sxs-lookup"><span data-stu-id="a705d-106">Content creators and end users can use a variety of tools and applications to encode content in Windows Media Audio or Windows Media Video streams.</span></span> <span data-ttu-id="a705d-107">例如，Windows Media 編碼器的設計目的是要讓編碼程式更簡單。</span><span class="sxs-lookup"><span data-stu-id="a705d-107">Windows Media Encoder, for example, is specifically designed to make the encoding process easy.</span></span> <span data-ttu-id="a705d-108">同樣地，Windows Media Player 是特別設計來與以 Windows Media 格式編碼的數位媒體資料搭配運作。</span><span class="sxs-lookup"><span data-stu-id="a705d-108">Likewise, Windows Media Player is specially designed to work well with digital media data that is encoded in Windows Media formats.</span></span> <span data-ttu-id="a705d-109">針對許多應用程式，使用 Windows Media 編碼器 SDK 或 Windows Media Player SDK 都是必要的。</span><span class="sxs-lookup"><span data-stu-id="a705d-109">For many applications, using the Windows Media Encoder SDK or the Windows Media Player SDK is all that is needed.</span></span> <span data-ttu-id="a705d-110">特別是，這兩項技術適用于類似其自動化工具功能的案例。</span><span class="sxs-lookup"><span data-stu-id="a705d-110">In particular, these two technologies are good for scenarios that resemble the functionality of the tools they automate.</span></span>

<span data-ttu-id="a705d-111">如果您需要更充分掌控編碼或解碼程式，但仍想使用 Advanced Systems 格式 (ASF) 作為媒體資料的容器，Windows Media Format SDK 可能是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="a705d-111">If you need greater control over the encoding or decoding process, but you still intend to use the Advanced Systems Format (ASF) as a container for your media data, the Windows Media Format SDK might be a good choice.</span></span> <span data-ttu-id="a705d-112">Windows Media Format SDK 的物件提供彈性的架構來建立 ASF 檔案，並提供 Windows Media 音訊和 Video 編解碼器的內建支援。</span><span class="sxs-lookup"><span data-stu-id="a705d-112">The objects of the Windows Media Format SDK provide a flexible framework for creating ASF files, and provide built-in support for the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="a705d-113">媒體基礎 SDK 是 Windows Vista 的新功能，藉由提供可自訂的媒體管線，大幅簡化編碼和解碼。</span><span class="sxs-lookup"><span data-stu-id="a705d-113">The Media Foundation SDK, which is new for Windows Vista, greatly simplifies encoding and decoding by providing a customizable media pipeline.</span></span> <span data-ttu-id="a705d-114">您可以設定輸入和輸出媒體屬性，媒體基礎拓撲載入器會為您設定必要的編解碼器和 Dsp。</span><span class="sxs-lookup"><span data-stu-id="a705d-114">You can set input and output media properties and the Media Foundation topology loader will configure the necessary codecs and DSPs for you.</span></span>

<span data-ttu-id="a705d-115">直接使用編解碼器物件的主要原因是要在 ASF 容器之外使用 Windows Media 音訊和影片編解碼器。</span><span class="sxs-lookup"><span data-stu-id="a705d-115">The primary reason for using the codec objects directly is to use the Windows Media Audio and Video codecs outside of the ASF container.</span></span> <span data-ttu-id="a705d-116">使用編解碼器和 DSP 物件也提供使用任何更抽象技術無法使用的控制層級。</span><span class="sxs-lookup"><span data-stu-id="a705d-116">Using the codec and DSP objects also provides a level of control that is unavailable using any of the more abstracted technologies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a705d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a705d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a705d-118">Windows Media 轉碼器</span><span class="sxs-lookup"><span data-stu-id="a705d-118">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



