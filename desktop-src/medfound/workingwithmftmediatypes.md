---
description: 使用 MFT 媒體類型
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: 使用 MFT 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195722"
---
# <a name="working-with-mft-media-types"></a><span data-ttu-id="7caa0-103">使用 MFT 媒體類型</span><span class="sxs-lookup"><span data-stu-id="7caa0-103">Working with MFT Media Types</span></span>

<span data-ttu-id="7caa0-104">媒體類型是描述媒體資料流程格式的方式。</span><span class="sxs-lookup"><span data-stu-id="7caa0-104">A media type is a way to describe the format of a media stream.</span></span> <span data-ttu-id="7caa0-105">在媒體基礎中，媒體類型會以 **IMFMediaType** 介面表示。</span><span class="sxs-lookup"><span data-stu-id="7caa0-105">In Media Foundation, media types are represented by the **IMFMediaType** interface.</span></span> <span data-ttu-id="7caa0-106">這個介面會繼承 **IMFAttributes** 介面。</span><span class="sxs-lookup"><span data-stu-id="7caa0-106">This interface inherits the **IMFAttributes** interface.</span></span> <span data-ttu-id="7caa0-107">媒體類型的詳細資料會指定為屬性。</span><span class="sxs-lookup"><span data-stu-id="7caa0-107">The details of a media type are specified as attributes.</span></span>

<span data-ttu-id="7caa0-108">若要建立新的媒體類型，請呼叫 **MFCreateMediaType** 函數。</span><span class="sxs-lookup"><span data-stu-id="7caa0-108">To create a new media type, call the **MFCreateMediaType** function.</span></span> <span data-ttu-id="7caa0-109">此函數會傳回 **IMFMediaType** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7caa0-109">This function returns a pointer to the **IMFMediaType** interface.</span></span> <span data-ttu-id="7caa0-110">媒體類型一開始沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="7caa0-110">The media type initially has no attributes.</span></span>

<span data-ttu-id="7caa0-111">媒體基礎 SDK 提供數個協助程式函式，可從格式結構初始化媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7caa0-111">The Media Foundation SDK provides several helper functions for initializing Media Types from format structures.</span></span> <span data-ttu-id="7caa0-112">例如，函式 **MFInitMediaTypeFromVideoInfoHeader** 會從 **VIDEOINFOHEADER** 結構初始化影片類型，而函數 **MFInitMediaTypeFromWaveFormatEx** 會從 **WAVEFORMATEX** 或 **WAVEFORMATEXTENSIBLE** 結構初始化影片類型。</span><span class="sxs-lookup"><span data-stu-id="7caa0-112">For example the function **MFInitMediaTypeFromVideoInfoHeader** initializes a video type from a **VIDEOINFOHEADER** structure, and the function **MFInitMediaTypeFromWaveFormatEx** initializes a video type from a **WAVEFORMATEX** or **WAVEFORMATEXTENSIBLE** structure.</span></span>

<span data-ttu-id="7caa0-113">編解碼器所使用的格式類型通常會限制為 **VIDEOINFOHEADER** 和 **WAVEFORMATEX** 結構所描述的格式類型。</span><span class="sxs-lookup"><span data-stu-id="7caa0-113">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span>

<span data-ttu-id="7caa0-114">如需有關建立及存取媒體基礎媒體類型的詳細資訊，請參閱媒體基礎 SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="7caa0-114">More information on creating and accessing Media Foundation media types is available in the Media Foundation SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7caa0-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="7caa0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7caa0-116">使用編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="7caa0-116">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



