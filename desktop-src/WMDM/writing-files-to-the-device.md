---
title: 將檔案寫入至裝置
description: 將檔案寫入至裝置
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Windows Media 裝置管理員，將檔案寫入裝置
- 裝置管理員，將檔案寫入裝置
- 程式設計指南，將檔案寫入裝置
- 桌面應用程式，將檔案寫入裝置
- 建立 Windows Media 裝置管理員應用程式，將檔案寫入裝置
- 將檔案寫入裝置，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d8b5234cc275eed1b4aa344c16a2b927b8122d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507057"
---
# <a name="writing-files-to-the-device"></a>將檔案寫入至裝置

將檔案傳送至裝置之前，您的應用程式必須找出裝置可以處理的檔和格式類型，讓應用程式可以在傳送或傳送未修改或未傳送的情況下，判斷是否應該轉碼檔案。

下列步驟說明如何將現有的檔案傳送至裝置。 若要在裝置上建立新檔案（例如播放清單），請參閱在 [裝置上建立播放清單](creating-a-playlist-on-the-device.md)。

1.  取得您想要傳送至裝置的檔案名格式。 如需詳細資訊，請參閱 [探索檔案的格式](discovering-a-files-format.md)。
2.  如果裝置打算播放檔案，
    -   查詢檔案的格式功能。 如需詳細資訊，請參閱 [探索裝置格式功能](discovering-device-format-capabilities.md)。
    -   尋找應用程式可從原始檔案建立的可接受格式。
    -   如果需要轉碼檔案，請轉碼該檔案。
3.  尋找新物件的父儲存體。 Windows Media 裝置管理員不會提供一種方式來探索任何特定檔案類型的標準儲存位置 (影片或音訊檔案、WMV 或 BMP、「我的最愛」資料夾等) ，所以您必須檢查每個裝置，以嘗試找出最適合儲存新物件的位置。  (其他應用程式會強制執行特定的資料夾結構，例如，Windows Media Player 會建立專輯、播放清單和音樂資料夾，其中的 [音樂] 資料夾包含演出者和 AlbumName 階層。 基於這個理由，而且因為某些裝置可能尚未使用 Windows Media Player 以外的軟體進行測試，請注意，在 [播放清單] 或 [專輯] 資料夾以外的任何資料夾中，播放清單或專輯物件的位置，有時可能會導致某些裝置上的 nonfunctioning 物件。 ) 
4.  如果目標儲存體支援 [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)，請呼叫 [**IWMDMStorage3：： CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject)來建立新的中繼資料介面。 在 [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) 介面上設定中繼資料。 如需詳細資訊，請參閱 [在檔案上設定中繼資料](setting-metadata-on-a-file.md)。 唯一必要的中繼資料是 g \_ wszWMDMFormatCode ([**WMDM \_ FORMATCODE**](wmdm-formatcode.md) 值，其描述內容) ，但您可以提供的中繼資料越多，服務提供者的傳送效率就愈高。
5.  使用 [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)、 [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)或 [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) 方法，將檔案傳送至裝置。 **Insert3** 可讓您在裝置上包含中繼資料作為方法的一部分。 如需詳細資訊，請參閱將檔案傳送 [至裝置](sending-the-file-to-the-device.md)。

示範每個步驟的程式碼都是在連結的主題頁面上提供。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows Media 裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




