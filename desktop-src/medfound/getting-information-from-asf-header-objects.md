---
description: ASF 標頭資訊儲存在媒體檔案的 ASF 標頭物件中。
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: 從 ASF 標頭物件取得資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346e57721137fd6064e4d6b9fd21080d96c10e740bb7f7ed45bf3fef4cc92722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974437"
---
# <a name="getting-information-from-asf-header-objects"></a>從 ASF 標頭物件取得資訊

ASF 標頭資訊儲存在媒體檔案的 ASF 標頭物件中。 媒體基礎提供 [ASF ContentInfo 物件](asf-contentinfo-object.md) 來使用標頭物件。 需要填入的 ContentInfo 物件，應用程式才能讀取現有檔案的標頭資訊。 這可以藉由呼叫 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)來達成。 如果剖析成功完成，檔案的 ASF 程式庫（由媒體基礎在內部維護）會填入來自各種標頭物件的標頭資訊。 其中有些屬性會公開給應用程式，它可以透過展示描述元、資料流程描述元、設定檔和中繼資料屬性上的屬性來取得。

如需屬性的完整清單，請參閱 [適用于 ASF 標頭物件的媒體基礎屬性](media-foundation-attributes-for-asf-header-objects.md)。

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>從簡報描述元中取出標頭資訊

簡報描述元物件包含特定媒體來源的說明，在此案例中為 ASF 媒體來源。 如果 **ParseHeader** 呼叫順利完成，就會將標頭物件中的檔案層級資訊儲存為表示描述項的屬性。 若要建立展示描述項，請呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)。 這個方法會傳回填入的表示描述元物件的指標，其中包含與 ContentInfo 物件相關聯之 ASF 檔案的這些屬性。 若要取得特定屬性的值，請在展示描述項上呼叫 **IMFAttributes：： Getxxx** 方法，並指定 **MF \_ PD \_ ASF \_ xxx** 屬性。

下列範例程式碼會抓取 ContentInfo 物件所指定之 ASF 檔案的播放持續時間。


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



如需一般展示描述項的詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。

如需完整的簡報描述元屬性集，請參閱 [展示描述項屬性](presentation-descriptor-attributes.md)。

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>從資料流程描述元中取出標頭資訊

資料流程描述元物件會公開 [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) 介面，並描述檔案中資料流程的特性。 ASF 內容的表示描述項包含一或多個代表標頭物件中所列之資料流程的資料流程描述項。 在 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) 的呼叫順利完成之後，基礎資料流程描述元會從不同的標頭物件填入資料流程層級資訊。 若要取得 ASF 資料流程的資料流程描述元，請在從 ContentInfo 物件產生的表示描述項上呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) 。

部分資料流程屬性會設定為數據流描述項的屬性。 在資料流程描述項上呼叫 **IMFAttributes：： Getxxx** 方法，並 **指定 \_ MF \_ SD ASF \_ xxx** 屬性。

如需完整的資料流程描述元屬性集，請參閱 [資料流程描述項屬性](stream-descriptor-attributes.md)中所列的「ASF 特定的資料流程描述元」屬性。

## <a name="retrieving-header-information-from-the-profile-object"></a>從設定檔物件中取出標頭資訊

除了資料流程描述元之外，ASF 設定檔物件也會描述資料流程屬性。 若要取得現有 ASF 檔案的設定檔，請呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)。 這個方法所傳回的 ASF 設定檔物件不包含任何 **MF \_ PD \_ ASF \_ xxx** 屬性。 這些屬性只會在呼叫 [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) 從展示描述項產生設定檔物件之後，才可供應用程式使用。 您可以使用設定檔來取得相互排除的指標，以及串流處理優先權的物件。

如需設定檔物件的詳細資訊，請參閱 [ASF 設定檔](asf-profile.md) 。

## <a name="retrieving-metadata-from-header-objects"></a>從標頭物件中取出中繼資料

ASF 檔案可以包含數個在檔案編碼期間設定的中繼資料屬性。 應用程式可以使用 ContentInfo 物件來列舉這些屬性。 其中有些屬性（例如變數位元速率 (VBR) 資訊）可透過展示描述元、串流描述項的屬性，以及媒體檔案的媒體類型，提供給應用程式使用。 這些屬性是在透過 [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 呼叫初始化期間，于 ContentInfo 物件上設定的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF ContentInfo 物件](asf-contentinfo-object.md)
</dt> </dl>

 

 



