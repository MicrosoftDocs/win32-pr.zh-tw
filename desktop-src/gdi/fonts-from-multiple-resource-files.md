---
description: 多個資源檔中的字型
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: 多個資源檔中的字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/17/2021
ms.locfileid: "104992447"
---
# <a name="fonts-from-multiple-resource-files"></a>多個資源檔中的字型

一般而言，字型會包含在單一字型資源檔中。 不過，某些字型的資訊會散佈在多個檔案中。 例如，輸入1多個主要字型需要兩個檔案：

-   pfm 適用于字型計量
-   pfb 適用于字型位

若要從多個檔案將字型新增至系統，請使用 [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) 或 [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) 函數。 這些函式中的 *lpszFilename* 參數必須指向字串，其中包含以分隔號分隔的檔案名或 ( ) 的管道 \| 。 例如，若要指定類型1字型的 abcxxxxx. pfm 和 abcxxxxx，請使用 "abcxxxxx. pfm \| abcxxxxx. pfb" 字串。

[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) 與 [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) 的不同之處在于，呼叫 **AddFontResourceEx** 的應用程式可以將字型指定為私用或不可列舉。

若要從記憶體影像新增字型，請使用 [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex)。 這可讓應用程式使用內嵌在檔或網頁中的字型。

若要移除來自多個資源檔的字型，請呼叫 [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) 或 [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)，視用來新增字型的函式而定。 您必須指定用來新增字型的相同旗標。 若要移除從記憶體影像新增的字型，請使用 [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex)。

使用來自多個字型資源檔的字型，與使用單一資源檔中的字型相同。

 

 
