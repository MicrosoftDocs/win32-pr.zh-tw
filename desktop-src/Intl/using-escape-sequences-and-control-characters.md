---
description: 當應用程式將字串從 ASCII 或 Windows (ANSI) 字碼頁轉換為 unicode 時，它應該會逐字元將 escape 序列轉譯成 unicode。
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: 使用 Escape 序列和控制字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea89997a8f94a9fdd573b2c8360dbdd5342d38ca8bd2e7a133aa29943c07e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389917"
---
# <a name="using-escape-sequences-and-control-characters"></a>使用 Escape 序列和控制字元

當應用程式將字串從 ASCII 或[Windows (ANSI) 字碼頁](code-pages.md)轉換為 unicode 時，它應該會逐字元將 escape 序列轉譯成 unicode。 將 ASCII 或其他8位文字檔轉換成 Unicode 時，稍後可能會將它轉換回來。 以逐字元為基礎將 escape 序列轉換成 Unicode，而不是將它們組合成單一 Unicode 字元，就可以執行反向轉換，而不需要辨識和剖析 escape 序列。 例如，ESC + A 應該變成 0x001B (ESC) ，0x0041 () ，而不是0x411B。

Unicode 中的第一個 32 16 位代碼值適用于32控制字元。 此規格支援現有的控制字元使用，以做為格式化用途。 Unicode 應用程式可以將這些控制字元視為處理其 ASCII 對等專案的方式，完全相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 中的特殊字元](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



