---
description: DirectShow 編輯服務簡介
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: DirectShow 編輯服務簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d12470b45e0b39c32c983176f07444a5136b9e97b99cc5be142974d05178f58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952546"
---
# <a name="introduction-to-directshow-editing-services"></a>DirectShow 編輯服務簡介

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

DirectShow 的核心是處理串流媒體的強大架構。 應用程式可以使用它來播放以各式各樣格式撰寫的多媒體內容，而開發人員不需要擔心檔案壓縮和其他繁瑣的詳細資料。 不過，在[DirectShow 編輯服務](directshow-editing-services.md) (DES) 之前，DirectShow 缺乏非線性編輯所需的彈性。

例如，假設您想要建立由來源 A 4 秒組成的影片序列，後面接著來源 B 的10秒，並以來源 C 的5秒結尾。您可以很輕鬆地使用核心 DirectShow API 來完成。

但是，如果您決定來源 C 應該在來源 B 之前，不是在之後，順序應該使用來自來源 A 的8秒，而不是4。而整個生產需要在背景中播放個別的音訊播放軌嗎？ 即使是微小的變更（例如這些變更）也很難實行。 但是剛剛所述的案例是 DES 的簡單編輯專案—您可以使用少數的方法呼叫來進行。

以下是一些 DES 帶來 DirectShow 的功能：

-   將影片和音訊曲目組織成嵌套圖層的時間軸模型，可讓您輕鬆地操作最終生產環境
-   即時預覽影片專案的能力
-   透過以 XML 為基礎的格式 Project 持續性
-   支援影片和音訊效果，以及影片曲目之間的轉換 (例如淡化和抹除) 
-   超過100標準抹除，如運動圖片和電視工程師的社會所定義 (SMPTE) 
-   以色調、亮度、RGB 值或 Alpha 值為基礎的金鑰
-   自動轉換畫面播放速率和音訊取樣率，讓生產環境使用異類來源
-   調整大小或裁剪影片

限制：

-   DES 不支援 MPEG-2 或 h.264 影片來源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow編輯服務](directshow-editing-services.md)
</dt> </dl>

 

 



