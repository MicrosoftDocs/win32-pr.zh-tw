---
description: 下列主題描述如何執行簡單的播放。
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: 簡單播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975322"
---
# <a name="simple-playback"></a><span data-ttu-id="422ac-103">簡單播放</span><span class="sxs-lookup"><span data-stu-id="422ac-103">Simple Playback</span></span>

<span data-ttu-id="422ac-104">下列主題描述如何執行簡單的播放。</span><span class="sxs-lookup"><span data-stu-id="422ac-104">The following topic describes how to perform simple playback.</span></span>

<span data-ttu-id="422ac-105">**執行簡單的播放**</span><span class="sxs-lookup"><span data-stu-id="422ac-105">**To perform simple playback**</span></span>

1.  <span data-ttu-id="422ac-106">在呼叫層級選取檔案播放終端機。</span><span class="sxs-lookup"><span data-stu-id="422ac-106">Select the File Playback Terminal at the call level.</span></span>
2.  <span data-ttu-id="422ac-107">在 TAPI 通話上建立播放終端機。</span><span class="sxs-lookup"><span data-stu-id="422ac-107">Create the Playback Terminal on the TAPI call.</span></span>
3.  <span data-ttu-id="422ac-108">設定屬性：儲存的檔案名和類型。</span><span class="sxs-lookup"><span data-stu-id="422ac-108">Set properties—file name and type of storage.</span></span>
4.  <span data-ttu-id="422ac-109">在檔案播放終端機上呼叫 [**start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) 方法以開始播放資料流程。</span><span class="sxs-lookup"><span data-stu-id="422ac-109">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of streams.</span></span>

<span data-ttu-id="422ac-110">下列範例程式碼示範簡單的播放。</span><span class="sxs-lookup"><span data-stu-id="422ac-110">The following example code demonstrates simple playback.</span></span>

<span data-ttu-id="422ac-111">首先，使用 [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) 介面建立錄製的終端機。</span><span class="sxs-lookup"><span data-stu-id="422ac-111">First, use the [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) interface to create the terminal for recording.</span></span> <span data-ttu-id="422ac-112">這會指示 TSP/MSP 在此呼叫上執行檔案播放。</span><span class="sxs-lookup"><span data-stu-id="422ac-112">This instructs the TSP/MSP to perform file playback on this call.</span></span> <span data-ttu-id="422ac-113">TSP/MSP 會建立應用程式要使用的終端機，並在成功時傳回。</span><span class="sxs-lookup"><span data-stu-id="422ac-113">The TSP/MSP creates a terminal for the application to use, and returns it on success.</span></span>


```C++

```



<span data-ttu-id="422ac-114">從終端介面取得 [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) 介面指標，並用它來設定要播放的檔案名。</span><span class="sxs-lookup"><span data-stu-id="422ac-114">Get the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface pointer from the terminal interface and use it to set the file name to play back.</span></span>


```C++
pMediaPlayback->Release();
```



<span data-ttu-id="422ac-115">假設檔案包含一個音訊串流，而且此呼叫具有 capture 音訊串流，檔案中的音訊內容將會在該資料流程上播放。</span><span class="sxs-lookup"><span data-stu-id="422ac-115">Assuming that the file contains one audio stream, and the call has a capture audio stream, the audio content in the file will play back on that stream.</span></span>

 

 



