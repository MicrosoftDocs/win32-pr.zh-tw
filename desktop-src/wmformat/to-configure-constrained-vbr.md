---
title: 設定限制的 VBR
description: 設定限制的 VBR
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- 串流，設定 VBR 資料流程
- '資料流程、變數位元速率 (VBR) '
- 變數位速率 (VBR) ，資料流程
- VBR (變數位速率) ，資料流程
- 資料流程，設定限制的 VBR
- 變數位元速率 (VBR) ，設定限制
- VBR (變數位速率) ，設定限制
- 設定檔，設定受限制的 VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023164"
---
# <a name="to-configure-constrained-vbr"></a><span data-ttu-id="624d5-111">設定限制的 VBR</span><span class="sxs-lookup"><span data-stu-id="624d5-111">To Configure Constrained VBR</span></span>

<span data-ttu-id="624d5-112">您可以在資料流程上使用受限制的變數位元速率 (VBR) 編碼方式，以指定將在編碼內容中維護的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="624d5-112">You can use constrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="624d5-113">您也可以指定資料流程的最大位元速率，以及所需的最大緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="624d5-113">You also specify the maximum bit rate of the stream and the maximum required buffer window.</span></span>

<span data-ttu-id="624d5-114">在編碼之前，您不能知道條件約束的 VBR 資料流程的平均位元速率，但您可以使用粗略估計。</span><span class="sxs-lookup"><span data-stu-id="624d5-114">You cannot know what the average bit rate will be for a constrained VBR stream before encoding, but you can use a rough estimate.</span></span> <span data-ttu-id="624d5-115">一般來說，您指定的最大位元速率，最後會是平均位元速率的兩到三倍。</span><span class="sxs-lookup"><span data-stu-id="624d5-115">As a general rule, the maximum bit rate you specify will end up being two to three times the average bit rate.</span></span>

<span data-ttu-id="624d5-116">限制的 VBR 必須搭配雙通編碼使用。</span><span class="sxs-lookup"><span data-stu-id="624d5-116">Constrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="624d5-117">設定檔中未設定雙通編碼。</span><span class="sxs-lookup"><span data-stu-id="624d5-117">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="624d5-118">您必須將寫入器設定為在寫入資料流程之前執行前置處理階段。</span><span class="sxs-lookup"><span data-stu-id="624d5-118">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="624d5-119">如需使用雙通編碼的詳細資訊，請參閱 [使用 Two-Pass 編碼](using-two-pass-encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="624d5-119">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="624d5-120">若要將設定檔中的串流設定為使用受限制的 VBR 編碼，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="624d5-120">To configure a stream in a profile to use constrained VBR encoding, perform the following steps.</span></span>

1.  <span data-ttu-id="624d5-121">藉由呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數來建立配置檔案管理員物件。</span><span class="sxs-lookup"><span data-stu-id="624d5-121">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="624d5-122">開啟您要新增 VBR 支援的現有設定檔。</span><span class="sxs-lookup"><span data-stu-id="624d5-122">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="624d5-123">如需開啟設定檔的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="624d5-123">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="624d5-124">藉由呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) 或 [**IWMProfile：： GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)，取得您想要使用之資料流程的資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="624d5-124">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="624d5-125">藉由呼叫 **IWMStreamConfig：： QueryInterface**，取得資料流程設定物件之 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="624d5-125">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="624d5-126">針對 **g \_ wszVBREnabled** 屬性呼叫 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) ，以啟用資料流程的 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="624d5-126">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="624d5-127">使用 **IWMPropertyVault：： SetProperty** 的呼叫來設定 **g \_ wszVBRBitrateMax** 和 **g \_ wszVBRBufferWindowMax** 屬性所需的最大值。</span><span class="sxs-lookup"><span data-stu-id="624d5-127">Use calls to **IWMPropertyVault::SetProperty** to set the desired maximum values for the **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** properties.</span></span>
7.  <span data-ttu-id="624d5-128">藉由呼叫 [**IWMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)，儲存對資料流程所做的變更。</span><span class="sxs-lookup"><span data-stu-id="624d5-128">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="624d5-129">儲存設定檔，或將其傳遞至寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="624d5-129">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="624d5-130">設定寫入器以執行前置處理階段。</span><span class="sxs-lookup"><span data-stu-id="624d5-130">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="624d5-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="624d5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="624d5-132">**設定 VBR 資料流程**</span><span class="sxs-lookup"><span data-stu-id="624d5-132">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




