---
title: 設定未受限制的 VBR
description: 設定未受限制的 VBR
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- 串流，設定 VBR 資料流程
- '資料流程、變數位元速率 (VBR) '
- 變數位速率 (VBR) ，資料流程
- VBR (變數位速率) ，資料流程
- 資料流程，設定未受限制的 VBR
- 變數位元速率 (VBR) ，設定不受限制
- VBR (變數位速率) ，設定不受限制
- 設定檔，設定未受限制的 VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092581"
---
# <a name="to-configure-unconstrained-vbr"></a><span data-ttu-id="1d8e2-111">設定未受限制的 VBR</span><span class="sxs-lookup"><span data-stu-id="1d8e2-111">To Configure Unconstrained VBR</span></span>

<span data-ttu-id="1d8e2-112">您可以在資料流程上使用不受限制的變數位元速率 (VBR) 編碼方式，以指定將在編碼內容中維護的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-112">You can use unconstrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="1d8e2-113">未受限制的 VBR 與一般 CBR 不同之處在于，在整個資料流程中，位元速率的變異數可能更大。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-113">Unconstrained VBR differs from normal CBR in that the variance in bit rate throughout the stream can be greater.</span></span>

<span data-ttu-id="1d8e2-114">資料流程的位元速率（以 [**IWMStreamConfig：： SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)設定）是用來做為所需的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-114">The bit rate of the stream, set with [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), is used as the desired average bit rate.</span></span> <span data-ttu-id="1d8e2-115">當資料流程的編碼完成時，您可以使用 [**IWMPropertyVault：： GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) 抓取兩個額外的屬性： **g \_ wszVBRPeak** 和 **g \_ wszBufferAverage**。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-115">When encoding of the stream is complete, you can use [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) to retrieve two additional properties: **g\_wszVBRPeak** and **g\_wszBufferAverage**.</span></span> <span data-ttu-id="1d8e2-116">這些屬性會分別描述編碼內容的尖峰位元速率，以及內容的平均緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-116">These properties describe the peak bit rate of the encoded content and the average buffer window of the content, respectively.</span></span>

<span data-ttu-id="1d8e2-117">未受限制的 VBR 必須搭配雙通編碼使用。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-117">Unconstrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="1d8e2-118">設定檔中未設定雙通編碼。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-118">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="1d8e2-119">您必須將寫入器設定為在寫入資料流程之前執行前置處理階段。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-119">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="1d8e2-120">如需使用雙通編碼的詳細資訊，請參閱 [使用 Two-Pass 編碼](using-two-pass-encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-120">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="1d8e2-121">若要將設定檔中的串流設定為使用未受限制的 VBR 進行編碼，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1d8e2-121">To configure a stream in a profile to be encoded with unconstrained VBR, perform the following steps:</span></span>

1.  <span data-ttu-id="1d8e2-122">藉由呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數來建立配置檔案管理員物件。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-122">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="1d8e2-123">開啟您要新增 VBR 支援的現有設定檔。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-123">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="1d8e2-124">如需開啟設定檔的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-124">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="1d8e2-125">藉由呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) 或 [**IWMProfile：： GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)，取得您想要使用之資料流程的資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-125">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="1d8e2-126">藉由呼叫 **IWMStreamConfig：： QueryInterface**，取得資料流程設定物件之 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-126">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="1d8e2-127">針對 **g \_ wszVBREnabled** 屬性呼叫 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) ，以啟用資料流程的 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-127">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="1d8e2-128">使用 **IWMPropertyVault：： SetProperty** 將 **g \_ wszVBRBitrateMax** 和 **g \_ wszVBRBufferWindowMax** 兩者都設定為零。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-128">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
7.  <span data-ttu-id="1d8e2-129">藉由呼叫 [**IWMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)，儲存對資料流程所做的變更。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-129">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="1d8e2-130">儲存設定檔，或將其傳遞至寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-130">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="1d8e2-131">設定寫入器以執行前置處理階段。</span><span class="sxs-lookup"><span data-stu-id="1d8e2-131">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d8e2-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d8e2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d8e2-133">**設定 VBR 資料流程**</span><span class="sxs-lookup"><span data-stu-id="1d8e2-133">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




