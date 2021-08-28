---
description: DirectShow系統總覽
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: DirectShow系統總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb7855277029adc563cc032740d3a59b3691fcf12ed2b2595d37a1abd0d923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966348"
---
# <a name="directshow-system-overview"></a>DirectShow系統總覽

**多媒體的挑戰**

使用多媒體會帶來幾項重大挑戰：

-   多媒體串流包含大量資料，必須非常快速地處理。
-   音訊和影片必須進行同步處理，以同時開始和停止，並以相同的速率播放。
-   資料可能來自許多來源，包括本機檔案、電腦網路、電視廣播和攝影機。
-   資料有各種不同的格式，例如 Audio-Video 交錯 (AVI) 、先進的串流格式 (ASF) 、運動圖片專家群組 (MPEG) 和數位視訊 (DV) 。
-   程式設計師事先不知道使用者的系統上會有哪些硬體裝置。

**DirectShow 的解決方案**

DirectShow 的設計目的是要解決這些挑戰。 其主要設計目標是要簡化在 Windows 平臺上建立數位媒體應用程式的工作，方法是將應用程式與資料傳輸、硬體差異和同步處理的複雜性隔離。

為了達成串流影片和音訊所需的輸送量，DirectShow 盡可能使用 Direct3D 和 DirectSound。 這些技術會將資料有效率地轉譯成使用者的音效和圖形卡。 DirectShow 藉由在時間戳記範例中封裝媒體資料，來同步處理播放。 DirectShow 使用模組化架構，讓應用程式混合和比對不同的軟體元件（稱為 *篩選器*），以處理可能的各種來源、格式和硬體裝置。

DirectShow 提供的篩選器可支援根據 Windows Driver Model (WDM) 來捕捉和調整裝置，以及支援 Windows (VfW) 取得卡的較舊影片的篩選器，以及針對音訊壓縮管理員所撰寫的編解碼器 () 和影片壓縮管理員 (bc-vcm-lvm-hyperv) 介面。

下圖顯示應用程式、DirectShow 元件，以及 DirectShow 支援的一些硬體和軟體元件之間的關聯性。

![高層級架構](images/arch-oview2.png)

如下所示，DirectShow 篩選器會與各種裝置（包括本機檔案系統、電視調諧器和影片捕捉卡、VfW 編解碼器、影片顯示 (透過 DirectDraw 或 GDI) ），以及透過 DirectSound)  (的音效卡進行通訊。 因此，DirectShow 將應用程式與這些裝置的許多複雜性隔離。 DirectShow 也會提供特定檔案格式的原生壓縮和解壓縮篩選。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DirectShow](about-directshow.md)
</dt> </dl>

 

 



