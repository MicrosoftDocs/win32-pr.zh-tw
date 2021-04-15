---
description: 關於轉譯引擎
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: 關於轉譯引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510220"
---
# <a name="about-the-render-engines"></a>關於轉譯引擎

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本文說明 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 如何呈現影片編輯專案。

在 DES 中，專案會以時間軸表示。 時間軸會很有用，因為它可簡化影片編輯中最常見的工作，例如重新排列來源剪輯以及新增影片效果。 另一方面，DirectShow 資料流程架構需要篩選圖形。 因此，若要轉譯您的專案，您必須將時間軸轉譯為篩選圖形。 執行這項工作的元件稱為轉譯 *引擎*。 DirectShow 提供兩種轉譯引擎：

-   基本轉譯引擎：建立可傳遞未壓縮輸出的篩選圖形。
-   智慧型轉譯引擎：建立可傳遞壓縮輸出的篩選圖形。

智慧型轉譯引擎會使用智慧型 recompression 來改善效能。 使用智慧型 recompression 時，只有在原始檔案格式與最終輸出格式不同時，才會 recompressed 來源檔案。 如果格式相符，則永遠不會解壓縮來源。 只有視訊壓縮支援 Smart recompression，不適用於音訊壓縮。

若為預覽版本，請使用基本轉譯引擎。 智慧型轉譯引擎也可以預覽，但效率較低，因為它必須解壓縮壓縮的資料流程。 針對寫入檔案，如果您想要 smart recompression，請使用智慧型轉譯引擎。 否則，請使用基本轉譯引擎。 Smart recompression 可以大幅減少寫入檔案所花費的時間。

> [!IMPORTANT]
> 請勿使用智慧型轉譯引擎來讀取或寫入 Windows Media 檔案。

 

> [!IMPORTANT]
> 這兩種轉譯引擎都會建立一個不可見的視窗來處理訊息。 建立轉譯引擎的執行緒必須有訊息迴圈，才能分派訊息。 此外，必須等到轉譯引擎和篩選圖形管理員釋出之後，該執行緒才能結束。 否則，應用程式可能會鎖死。

 

建立篩選圖形

篩選圖形的建立方式有兩個階段。 在第一個階段中，轉譯引擎會構造「前端」，這是部分篩選圖形。 下圖說明典型的前端：

![篩選圖形前端](images/rendeng1.png)

子系統包含各種不同的特殊篩選準則，轉譯引擎會自動組合這些篩選器。 前端在時間軸中包含每個群組的一個輸出圖釘。 如果您使用基本轉譯引擎，輸出圖釘會傳遞未壓縮的資料，如果您使用智慧型轉譯引擎，則會傳遞壓縮的資料。

在第二個步驟中，輸出圖釘會連接到轉譯篩選。 針對預覽，轉譯篩選器為影片和音訊轉譯器。 針對檔案寫入，轉譯篩選器是 (mux) 篩選器和檔案寫入器篩選器的多工器。

![完成篩選圖形](images/rendeng2.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預覽專案](previewing-a-project.md)
</dt> <dt>

[將專案寫入檔案](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



