---
title: 所有資料流程通用的設定
description: 所有資料流程通用的設定
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- 設定檔，所有資料流程通用的設定
- 資料流程，一般設定
- 資料流程，名稱
- 資料流程，連接名稱
- 資料流程、數位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104374849"
---
# <a name="configuration-common-to-all-streams"></a><span data-ttu-id="807f9-108">所有資料流程通用的設定</span><span class="sxs-lookup"><span data-stu-id="807f9-108">Configuration Common to All Streams</span></span>

<span data-ttu-id="807f9-109">無論何種類型，所有的資料流程都應該指派資料流程名稱、連接名稱和資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="807f9-109">All streams, regardless of type, should be assigned a stream name, a connection name, and a stream number.</span></span>

<span data-ttu-id="807f9-110">資料流程名稱只是您指派給資料流程的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="807f9-110">The stream name is simply a descriptive name you assign to the stream.</span></span> <span data-ttu-id="807f9-111">資料流程不需要有資料流程名稱，但它可在稍後編輯設定檔時，協助您識別該資料流程。</span><span class="sxs-lookup"><span data-stu-id="807f9-111">A stream does not need to have a stream name, but it helps you to identify the stream when editing the profile at a later time.</span></span> <span data-ttu-id="807f9-112">您可以藉由呼叫 [**IWMStreamConfig：： SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname)來設定資料流程的名稱。</span><span class="sxs-lookup"><span data-stu-id="807f9-112">You can set a name for the stream by calling [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span></span>

<span data-ttu-id="807f9-113">每個資料流程都應該有連接名稱，也稱為輸入名稱。</span><span class="sxs-lookup"><span data-stu-id="807f9-113">Every stream should have a connection name, also called an input name.</span></span> <span data-ttu-id="807f9-114">當您將寫入器物件中的設定檔設定為寫入檔案時，寫入器會將每個連接名稱與輸入產生關聯。</span><span class="sxs-lookup"><span data-stu-id="807f9-114">When you set the profile in the writer object to write a file, the writer will associate each connection name with an input.</span></span> <span data-ttu-id="807f9-115">若要識別輸入，您必須呼叫 [**IWMInputMediaProps：： GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) 來取出連接名稱。</span><span class="sxs-lookup"><span data-stu-id="807f9-115">To identify the inputs, you must call [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) to retrieve the connection name.</span></span> <span data-ttu-id="807f9-116">一般連接名稱是內容的簡單描述，例如「音訊」。</span><span class="sxs-lookup"><span data-stu-id="807f9-116">Typical connection names are simple descriptions of the content, such as "audio".</span></span> <span data-ttu-id="807f9-117">如果您的設定檔包含以位元速率互斥的資料流程，每個互斥資料流程都必須有相同的連接名稱。</span><span class="sxs-lookup"><span data-stu-id="807f9-117">If your profile contains streams that are mutually exclusive by bit rate, each of the mutually exclusive streams must have the same connection name.</span></span> <span data-ttu-id="807f9-118">如果不是，則設定檔無效，寫入器將會拒絕此設定檔。</span><span class="sxs-lookup"><span data-stu-id="807f9-118">If they do not, the profile is invalid and will be rejected by the writer.</span></span> <span data-ttu-id="807f9-119">您可以藉由呼叫 [**IWMStreamConfig：： SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname)來設定連接名稱。</span><span class="sxs-lookup"><span data-stu-id="807f9-119">You can set a connection name by calling [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span></span>

<span data-ttu-id="807f9-120">資料流程號碼會識別檔案內的資料流程。</span><span class="sxs-lookup"><span data-stu-id="807f9-120">The stream number identifies the stream within the file.</span></span> <span data-ttu-id="807f9-121">不同于輸入編號和輸出編號，資料流程號碼從1開始，而不是0。</span><span class="sxs-lookup"><span data-stu-id="807f9-121">Unlike input numbers and output numbers, stream numbers start at 1, not 0.</span></span> <span data-ttu-id="807f9-122">資料流程號碼與資料流程索引不同，您在使用 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)取得設定檔中的資料流程時，會使用此索引。</span><span class="sxs-lookup"><span data-stu-id="807f9-122">A stream number is different than a stream index, which you use when getting streams in a profile by using [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span> <span data-ttu-id="807f9-123">資料流程索引是由設定檔物件指派給資料流程的數位。</span><span class="sxs-lookup"><span data-stu-id="807f9-123">The stream index is a number assigned to the stream by the profile object.</span></span> <span data-ttu-id="807f9-124">資料流程索引的範圍介於0到1之間，且小於 [**IWMProfile：： GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount)所抓取的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="807f9-124">Stream indexes range between 0 and one less than the number of streams retrieved by [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span></span> <span data-ttu-id="807f9-125">資料流程號碼不需要是連續的，但它們通常都是，而且範圍可以從1到63。</span><span class="sxs-lookup"><span data-stu-id="807f9-125">Stream numbers need not be sequential, though they usually are, and can range from 1 to 63.</span></span> <span data-ttu-id="807f9-126">您可以藉由呼叫 [**IWMStreamConfig：： SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber)來設定串流號碼。</span><span class="sxs-lookup"><span data-stu-id="807f9-126">You can set a stream number by calling [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span></span>

## <a name="related-topics"></a><span data-ttu-id="807f9-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="807f9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="807f9-128">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="807f9-128">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="807f9-129">**輸入、串流和輸出**</span><span class="sxs-lookup"><span data-stu-id="807f9-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




