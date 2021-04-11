---
description: 編解碼器可用性和平臺支援
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: 編解碼器可用性和平臺支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194119"
---
# <a name="codec-availability-and-platform-support"></a>編解碼器可用性和平臺支援

Microsoft 建議相機廠商在使用新攝影機的軟體發佈中， (WIC) 編解碼器，並將更新的編解碼器安裝在 Windows 7、Windows Vista 和 Windows XP 的預設廠商軟體上，以更新 Windows 影像處理元件。 攝影機廠商也應提供最新的 WIC 編解碼器，以從其支援網站下載。

## <a name="codec-discovery"></a>編解碼器探索

Microsoft 正在進行下列動作，以協助將使用者指向廠商的網站，以取得編解碼器下載：

-   在 Windows 檔案總管中，如果使用者按兩下無法辨識的檔案 (預設情況下，當原始檔案在電腦上，但尚未) 安裝編解碼器時，對話方塊會回報檔案無法辨識，並詢問使用者是否想要尋找可理解檔案的程式。 Microsoft 會維護現有的重新導向服務，將使用者轉寄給廠商的網站，而這些網站可提供程式來瞭解檔案。 這項功能存在於 Windows XP 和 Windows Vista 中。
-   Windows 影像中心、Windows Live 影像中心和 Windows 7 相片檢視器會將一組副檔名辨識為原始檔案。 如果該集合中的檔案位於任何這些應用程式所查看的資料夾中，而且尚未安裝該檔案的編解碼器，則會出現一個對話方塊，如前面段落中所述。

如需有關編解碼器探索的詳細資訊，請參閱編解碼器可用性和平臺支援。

## <a name="windows-xp-platform-support"></a>Windows XP 平臺支援

Microsoft 已發行具有 WIC 的 Windows XP SP3，以及適用于 Windows XP SP2 的獨立 WIC 安裝程式。 這些會使用 WIC 編解碼器來啟用在這些平臺上的縮圖和預覽支援。 因此，在 Windows 7、Windows Vista 和 Windows XP 上支援和測試編解碼器下載和安裝是很重要的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



