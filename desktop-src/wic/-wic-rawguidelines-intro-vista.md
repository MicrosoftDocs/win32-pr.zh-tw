---
description: Windows Vista 中的原始影像格式
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Windows Vista 中的原始影像格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88026e85780706ca2bd5f23f5ca43ec49ae614d4c65e42ec19367b01b3f43423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709856"
---
# <a name="raw-image-formats-in-windows-vista"></a>Windows Vista 中的原始影像格式

Windows在電腦上安裝適當的編解碼器時，vista Explorer、Windows vista 影像中心、Window Live 影像中心和 Windows 7 相片檢視器全都使用 Windows 影像處理元件 (WIC) ，因此支援原始影像格式。

因為 WIC 是可延伸的映射架構，所以任何 WIC 應用程式都可以在系統上安裝新的編解碼器時，立即取用新的映射格式。 這讓 WIC 更適合用來做為數位攝影機所產生之原始影像格式的隨插即用解決方案。 透過 WIC，Windows 的應用程式可以在每次有更新的編解碼器可供使用時，隨時取得新相機模型的支援 (理想的) 新攝影機。 編解碼器作者可以藉由執行所有映射類型通用的 WIC 介面來支援這些案例，如本檔中的詳細說明。

現今，大部分的主要取用者應用程式都不會對原始影像格式有特別的認識，也不會公開使用者介面來調整原始的處理設定。

不過，為了支援特殊的影像處理應用程式，原始編解碼器作者也必須執行 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 介面。 此介面會公開原始影像的特殊功能，例如，可進行常見的影像調整，以及處理 (將) 原始影像開發成指定的紅色-綠色-藍色 (RGB) 色彩空間的功能。

其他數個 WIC 介面對於原始編解碼器作者而言很重要。 這些主題將在這一系列主題中更詳細地討論。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



