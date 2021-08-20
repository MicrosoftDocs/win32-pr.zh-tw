---
description: 如何播放包含受 DRM 保護之媒體的檔案。
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: 如何播放受保護的媒體檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20a2b525f8acc3a602bcaae2630726d01269881beec07ac214f4d0bd02ee1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942338"
---
# <a name="how-to-play-protected-media-files"></a>如何播放受保護的媒體檔案

受保護的媒體檔案是具有使用內容之相關規則的任何媒體檔案。 在某些情況下，受保護的媒體檔案會使用某種形式的數位版權管理 (DRM) 加密來加密。 若要播放受保護的媒體檔案，播放必須在受保護的媒體路徑內進行 (PMP) 。 此外，使用者可能必須取得內容的許可權。

「權利取得」（rights）是指應用程式在使用者可以播放內容之前必須執行的任何動作。 最常見的範例是取得 DRM 授權，但是媒體基礎定義可支援其他許可權取得類型的一般機制。 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)介面會定義此泛型機制。

您必須從應用程式進程，在 PMP 之外完成許可權取得。 媒體會話會透過應用程式所執行的 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) 介面，通知應用程式。 媒體會話會使用 **IMFContentProtectionManager** 介面，將內容啟用程式物件轉送至應用程式。 內容啟用會執行 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面。 應用程式會使用此介面來取得必要的許可權。

內容啟用程式可能支援自動取得許可權，在這種情況下，內容啟用程式會執行整個進程，而應用程式只會監視狀態。 否則，應用程式必須使用非無訊息的許可權取得，也就是應用程式會將 HTTP POST 資料傳送到內容啟用程式所提供的 URL。

若要播放受保護的媒體，應用程式會遵循與 [如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案中的相同步驟，並提供下列額外步驟：

1.  查詢媒體來源是否包含受保護的內容。 (選擇性。)
2.  在 PMP 程式中建立媒體會話，而不是應用程式進程。
3.  如果媒體會話通知您，請執行取得許可權。 這項作業是由應用程式以非同步方式執行。
4.  完成非同步作業。

## <a name="query-for-protected-content"></a>查詢受保護的內容

若要查詢媒體來源是否包含受保護的內容，請在媒體來源的展示描述項上呼叫 [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) 函式。 如果函式傳回 S \_ OK，您必須使用 PMP 來播放內容。 如果函式傳回 \_ FALSE，則不需要 PMP，而且您可以在應用程式進程中建立媒體會話。 或者，您也可以使用 PMP 來播放這兩種類型的內容：受保護和未受保護。 如果您這麼做，就不需要呼叫 **MFRequireProtectedEnvironment**。

如需簡報描述項的詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。

## <a name="create-the-pmp-media-session"></a>建立 PMP 媒體會話

若要在 PMP 中建立媒體會話，請呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)。 此函式類似于 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)，但不會在應用程式的進程中建立媒體會話，而是在 PMP 進程中建立媒體會話。 應用程式會接收媒體會話的 proxy 物件指標。 應用程式會在 proxy 物件上呼叫 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 方法，就像在媒體會話一樣。 Proxy 物件會將呼叫轉送到跨進程界限的媒體會話。

建立 PMP 媒體會話，如下所示：

1.  藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)來建立新的屬性存放區。
2.  在屬性存放區上設定 [ [**MF \_ 會話 \_ 內容 \_ 保護 \_ 管理員**](mf-session-content-protection-manager-attribute.md) ] 屬性。 這個屬性的值是應用程式的 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)執行指標。 呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) 來設定屬性。
3.  呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) ，以在 PMP 進程中建立媒體會話。 *PConfiguration* 參數是屬性存放區的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標。


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



接下來，建立播放拓撲並在媒體會話上將它排入佇列，如 [建立播放拓撲](creating-playback-topologies.md)中所述。

## <a name="perform-rights-acquisition"></a>執行許可權取得

如果播放需要取得許可權，媒體會話就會呼叫 [**IMFContentProtectionManager：： BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)。 這個方法的 *pEnablerActivate* 參數是 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。 使用此介面來建立內容啟用程式物件，此物件會公開 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面。 然後使用內容啟用程式來執行「許可權取得」步驟。

若要建立內容啟用程式，請呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)：


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



查詢所傳回的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)介面 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)指標。 使用這個介面從內容啟用程式物件取得事件。 如需事件的詳細資訊，請參閱 [媒體事件](media-event-generators.md)產生器。

若要瞭解內容啟用程式是否支援自動取得，請呼叫 [**IMFContentEnabler：： IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported)。 如果這個方法傳回 **TRUE** 值，則應用程式應該使用自動取得。 否則，請使用非無訊息的取得。

[**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)方法是非同步。 應用程式應該在應用程式的執行緒上執行取得步驟。 其中一個方法是將私用視窗訊息張貼至應用程式的主視窗，通知應用程式執行緒執行取得。 當作業暫止時，應用程式必須儲存回呼指標以及它在 **BeginEnableContent** 的 *pCallback* 和 *punkState* 參數中收到的狀態物件。 這些將用來完成非同步作業。

### <a name="automatic-acquisition"></a>自動取得

若要執行自動取得，請呼叫 [**IMFContentEnabler：： AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)。 這個方法是非同步方法。 當作業完成時，內容啟用程式會傳送 [MEEnablerCompleted](meenablercompleted.md) 事件。 事件的狀態碼會指出作業是否成功。 如果來自 MEEnablerCompleted 事件的狀態碼是 NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED，應用程式應該嘗試使用非無訊息的取得。

取得作業正在進行時，啟用程式物件可能會傳送 [MEEnablerProgress](meenablerprogress.md) 事件，以指出作業的進度。 若要取消作業，請呼叫 [**IMFContentEnabler：： cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel)。

### <a name="non-silent-acquisition"></a>非無訊息取得

如果 [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) 方法傳回 **FALSE** 或 [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) 方法失敗，並出現錯誤碼 NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED，則應用程式應該執行非無訊息的取得，如下列步驟所述：

1.  呼叫 [**IMFContentEnabler：： GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) 來取得取得許可權的 URL。 這個方法也會傳回旗標，指出 URL 是否受信任。
2.  呼叫 [**IMFContentEnabler：： GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) 來取得 HTTP POST 資料。
3.  呼叫 [**IMFContentEnabler：： MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)。 此方法會導致內容啟用程式監視許可權取得動作的進度。

4.  使用 HTTP POST 動作將資料提交至 rights 取得 URL。 您可以使用 Internet Explorer 控制項或 Windows 的網際網路 (WinINet) api。

下列程式碼顯示步驟1–3。 步驟4取決於您應用程式的特定需求。


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



當作業完成時，內容啟用程式會傳送 [MEEnablerCompleted](meenablercompleted.md) 事件。

## <a name="complete-the-asynchronous-operation"></a>完成非同步作業

當權限取得完成時，應用程式必須透過叫用 [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) 方法中提供的回呼指標，來通知媒體會話。

1.  藉由呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult)來建立異步結果物件。
2.  藉由呼叫 [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback)來叫用媒體會話的回呼。
3.  媒體會話將呼叫 [**IMFContentProtectionManager：： EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent)。 在此方法的執行中，請釋放您在 [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)內配置的任何指標或資源。 傳回 **HRESULT** ，指出作業的整體成功與否。 如果許可權取得失敗或使用者在完成之前取消，則會傳回錯誤碼。

下列程式碼示範如何建立異步結果並叫用回呼。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> </dl>

 

 



