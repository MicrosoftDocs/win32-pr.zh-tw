---
description: TrueType 字型檔案包含 PANOSE 數位，可讓應用程式用來選擇與規格相符的字型。
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: 使用 PANOSE 號碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a974a0d1e708cac931e06e386e2df0802cbea79e5c9d499ca460d6deb5b0bab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037456"
---
# <a name="using-panose-numbers"></a>使用 PANOSE 號碼

TrueType 字型檔案包含 PANOSE 數位，可讓應用程式用來選擇與規格相符的字型。 PANOSE 系統會將臉部分類為10個不同的屬性。 如需這些屬性的詳細資訊，請參閱 [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose)。 **PANOSE** 結構是 [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)結構的一部分， (其值會藉由呼叫 [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)函數) 來填入。

PANOSE 屬性會依比例個別分級。 產生的值會串連以產生數位。 如果字型的這個數位和數學標準來測量 PANOSE 空間中的距離，應用程式可以決定最接近的相鄰專案。

 

 



