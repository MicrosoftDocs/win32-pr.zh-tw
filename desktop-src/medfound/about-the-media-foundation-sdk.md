---
description: Microsoft 媒體基礎是 Windows 的新一代多媒體平臺，可讓開發人員、取用者及內容提供者利用增強的強大功能、無與倫比的品質，以及無縫的互通性，來採用新的新 wave 內容 wave。
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: 關於媒體基礎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986008"
---
# <a name="about-media-foundation"></a>關於媒體基礎

Microsoft 媒體基礎是 Windows 的新一代多媒體平臺，可讓開發人員、取用者及內容提供者利用增強的強大功能、無與倫比的品質，以及無縫的互通性，來採用新的新 wave 內容 wave。

媒體基礎需要 Windows Vista 或更新版本。 它使用元件物件模型 (COM) ，而且需要 C/c + +。 Microsoft 不會提供媒體基礎的受控 API。

媒體基礎 Api 是 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)的一部分。 若要開發媒體基礎的應用程式，請安裝最新版本的 Windows SDK。

## <a name="audio-and-video-quality"></a>音訊和影片品質

媒體基礎的設計目的是要滿足高定義內容所造成的挑戰。 整個平臺中的音訊和影片品質增強功能現在可讓您為下一代的高定義內容提供絕佳的體驗。

-   DirectX Video 加速 (DXVA) 2.0 提供更有效率的影片加速，相較于 DXVA 1.0，其具有更強大且更有效率的影片解碼，並可在影片處理中擴充硬體的使用。 使用 DXVA 2.0，Windows 可以處理一些需求最高的高定義內容，而且具有高品質且改良的故障恢復功能。

-   整個影片管線都會保留色彩空間資訊。 使用者可以完整的精確度享受影片內容。 色彩資訊和交錯影像現在會傳遞給單一傳遞組合的硬體。 保留色彩空間資訊也可減少不必要的色彩空間轉換，以釋出更多的週期來處理要求的 HD 內容。
-   增強的影片轉譯器 (EVR) 提供更佳的時間支援、增強的影片處理，以及改善的故障恢復功能。 全螢幕播放支援已增強，而視窗模式中的影片撕裂已降至最低。
-   媒體基礎使用多媒體類別排程器服務 (MMCSS) 是 Windows Vista 中的新系統服務。 MMCSS 可讓多媒體應用程式確保其時間緊迫的處理會獲得 CPU 資源的優先存取權。

## <a name="content-access"></a>內容存取

當數位娛樂移入高定義時代，而內容變得更容易攜帶和普及時，內容保護將成為數位媒體產品不可或缺的一部分。 媒體基礎的擴充性可確保它可以支援這些趨勢。

此外，媒體基礎擴充性可讓不同的內容保護系統一起運作。

## <a name="about-media-foundation"></a>關於媒體基礎

本章節包含媒體基礎 Api 的一般資訊。 您可以在 [媒體基礎程式設計指南](media-foundation-programming-guide.md)中找到詳細的程式設計資訊。



| 區段                                                                              | 描述                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [媒體基礎的新功能](whats-new-for-media-foundation.md)                | 描述媒體基礎中的新功能。                               |
| [媒體基礎的標頭和程式庫](media-foundation-headers-and-libraries.md) | 列出定義媒體基礎 Api 的標頭和程式庫檔案。 |
| [媒體基礎工具](media-foundation-tools.md)                                 | 描述適用于媒體基礎的開發工具。  |



 

媒體基礎不包含在 Windows 8 的 N 和 KN 版本中。 如需詳細資訊，請參閱 [Microsoft Windows Media Feature Pack 的 N 和 KN 版本的所有 Windows 8 版本](https://support.microsoft.com/kb/2703761)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft 媒體基礎](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



