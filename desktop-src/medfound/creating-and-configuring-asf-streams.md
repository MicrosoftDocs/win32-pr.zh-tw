---
description: 每個 ASF 檔案都包含一或多個資料流程。 ASF 設定檔物件代表一組 ASF 資料流程。 針對 ASF 編碼，您必須建立並設定要編碼的資料流程。
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: 建立和設定 ASF 資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eabce588022dd66947f34e4dcd9db61f26448b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999843"
---
# <a name="creating-and-configuring-asf-streams"></a>建立和設定 ASF 資料流程

每個 ASF 檔案都包含一或多個資料流程。 [Asf 設定檔](asf-profile.md)物件代表一組 asf 資料流程。 針對 ASF 編碼，您必須建立並設定要編碼的資料流程。

應用程式可以使用 ASF 設定檔物件來執行下列工作：

-   新增或移除資料流程。
-   取得資料流程的設定。
-   設定承載延伸模組。
-   新增、移除或修改 ASF 相互排除物件。

本主題包含下列各節。

-   [建立新的資料流程](#creating-a-new-stream)
-   [指派資料流程號碼](#assigning-stream-numbers)
-   [設定有漏洞 Bucket 值](#setting-leaky-bucket-values)
-   [承載延伸模組](#payload-extensions)
-   [將資料流程新增至設定檔](#adding-a-stream-to-the-profile)
-   [相關主題](#related-topics)

## <a name="creating-a-new-stream"></a>建立新的資料流程

ASF 設定檔物件必須包含至少一個 ASF 資料流程的設定。 每個資料流程都會以 *資料流程* 設定物件來表示，此物件會公開 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面。 資料流程設定物件中的資訊會對應至 ASF 檔案標頭中的資料流程屬性物件和擴充資料流程屬性物件。  (查看 [ASF 檔案結構](asf-file-structure.md)。 ) 

若要將資料流程新增至 ASF 設定檔，請執行下列步驟：

1.  建立空的資料流程資料流程設定物件。
2.  根據應用程式的需求設定串流。
3.  將資料流程新增至設定檔。

若要建立設定檔的資料流程，請呼叫 [**IMFASFProfile：： CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) 來建立空白的資料流程設定物件，並在 *ppIStream* 參數中接收指標。 **CreateStream** 需要知道要建立的資料流程型別。 ASF 檔案中最常見的資料流程類型是音訊和影片串流。 在媒體基礎中，資料流程類型是由公開 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的媒體類型物件表示。 媒體類型的主要類型會定義數位媒體資料流程的類別，例如音訊或影片。 子類型定義主要類型的格式。 您可以使用「串流設定」物件來變更 **CreateStream** 設定的初始媒體類型。 若要抓取資料流程的媒體類型，請呼叫 [**IMFASFStreamConfig：： GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) ，或取得主要類型呼叫 [**IMFASFStreamConfig：： GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype)。 您可以藉由呼叫 [**IMFASFStreamConfig：： SetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype)，將資料流程的初始媒體類型取代為新設定的媒體類型。

如果應用程式透過呼叫 [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor)，從有效的表示描述項建立設定檔。 此函式會自動設定每個資料流程的資料流程設定物件，並在設定檔上進行設定。 串流媒體類型是根據與展示描述項相關聯的資料流程描述項來設定。

## <a name="assigning-stream-numbers"></a>指派資料流程號碼

所有類型的資料流程都必須獲派串流號碼。 資料流程號碼不需要是連續的，但必須介於1到127之間。 若要指派資料流程號碼，請呼叫 [**IMFASFStreamConfig：： SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber)。 若要取得串流號碼呼叫，請 [**IMFASFStreamConfig：： GetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber)。

> [!Note]  
> 資料流程號碼與資料流程索引不同，它是在使用 [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)取得設定檔中的資料流程時使用。 資料流程索引是由設定檔物件指派給資料流程的數位。 資料流程索引的範圍介於0到1之間，且小於 [**IMFASFProfile：： GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)所抓取的資料流程數目。 您也可以呼叫 [**IMFASFProfile：： GetStreamByNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)，依串流號碼從設定檔取得資料流程。

 

## <a name="setting-leaky-bucket-values"></a>設定有漏洞 Bucket 值

代表資料流程的每個串流設定物件都必須有相關聯的有漏洞值區參數、位元速率和緩衝區視窗值。

您可以透過 [**mf \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) 屬性和 [**mf \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) 屬性，將這些值提供給應用程式。 針對檔案編碼，實際的值取決於編碼類型，而且會由編碼器決定。 如果您已經設定編碼器，並且在編碼器上設定輸出類型，應用程式必須查詢有漏洞 bucket 參數的編碼器，並設定這些屬性中的值。

如果您使用管線層元件，並設定 ASF 媒體接收器的資料流程，很可能是您沒有設定的編碼器。 在此情況下，您必須查詢編碼器的媒體型別協商，並在 ASF 媒體接收器屬性存放區的 [**MFPKEY \_ ASFSTREAMSINK \_ 更正 \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) 屬性中設定更新的值。 編碼屬性存放區是透過與設定檔相關聯之 ContentInfo 物件的來抓取。 更新的值會自動反映在資料流程的有漏洞 bucket 屬性值中。 如需有關有漏洞 bucket 的一般資訊，以及如何從編碼器取得有漏洞 bucket 值，請參閱 [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)。

## <a name="payload-extensions"></a>承載延伸模組

這些資料流程的媒體資料會以[asf](asf-multiplexer.md)多工器的[媒體範例](media-samples.md)的形式新增至 asf 資料物件。 這些媒體範例可以包含承載延伸模組資料： SMPTE 時間碼資料、非正方形圖元外觀比例、範例持續時間，以及範例是否包含它（影片主要畫面格）。 如需支援的承載延伸模組類型清單，請參閱 [ASF 承載延伸模組 guid](asf-payload-extension-guids.md)。

資料流程必須設定為接受承載延伸模組，以便在產生範例期間，多工器可以將補充資料新增至該資料流程的每個範例。

若要取得在資料流程上設定的承載延伸模組總數，請呼叫 [**IMFASFStreamConfig：： GetPayloadExtensionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) ，然後藉由呼叫 [**IMFASFStreamConfig：： GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)來列舉清單。 若要加入資料流程的裝載延伸模組，請呼叫 [**IMFASFStreamConfig：： AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)。 這會將補充資料新增至針對資料流程產生的個別媒體範例。

若要移除與資料流程相關聯的現有承載延伸模組，請呼叫 [**IMFASFStreamConfig：： RemoveAllPayloadExtensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions)。

## <a name="adding-a-stream-to-the-profile"></a>將資料流程新增至設定檔

設定資料流程之後，請呼叫 [**IMFASFProfile：： SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) 將資料流程新增至設定檔。

若要移除設定檔中現有的資料流程，請呼叫 [**IMFASFProfile：： RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream)。

您必須藉由呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)，在 ContentInfo 物件上設定所設定的設定檔。 如果對現有的資料流程進行變更，您必須將它再次新增至設定檔，並在 ContentInfo 物件上設定設定檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 設定檔](asf-profile.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> <dt>

[WMContainer ASF 元件](wmcontainer-asf-components.md)
</dt> </dl>

 

 



