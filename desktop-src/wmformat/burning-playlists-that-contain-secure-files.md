---
title: 燒錄包含安全檔案的播放清單
description: 燒錄包含安全檔案的播放清單
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK，以安全檔案燒錄播放清單
- Windows Media Format SDK，包含安全檔案的播放清單
- Advanced Systems Format (ASF) ，以安全檔案燒錄播放清單
- ASF (Advanced Systems Format) ，以安全檔案燒錄播放清單
- Advanced Systems Format (ASF) 、具有安全檔案的播放清單
- ASF (Advanced Systems Format) ，包含安全檔案的播放清單
- 數位版權管理 (DRM) ，以安全檔案燒錄播放清單
- DRM (數位版權管理) ，以安全檔案燒錄播放清單
- 數位版權管理 (DRM) ，包含安全檔案的播放清單
- DRM (數位版權管理) ，包含安全檔案的播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106968085"
---
# <a name="burning-playlists-that-contain-secure-files"></a>燒錄包含安全檔案的播放清單

使用 Windows Media Rights Manager 10 SDK 的物件建立的授權可以指定將檔案複製到光碟作為播放清單一部分的許可權。 這項功能稱為播放清單燒錄，需要您先確認播放清單中所有檔案的授權，再開始複製資料。 Windows Media Format SDK 提供 [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) 介面，可為您執行檔案驗證。

若要執行播放清單燒錄，請執行下列步驟：

1.  建立 reader 物件的實例，或同步讀取器物件。 如需詳細資訊，請參閱 [讀取 ASF](reading-asf-files.md)檔。
2.  呼叫讀取器介面的 **QueryInterface** 方法 ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) 或 [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) ，以取得 [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) 介面的指標。
3.  將檔案名從播放清單複製到寬字元字串的陣列。 陣列中的檔案名必須與播放清單中出現的順序相同。
4.  呼叫 [**IWMReaderPlaylistBurn：： InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) 方法，將指標傳入步驟3所建立的陣列，以初始化檔案的授權驗證。
5.  當授權驗證完成時，讀取器物件會將 WMT \_ INIT \_ 播放清單 \_ 燒錄訊息傳送至您的 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法的執行。 當您的回呼收到此訊息時，請呼叫 [**IWMReaderPlaylistBurn：： GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) 方法以取得授權檢查的結果。 這個方法會採用 **HRESULT** 變數陣列，這些變數會對應至傳遞給 **InitPlaylistBurn** 的陣列中的檔案名。 如果結果陣列中的所有值都等於 S \_ ，您可以繼續。 如果有任何結果是錯誤碼，則不能複製播放清單。
6.  使用相同的讀取器實例，開啟並讀取每個檔案。 您必須依檔案名在傳遞至 **InitPlaylistBurn** 的檔案名陣列中出現的順序開啟檔案。
7.  當您複製播放清單中的所有檔案時，請呼叫 [**IWMReaderPlaylistBurn：： EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) 完成播放清單燒錄程式，並釋放讀取器所使用的資源。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




