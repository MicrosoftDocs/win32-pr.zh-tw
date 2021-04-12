---
description: 使用限制領域
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: 使用限制領域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16f57de7642fa789a08c886a32bf906faffb72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317964"
---
# <a name="field-of-use-restrictions"></a><span data-ttu-id="577f3-103">使用限制領域</span><span class="sxs-lookup"><span data-stu-id="577f3-103">Field of Use Restrictions</span></span>

> [!Note]  
> <span data-ttu-id="577f3-104">本主題適用于 Windows 7 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="577f3-104">This topic applies to Windows 7 or later.</span></span>

 

<span data-ttu-id="577f3-105">*使用* 規定限制是一種規定，可限制特定技術授權的使用方式。</span><span class="sxs-lookup"><span data-stu-id="577f3-105">A *field-of-use* restriction is a provision that limits how a license for a particular technology can be used.</span></span>

<span data-ttu-id="577f3-106">媒體基礎提供一種機制，可在媒體基礎轉換 (MFTs) （特別是編解碼器）上強制執行限制的限制。</span><span class="sxs-lookup"><span data-stu-id="577f3-106">Media Foundation provides a mechanism for enforcing field-of-use restrictions on Media Foundation transforms (MFTs), particularly codecs.</span></span> <span data-ttu-id="577f3-107">這項機制需要使用 MFT 來封鎖應用程式的使用，直到應用程式執行與 MFT 之間的交握為止。</span><span class="sxs-lookup"><span data-stu-id="577f3-107">This mechanism requires the MFT to block its own use by applications until the application has performed a handshake with the MFT.</span></span> <span data-ttu-id="577f3-108">媒體基礎不會定義交握，通常會牽涉到某種類型的密碼編譯交換。</span><span class="sxs-lookup"><span data-stu-id="577f3-108">Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

### <a name="registration-and-enumeration"></a><span data-ttu-id="577f3-109">註冊和列舉</span><span class="sxs-lookup"><span data-stu-id="577f3-109">Registration and Enumeration</span></span>

<span data-ttu-id="577f3-110">如果某個 MFT 有使用中的限制，請在您註冊 MFT 時設定 **mft \_ 列舉 \_ 旗標 \_ FIELDOFUSE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="577f3-110">If an MFT has field-of-use restrictions, set the **MFT\_ENUM\_FLAG\_FIELDOFUSE** flag when you register the MFT.</span></span> <span data-ttu-id="577f3-111">此旗標適用于下列的 MFT 註冊 Api：</span><span class="sxs-lookup"><span data-stu-id="577f3-111">This flag applies to the following MFT registration APIs:</span></span>

