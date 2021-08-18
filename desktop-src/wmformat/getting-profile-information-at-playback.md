---
title: 在播放時取得設定檔資訊
description: 在播放時取得設定檔資訊
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows媒體格式 SDK，設定檔
- Advanced Systems Format (ASF) ，設定檔
- ASF (Advanced Systems Format) ，設定檔
- Advanced Systems Format (ASF) ，相互排除
- ASF (Advanced Systems Format) ，相互排除
- Advanced Systems Format (ASF) 、頻寬共用
- ASF (Advanced 系統格式) 、頻寬共用
- 串流，在播放時取得設定檔資訊
- 設定檔，在播放時取得資訊
- 相互排除，在播放時取得設定檔資訊
- 頻寬共用，在播放時取得設定檔資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0f9386301b426adb3c4c425ac9329309c7e45146e312cc41df0bd1c453d485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839918"
---
# <a name="getting-profile-information-at-playback"></a>在播放時取得設定檔資訊

用來建立檔案之設定檔中的資訊會儲存在檔案的標頭區段中。 這兩個讀取器物件都可以從檔案標頭存取設定檔資訊。 有幾個原因可能會讓您想要從讀取器存取設定檔資料。 最常見的情況是，您需要捕獲資料流程、互斥物件和頻寬共用物件的相關資訊。

您可以針對 [**IWMProfile**](iwmprofile.md) 介面查詢非同步讀取器物件和同步讀取器物件。 對設定檔資訊進行的任何變更，對讀取器中的檔案都不會有任何影響。 如需存取設定檔資訊的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。

## <a name="stream-information"></a>串流資訊

有時候必須知道串流的設定方式。 當您從讀取器物件的任一個取得媒體屬性時，您會取得輸出的屬性。 輸出屬性會描述讀取器如何傳遞來自資料流程的未壓縮資料，而不是在 ASF 檔案內設定資料流程的方式。

從任一個 reader 物件接收未壓縮的資料流程範例時，您必須使用設定檔資訊來識別壓縮資料的格式。 如果您要將壓縮的串流寫入另一個 ASF 檔，這點特別重要。

使用智慧型 recompression 將音訊串流轉碼至較低的位元速率時，您也需要存取資料流程資訊。

您可能會想要判斷資料流程是否使用變數位元速率來撰寫 (VBR) 編碼。 您無法從任一個 reader 物件的 **IWMProfile** 介面存取任何 VBR 資訊。 這是因為在編碼之後，不會將 VBR 資訊儲存在檔案中。 您可以藉由取得讀取器物件的 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面指標並呼叫 [**IWMHeaderInfo：： GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)，來判斷資料流程是否使用 VBR 編碼來建立。 您必須指定串流號碼，並傳遞 g \_ wszIsVBR 做為屬性名稱。

## <a name="mutual-exclusion-information"></a>相互排除資訊

如果您想要建立使用相互排除的讀取應用程式，您會想要存取設定檔中所包含之任何互斥物件的相關資訊。 若為所有相互排斥類型（位元速率不同），讀取應用程式會負責任何需要的資料流程切換。 若要切換資料流程，您需要知道哪些資料流程是哪些。

## <a name="bandwidth-sharing-information"></a>頻寬共用資訊

設定檔中包含的頻寬共用物件僅供資訊參考之用。 寫入器物件或其中一個讀取器物件都不會因為頻寬共用資料而採取任何動作。 如果您想要在讀取應用程式中使用頻寬共用，您必須從設定檔資料存取頻寬共用資訊。

> [!Note]  
> 並非所有用來建立檔案的設定檔資訊都出現在檔案標頭中。 一般來說，只有在編碼時使用的資料不會保存在檔案中。 這包括使用 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) 方法設定的輸入設定，以及使用 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) 方法設定的屬性。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMProfile 介面**](iwmprofile.md)
</dt> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> </dl>

 

 




