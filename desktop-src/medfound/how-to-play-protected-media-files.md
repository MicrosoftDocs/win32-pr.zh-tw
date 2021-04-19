---
description: 如何播放包含受 DRM 保護之媒體的檔案。
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: 如何播放受保護的媒體檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986670"
---
# <a name="how-to-play-protected-media-files"></a><span data-ttu-id="33943-103">如何播放受保護的媒體檔案</span><span class="sxs-lookup"><span data-stu-id="33943-103">How to Play Protected Media Files</span></span>

<span data-ttu-id="33943-104">受保護的媒體檔案是具有使用內容之相關規則的任何媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="33943-104">A protected media file is any media file that has associated rules for using the content.</span></span> <span data-ttu-id="33943-105">在某些情況下，受保護的媒體檔案會使用某種形式的數位版權管理 (DRM) 加密來加密。</span><span class="sxs-lookup"><span data-stu-id="33943-105">In some cases, a protected media file is encrypted using some form of digital rights management (DRM) encryption.</span></span> <span data-ttu-id="33943-106">若要播放受保護的媒體檔案，播放必須在受保護的媒體路徑內進行 (PMP) 。</span><span class="sxs-lookup"><span data-stu-id="33943-106">To play a protected media file, playback must occur inside the protected media path (PMP).</span></span> <span data-ttu-id="33943-107">此外，使用者可能必須取得內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="33943-107">In addition, the user might have to acquire rights to the content.</span></span>

<span data-ttu-id="33943-108">「權利取得」（rights）是指應用程式在使用者可以播放內容之前必須執行的任何動作。</span><span class="sxs-lookup"><span data-stu-id="33943-108">The term rights acquisition refers to any action that the application must perform before the user can play the content.</span></span> <span data-ttu-id="33943-109">最常見的範例是取得 DRM 授權，但是媒體基礎定義可支援其他許可權取得類型的一般機制。</span><span class="sxs-lookup"><span data-stu-id="33943-109">The most common example is obtaining a DRM license, but Media Foundation defines a generic mechanism that can support other types of rights acquisition.</span></span> <span data-ttu-id="33943-110">[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)介面會定義此泛型機制。</span><span class="sxs-lookup"><span data-stu-id="33943-110">The [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface defines this generic mechanism.</span></span>

<span data-ttu-id="33943-111">您必須從應用程式進程，在 PMP 之外完成許可權取得。</span><span class="sxs-lookup"><span data-stu-id="33943-111">Rights acquisition must be done outside of the PMP, from the application process.</span></span> <span data-ttu-id="33943-112">媒體會話會透過應用程式所執行的 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) 介面，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="33943-112">The Media Session notifies the application through the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface, which is implemented by the application.</span></span> <span data-ttu-id="33943-113">媒體會話會使用 **IMFContentProtectionManager** 介面，將內容啟用程式物件轉送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="33943-113">The Media Session uses the **IMFContentProtectionManager** interface to forward a content enabler object to the application.</span></span> <span data-ttu-id="33943-114">內容啟用會執行 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面。</span><span class="sxs-lookup"><span data-stu-id="33943-114">Content enablers implement the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="33943-115">應用程式會使用此介面來取得必要的許可權。</span><span class="sxs-lookup"><span data-stu-id="33943-115">The application uses this interface to acquire the necessary rights.</span></span>

<span data-ttu-id="33943-116">內容啟用程式可能支援自動取得許可權，在這種情況下，內容啟用程式會執行整個進程，而應用程式只會監視狀態。</span><span class="sxs-lookup"><span data-stu-id="33943-116">A content enabler might support automatic rights acquisition, in which case the content enabler implements the entire process, and the application simply monitors the status.</span></span> <span data-ttu-id="33943-117">否則，應用程式必須使用非無訊息的許可權取得，也就是應用程式會將 HTTP POST 資料傳送到內容啟用程式所提供的 URL。</span><span class="sxs-lookup"><span data-stu-id="33943-117">Otherwise, the application must use non-silent rights acquisition, which is a process where the application sends HTTP POST data to a URL provided by the content enabler.</span></span>

