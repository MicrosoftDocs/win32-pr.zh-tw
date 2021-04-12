---
description: 設定編解碼器 MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: 設定編解碼器 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468636"
---
# <a name="configuring-codec-mfts"></a><span data-ttu-id="94fea-103">設定編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="94fea-103">Configuring Codec MFTs</span></span>

<span data-ttu-id="94fea-104">本主題說明設定編解碼器 MFTs 的流程。</span><span class="sxs-lookup"><span data-stu-id="94fea-104">This topic describes the process of configuring the codec MFTs.</span></span> <span data-ttu-id="94fea-105">每個編解碼器都有特定的程式，但此處所述的全部資訊都有提供。</span><span class="sxs-lookup"><span data-stu-id="94fea-105">Each codec has specific procedures, but the information common to all is described here.</span></span>

## <a name="configuring-mft-inputs-and-outputs"></a><span data-ttu-id="94fea-106">設定 MFT 輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="94fea-106">Configuring MFT Inputs and Outputs</span></span>

<span data-ttu-id="94fea-107">每個 MFT 都支援特定的輸入和輸出類型。</span><span class="sxs-lookup"><span data-stu-id="94fea-107">Every MFT supports specific input and output types.</span></span> <span data-ttu-id="94fea-108">您可以藉由重複呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)來取得支援的輸入類型，並以每個呼叫遞增類型索引。</span><span class="sxs-lookup"><span data-stu-id="94fea-108">You can retrieve supported input types by repeatedly calling [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementing the type index with each call.</span></span> <span data-ttu-id="94fea-109">當您找到適當的類型時，請呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)來設定輸入類型。</span><span class="sxs-lookup"><span data-stu-id="94fea-109">When you find an appropriate type, set the input type by calling [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span> <span data-ttu-id="94fea-110">然後，您可以使用呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 和 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)，針對輸出類型重複此程式。</span><span class="sxs-lookup"><span data-stu-id="94fea-110">You can then repeat the process for the output type using the calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) and [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="94fea-111">您必須在設定輸入類型之後，才查詢或設定可用的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="94fea-111">You must query or set the available output types only after setting the input type.</span></span>

## <a name="configuring-the-codec-mfts-for-encoding"></a><span data-ttu-id="94fea-112">設定編碼的編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="94fea-112">Configuring the Codec MFTs for Encoding</span></span>

<span data-ttu-id="94fea-113">所有的 Windows Media 音訊和影片編解碼器都支援各種不同的編碼功能。</span><span class="sxs-lookup"><span data-stu-id="94fea-113">All of the Windows Media Audio and Video codecs support a variety of encoding features.</span></span> <span data-ttu-id="94fea-114">這些功能通常是藉由使用 **IPropertyStore** 介面的方法，在 MFT 上設定屬性來設定。</span><span class="sxs-lookup"><span data-stu-id="94fea-114">These features are generally configured by setting properties on the MFT by using the methods of the **IPropertyStore** interface.</span></span> <span data-ttu-id="94fea-115">有些屬性是使用特製化的編解碼器介面進行設定。</span><span class="sxs-lookup"><span data-stu-id="94fea-115">Some properties are configured using specialized codec interfaces.</span></span> <span data-ttu-id="94fea-116">在 [編解碼器物件](codecobjects.md)的區段中，會列出每個編解碼器的這些介面。</span><span class="sxs-lookup"><span data-stu-id="94fea-116">These interfaces are listed for each codec in the section [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="94fea-117">設定編碼 MFT 的一般作業順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="94fea-117">The general order of operations for configuring an encoding MFT is as follows:</span></span>

1.  <span data-ttu-id="94fea-118">使用 **IPropertyStore** 的方法來設定所需的編解碼器功能。</span><span class="sxs-lookup"><span data-stu-id="94fea-118">Configure codec features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="94fea-119">如有需要，請使用編解碼器 MFT 介面來設定其他功能。</span><span class="sxs-lookup"><span data-stu-id="94fea-119">Use the codec MFT interfaces to configure additional features, if needed.</span></span>
3.  <span data-ttu-id="94fea-120">設定輸入和輸出類型。</span><span class="sxs-lookup"><span data-stu-id="94fea-120">Configure the input and output types.</span></span> <span data-ttu-id="94fea-121">設定類型的順序會因個別編解碼器而異。</span><span class="sxs-lookup"><span data-stu-id="94fea-121">The order in which the types should be configured varies for individual codecs.</span></span> <span data-ttu-id="94fea-122">如需詳細資訊，請參閱使用 [音訊](workingwithaudio.md) 和使用 [影片](workingwithvideo.md)。</span><span class="sxs-lookup"><span data-stu-id="94fea-122">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

## <a name="configuring-the-codec-mfts-for-decoding"></a><span data-ttu-id="94fea-123">設定編解碼器 MFTs 進行解碼</span><span class="sxs-lookup"><span data-stu-id="94fea-123">Configuring the Codec MFTs for Decoding</span></span>

<span data-ttu-id="94fea-124">解碼比編碼更簡單，因為支援的解碼器功能較少。</span><span class="sxs-lookup"><span data-stu-id="94fea-124">Decoding is simpler than encoding, as fewer decoder features are supported.</span></span>

<span data-ttu-id="94fea-125">設定解碼 MFT 的一般作業順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="94fea-125">The general order of operations for configuring a decoding MFT is as follows:</span></span>

1.  <span data-ttu-id="94fea-126">使用 **IPropertyStore** 的方法來設定所需的解碼器功能。</span><span class="sxs-lookup"><span data-stu-id="94fea-126">Configure decoder features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="94fea-127">將輸入類型設定為用於編碼器輸出的類型。</span><span class="sxs-lookup"><span data-stu-id="94fea-127">Set the input type to the type used for the encoder output.</span></span>
3.  <span data-ttu-id="94fea-128">設定輸出類型。</span><span class="sxs-lookup"><span data-stu-id="94fea-128">Configure the output type.</span></span> <span data-ttu-id="94fea-129">針對不同的輸入，支援的輸出類型是不同的。</span><span class="sxs-lookup"><span data-stu-id="94fea-129">The supported output types are different for different inputs.</span></span>

> [!Note]  
> <span data-ttu-id="94fea-130">請務必將相同的媒體類型用於編碼器輸入，如同用於編碼器輸出一樣。</span><span class="sxs-lookup"><span data-stu-id="94fea-130">It is important to use the same media type for the decoder input as was used for the encoder output.</span></span> <span data-ttu-id="94fea-131">這是因為 Windows Media 音訊和影片編解碼器使用媒體格式搭配額外的資料。</span><span class="sxs-lookup"><span data-stu-id="94fea-131">This is because the Windows Media Audio and Video codecs use media formats with extra data.</span></span> <span data-ttu-id="94fea-132">如果沒有延伸格式資料，您就無法將壓縮的內容解碼。</span><span class="sxs-lookup"><span data-stu-id="94fea-132">Without the extended format data, you cannot decode the compressed content.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="94fea-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="94fea-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94fea-134">使用編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="94fea-134">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



