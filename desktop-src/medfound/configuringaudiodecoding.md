---
description: 設定音訊解碼
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: '設定音訊解碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689343"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a><span data-ttu-id="b4bf6-103">設定音訊解碼 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="b4bf6-103">Configuring Audio Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="b4bf6-104">解碼 Windows Media 音訊內容比編碼更容易。</span><span class="sxs-lookup"><span data-stu-id="b4bf6-104">Decoding Windows Media Audio content is much easier than encoding it.</span></span> <span data-ttu-id="b4bf6-105">建立音訊解碼物件之後，請使用 **IMediaObject：： SetInputType** 或 **IMFTransform：： SetInputType** 方法設定輸入類型。</span><span class="sxs-lookup"><span data-stu-id="b4bf6-105">After creating an audio decoder object, set the input type by using the **IMediaObject::SetInputType** or **IMFTransform::SetInputType** method.</span></span> <span data-ttu-id="b4bf6-106">您用於解碼器輸入的媒體類型，必須符合編碼內容時所使用的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="b4bf6-106">The media type that you use for the decoder input must match the output type that was used when the content was encoded.</span></span> <span data-ttu-id="b4bf6-107">這包括附加至 **WAVEFORMATEX** 結構的延伸格式資料。</span><span class="sxs-lookup"><span data-stu-id="b4bf6-107">This includes the extended format data appended to the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="b4bf6-108">您必須確保這項資料正確無誤，因為解碼器無法處理沒有它的範例。</span><span class="sxs-lookup"><span data-stu-id="b4bf6-108">You must ensure that this data is correct, because the decoder cannot process samples without it.</span></span>

<span data-ttu-id="b4bf6-109">設定輸入類型之後，您可以設定您想要使用的任何解碼功能。</span><span class="sxs-lookup"><span data-stu-id="b4bf6-109">After setting the input type, you can configure any decoder features you want to use.</span></span> <span data-ttu-id="b4bf6-110">使用 **IPropertyBag** 或 **IPropertyStore** 的方法，可以設定像用於編碼的編碼器功能。</span><span class="sxs-lookup"><span data-stu-id="b4bf6-110">Decoder features, like those used for encoding, are set using the methods of **IPropertyBag** or **IPropertyStore**.</span></span>

<span data-ttu-id="b4bf6-111">設定輸入型別並設定所有的解碼器功能之後，您可以呼叫 **IMediaObject：： GetOutputType** 或 **IMFTransform：： GetOutputType**，以列舉此解碼器所支援的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="b4bf6-111">After the input type is set and all decoder features are configured, you can enumerate the output types supported by the decoder by making calls to **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4bf6-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4bf6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4bf6-113">使用音訊</span><span class="sxs-lookup"><span data-stu-id="b4bf6-113">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