<span data-ttu-id="33943-118">若要播放受保護的媒體，應用程式會遵循與 [如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案中的相同步驟，並提供下列額外步驟：</span><span class="sxs-lookup"><span data-stu-id="33943-118">To play protected media, an application follows the same steps given in the topic [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), with the following additional steps:</span></span>

1.  <span data-ttu-id="33943-119">查詢媒體來源是否包含受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="33943-119">Query whether the media source contains protected content.</span></span> <span data-ttu-id="33943-120">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="33943-120">(Optional.)</span></span>
2.  <span data-ttu-id="33943-121">在 PMP 程式中建立媒體會話，而不是應用程式進程。</span><span class="sxs-lookup"><span data-stu-id="33943-121">Create the Media Session in the PMP process, instead of the application process.</span></span>
3.  <span data-ttu-id="33943-122">如果媒體會話通知您，請執行取得許可權。</span><span class="sxs-lookup"><span data-stu-id="33943-122">Perform rights acquisition, if notified to do so by the Media Session.</span></span> <span data-ttu-id="33943-123">這項作業是由應用程式以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="33943-123">This operation is performed asynchronously by the application.</span></span>
4.  <span data-ttu-id="33943-124">完成非同步作業。</span><span class="sxs-lookup"><span data-stu-id="33943-124">Complete the asynchronous operation.</span></span>

## <a name="query-for-protected-content"></a><span data-ttu-id="33943-125">查詢受保護的內容</span><span class="sxs-lookup"><span data-stu-id="33943-125">Query for Protected Content</span></span>

<span data-ttu-id="33943-126">若要查詢媒體來源是否包含受保護的內容，請在媒體來源的展示描述項上呼叫 [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) 函式。</span><span class="sxs-lookup"><span data-stu-id="33943-126">To query whether a media source contains protected content, call the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function on the media source's presentation descriptor.</span></span> <span data-ttu-id="33943-127">如果函式傳回 S \_ OK，您必須使用 PMP 來播放內容。</span><span class="sxs-lookup"><span data-stu-id="33943-127">If the function returns S\_OK, you must use the PMP to play the content.</span></span> <span data-ttu-id="33943-128">如果函式傳回 \_ FALSE，則不需要 PMP，而且您可以在應用程式進程中建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="33943-128">If the function returns S\_FALSE, the PMP is not required, and you can create the Media Session in the application process.</span></span> <span data-ttu-id="33943-129">或者，您也可以使用 PMP 來播放這兩種類型的內容：受保護和未受保護。</span><span class="sxs-lookup"><span data-stu-id="33943-129">Alternatively, you can use the PMP to play both types of content, protected and unprotected.</span></span> <span data-ttu-id="33943-130">如果您這麼做，就不需要呼叫 **MFRequireProtectedEnvironment**。</span><span class="sxs-lookup"><span data-stu-id="33943-130">If you do that, you do not need to call **MFRequireProtectedEnvironment**.</span></span>

<span data-ttu-id="33943-131">如需簡報描述項的詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。</span><span class="sxs-lookup"><span data-stu-id="33943-131">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

## <a name="create-the-pmp-media-session"></a><span data-ttu-id="33943-132">建立 PMP 媒體會話</span><span class="sxs-lookup"><span data-stu-id="33943-132">Create the PMP Media Session</span></span>

<span data-ttu-id="33943-133">若要在 PMP 中建立媒體會話，請呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)。</span><span class="sxs-lookup"><span data-stu-id="33943-133">To create the Media Session in the PMP, call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="33943-134">此函式類似于 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)，但不會在應用程式的進程中建立媒體會話，而是在 PMP 進程中建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="33943-134">This function is similar to [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), but instead of creating the Media Session in the application's process, it creates the Media Session in the PMP process.</span></span> <span data-ttu-id="33943-135">應用程式會接收媒體會話的 proxy 物件指標。</span><span class="sxs-lookup"><span data-stu-id="33943-135">The application receives a pointer to a proxy object for the Media Session.</span></span> <span data-ttu-id="33943-136">應用程式會在 proxy 物件上呼叫 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 方法，就像在媒體會話一樣。</span><span class="sxs-lookup"><span data-stu-id="33943-136">The application calls [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods on the proxy object, just as it would on the Media Session.</span></span> <span data-ttu-id="33943-137">Proxy 物件會將呼叫轉送到跨進程界限的媒體會話。</span><span class="sxs-lookup"><span data-stu-id="33943-137">The proxy object forwards the calls to the Media Session across the process boundary.</span></span>

