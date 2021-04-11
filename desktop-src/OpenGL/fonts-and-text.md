---
title: '字體和文字 (OpenGL) '
description: Microsoft 在 Windows 中執行 OpenGL 在單一緩衝的 OpenGL 視窗中支援 GDI 圖形。
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- Windows 上的 OpenGL，字型
- Windows 上的 OpenGL，文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383665"
---
# <a name="fonts-and-text-opengl"></a>字體和文字 (OpenGL) 

Microsoft 在 Windows 中執行 OpenGL 在單一緩衝的 OpenGL 視窗中支援 GDI 圖形。 它不支援雙緩衝 OpenGL 視窗中的 GDI 圖形。 因此，您只能呼叫標準 GDI 字型和文字函式，以在單一緩衝的 OpenGL 視窗中繪製文字;您無法呼叫這些函式，以在雙重緩衝的 OpenGL 視窗中繪製文字。

這項限制對於雙重緩衝視窗中的文字有因應措施：建立字元點陣圖影像的 OpenGL 顯示清單，然後執行這些顯示清單來繪製字元。 此程式有三個主要步驟：

1.  選取裝置內容的字型，並視需要設定字型的屬性。
2.  根據裝置內容字型中的字元，建立一組點陣圖顯示清單，應用程式將繪製的每個圖像都有一個顯示清單。
3.  使用這些點陣圖顯示清單，在字串中繪製每個字元。

若要建立顯示清單，請呼叫 [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) 和 [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) 函數。 若要使用這些顯示清單來繪製字串中的字元，請呼叫 [**glCallLists**](glcalllists.md)。

若要建立容易當地語系化的應用程式，並謹慎使用資源，必須小心地管理這些圖像顯示清單的建立和儲存。 不同于英文的許多語言都有字母，其字元碼範圍會超過相當大的值集。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型和文字函數](font-and-text-functions.md)
</dt> </dl>

 

 




