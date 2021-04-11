---
description: 下表描述 RecognizerCoNtext 物件事件可以引發的執行緒。EventThreadsRecognitionFires 在背景辨識執行緒上，或在呼叫 RecognizerCoNtext 物件之辨識方法的執行緒上。在背景辨識執行緒上 RecognitionWithAlternatesFires。
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: RecognizerCoNtext 物件事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944780"
---
# <a name="recognizercontext-object-events"></a><span data-ttu-id="f7feb-103">RecognizerCoNtext 物件事件</span><span class="sxs-lookup"><span data-stu-id="f7feb-103">RecognizerContext Object Events</span></span>

<span data-ttu-id="f7feb-104">下表描述 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件事件可以引發的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f7feb-104">The following table describes which threads the [**RecognizerContext**](inkrecognizercontext-class.md) object events can fire on.</span></span>



| <span data-ttu-id="f7feb-105">事件</span><span class="sxs-lookup"><span data-stu-id="f7feb-105">Event</span></span>                                                                               | <span data-ttu-id="f7feb-106">執行緒</span><span class="sxs-lookup"><span data-stu-id="f7feb-106">Threads</span></span>                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7feb-107">**辨識**</span><span class="sxs-lookup"><span data-stu-id="f7feb-107">**Recognition**</span></span>](inkrecognizercontext-recognition.md)                             | <span data-ttu-id="f7feb-108">在背景辨識執行緒或呼叫 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件之 [**辨識**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) 方法的執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="f7feb-108">Fires on the background recognition thread, or on the thread which calls the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method.</span></span><br/> |
| [<span data-ttu-id="f7feb-109">**RecognitionWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="f7feb-109">**RecognitionWithAlternates**</span></span>](inkrecognizercontext-recognitionwithalternates.md) | <span data-ttu-id="f7feb-110">在背景辨識執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="f7feb-110">Fires on the background recognition thread.</span></span><br/>                                                                                                                                                               |



 

 

 




