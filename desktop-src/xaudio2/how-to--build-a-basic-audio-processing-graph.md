---
description: 啟用 XAudio2 以播放音訊資料的最低需求是音訊處理圖形，它是由單一的控制語音和單一來源語音所構成。
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 使用方法：建立基本音訊處理圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988278"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="5c68c-103">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="5c68c-103">How to: Build a Basic Audio Processing Graph</span></span>

<span data-ttu-id="5c68c-104">啟用 XAudio2 以播放音訊資料的最低需求是音訊處理圖形，它是由單一的控制語音和單一來源語音所構成。</span><span class="sxs-lookup"><span data-stu-id="5c68c-104">The minimum requirement for enabling XAudio2 to play audio data is an audio processing graph, which is constructed from a single mastering voice and a single source voice.</span></span>

## <a name="to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="5c68c-105">建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="5c68c-105">To build a basic audio processing graph</span></span>

1.  <span data-ttu-id="5c68c-106">遵循 [如何：初始化 XAudio2](how-to--initialize-xaudio2.md)中所述的步驟，初始化 XAudio2 引擎。</span><span class="sxs-lookup"><span data-stu-id="5c68c-106">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="5c68c-107">依照 how [to：在 XAUDIO2 中載入音訊資料檔案](how-to--load-audio-data-files-in-xaudio2.md)中所述的步驟，填入 **WAVEFORMATEX** 和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構。</span><span class="sxs-lookup"><span data-stu-id="5c68c-107">Populate a **WAVEFORMATEX** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
3.  <span data-ttu-id="5c68c-108">使用 [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) 函數建立來源語音。</span><span class="sxs-lookup"><span data-stu-id="5c68c-108">Create a source voice using the [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) function.</span></span>

    <span data-ttu-id="5c68c-109">當您針對 [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)的 pSendList 引數指定 Null 時，來源語音的輸出會移至在步驟1中建立的「控制」聲音。</span><span class="sxs-lookup"><span data-stu-id="5c68c-109">When you specify NULL for the pSendList argument of [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), the source voice's output goes to the mastering voice created in step 1.</span></span>

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    <span data-ttu-id="5c68c-110">完成此步驟之後，會有一個簡單的音訊圖表，其中包含來源語音、主控語音和音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="5c68c-110">After you finish this step, there is a simple audio graph consisting of the source voice, the mastering voice, and the audio device.</span></span> <span data-ttu-id="5c68c-111">此「作法」主題中的其餘步驟會示範如何啟動流經圖形的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="5c68c-111">The remaining steps in this how-to topic show you how to start audio data flowing through the graph.</span></span>

    <span data-ttu-id="5c68c-112">簡單的音訊圖形</span><span class="sxs-lookup"><span data-stu-id="5c68c-112">A simple audio graph</span></span>

    ![簡單的音訊圖形。](images/xaudio2-audio-graph.png)

4.  <span data-ttu-id="5c68c-114">使用函式 [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) 提交 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 至來源聲音。</span><span class="sxs-lookup"><span data-stu-id="5c68c-114">Use the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) to submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice.</span></span>

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  <span data-ttu-id="5c68c-115">使用 [**start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) 函數啟動來源聲音。</span><span class="sxs-lookup"><span data-stu-id="5c68c-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span>

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5c68c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c68c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c68c-117">音訊圖形</span><span class="sxs-lookup"><span data-stu-id="5c68c-117">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="5c68c-118">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="5c68c-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
