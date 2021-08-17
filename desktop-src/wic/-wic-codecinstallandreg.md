---
description: 當您安裝編解碼器時，必須在登錄中進行註冊。 如果電腦上已經有任何格式的影像，您也必須確定縮圖快取已更新。
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: 編解碼器安裝和註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc13a2d937e82eae3517b9b20440f4acbb10b16af3fa0b872eb0ddd6c2a8d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965177"
---
# <a name="codec-installation-and-registration"></a>編解碼器安裝和註冊

當您安裝編解碼器時，必須在登錄中進行註冊。 如果電腦上已經有任何格式的影像，您也必須確定縮圖快取已更新。

本主題包含下列幾節：

-   [註冊編解碼器](#registering-a-codec)
-   [安裝編解碼器時，更新縮圖快取](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [讓使用者使用您的 WIC-Enabled 編解碼器](#making-your-wic-enabled-codec-available-to-users)
-   [相關主題](#related-topics)

## <a name="registering-a-codec"></a>註冊編解碼器

當您註冊編解碼器時，實際上是註冊兩個元件：編碼器和解碼器。 您也需要建立登錄專案，以針對影像格式所支援的元資料格式，使用元資料處理程式來註冊您的容器格式。

下列主題描述您註冊編解碼器所需的登錄專案：

[一般登錄專案](-wic-generalregentries.md)

[編碼器特定的登錄專案](-wic-encoderregentries.md)

[特定解碼器的登錄專案](-wic-decoderregentries.md)

[與 Windows 影像中心和 Windows 檔案總管整合](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>安裝編解碼器時，更新縮圖快取

安裝編解碼器之後，安裝程式必須在寫入其登錄專案之後呼叫下列函式。


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



此呼叫會通知 Windows 有新的檔案關聯資訊可供使用。 如果影像格式中的影像已經存在於電腦上，縮圖快取將包含它們的預設縮圖，因為在第一次取得映射時，沒有可用的解碼器可將縮圖解壓縮。 當您通知 Windows 有新的檔案關聯可用時，縮圖快取會捨棄任何空白的縮圖，並從現在可解碼的檔案中解壓縮實際的縮圖。

## <a name="making-your-wic-enabled-codec-available-to-users"></a>讓使用者使用您的 WIC-Enabled 編解碼器

如果您是一家攝影機製造商，可以將您的原始編解碼器連同攝影機一起寄送。 您也可以在網站的下載頁面上張貼編解碼器。 不過，如果使用者從其他來源（例如朋友、商務夥伴或其他網站）取得格式的影像檔案，他們可能不知道要使用哪個編解碼器來將它解碼。

基於這個問題，Windows 為您的影像格式使用者提供更簡單的方法來尋找您的編解碼器，並將其下載到電腦上，從 Windows Vista 開始。 如果 Windows 影像中心將副檔名辨識為影像格式，且未安裝該格式的編解碼器，對話方塊會告知使用者無法顯示照片，並詢問使用者是否要下載顯示該相片所需的軟體。 當使用者接受時，會出現 Microsoft 裝載的網站，其中包含編解碼器製造商下載網站的連結。  (選擇性地，您可以要求使用者直接前往您的下載網站。 ) 

如果您想要 Windows 影像中心辨識影像格式的副檔名，讓使用者可以導向至您的下載網站，您必須執行下列動作：

1.  提供編解碼器的下載網站。  (您所提供的每個編解碼器都可以有個別的頁面，或針對所有編解碼器提供下載的單一頁面。 ) 

    下載網站應經過當地語系化，而且可由相機型號輕鬆搜尋。

2.  為 Microsoft 提供您影像格式的延伸模組清單，以及下載網站的 Url。

您必須通知 Microsoft 這些延伸模組適用于您未來開發的任何新編解碼器，以及下載網站 url 的任何變更，以便將新的資訊新增至 Windows 影像中心。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[執行 IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[結論 (如何撰寫 WIC-Enabled 編解碼器) ](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



