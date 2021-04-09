---
title: XAudio2 程式設計指南
description: 本節列出 (API) 的 XAudio2 應用程式設計介面的總覽主題。
ms.assetid: 3d366a18-290d-5de8-4bcc-2178bd7c4c2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39dc28be35f94909aacced8dfbdae935c9739e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945341"
---
# <a name="xaudio2-programming-guide"></a><span data-ttu-id="78536-103">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="78536-103">XAudio2 programming guide</span></span>

<span data-ttu-id="78536-104">本節列出 (API) 的 XAudio2 應用程式設計介面的總覽主題。</span><span class="sxs-lookup"><span data-stu-id="78536-104">This section lists the overview topics for the XAudio2 application programming interface (API).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="78536-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="78536-105">In this section</span></span>



| <span data-ttu-id="78536-106">詞彙</span><span class="sxs-lookup"><span data-stu-id="78536-106">Term</span></span>                                                                                                                                                                                       | <span data-ttu-id="78536-107">描述</span><span class="sxs-lookup"><span data-stu-id="78536-107">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78536-108"><span id="XAudio2_Introduction"></span><span id="xaudio2_introduction"></span><span id="XAUDIO2_INTRODUCTION"></span>[XAudio2 簡介](xaudio2-introduction.md)</span><span class="sxs-lookup"><span data-stu-id="78536-108"><span id="XAudio2_Introduction"></span><span id="xaudio2_introduction"></span><span id="XAUDIO2_INTRODUCTION"></span>[XAudio2 Introduction](xaudio2-introduction.md)</span></span><br/>           | <span data-ttu-id="78536-109">介紹重要的 XAudio2 概念。</span><span class="sxs-lookup"><span data-stu-id="78536-109">Introduces key XAudio2 concepts.</span></span><br/>                                                                                              |
| <span data-ttu-id="78536-110"><span id="Common_Audio_Concepts"></span><span id="common_audio_concepts"></span><span id="COMMON_AUDIO_CONCEPTS"></span>[常見的音訊概念](common-audio-concepts.md)</span><span class="sxs-lookup"><span data-stu-id="78536-110"><span id="Common_Audio_Concepts"></span><span id="common_audio_concepts"></span><span id="COMMON_AUDIO_CONCEPTS"></span>[Common Audio Concepts](common-audio-concepts.md)</span></span><br/>      | <span data-ttu-id="78536-111">概要說明音訊開發人員應該熟悉的常見音訊概念。</span><span class="sxs-lookup"><span data-stu-id="78536-111">Provides an overview of common audio concepts with which an audio developer should be familiar.</span></span><br/>                               |
| <span data-ttu-id="78536-112"><span id="Getting_Started"></span><span id="getting_started"></span><span id="GETTING_STARTED"></span>[開始使用](getting-started.md)</span><span class="sxs-lookup"><span data-stu-id="78536-112"><span id="Getting_Started"></span><span id="getting_started"></span><span id="GETTING_STARTED"></span>[Getting Started](getting-started.md)</span></span><br/>                                    | <span data-ttu-id="78536-113">描述在遊戲中設定 XAudio2。</span><span class="sxs-lookup"><span data-stu-id="78536-113">Describes setting up XAudio2 in game.</span></span><br/>                                                                                         |
| <span data-ttu-id="78536-114"><span id="Voices"></span><span id="voices"></span><span id="VOICES"></span>[聲音](voices.md)</span><span class="sxs-lookup"><span data-stu-id="78536-114"><span id="Voices"></span><span id="voices"></span><span id="VOICES"></span>[Voices](voices.md)</span></span><br/>                                                                                 | <span data-ttu-id="78536-115">描述 XAudio2 聲音的類型，以及其使用方式。</span><span class="sxs-lookup"><span data-stu-id="78536-115">Describes the types of XAudio2 voices, and how to use them.</span></span><br/>                                                                   |
| <span data-ttu-id="78536-116"><span id="Callbacks"></span><span id="callbacks"></span><span id="CALLBACKS"></span>[回檔](callbacks.md)</span><span class="sxs-lookup"><span data-stu-id="78536-116"><span id="Callbacks"></span><span id="callbacks"></span><span id="CALLBACKS"></span>[Callbacks](callbacks.md)</span></span><br/>                                                                  | <span data-ttu-id="78536-117">提供可與 XAudio2 搭配使用之回呼的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="78536-117">Provides details about the callbacks available for use with XAudio2.</span></span><br/>                                                          |
| <span data-ttu-id="78536-118"><span id="Audio_Graph"></span><span id="audio_graph"></span><span id="AUDIO_GRAPH"></span>[音訊圖形](audio-graphs.md)</span><span class="sxs-lookup"><span data-stu-id="78536-118"><span id="Audio_Graph"></span><span id="audio_graph"></span><span id="AUDIO_GRAPH"></span>[Audio Graph](audio-graphs.md)</span></span><br/>                                                       | <span data-ttu-id="78536-119">描述 XAudio2 音訊圖形。</span><span class="sxs-lookup"><span data-stu-id="78536-119">Describes the XAudio2 audio graph.</span></span><br/>                                                                                            |
| <span data-ttu-id="78536-120"><span id="Audio_Effects"></span><span id="audio_effects"></span><span id="AUDIO_EFFECTS"></span>[音訊效果](audio-effects.md)</span><span class="sxs-lookup"><span data-stu-id="78536-120"><span id="Audio_Effects"></span><span id="audio_effects"></span><span id="AUDIO_EFFECTS"></span>[Audio Effects](audio-effects.md)</span></span><br/>                                              | <span data-ttu-id="78536-121">說明如何使用 XAudio2 的數位信號處理效果。</span><span class="sxs-lookup"><span data-stu-id="78536-121">Describes using digital signal processing effects with XAudio2.</span></span><br/>                                                               |
| <span data-ttu-id="78536-122"><span id="Streaming_Audio_Data"></span><span id="streaming_audio_data"></span><span id="STREAMING_AUDIO_DATA"></span>[串流音訊資料](streaming-audio-data.md)</span><span class="sxs-lookup"><span data-stu-id="78536-122"><span id="Streaming_Audio_Data"></span><span id="streaming_audio_data"></span><span id="STREAMING_AUDIO_DATA"></span>[Streaming Audio Data](streaming-audio-data.md)</span></span><br/>           | <span data-ttu-id="78536-123">說明如何使用 XAudio2 從磁片串流音效。</span><span class="sxs-lookup"><span data-stu-id="78536-123">Describes how to stream a sound from disk using XAudio2.</span></span><br/>                                                                      |
| <span data-ttu-id="78536-124"><span id="X3DAudio_Overview"></span><span id="x3daudio_overview"></span><span id="X3DAUDIO_OVERVIEW"></span>[X3DAudio 總覽](x3daudio.md)</span><span class="sxs-lookup"><span data-stu-id="78536-124"><span id="X3DAudio_Overview"></span><span id="x3daudio_overview"></span><span id="X3DAUDIO_OVERVIEW"></span>[X3DAudio Overview](x3daudio.md)</span></span><br/>                                   | <span data-ttu-id="78536-125">描述如何搭配使用 X3DAudio 與 XAudio2，以建立來自3D 空間中某個點的音效假像。</span><span class="sxs-lookup"><span data-stu-id="78536-125">Describes how X3DAudio is used in conjunction with XAudio2 to create the illusion of a sound coming from a point in 3D space.</span></span><br/> |
| <span data-ttu-id="78536-126"><span id="XAudio2_Operation_Sets"></span><span id="xaudio2_operation_sets"></span><span id="XAUDIO2_OPERATION_SETS"></span>[XAudio2 操作集](xaudio2-operation-sets.md)</span><span class="sxs-lookup"><span data-stu-id="78536-126"><span id="XAudio2_Operation_Sets"></span><span id="xaudio2_operation_sets"></span><span id="XAUDIO2_OPERATION_SETS"></span>[XAudio2 Operation Sets](xaudio2-operation-sets.md)</span></span><br/> | <span data-ttu-id="78536-127">描述 XAudio2 操作集，並概述一些特定的使用案例。</span><span class="sxs-lookup"><span data-stu-id="78536-127">Describes XAudio2 operation sets, and outlines some specific usage scenarios.</span></span><br/>                                                 |
| <span data-ttu-id="78536-128"><span id="Debugging_Facilities"></span><span id="debugging_facilities"></span><span id="DEBUGGING_FACILITIES"></span>[調試功能](debugging-facilities.md)</span><span class="sxs-lookup"><span data-stu-id="78536-128"><span id="Debugging_Facilities"></span><span id="debugging_facilities"></span><span id="DEBUGGING_FACILITIES"></span>[Debugging Facilities](debugging-facilities.md)</span></span><br/>           | <span data-ttu-id="78536-129">描述 XAudio2 的調試功能。</span><span class="sxs-lookup"><span data-stu-id="78536-129">Describes the XAudio2 debugging facilities.</span></span> <br/>                                                                                  |
| <span data-ttu-id="78536-130"><span id="ADPCM_Overview"></span><span id="adpcm_overview"></span><span id="ADPCM_OVERVIEW"></span>[ADPCM 總覽](adpcm-overview.md)</span><span class="sxs-lookup"><span data-stu-id="78536-130"><span id="ADPCM_Overview"></span><span id="adpcm_overview"></span><span id="ADPCM_OVERVIEW"></span>[ADPCM Overview](adpcm-overview.md)</span></span><br/>                                         | <span data-ttu-id="78536-131">描述適應性差異脈衝程式碼 (ADPCM) 壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="78536-131">Describes the Adaptive Differential Pulse Code Modulation (ADPCM) compression format.</span></span><br/>                                         |



 

## <a name="related-topics"></a><span data-ttu-id="78536-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="78536-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78536-133">XAudio2 API</span><span class="sxs-lookup"><span data-stu-id="78536-133">XAudio2 APIs</span></span>](xaudio2-apis-portal.md)
</dt> <dt>

[<span data-ttu-id="78536-134">XAudio2 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="78536-134">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




