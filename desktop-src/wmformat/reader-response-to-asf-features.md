---
title: ASF 功能的讀取器回應
description: ASF 功能的讀取器回應
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media 格式 SDK，讀取器回應 ASF 功能
- Advanced Systems Format (ASF) ，讀取器對功能的回應
- ASF (Advanced 系統格式) ，讀取器回應功能
- 對 ASF 功能的讀取器回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967420"
---
# <a name="reader-response-to-asf-features"></a>ASF 功能的讀取器回應

大部分的特殊 ASF 檔案功能都可以在檔案中設定，以與設計用來處理它們的自訂播放應用程式互動。 不過，某些功能在 reader 物件中有內建支援。

讀取器物件會自動從以位元速率互斥的集合中選取資料流程。 這種特殊案例稱為 (MBR) 的多重位元速率。 讀取器選取的資料流程是以資料流程的位元速率為基礎。 資料流程號碼和將其加入至互斥物件的順序與自動選取無關。 如果檔案包含多個以位元速率互斥的資料流程集合，則讀取器會根據可用頻寬的最佳使用方式來選取資料流程。

以語言為基礎的相互排除是在播放之前使用輸出設定來設定。 如果您結合了語言和以位速率為基礎的相互排除，您應該依語言將以位速率為基礎的互斥資料流程分組，然後讓群組依語言相互排斥。 讀取器會先檢查語言，然後判斷要使用的位元速率。

資料流程優先順序是使用記錄的陣列設定。 陣列中的記錄依優先權的遞減順序排列。 陣列中的最後一個資料流程是讀取器將卸載的第一個資料流程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**互斥**](mutual-exclusion.md)
</dt> <dt>

[**資料流程優先順序**](stream-prioritization.md)
</dt> </dl>

 

 




