---
title: 在裝置上建立播放清單
description: 在裝置上建立播放清單
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media 裝置管理員、播放清單
- 裝置管理員，播放清單
- 程式設計指南，播放清單
- 桌面應用程式，播放清單
- 建立 Windows Media 裝置管理員應用程式、播放清單
- 摘要播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300611"
---
# <a name="creating-a-playlist-on-the-device"></a>在裝置上建立播放清單

Windows Media 裝置管理員 SDK 提供 MTP 應用程式在裝置上建立播放清單的方法。 這種類型的播放清單稱為「摘要播放清單」（ *abstract* 播放清單），因為在裝置上建立的檔案不包含媒體資料，而只有中繼資料（保存播放清單中媒體檔案的連結）。

您可以在裝置上建立的其他抽象專案包括專輯 (基本上是具有額外屬性的播放清單，例如封面) 、連絡人和訊息。

**建立播放清單**

1.  取得目標裝置的 [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) 介面。
2.  呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) 以取得 g \_ wszWMDMFormatsSupported 屬性。
3.  如果不支援播放清單的格式，則不允許將播放清單傳送至裝置，並略過下列步驟。 否則，請選擇與最接近預期物件類型相符的裝置支援格式代碼。 一般 WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST 和 WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST 格式代碼是最常支援的。
4.  取得儲存體 (您要在其中建立物件) 根目錄或資料夾的 [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) 介面。 如果播放清單物件放在名為「播放清單」的最上層資料夾中，某些裝置的效果最佳。
5.  使用 [**IWMDMStorage3：： CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject)建立空白的中繼資料物件。
6.  使用上一個步驟中取得的 **IWMDMMetaData** 介面，呼叫 [**IWMDMMetaData：： AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) 將您選擇的格式程式碼 (從步驟 3) 新增至儲存體中繼資料屬性。
7.  從 **IWMDMStorage3** 介面取得 [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)介面。
8.  呼叫 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) ，以在選取的儲存體中插入新的播放清單檔案。 此檔案包含您在步驟5中建立並傳遞至 **Insert3** 之 **IWMDMMetaData** 介面所代表的中繼資料。 方法會傳回播放清單檔案的 **IWMDMStorage** 介面;您可以查詢 [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) 介面。
9.  呼叫 [**IWMDMStorage4：： SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) ，以建立播放清單中媒體檔案的 **IWMDMStorage** 介面參考。

如需範例程式碼，請參閱 \_ [範例桌面應用程式](sample-desktop-application.md)中的 OnCreatePlaylist 函式。

> [!Note]  
> Microsoft 提供的 MTP 服務提供者可讓應用程式在中繼資料中設定參考。 若要執行播放清單，您的應用程式必須與 MTP 裝置進行通訊，或使用可處理抽象物件的自訂服務提供者。 CE 服務提供者會處理播放清單和專輯物件。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將檔案寫入至裝置**](writing-files-to-the-device.md)
</dt> </dl>

 

 




