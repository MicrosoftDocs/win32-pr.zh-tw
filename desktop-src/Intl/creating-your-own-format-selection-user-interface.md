---
description: 國際文字顯示
ms.assetid: e6cc5169-1a6e-40f8-b616-e76ec919195c
title: 國際文字顯示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8ba7eb6f1a043bb642945e178f3545bcd51738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027361"
---
# <a name="international-text-display"></a>國際文字顯示

有四個可能的選項可用來顯示國際文字，而這也需要複雜字集的輸出：

-   呼叫 Windows 文字 Api
-   具現化 Windows 標準編輯控制項
-   具現化 rich edit 控制項
-   呼叫 Uniscribe

如需這些選項的說明和優點，請參閱 [顯示文字的選項](https://msdn.microsoft.com/globalization/mt662335) 。 然後，您可以根據應用程式的複雜度和其設計功能，決定哪一個是您應用程式的最佳選項。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta)
</dt> <dt>

[**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)
</dt> <dt>

[**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta)
</dt> <dt>

[**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)
</dt> <dt>

[**GetTabbedTextExtent**](/windows/win32/api/winuser/nf-winuser-gettabbedtextextenta)
</dt> <dt>

[**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a)
</dt> <dt>

[**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa)
</dt> <dt>

[**編輯控制項**](../msi/edit-control.md)
</dt> <dt>

[Rich Edit](../controls/about-rich-edit-controls.md)
</dt> <dt>

[Uniscribe](uniscribe.md)
</dt> </dl>

 

 
