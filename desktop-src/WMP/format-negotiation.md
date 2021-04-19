---
title: 格式協調
description: 格式協調
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Windows Media Player 外掛程式，格式協調
- 外掛程式，格式協調
- 數位信號處理外掛程式，格式協調
- DSP 外掛程式，格式協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967434"
---
# <a name="format-negotiation"></a><span data-ttu-id="e5454-107">格式協調</span><span class="sxs-lookup"><span data-stu-id="e5454-107">Format Negotiation</span></span>

<span data-ttu-id="e5454-108">針對 Windows Media Player 和 DSP 外掛程式以共用資料，這兩個程式都必須同意其正在處理的資料格式。</span><span class="sxs-lookup"><span data-stu-id="e5454-108">For Windows Media Player and a DSP plug-in to share data, both programs must agree on the format of the data they are processing.</span></span> <span data-ttu-id="e5454-109">DSP 外掛程式會執行播放機呼叫的方法，以判斷外掛程式所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="e5454-109">The DSP plug-in implements methods that the Player calls to determine which formats the plug-in supports.</span></span> <span data-ttu-id="e5454-110">此外掛程式也會執行播放機呼叫以設定目前格式的方法。</span><span class="sxs-lookup"><span data-stu-id="e5454-110">The plug-in also implements methods that the Player calls to set the current format.</span></span>

<span data-ttu-id="e5454-111">如果外掛程式作為 DirextX 媒體物件 (]) ，Windows Media Player 藉由呼叫 **IMediaObject** 介面的方法來探索和設定媒體格式。</span><span class="sxs-lookup"><span data-stu-id="e5454-111">If the plug-in is acting as a DirextX Media Object (DMO), Windows Media Player discovers and sets media formats by calling methods of the **IMediaObject** interface.</span></span> <span data-ttu-id="e5454-112">例如，播放程式會重複呼叫外掛程式的 **IMediaObject：： GetInputType** ，以取得外掛程式所支援的所有輸入格式清單。</span><span class="sxs-lookup"><span data-stu-id="e5454-112">For example, the Player calls the plug-in's **IMediaObject::GetInputType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="e5454-113">SQL-DMO 外掛程式使用 **Sql-dmo \_ 媒體 \_ 類型** 結構來組織指定媒體格式的資訊。</span><span class="sxs-lookup"><span data-stu-id="e5454-113">DMO plug-ins use the **DMO\_MEDIA\_TYPE** structure to organize the information that specifies a media format.</span></span> <span data-ttu-id="e5454-114">如需有關 SQL-DMO 外掛程式和播放機如何協商格式的詳細資訊，請參閱 [關於 IMediaObject](about-imediaobject.md)。</span><span class="sxs-lookup"><span data-stu-id="e5454-114">For more information about how DMO plug-ins and the Player negotiate format, see [About IMediaObject](about-imediaobject.md).</span></span>

<span data-ttu-id="e5454-115">如果外掛程式做為媒體基礎轉換 (MFT) ，Windows Media Player 會藉由呼叫 **IMFTransform** 介面的方法，來探索和設定媒體格式。</span><span class="sxs-lookup"><span data-stu-id="e5454-115">If the plug-in is acting as a Media Foundation Transform (MFT), Windows Media Player discovers and sets media formats by calling methods of the **IMFTransform** interface.</span></span> <span data-ttu-id="e5454-116">例如，播放程式會重複呼叫外掛程式的 **IMFTransform：： GetInputAvailableType** ，以取得外掛程式所支援的所有輸入格式清單。</span><span class="sxs-lookup"><span data-stu-id="e5454-116">For example, the Player calls the plug-in's **IMFTransform::GetInputAvailableType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="e5454-117">MFT 外掛程式和播放機會使用 **IMFMediaType** 介面來組織和交換格式資訊。</span><span class="sxs-lookup"><span data-stu-id="e5454-117">MFT plug-ins and the Player use the **IMFMediaType** interface to organize and exchange format information.</span></span>

<span data-ttu-id="e5454-118">只有當外掛程式支援與所播放數位音訊的相同位深度時，Windows Media Player 才會使用音訊 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e5454-118">Windows Media Player will use an audio DSP plug-in only if the plug-in supports the same bit depth as the digital audio being played.</span></span> <span data-ttu-id="e5454-119">比方說，如果數位音訊是20位，則必須撰寫外掛程式來處理20位音訊。</span><span class="sxs-lookup"><span data-stu-id="e5454-119">For instance, if the digital audio is 20-bit, the plug-in must be written to process 20-bit audio.</span></span> <span data-ttu-id="e5454-120">針對 CD 音訊，DSP 外掛程式必須支援20位處理。</span><span class="sxs-lookup"><span data-stu-id="e5454-120">For CD audio, DSP plug-ins must support 20-bit processing.</span></span>

<span data-ttu-id="e5454-121">在設定為使用身歷聲喇叭的電腦上進行多重通道內容的格式協調期間，Windows Media Player 先嘗試透過呼叫 **IMediaObject：： SetInputType** 和 **IMediaObject：： SetOutputType** 來連線到使用現有輸入和輸出格式的音訊 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e5454-121">During format negotiation of multi-channel content on a computer configured for use with stereo speakers, Windows Media Player first attempts to connect to an audio DSP plug-in using the existing input and output format by calling **IMediaObject::SetInputType** and **IMediaObject::SetOutputType**.</span></span> <span data-ttu-id="e5454-122">一旦發生此初始協商，播放程式就會列舉外掛程式所支援的格式，並嘗試協調播放機和外掛程式的最佳格式組合。</span><span class="sxs-lookup"><span data-stu-id="e5454-122">Once this initial negotiation occurs, the Player then enumerates the formats the plug-in supports and attempts to negotiate the best format combination for the Player and the plug-in.</span></span> <span data-ttu-id="e5454-123">如果外掛程式接受 **WAVEFORMATEX** 結構所定義的身歷聲音訊 () 為初始協商期間的輸入格式，然後只接受 **WAVEFORMATEXTENSIBLE** 結構) 所定義的多頻道音訊 (，則播放程式會提供多頻道音訊做為外掛程式的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="e5454-123">If the plug-in accepts stereo audio (defined by a **WAVEFORMATEX** structure) as the input format during the initial negotiation, and then subsequently accepts only multi-channel audio (defined by a **WAVEFORMATEXTENSIBLE** structure), the Player will provide multi-channel audio as the input format to the plug-in.</span></span> <span data-ttu-id="e5454-124">格式協調期間的這個行為可用於 Microsoft Windows XP 作業系統。</span><span class="sxs-lookup"><span data-stu-id="e5454-124">This behavior during format negotiation is available for use in the Microsoft Windows XP operating system.</span></span> <span data-ttu-id="e5454-125">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="e5454-125">It may be altered or unavailable in subsequent versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5454-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5454-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5454-127">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="e5454-127">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