<span data-ttu-id="33943-138">建立 PMP 媒體會話，如下所示：</span><span class="sxs-lookup"><span data-stu-id="33943-138">Create the PMP Media Session as follows:</span></span>

1.  <span data-ttu-id="33943-139">藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="33943-139">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="33943-140">在屬性存放區上設定 [ [**MF \_ 會話 \_ 內容 \_ 保護 \_ 管理員**](mf-session-content-protection-manager-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="33943-140">Set the [**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**](mf-session-content-protection-manager-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="33943-141">這個屬性的值是應用程式的 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)執行指標。</span><span class="sxs-lookup"><span data-stu-id="33943-141">The value of this attribute is a pointer to your application's implementation of [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span></span> <span data-ttu-id="33943-142">呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) 來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="33943-142">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the attribute.</span></span>
3.  <span data-ttu-id="33943-143">呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) ，以在 PMP 進程中建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="33943-143">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session in the PMP process.</span></span> <span data-ttu-id="33943-144">*PConfiguration* 參數是屬性存放區的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標。</span><span class="sxs-lookup"><span data-stu-id="33943-144">The *pConfiguration* parameter is a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the attribute store.</span></span>


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



<span data-ttu-id="33943-145">接下來，建立播放拓撲並在媒體會話上將它排入佇列，如 [建立播放拓撲](creating-playback-topologies.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="33943-145">Next, create a playback topology and queue it on the Media Session, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

## <a name="perform-rights-acquisition"></a><span data-ttu-id="33943-146">執行許可權取得</span><span class="sxs-lookup"><span data-stu-id="33943-146">Perform Rights Acquisition</span></span>

<span data-ttu-id="33943-147">如果播放需要取得許可權，媒體會話就會呼叫 [**IMFContentProtectionManager：： BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)。</span><span class="sxs-lookup"><span data-stu-id="33943-147">If playback requires rights acquisition, the Media Session calls [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="33943-148">這個方法的 *pEnablerActivate* 參數是 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="33943-148">The *pEnablerActivate* parameter of this method is a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="33943-149">使用此介面來建立內容啟用程式物件，此物件會公開 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面。</span><span class="sxs-lookup"><span data-stu-id="33943-149">Use this interface to create the content enabler object, which exposes the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="33943-150">然後使用內容啟用程式來執行「許可權取得」步驟。</span><span class="sxs-lookup"><span data-stu-id="33943-150">Then use the content enabler to perform the rights acquisition step.</span></span>

<span data-ttu-id="33943-151">若要建立內容啟用程式，請呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)：</span><span class="sxs-lookup"><span data-stu-id="33943-151">To create the content enabler, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span></span>


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



<span data-ttu-id="33943-152">查詢所傳回的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)介面 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)指標。</span><span class="sxs-lookup"><span data-stu-id="33943-152">Query the returned [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pointer for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="33943-153">使用這個介面從內容啟用程式物件取得事件。</span><span class="sxs-lookup"><span data-stu-id="33943-153">Use this interface to get events from the content enabler object.</span></span> <span data-ttu-id="33943-154">如需事件的詳細資訊，請參閱 [媒體事件](media-event-generators.md)產生器。</span><span class="sxs-lookup"><span data-stu-id="33943-154">For more information about events, see [Media Event Generators](media-event-generators.md).</span></span>

<span data-ttu-id="33943-155">若要瞭解內容啟用程式是否支援自動取得，請呼叫 [**IMFContentEnabler：： IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported)。</span><span class="sxs-lookup"><span data-stu-id="33943-155">To find out whether the content enabler supports automatic acquisition, call [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span></span> <span data-ttu-id="33943-156">如果這個方法傳回 **TRUE** 值，則應用程式應該使用自動取得。</span><span class="sxs-lookup"><span data-stu-id="33943-156">If this method returns the value **TRUE**, the application should use automatic acquisition.</span></span> <span data-ttu-id="33943-157">否則，請使用非無訊息的取得。</span><span class="sxs-lookup"><span data-stu-id="33943-157">Otherwise, use non-silent acquisition.</span></span>

<span data-ttu-id="33943-158">[**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)方法是非同步。</span><span class="sxs-lookup"><span data-stu-id="33943-158">The [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method is asynchronous.</span></span> <span data-ttu-id="33943-159">應用程式應該在應用程式的執行緒上執行取得步驟。</span><span class="sxs-lookup"><span data-stu-id="33943-159">The application should perform the acquisition step on the application's thread.</span></span> <span data-ttu-id="33943-160">其中一個方法是將私用視窗訊息張貼至應用程式的主視窗，通知應用程式執行緒執行取得。</span><span class="sxs-lookup"><span data-stu-id="33943-160">One approach is to post a private window message to the application's main window, notifying the application thread to perform the acquisition.</span></span> <span data-ttu-id="33943-161">當作業暫止時，應用程式必須儲存回呼指標以及它在 **BeginEnableContent** 的 *pCallback* 和 *punkState* 參數中收到的狀態物件。</span><span class="sxs-lookup"><span data-stu-id="33943-161">While the operation is pending, the application must store the callback pointer and the state object that it received in the *pCallback* and *punkState* parameters of **BeginEnableContent**.</span></span> <span data-ttu-id="33943-162">這些將用來完成非同步作業。</span><span class="sxs-lookup"><span data-stu-id="33943-162">These will be used to complete the asynchronous operation.</span></span>

### <a name="automatic-acquisition"></a><span data-ttu-id="33943-163">自動取得</span><span class="sxs-lookup"><span data-stu-id="33943-163">Automatic Acquisition</span></span>

<span data-ttu-id="33943-164">若要執行自動取得，請呼叫 [**IMFContentEnabler：： AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)。</span><span class="sxs-lookup"><span data-stu-id="33943-164">To perform automatic acquisition, call [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span></span> <span data-ttu-id="33943-165">這個方法是非同步方法。</span><span class="sxs-lookup"><span data-stu-id="33943-165">This method is asynchronous.</span></span> <span data-ttu-id="33943-166">當作業完成時，內容啟用程式會傳送 [MEEnablerCompleted](meenablercompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="33943-166">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span> <span data-ttu-id="33943-167">事件的狀態碼會指出作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="33943-167">The event's status code indicates whether the operation was successful.</span></span> <span data-ttu-id="33943-168">如果來自 MEEnablerCompleted 事件的狀態碼是 NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED，應用程式應該嘗試使用非無訊息的取得。</span><span class="sxs-lookup"><span data-stu-id="33943-168">If the status code from the MEEnablerCompleted event is NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should try using non-silent acquisition.</span></span>

<span data-ttu-id="33943-169">取得作業正在進行時，啟用程式物件可能會傳送 [MEEnablerProgress](meenablerprogress.md) 事件，以指出作業的進度。</span><span class="sxs-lookup"><span data-stu-id="33943-169">While the acquisition operation is in progress, the enabler object might send the [MEEnablerProgress](meenablerprogress.md) event to indicate the progress of the operation.</span></span> <span data-ttu-id="33943-170">若要取消作業，請呼叫 [**IMFContentEnabler：： cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel)。</span><span class="sxs-lookup"><span data-stu-id="33943-170">To cancel the operation, call [**IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span></span>

### <a name="non-silent-acquisition"></a><span data-ttu-id="33943-171">非無訊息取得</span><span class="sxs-lookup"><span data-stu-id="33943-171">Non-Silent Acquisition</span></span>

<span data-ttu-id="33943-172">如果 [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) 方法傳回 **FALSE** 或 [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) 方法失敗，並出現錯誤碼 NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED，則應用程式應該執行非無訊息的取得，如下列步驟所述：</span><span class="sxs-lookup"><span data-stu-id="33943-172">If the [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) method returns **FALSE** or the [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method fails with the error code NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should perform non-silent acquisition as described in the following steps:</span></span>

1.  <span data-ttu-id="33943-173">呼叫 [**IMFContentEnabler：： GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) 來取得取得許可權的 URL。</span><span class="sxs-lookup"><span data-stu-id="33943-173">Call [**IMFContentEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) to get the URL for the rights acquisition.</span></span> <span data-ttu-id="33943-174">這個方法也會傳回旗標，指出 URL 是否受信任。</span><span class="sxs-lookup"><span data-stu-id="33943-174">This method also returns a flag indicating whether the URL is trusted.</span></span>
2.  <span data-ttu-id="33943-175">呼叫 [**IMFContentEnabler：： GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) 來取得 HTTP POST 資料。</span><span class="sxs-lookup"><span data-stu-id="33943-175">Call [**IMFContentEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) to get the HTTP POST data.</span></span>
3.  <span data-ttu-id="33943-176">呼叫 [**IMFContentEnabler：： MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)。</span><span class="sxs-lookup"><span data-stu-id="33943-176">Call [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span></span> <span data-ttu-id="33943-177">此方法會導致內容啟用程式監視許可權取得動作的進度。</span><span class="sxs-lookup"><span data-stu-id="33943-177">This method causes the content enabler to monitor the progress of the rights acquisition action.</span></span>

4.  <span data-ttu-id="33943-178">使用 HTTP POST 動作將資料提交至 rights 取得 URL。</span><span class="sxs-lookup"><span data-stu-id="33943-178">Submit the data to the rights acquisition URL by using an HTTP POST action.</span></span> <span data-ttu-id="33943-179">您可以使用 Internet Explorer 控制項或 Windows 網際網路 (WinINet) Api。</span><span class="sxs-lookup"><span data-stu-id="33943-179">You can use the Internet Explorer control or the Windows Internet (WinINet) APIs.</span></span>

<span data-ttu-id="33943-180">下列程式碼顯示步驟1–3。</span><span class="sxs-lookup"><span data-stu-id="33943-180">The following code shows steps 1–3.</span></span> <span data-ttu-id="33943-181">步驟4取決於您應用程式的特定需求。</span><span class="sxs-lookup"><span data-stu-id="33943-181">Step 4 depends on your application's particular requirements.</span></span>


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



<span data-ttu-id="33943-182">當作業完成時，內容啟用程式會傳送 [MEEnablerCompleted](meenablercompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="33943-182">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span>

## <a name="complete-the-asynchronous-operation"></a><span data-ttu-id="33943-183">完成非同步作業</span><span class="sxs-lookup"><span data-stu-id="33943-183">Complete the Asynchronous Operation</span></span>

<span data-ttu-id="33943-184">當權限取得完成時，應用程式必須透過叫用 [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) 方法中提供的回呼指標，來通知媒體會話。</span><span class="sxs-lookup"><span data-stu-id="33943-184">When the rights acquisition is completed, successfully or otherwise, the application must notify the Media Session, by invoking the callback pointer given in the [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

1.  <span data-ttu-id="33943-185">藉由呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult)來建立異步結果物件。</span><span class="sxs-lookup"><span data-stu-id="33943-185">Create an asynchronous result object by calling [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span></span>
2.  <span data-ttu-id="33943-186">藉由呼叫 [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)來叫用媒體會話的回呼。</span><span class="sxs-lookup"><span data-stu-id="33943-186">Invoke the Media Session's callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>
3.  <span data-ttu-id="33943-187">媒體會話將呼叫 [**IMFContentProtectionManager：： EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent)。</span><span class="sxs-lookup"><span data-stu-id="33943-187">The Media Session will call [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span></span> <span data-ttu-id="33943-188">在此方法的執行中，請釋放您在 [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)內配置的任何指標或資源。</span><span class="sxs-lookup"><span data-stu-id="33943-188">In your implementation of this method, release any pointers or resources that you allocated inside [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="33943-189">傳回 **HRESULT** ，指出作業的整體成功與否。</span><span class="sxs-lookup"><span data-stu-id="33943-189">Return an **HRESULT** that indicates the overall success of the operation.</span></span> <span data-ttu-id="33943-190">如果許可權取得失敗或使用者在完成之前取消，則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="33943-190">If the rights acquisition failed or the user canceled before it was completed, return an error code.</span></span>

<span data-ttu-id="33943-191">下列程式碼示範如何建立異步結果並叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="33943-191">The following code shows how to create the asynchronous result and invoke the callback.</span></span>


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a><span data-ttu-id="33943-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="33943-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33943-193">媒體會話</span><span class="sxs-lookup"><span data-stu-id="33943-193">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="33943-194">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="33943-194">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



