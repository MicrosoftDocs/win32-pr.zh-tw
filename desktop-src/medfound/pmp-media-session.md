---
description: .
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: PMP 媒體會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e14d9e403620d273bb4aeb3347cba523f304b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321447"
---
# <a name="pmp-media-session"></a>PMP 媒體會話

應用程式可以在稱為[受保護媒體路徑](protected-media-path.md) (PMP) 進程的個別進程中建立[媒體會話](media-session.md)。 PMP 程式的主要目的是要使用數位版權管理 (DRM) 來啟用受保護內容的播放。 根據預設，PMP 程式會在受保護的環境內建立 (PE) 。 只有受信任的、簽署的元件可以載入 PE 內。 PMP 程式的第二個優點是它會將應用程式進程與媒體管線隔離。 如需 PMP 程式的詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。

若要在 PMP 進程內建立媒體會話，請呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) 函式。 （選擇性）您可以傳入 **MFPMPSESSION 未 \_ 受保護的 \_ 進程** 旗標。 如果設定此旗標，則會在未受保護的進程內建立 PMP 進程，而不是在 PE 進程中建立。 未受保護的進程無法用於 DRM 播放，但可提供程式隔離的優點。

[**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函式會將指標傳回給媒體會話的 proxy 物件。 應用程式會透過 proxy 與媒體會話進行通訊。

![pmp 流程內媒體會話的圖例](images/pmp01.png)

根據預設，當應用程式建立拓撲時，會在應用程式進程內建立媒體來源。 媒體來源的 proxy 是在 PMP 進程內建立的。 媒體來源可以使用 [**IMFPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) 介面，在 PMP 進程內建立物件。 例如，為了支援 DRM，媒體來源會建立名為「 *輸入信任授權* 單位」的物件 (ITA) 。 您必須在 PMP 程式內建立 ITA。  (需 ITAs 的詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。 ) 若要使用 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 介面，請執行下列動作：

1.  媒體來源必須執行 [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) 介面。
2.  在拓撲解析期間，媒體會話 proxy 會呼叫媒體來源上的 [**IMFPMPClient：： SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) 方法。
3.  媒體來源會呼叫 [**IMFPMPHost：： CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) ，以在 PMP 進程內建立物件。 物件必須有已註冊的 CLSID。 此外，若要在 PE 中載入，物件必須是受信任且經過數位簽署。 如需程式碼簽署受保護媒體元件的相關資訊，請參閱 [Windows Vista 中受保護媒體元件的白皮書程式碼簽署](/windows-hardware/test/hlk/)

下圖顯示在應用程式進程中建立的媒體來源。

![應用程式進程中媒體來源的圖例。](images/pmp02.png)

另一個替代方式是在 PMP 會話內建立媒體來源。

1.  當您建立媒體會話時，請設定 [ [**MF \_ 會話 \_ 遠端 \_ 來源 \_ 模式]**](mf-session-remote-source-mode-attribute.md) 屬性。 設定屬性是在 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數中指定。
2.  在媒體會話上呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ，以取得 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 介面的指標。 服務識別碼為 **MF \_ PMP \_ 服務**。
3.  使用類別識別碼 **CLSID \_ MFSourceResolver** 來呼叫 [**IMFPMPHost：： CREATEOBJECTBYCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) ，以在 PMP 流程內建立來源解析程式。 方法會將指標傳回給來源解析程式的 proxy。
4.  呼叫 [**IMFSourceResolver：： BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) 或 [**IMFSourceResolver：： BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) 來建立媒體來源。
    > [!Note]  
    > 在此情況下，您必須使用這些方法的非同步版本，因為同步版本無法遠端處理。

     

下圖顯示在 PMP 流程中建立的媒體來源。

![pmp 流程中媒體來源的圖例。](images/pmp03.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何播放受保護的媒體檔案](how-to-play-protected-media-files.md)
</dt> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[受保護的媒體路徑](protected-media-path.md)
</dt> </dl>

 

 
