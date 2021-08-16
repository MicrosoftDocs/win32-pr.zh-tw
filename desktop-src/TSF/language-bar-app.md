---
title: 'Language Bar (TSF 應用程式) '
description: 應用程式無法將專案新增至語言列;只有文字服務可以將專案新增至語言列。
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- 文字服務架構 (TSF) 、language bar
- TSF (文字服務架構) 、language bar
- 啟用 TSF 的應用程式，語言列
- 語言列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0adeacdfe105700efba761b0622432f4ac382d147bd82145242be9fdd71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952106"
---
# <a name="language-bar-tsf-applications"></a>Language Bar (TSF 應用程式) 

應用程式無法將專案新增至語言列;只有文字服務可以將專案新增至語言列。 應用程式可能會影響語言列上特定專案的顯示方式。

[GUID 區間 \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md)區間用來表示應用程式可接受的語音輸入類型：直接文字輸入 (聽寫) 和/或語音命令。 依預設，會啟用聽寫並停用語音命令。 如果應用程式可以接受語音命令，則應該在 GUID 區間語音 DICTATIONSTAT 區間中設定 [TF 命令 \_ \_ ENABLED](speech-recognition-constants.md) 值 \_ \_ \_ 。 如果應用程式可以接受聽寫，則應該 \_ \_ 在 GUID 區間語音 DICTATIONSTAT 區間中設定 TF 聽寫啟用的值 \_ \_ \_ 。 此區間的值上的 TF \_ 聽寫 \_ ON 或 tf \_ 命令， \_ 會決定 (聽寫或命令) 語音輸入目前在哪個模式。

如果應用程式支援屬性資料的持續性儲存，則應該將 [GUID \_ 區間 \_ PERSISTMENUENABLED](predefined-compartments.md) 區間設定為非零值。 這會導致語音文字服務啟用 [ **儲存語音資料** ] 功能表項目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何設定文字服務架構](how-to-set-up-tsf.md)
</dt> <dt>

[Language Bar (Text Services) ](language-bar.md)
</dt> </dl>

 

 




