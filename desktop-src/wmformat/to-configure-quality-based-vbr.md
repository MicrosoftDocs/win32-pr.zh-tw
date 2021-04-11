---
title: 設定 Quality-Based VBR
description: 設定 Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- 串流，設定 VBR 資料流程
- '資料流程、變數位元速率 (VBR) '
- 變數位速率 (VBR) ，資料流程
- VBR (變數位速率) ，資料流程
- 串流，設定以品質為基礎的 VBR
- 變數位元速率 (VBR) ，設定品質型
- VBR (變數位元速率) ，設定品質型
- 設定檔，設定以品質為基礎的 VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103933004"
---
# <a name="to-configure-quality-based-vbr"></a><span data-ttu-id="6bb1b-111">設定 Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="6bb1b-111">To Configure Quality-Based VBR</span></span>

<span data-ttu-id="6bb1b-112">您可以在資料流程上使用以品質為基礎的變數位元速率 (VBR) 編碼方式，以指定將針對整個資料流程維護的品質等級，不論產生的位元速率需求為何。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-112">You can use quality-based variable bit rate (VBR) encoding on a stream to specify a quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>

<span data-ttu-id="6bb1b-113">針對品質型的 VBR 影片串流，您必須指定從1到100的品質等級，100表示最高品質。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-113">For quality-based VBR video streams, you must specify a quality level from 1 to 100, with 100 representing the highest quality.</span></span> <span data-ttu-id="6bb1b-114">目前只有30個離散品質設定。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-114">At present there are only 30 discrete quality settings.</span></span> <span data-ttu-id="6bb1b-115">下列品質層級等於離散品質設定：1、4、8、11、15、18、22、25、29、33、36、40、43、47、50、54、58、61、65、68、72、75、79、83、86、90、93、97。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-115">The following quality levels equate to discrete quality settings: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span></span> <span data-ttu-id="6bb1b-116">上述清單中兩個連續值之間的數位，會等於與較低數位相同的品質設定。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-116">Numbers between two consecutive values in the preceding list equate to the same quality setting as the lower number.</span></span> <span data-ttu-id="6bb1b-117">例如，系統會列出1和4，因此2和3兩者都會產生與1相同的品質設定。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-117">For example, 1 and 4 are listed, so 2 and 3 both result in the same quality setting as 1.</span></span>

<span data-ttu-id="6bb1b-118">針對音訊串流，您可以列舉可用的模式並取出串流設定物件。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-118">For audio streams, you can enumerate the available modes and retrieve a stream configuration object.</span></span> <span data-ttu-id="6bb1b-119">如需詳細資訊，請參閱 [列舉編解碼器格式](to-enumerate-codec-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-119">For more information, see [To Enumerate Codec Formats](to-enumerate-codec-formats.md).</span></span>

<span data-ttu-id="6bb1b-120">使用以品質為基礎的 VBR 影片時，您必須將 [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)結構的 **dwBitrate** 成員設為正值。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-120">When using quality-based VBR video, you must set the **dwBitrate** member of the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to a positive value.</span></span> <span data-ttu-id="6bb1b-121">寫入器不會使用這個值，但傳遞零或負數可能會在寫入時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-121">This value is not used by the writer, but passing zero or a negative number can cause errors when writing.</span></span>

<span data-ttu-id="6bb1b-122">若要在設定檔中設定串流以以品質為基礎的 VBR 進行編碼，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-122">To configure a stream in a profile to be encoded with quality-based VBR, perform the following steps.</span></span>

1.  <span data-ttu-id="6bb1b-123">藉由呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數來建立配置檔案管理員物件。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-123">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="6bb1b-124">開啟您要新增 VBR 支援的現有設定檔。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-124">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="6bb1b-125">如需開啟設定檔的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-125">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="6bb1b-126">藉由呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) 或 [**IWMProfile：： GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)，取得您想要使用之資料流程的資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-126">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="6bb1b-127">藉由呼叫 **IWMStreamConfig：： QueryInterface**，取得資料流程設定物件之 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-127">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="6bb1b-128">針對 **g \_ wszVBREnabled** 屬性呼叫 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) ，為數據流啟用 VBR。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-128">Enable VBR for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="6bb1b-129">針對 **g \_ wszVBRQuality** 屬性呼叫 **IWMPropertyVault：： SETPROPERTY** ，以設定 VBR 資料流程的品質等級。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-129">Set the quality level for the VBR stream by calling **IWMPropertyVault::SetProperty** for the **g\_wszVBRQuality** property.</span></span>
7.  <span data-ttu-id="6bb1b-130">使用 **IWMPropertyVault：： SetProperty** 將 **g \_ wszVBRBitrateMax** 和 **g \_ wszVBRBufferWindowMax** 兩者都設定為零。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-130">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
8.  <span data-ttu-id="6bb1b-131">藉由呼叫 [**IWMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)，儲存對資料流程所做的變更。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-131">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
9.  <span data-ttu-id="6bb1b-132">儲存設定檔，或將其傳遞至寫入器物件，然後開始撰寫。</span><span class="sxs-lookup"><span data-stu-id="6bb1b-132">Save the profile, or pass it to the writer object and start writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bb1b-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="6bb1b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bb1b-134">**設定 VBR 資料流程**</span><span class="sxs-lookup"><span data-stu-id="6bb1b-134">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




