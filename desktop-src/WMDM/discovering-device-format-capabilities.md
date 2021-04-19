---
title: 探索裝置格式功能
description: 探索裝置格式功能
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Media 裝置管理員，裝置功能
- 裝置管理員，裝置功能
- 程式設計指南，裝置功能
- 桌面應用程式，裝置功能
- 建立 Windows Media 裝置管理員應用程式，裝置功能
- 將檔案寫入裝置、裝置功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ee05476f6b84bc85bb81cc7cff5815649f5842
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968218"
---
# <a name="discovering-device-format-capabilities"></a>探索裝置格式功能

您的應用程式可能會先嘗試判斷裝置的播放功能，然後再將檔案傳送給它。 如果裝置無法處理您想要傳送的檔案格式，您的應用程式可能會嘗試將檔案轉碼成裝置可使用的格式，或通知使用者裝置無法支援要求的檔案。

請注意，某些裝置（例如大型儲存裝置類別）可能只會作為卸除式存放裝置媒體，而不會有播放功能。 在這種情況下，您的應用程式在將檔案傳送到裝置之前，不適合轉碼檔案。

雖然 [**IWMDMDevice：： GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) 方法可讓裝置報告其功能，但某些裝置會針對此方法傳回不正確的值。 將檔案複製到裝置之前，您可能會想要詢問使用者是否要播放，如果是，則嘗試將檔案轉碼為裝置的其中一種回報格式 (或合理格式，如果裝置宣告支援任何格式) 。 另一種方法是假設裝置所支援的任何格式都是要播放，而所有其他檔案則應以未修改的方式傳輸。

探索要傳送的檔案格式以及裝置所支援的格式之後，您可以決定哪一個是轉碼的最佳目標格式。

在過去，應用程式通常會針對屬性傳回零，以表示支援該屬性的任何值。 例如， [**\_ WAVEFORMATEX**](-waveformatex.md)的值為零時，nSamplesPerSec 會指出支援任何位元速率。 現在，建議的方法是指出對任何值的支援，就是 \_ \_ \_ \_ \_ 在 WMDM 的 [說明] [**\_ \_ DESC**](wmdm-prop-desc.md)中指定 WMDM 列舉的有效值。ValidValuesForm. 不過，某些屬性可以合法地傳回零以表示特定的支援。 例如，如果 [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md). biSizeImage 設定為零，則表示 BI \_ RGB 點陣圖。 相關結構的檔中會注明零值的例外狀況。

不過，請務必注意，裝置通常不會正確地報告其格式功能，也不會以標準方式回報。 例如，裝置通常會回報它們支援任何格式，事實上它們只能處理特定格式，或是格式類型內的特定位費率。 您可以決定應用程式是否應該接受這類報表，或是否應該對裝置的播放 (能力採用某種上限，例如 192 kbps) 。

要求裝置格式支援的建議方法是 [**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)。 如果不支援這個方法，您的應用程式應該會在 [**IWMDMDevice：： GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)回復。 **GetFormatSupport** 與 **GetFormatSupport2** 不同，不會傳回影片資訊。

應用程式要求裝置格式功能的方式取決於應用程式所支援的介面。 如需詳細資料，請參閱下列主題：

-   [在支援 IWMDMDevice3 的裝置上取得格式功能](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [在僅支援 IWMDMDevice 的裝置上取得格式功能](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將檔案寫入至裝置**](writing-files-to-the-device.md)
</dt> </dl>

 

 




