---
title: 重複使用串流設定
description: 重複使用串流設定
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- 串流，重複使用設定
- 設定檔，重複使用串流設定
- 重複使用串流設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af10fd026904ccef33aba28d28e0e6a4975d3fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106969687"
---
# <a name="reusing-stream-configurations"></a><span data-ttu-id="da530-106">重複使用串流設定</span><span class="sxs-lookup"><span data-stu-id="da530-106">Reusing Stream Configurations</span></span>

<span data-ttu-id="da530-107">有時您會想要重複使用現有設定檔中的串流設定物件。</span><span class="sxs-lookup"><span data-stu-id="da530-107">There are often times when you want to reuse a stream configuration object from an existing profile.</span></span> <span data-ttu-id="da530-108">您可能會有需要更新的舊設定檔，或您可能需要與系統設定檔中的相同的資料流程。</span><span class="sxs-lookup"><span data-stu-id="da530-108">You may have old profiles that need updating or you may need a stream identical to one in a system profile.</span></span> <span data-ttu-id="da530-109">您可以更輕鬆地重複使用串流設定，而不是建立新的串流設定，而且您通常可以變更設定中的一些設定，以符合您的需求，而不是建立全新的設定。</span><span class="sxs-lookup"><span data-stu-id="da530-109">It is easier to reuse stream configurations than to create new ones, and you can often change a few settings in a configuration to meet your needs rather than creating an entirely new one.</span></span>

<span data-ttu-id="da530-110">請注意，您可以變更資料流程設定的方式有所限制。</span><span class="sxs-lookup"><span data-stu-id="da530-110">Be aware that there are limitations to how you can change stream configurations.</span></span> <span data-ttu-id="da530-111">如果您以錯誤的方式變更設定，您的設定檔可能不會接受串流設定物件。</span><span class="sxs-lookup"><span data-stu-id="da530-111">If you change settings in the wrong way, your profile may not accept the stream configuration object.</span></span> <span data-ttu-id="da530-112">設定檔通常會接受不正確的串流設定，但會導致寫入器物件拒絕設定檔。</span><span class="sxs-lookup"><span data-stu-id="da530-112">Incorrect stream configurations are frequently accepted by the profile but cause the writer object to reject the profile.</span></span> <span data-ttu-id="da530-113">使用和修改現有的串流設定時，請注意下列限制和問題。</span><span class="sxs-lookup"><span data-stu-id="da530-113">Be aware of the following limitations and issues when using and modifying existing stream configurations.</span></span>

-   <span data-ttu-id="da530-114">絕對不要改變 prx 檔案的內容以變更資料流程設定。</span><span class="sxs-lookup"><span data-stu-id="da530-114">Never alter the contents of a .prx file to change stream settings.</span></span> <span data-ttu-id="da530-115">當設定檔儲存至 XML 字串並寫入至 prx 檔案時，可以使用任何文字編輯器來讀取這些設定檔。</span><span class="sxs-lookup"><span data-stu-id="da530-115">When profiles are saved to XML strings and written to a .prx file they can be read with any text editor.</span></span> <span data-ttu-id="da530-116">查看儲存的設定檔可協助您瞭解設定檔的運作方式。</span><span class="sxs-lookup"><span data-stu-id="da530-116">Looking at a saved profile can help you understand how profiles work.</span></span> <span data-ttu-id="da530-117">不過，您絕對不應該以任何方式改變 prx 檔。</span><span class="sxs-lookup"><span data-stu-id="da530-117">However, you should never alter a .prx file in any way.</span></span> <span data-ttu-id="da530-118">即使是看似簡單的變更，也可能使設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="da530-118">Even seemingly trivial changes can invalidate the profile.</span></span>
-   <span data-ttu-id="da530-119">Windows Media 音訊編解碼器的數個版本使用相同的串流設定。</span><span class="sxs-lookup"><span data-stu-id="da530-119">Several versions of the Windows Media Audio codec use the same stream configurations.</span></span> <span data-ttu-id="da530-120">如果您有設定為子類型 WMMEDIASUBTYPE \_ WMAudioV2、WMMEDIASUBTYPE \_ WMAUDIOV7 或 WMMEDIASUBTYPE WMAudioV8 的串流設定物件 \_ ，則會使用最新的 Windows Media 音訊編解碼器來壓縮產生的串流。</span><span class="sxs-lookup"><span data-stu-id="da530-120">If you have a stream configuration object that is configured as subtype WMMEDIASUBTYPE\_WMAudioV2, WMMEDIASUBTYPE\_WMAudioV7, or WMMEDIASUBTYPE\_WMAudioV8, the resulting stream will be compressed with the latest Windows Media Audio codec.</span></span> <span data-ttu-id="da530-121">不過，在使用現有的音訊編解碼器之前，您應該先評估您的需求。</span><span class="sxs-lookup"><span data-stu-id="da530-121">However, you should evaluate your needs before using an existing audio codec.</span></span> <span data-ttu-id="da530-122">升級至最新版的 Windows Media 音訊 Professional 編解碼器或 Windows Media 音訊的無失真編解碼器，可以改善許多類型的檔案。</span><span class="sxs-lookup"><span data-stu-id="da530-122">Many types of files can be improved by upgrading to the latest version of the Windows Media Audio Professional codec, or the Windows Media Audio Lossless codec.</span></span>
-   <span data-ttu-id="da530-123">請勿變更資料流程的子類型，以升級為新的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="da530-123">Never change the subtype of a stream to upgrade to a new codec.</span></span> <span data-ttu-id="da530-124">當您使用 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) 的方法來取得資料流程設定時，編解碼器會附加一些資料來識別位流格式。</span><span class="sxs-lookup"><span data-stu-id="da530-124">When you use the methods of [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) to obtain a stream configuration, the codec attaches some data to it that identifies the bit stream format.</span></span> <span data-ttu-id="da530-125">如果您變更現有資料流程設定物件的子類型，子類型將不會符合編解碼器資料。</span><span class="sxs-lookup"><span data-stu-id="da530-125">If you change the subtype of an existing stream configuration object, the subtype will not match the codec data.</span></span> <span data-ttu-id="da530-126">寫入器物件不會接受具有這類串流設定的設定檔。</span><span class="sxs-lookup"><span data-stu-id="da530-126">A profile with such a stream configuration will not be accepted by the writer object.</span></span>
-   <span data-ttu-id="da530-127">請勿改變壓縮音訊串流設定的設定。</span><span class="sxs-lookup"><span data-stu-id="da530-127">Do not alter the settings of compressed audio stream configurations.</span></span> <span data-ttu-id="da530-128">如果音訊串流的設定不符合您的需求，請使用 **IWMCodecInfo3** 的方法從編解碼器取得新的串流設定。</span><span class="sxs-lookup"><span data-stu-id="da530-128">If the settings of an audio stream do not suit your needs, obtain a new stream configuration from the codec using the methods of **IWMCodecInfo3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da530-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="da530-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da530-130">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="da530-130">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="da530-131">**從編解碼器取得串流設定資訊**</span><span class="sxs-lookup"><span data-stu-id="da530-131">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