-   [<span data-ttu-id="577f3-112">**MFTRegister**</span><span class="sxs-lookup"><span data-stu-id="577f3-112">**MFTRegister**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [<span data-ttu-id="577f3-113">**MFTRegisterLocal**</span><span class="sxs-lookup"><span data-stu-id="577f3-113">**MFTRegisterLocal**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [<span data-ttu-id="577f3-114">**MFTRegisterLocalByCLSID**</span><span class="sxs-lookup"><span data-stu-id="577f3-114">**MFTRegisterLocalByCLSID**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [<span data-ttu-id="577f3-115">**IMFLocalMFTRegistration::RegisterMFTs**</span><span class="sxs-lookup"><span data-stu-id="577f3-115">**IMFLocalMFTRegistration::RegisterMFTs**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

<span data-ttu-id="577f3-116">根據預設，使用此旗標注冊的 MFTs 會從列舉結果中排除。</span><span class="sxs-lookup"><span data-stu-id="577f3-116">By default, MFTs registered with this flag are excluded from enumeration results.</span></span> <span data-ttu-id="577f3-117">若要以使用中的限制列舉 MFTs，請呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 並在 Flags 參數中指定 **MFT \_ 列舉 \_ 旗標 \_ FIELDOFUSE** 旗 *標* 。</span><span class="sxs-lookup"><span data-stu-id="577f3-117">To enumerate MFTs with field-of-use restrictions, call [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) and specify the **MFT\_ENUM\_FLAG\_FIELDOFUSE** flag in the *Flags* parameter.</span></span> <span data-ttu-id="577f3-118">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="577f3-118">The following diagram illustrates this process.</span></span>

![顯示 mft 和應用程式將資料傳送至登錄的圖表](images/mft-fou01.gif)

<span data-ttu-id="577f3-120">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)函數一律會排除具有使用規定限制的任何 MFTs。</span><span class="sxs-lookup"><span data-stu-id="577f3-120">The [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function always excludes any MFTs that have field-of-use restrictions.</span></span>

### <a name="unlocking-the-mft"></a><span data-ttu-id="577f3-121">解除鎖定 MFT</span><span class="sxs-lookup"><span data-stu-id="577f3-121">Unlocking the MFT</span></span>

<span data-ttu-id="577f3-122">若要搭配使用具有欄位限制的 MFT，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="577f3-122">To use an MFT with field-of-use restrictions, perform the following steps:</span></span>

1.  <span data-ttu-id="577f3-123">應用程式會執行 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 介面。</span><span class="sxs-lookup"><span data-stu-id="577f3-123">The application implements the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface.</span></span>
2.  <span data-ttu-id="577f3-124">[**IMFFieldOfUseMFTUnlock：： Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock)方法會接受對 MFT 之 **IUnknown** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="577f3-124">The [**IMFFieldOfUseMFTUnlock::Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) method takes a pointer to the **IUnknown** interface of the MFT.</span></span>
3.  <span data-ttu-id="577f3-125">在 [**解除鎖定**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) 方法中，應用程式會使用由 MFT 定義的任何機制來執行所需的交握。</span><span class="sxs-lookup"><span data-stu-id="577f3-125">In the [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) method, the application performs the required handshake, using whatever mechanism is defined by the MFT.</span></span> <span data-ttu-id="577f3-126">媒體基礎 API 不會定義此步驟。</span><span class="sxs-lookup"><span data-stu-id="577f3-126">This step is not defined by Media Foundation API.</span></span>
4.  <span data-ttu-id="577f3-127">如果 [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) 方法成功，則是由 MFT 解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="577f3-127">If the [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) method succeeds, the MFT unlocks itself.</span></span>

<span data-ttu-id="577f3-128">應用程式會藉由設定 [MFT \_ FIELDOFUSE \_ UNLOCK \_ Attribute](mft-fieldofuse-unlock-attribute.md)屬性來指定 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)指標。</span><span class="sxs-lookup"><span data-stu-id="577f3-128">The application specifies the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer by setting the [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span> <span data-ttu-id="577f3-129">有幾種不同的方式可以設定此屬性，端視您的應用程式建立解碼器或編碼管線的方式而定：</span><span class="sxs-lookup"><span data-stu-id="577f3-129">There are several different ways to set this attribute, depending on how your application creates the decoder or encoding pipeline:</span></span>



| <span data-ttu-id="577f3-130">API</span><span class="sxs-lookup"><span data-stu-id="577f3-130">API</span></span>                   | <span data-ttu-id="577f3-131">如何解除鎖定使用中的欄位</span><span class="sxs-lookup"><span data-stu-id="577f3-131">How to Unlock Field-Of-Use</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="577f3-132">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="577f3-132">Source Reader</span></span>         | <span data-ttu-id="577f3-133">如果您的應用程式使用 [來源讀取器](source-reader.md) 來解碼媒體檔案，請在設定參數中設定 [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="577f3-133">If your application uses the [Source Reader](source-reader.md) to decode a media file, set the [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute in the configuration parameters.</span></span> <span data-ttu-id="577f3-134">請參閱 [來源讀取器屬性](source-reader-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="577f3-134">See [Source Reader Attributes](source-reader-attributes.md).</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="577f3-135">接收寫入器</span><span class="sxs-lookup"><span data-stu-id="577f3-135">Sink Writer</span></span>           | <span data-ttu-id="577f3-136">如果您的應用程式使用接收寫入器來編碼媒體檔案，請在設定參數中設定 [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="577f3-136">If your application uses the sink writer to encode a media file, set the [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute in the configuration parameters.</span></span> <span data-ttu-id="577f3-137">請參閱 [接收寫入器屬性](sink-writer-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="577f3-137">See [Sink Writer Attributes](sink-writer-attributes.md).</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="577f3-138">快速轉碼</span><span class="sxs-lookup"><span data-stu-id="577f3-138">Fast Transcode</span></span>        | <span data-ttu-id="577f3-139">如果您的應用程式使用快速轉碼功能來建立編碼拓撲，請在呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)時設定 [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="577f3-139">If your application uses the Fast Transcode feature to create an encoding topology, set the [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) when you call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span> <span data-ttu-id="577f3-140">如需快速轉碼功能的詳細資訊，請參閱 [轉碼 API](transcode-api.md)。</span><span class="sxs-lookup"><span data-stu-id="577f3-140">For more information about the Fast Transcode feature, see [Transcode API](transcode-api.md).</span></span>                                                                                                                                                                      |
| <span data-ttu-id="577f3-141">拓撲</span><span class="sxs-lookup"><span data-stu-id="577f3-141">Topology</span></span>              | <span data-ttu-id="577f3-142">如果您直接建立拓撲，請將 [ [MFT \_ FIELDOFUSE \_ 解除鎖定] \_ 屬性](mft-fieldofuse-unlock-attribute.md) 設定為拓撲上的屬性。</span><span class="sxs-lookup"><span data-stu-id="577f3-142">If you create a topology directly, set the [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) as an attribute on the topology.</span></span> <span data-ttu-id="577f3-143">請參閱 [拓撲屬性](topology-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="577f3-143">See [Topology Attributes](topology-attributes.md).</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="577f3-144">MFT 啟用物件</span><span class="sxs-lookup"><span data-stu-id="577f3-144">MFT Activation Object</span></span> | <span data-ttu-id="577f3-145">如果您的應用程式直接列舉將使用的解碼器或編碼器，請在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定 [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="577f3-145">If your application directly enumerates the decoders or encoders that it will use, set the [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <br/> <span data-ttu-id="577f3-146">先設定屬性再呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ，以建立 MFT。</span><span class="sxs-lookup"><span data-stu-id="577f3-146">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the MFT.</span></span> <span data-ttu-id="577f3-147">啟始物件會在建立 MFT 時呼叫 [**IMFFieldOfUseMFTUnlock：： Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) 。</span><span class="sxs-lookup"><span data-stu-id="577f3-147">The activation object calls [**IMFFieldOfUseMFTUnlock::Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) when it creates the MFT.</span></span><br/> |



 

<span data-ttu-id="577f3-148">下圖顯示 MFT 啟用物件和 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 介面之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="577f3-148">The following diagram shows the relation between MFT activation objects and the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface.</span></span>

![此圖顯示應用程式、啟用物件和包含箭號給 fou ... 物件的 mft，此物件的箭號會傳回給 mft](images/mft-fou02.gif)

## <a name="related-topics"></a><span data-ttu-id="577f3-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="577f3-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="577f3-151">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="577f3-151">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




