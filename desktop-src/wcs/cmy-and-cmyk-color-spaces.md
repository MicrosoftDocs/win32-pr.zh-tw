---
title: CMY 和 CMYK 色彩空間
description: CMY 和 CMYK 色彩空間通常用於彩色列印。 CMY 色彩空間使用青色、洋紅和黃色 (CMY) 作為其主要色彩。 紅色、綠色和藍色是次要色彩。
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Color System (WCS) ，CMY 色彩空間
- WCS (Windows 色彩系統) ，CMY 色彩空間
- 影像色彩管理、CMY 色彩空間
- 色彩管理，CMY 色彩空間
- 色彩，CMY 色彩空間
- 色彩空間、CMY
- CMY 色彩空間
- Windows Color System (WCS) 、CMYK 色彩空間
- WCS (Windows 色彩系統) 、CMYK 色彩空間
- 影像色彩管理、CMYK 色彩空間
- 色彩管理，CMYKcolor 空間
- 色彩、CMYK 色彩空間
- 色彩空間、CMYK
- CMYK 色彩空間
- 青色
- 洋紅
- 黃色
- '青色洋紅黃色 (CMY) '
- 'CMY (青色洋紅黃色) '
- '青色洋紅色黃色黑色 (CMYK) '
- 'CMYK (青色洋黃色黑色) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106982782"
---
# <a name="cmy-and-cmyk-color-spaces"></a>CMY 和 CMYK 色彩空間

CMY 和 CMYK [色彩空間](c.md) 通常用於彩色列印。 CMY 色彩空間使用青色、洋紅和黃色 (CMY) 作為其 [主要色彩](p.md)。 紅色、綠色和藍色是次要色彩。

下圖是 CMY 色彩空間的色彩標記法。 CMY 色彩空間已正規化。

![cmy 色彩空間 cube （最大值）](images/cmyclrs1.png)

![cmy 色彩空間 cube （最小值）](images/cmyclrs2.png)

CMY 色彩空間為 subtractive。 因此，白色是 (0.0、0.0、0.0) 和黑色 (1.0、1.0、1.0) 。 如果您以白色開頭且不能減去任何色彩，您會得到白色。 如果您以白色開頭，並同樣地減去所有色彩，則會得到黑色。

CMYK 色彩空間是 CMY 模型的變化。 它會將黑色 (青色、洋紅、黃色和黑色) 。 CMYK 色彩空間會關閉理論與實務之間的差距。 理論上，不需要額外的黑色元件。 不過，使用各種類型的墨水和紙張的經驗，會顯示當混合青色、洋紅和黃色油墨的相等元件時，結果通常是深棕色，而不是黑色。 將黑色筆墨新增至混合可解決此問題。

CMY 和 CMYK 色彩空間可與裝置無關，但最常使用於特定裝置的參考中。

 

 




