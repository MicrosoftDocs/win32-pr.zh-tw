---
description: 使用編輯決策清單進行編碼語音
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: 使用編輯決策清單進行編碼語音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975022"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a><span data-ttu-id="5602d-103">使用編輯決策清單進行編碼語音</span><span class="sxs-lookup"><span data-stu-id="5602d-103">Using an Editing Decision List for Encoding Voice</span></span>

<span data-ttu-id="5602d-104"> (EDL) 的編輯決策清單是提供給編解碼器的資料，提供有關內容特定部分之編碼方式的資訊。</span><span class="sxs-lookup"><span data-stu-id="5602d-104">An editing decision list (EDL), is data given to a codec that provides information about how specific portions of content should be encoded.</span></span> <span data-ttu-id="5602d-105">Windows Media 音訊9語音編解碼器支援簡單的 EDL，您可以在其中指定包含音樂的內容部分。</span><span class="sxs-lookup"><span data-stu-id="5602d-105">The Windows Media Audio 9 Voice codec supports a simple EDL in which you can specify the portions of content that contain music.</span></span> <span data-ttu-id="5602d-106">根據預設，編解碼器會在設定成編碼混合的內容時，偵測到音樂本身的段落。</span><span class="sxs-lookup"><span data-stu-id="5602d-106">By default, the codec detects passages of music itself when configured to encode mixed content.</span></span> <span data-ttu-id="5602d-107">只有當編解碼器未正確偵測內容類型時，才應該使用 EDL。</span><span class="sxs-lookup"><span data-stu-id="5602d-107">You should use an EDL only if the codec is not detecting the content types correctly.</span></span>

<span data-ttu-id="5602d-108">若要使用 EDL，必須將語音編碼器設定為編碼混合的內容。</span><span class="sxs-lookup"><span data-stu-id="5602d-108">To use an EDL, the voice encoder must be set to encode mixed content.</span></span> <span data-ttu-id="5602d-109">將 [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) 屬性設定為2，以將語音編解碼器的模式設定為「混合」。</span><span class="sxs-lookup"><span data-stu-id="5602d-109">Configure the mode of the voice codec to "mixed" by setting the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to 2.</span></span> <span data-ttu-id="5602d-110">使用 [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) 屬性來設定 EDL。</span><span class="sxs-lookup"><span data-stu-id="5602d-110">Set the EDL using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span> <span data-ttu-id="5602d-111">這個屬性的值是一個字串，其中包含以逗號分隔的清單，其中包含應編碼為音樂的內容中的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="5602d-111">The value of this property is a string containing a comma-delimited list of the time ranges in the content that should be encoded as music.</span></span> <span data-ttu-id="5602d-112">清單中的第一個專案是 EDL 的版本，一律為1。</span><span class="sxs-lookup"><span data-stu-id="5602d-112">The first item in the list is the version of the EDL, which is always 1.</span></span> <span data-ttu-id="5602d-113">第二個專案是清單中所述的音樂區段數目。</span><span class="sxs-lookup"><span data-stu-id="5602d-113">The second item is the number of music sections described in the list.</span></span> <span data-ttu-id="5602d-114">之後，第二個專案是等於第二個專案的幾個值配對;每一對值會描述音樂在內容中的開始和結束點（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5602d-114">Following the second item are a number of pairs of values equal to the second item; each pair of values describes the starting and ending point of a music passage in the content, in milliseconds.</span></span>

<span data-ttu-id="5602d-115">例如，EDL 字串 "1，4，1000，2000，5000，6000，9000，10000，13000，14000" 指定四個樂譜段，每個都是一秒。</span><span class="sxs-lookup"><span data-stu-id="5602d-115">For example, the EDL string "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifies four musical passages, each of which is one second long.</span></span> <span data-ttu-id="5602d-116">如果 EDL 字串中的資訊無效，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="5602d-116">If the information in the EDL string is invalid, it is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5602d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="5602d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5602d-118">使用 Windows Media 音訊9語音編解碼器</span><span class="sxs-lookup"><span data-stu-id="5602d-118">Using the Windows Media Audio 9 Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="5602d-119">使用音訊</span><span class="sxs-lookup"><span data-stu-id="5602d-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



