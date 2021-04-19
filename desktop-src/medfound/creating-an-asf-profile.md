---
description: 本主題說明如何在 Microsoft 媒體基礎中建立「ASF 設定檔」。
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: 建立 ASF 設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970746"
---
# <a name="creating-an-asf-profile"></a>建立 ASF 設定檔

本主題說明如何在 Microsoft 媒體基礎中建立「ASF 設定檔」。

-   [建立新的設定檔](#create-a-new-profile)
-   [從 ASF ContentInfo 物件取得設定檔](#get-the-profile-from-the-asf-contentinfo-object)
-   [從簡報描述項取得設定檔](#get-the-profile-from-a-presentation-descriptor)
-   [相關主題](#related-topics)

## <a name="create-a-new-profile"></a>建立新的設定檔

若要建立空白的 ASF 設定檔，請呼叫 [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) 函數。 此函數會傳回 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面的指標。 應用程式可以使用此介面將資料流程新增至設定檔，並設定每個資料流程。 如需詳細資訊，請參閱 [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md)。

（選擇性）應用程式可以將互斥物件新增至兩個或多個資料流程。 請參閱 [使用 ASF 資料流程的相互排除](using-mutual-exclusion-for-asf-streams.md)。

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>從 ASF ContentInfo 物件取得設定檔

應用程式可以從 [Asf ContentInfo 物件](asf-contentinfo-object.md)取得現有 asf 檔案的 asf 設定檔。 設定檔已設定，而且包含檔案中所有資料流程的設定。

藉由剖析檔案的 ASF 標頭物件來初始化 ContentInfo 物件。 這是透過 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 方法來完成。 讀取所有的標頭物件並填入 ASF 程式庫之後，就會產生此檔案的設定檔。 應用程式可以藉由呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)來取得這個已初始化設定檔的指標。

## <a name="get-the-profile-from-a-presentation-descriptor"></a>從簡報描述項取得設定檔

您可以從檔案的 [呈現描述](presentation-descriptors.md) 項，或從 [ASF ContentInfo](asf-contentinfo-object.md) 物件取得現有 ASF 檔案的設定檔物件。 在此情況下，已設定設定檔，並包含檔案中所有資料流程的設定。 如果您想要修改現有的 ASF 設定檔，這會很有用。 例如，您可能想要以較低的位元速率重新編碼 Windows Media 視訊檔案。

若要從呈現描述項取得設定檔，請呼叫 [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor)。 此函式會剖析展示描述項，並在 ASF 設定檔中填入媒體檔案的相關資訊。 函數會傳回 IMFASFProfile 介面的指標。 然後，您可以使用此介面來修改設定檔。

若要取得簡報描述項，請呼叫下列其中一種方法：

-   從 ASF 媒體來源，呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)。
-   從 [ASF ContentInfo](asf-contentinfo-object.md) 物件中，呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)。 在呼叫這個方法之前，請確定已初始化 ContentInfo 物件進行讀取。 如需詳細資訊，請參閱 [讀取現有檔案的 Asf 標頭物件](reading-the-asf-header-object-of-an-existing-file.md)中的「從現有的 ASF 檔案初始化 ContentInfo 物件」。 但是，如果您已經有初始化的 ContentInfo 物件，您可以直接從該物件取得設定檔。 這會在本主題稍後的「從 ContentInfo 物件取得設定檔」中說明。

下列範例示範如何從展示描述項建立設定檔。 此函式會建立檔案的媒體來源、從媒體來源取得簡報描述項，並建立設定檔。 此範例假設 *>pszfilename* 指定了 ASF 檔案的 URL。


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



此範例會使用 [SafeRelease](saferelease.md) 來釋放介面指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 設定檔](asf-profile.md)
</dt> </dl>

 

 



