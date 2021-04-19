---
description: DXVA 2 以及其與 DXVA 1 的關聯性總覽。
ms.assetid: 190ed399-a8a8-4087-8d18-b1a715690e4c
title: 關於 DXVA 2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f622c863f433be44bbce6460024ffb06bb1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970624"
---
# <a name="about-dxva-20"></a>關於 DXVA 2。0

DirectX Video 加速 (DXVA) 是 API 和對應的 DDI，可使用硬體加速來加速影片處理。 軟體編解碼器和軟體視頻處理器可以使用 DXVA，將某些需要大量 CPU 的作業卸載至 GPU。 例如，軟體解碼器可以卸載反向離散余弦轉換 (iDCT) 至 GPU。

在 DXVA 中，某些解碼作業是由圖形硬體驅動程式所執行。 這組功能稱為 *加速器*。 其他解碼作業是由使用者模式應用程式軟體（稱為 *主機解碼* 或 *軟體解碼器*）所執行。  (「 *主機解碼器* 」和「 *軟體解碼器* 」等詞彙都相等。此加速器所執行的 ) 處理稱為「 *外部主機處理*」。 加速器通常會使用 GPU 來加速某些作業。 每當加速器執行解碼作業時，主機解碼必須傳遞至包含執行作業所需資訊的加速器緩衝區

DXVA 2 API 需要 Windows Vista 或更新版本。 Windows Vista 仍支援 DXVA 1 API，以提供回溯相容性。 系統會提供模擬層，以在任一版本的 API 和相反版本的 DDI 之間進行轉換：

-   如果圖形驅動程式符合 Windows 顯示驅動程式模型 (WDDM) ，DXVA 1 API 呼叫會轉換成 DXVA 2 DDI 呼叫。
-   如果圖形驅動程式使用舊版的 Windows XP 顯示驅動程式模型 (XPDM) ，DXVA 2 API 呼叫會轉換成 DXVA 1 DDI 呼叫。

下表顯示每個 DXVA API 版本的作業系統需求和支援的影片轉譯器。



| API 版本 | 規格需求          | 影片轉譯器支援                        |
|-------------|-----------------------|-----------------------------------------------|
| DXVA 1      | Windows 2000 或更新版本 | 重迭混音器、VMR-7、VMR-9 (DirectShow 僅)  |
| DXVA 2      | Windows Vista         | EVR (DirectShow 和媒體基礎)          |



 

在 DXVA 1 中，軟體解碼器必須透過影片轉譯器存取 API。 沒有任何方法可以使用 DXVA 1 API，而不需要呼叫影片轉譯器。 DXVA 2 已移除這項限制。 使用 DXVA 2，主機解碼 (或任何應用程式) 都可以透過 [**IDirectXVideoDecoderService**](/windows/win32/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面直接存取 API。

DXVA 1 檔說明用於下列影片標準的解碼結構：

-   ITU-T Rec. H. 261
-   ITU-T Rec
-   MPEG-2 影片
-   MPEG-2 主要設定檔影片

下列規格定義適用于其他影片標準的 DXVA 延伸模組：

-   [H.264/AVC 解碼的 DXVA 規格](https://www.microsoft.com/downloads/details.aspx?FamilyID=3d1c290b-310b-4ea2-bf76-714063a6d7a6&displaylang=en)
-   [DXVA 規格： h.264/MPEG-2 AVC 多型的) 多型影片編碼 (MVC，包括身歷聲 High 設定檔](https://www.microsoft.com/download/details.aspx?id=25200)
-   [MPEG-2 VLD 的 DXVA 規格和組合的 mpeg-2/MPEG-2 VLD 影片解碼](https://www.microsoft.com/download/details.aspx?id=9374)。
-   [適用于 MPEG-2 的 Off-Host VLD 模式的 DXVA 規格第2部分影片解碼](https://www.microsoft.com/download/details.aspx?id=21100)
-   [Windows Media 視訊® v8、v9 和 vA 解碼 (的 DXVA 規格，包括 SMPTE 421M "VC-1" ) ](https://www.microsoft.com/downloads/details.aspx?FamilyID=8792dfdb-8459-4cb7-adb4-fef30b609b31&displaylang=en)
-   [DirectX Video 加速 (DXVA) 規格，適用于 h.264/MPEG 4 可調整的影片編碼 (SVC) Off-Host VLD 模式解碼](https://www.microsoft.com/downloads/details.aspx?FamilyID=a38538b6-f52c-470b-94be-0cf7c28d46cc&displaylang=en)
-   [適用于 VP8 和 VP9 影片編碼的 DirectX 影片加速規格](https://www.microsoft.com/download/details.aspx?id=49188)

DXVA 1 和 DXVA 2 使用相同的資料結構進行解碼。 不過，設定解碼會話的程式已變更。 DXVA 1 使用「探查和鎖定」機制，其中主機解碼器可以測試各種設定，然後在加速器上設定所需的設定。 在 DXVA 2 中，加速器會傳回一份支援的設定清單，而主機解碼器會從清單中選取一個。 下列各節提供詳細資料：

-   [支援 DirectShow 中的 DXVA 2。0](supporting-dxva-2-0-in-directshow.md)
-   [媒體基礎中支援 DXVA 2。0](supporting-dxva-2-0-in-media-foundation.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
