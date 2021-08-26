---
description: Windows 影像處理元件 (WIC) 是一種可延伸的平臺，可在 Windows Vista 和 Windows 7 作業系統上進行數位影像處理。
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: '簡介 (如何撰寫 WIC-Enabled 編解碼器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028246c323cfca16760f86f26d3b1d3694a39ff83a27e983320afa96d8fbf771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056508"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a>簡介 (如何撰寫 WIC-Enabled 編解碼器) 

Windows 影像處理元件 (WIC) 是一種可延伸的平臺，可在 Windows Vista 和 Windows 7 作業系統上進行數位影像處理。 WIC 也可在 Windows XP 和 Windows Server 2003 上取得，可作為 Microsoft .NET Framework 3.0 的一部分，或可供您重新發佈的個別元件。 任何使用 WIC 的應用程式都可以使用任何影像格式來存取、顯示、處理及列印影像，以提供已啟用 WIC 的編解碼器，並使用一組一致的介面，免除特定格式的特殊知識需求。

Windows vista Explorer、Windows vista 影像中心、Live 影像中心和 Windows 7 相片檢視器都建基於 WIC。 在 Windows Vista 或 Windows 7 系統上安裝已啟用 WIC 的編解碼器之後，作業系統會針對該平臺隨附的標準映射格式，提供相同的關聯映射格式支援層級。 因為您為自己的影像格式撰寫編解碼器，所以您可以在使用影像格式的任何地方確保一致的品質，並獲得完整平臺支援的優點。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件的運作方式](-wic-howwicworks.md)
</dt> <dt>

如何撰寫 WIC-Enabled 編解碼器
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



