---
title: Two-Pass 編碼
description: Two-Pass 編碼
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows媒體格式 SDK，雙通路編碼
- Windows媒體格式 SDK，2-傳遞編碼
- 編解碼器，雙通路編碼
- 編解碼器，2-通過編碼
- 雙通路編碼，關於
- 2-通過編碼，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cd769049b5fa3869c844e00d9ee14cfae596b197d06d414b04a544d831bbeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845336"
---
# <a name="two-pass-encoding"></a>Two-Pass 編碼

雙通編碼是可用於某些編解碼器的編碼方法，例如 Windows Media 視訊9編解碼器。 當您使用兩次傳遞編碼時，編解碼器會處理資料流程的所有範例。 在第一次傳遞時，編解碼器會收集有關資料流程內容的資訊。 在第二個階段，編解碼器會使用第一次傳遞時所收集的資訊來優化資料流程的編碼程式。

在「常數位速率編碼模式」中，以兩個階段編碼的檔案，通常比在單一傳遞中編碼的檔案更有效率。 以品質為基礎的 VBR （一次通過）會產生比以位速率為基礎的 VBR 更一致的品質，也就是兩個階段。

您無法在即時資料流上使用雙通編碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**編解碼器功能**](codec-features.md)
</dt> <dt>

[**使用 Two-Pass 編碼**](using-two-pass-encoding.md)
</dt> </dl>

 

 




