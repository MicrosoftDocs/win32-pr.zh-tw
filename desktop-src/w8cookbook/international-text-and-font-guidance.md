---
title: 國際文字與字型指導方針
description: 國際文字與字型指導方針
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375352"
---
# <a name="international-text-and-font-guidance"></a>國際文字與字型指導方針

## <a name="affected-platforms"></a>受影響的平臺

<dl> 用戶端-Windows 8 \| Windows 8。1  
伺服器-Windows Server 2012 \| Windows server 2012 R2  
</dl>

## <a name="description"></a>Description

自 Windows 2000 之前起，每個主要版本的 Windows 都已新增新腳本的文字顯示支援。 您可以在「[移至全球開發中心](https://msdn.microsoft.com/goglobal/default)」的[腳本和 Windows 檔的字型支援](https://msdn.microsoft.com/goglobal/bb688099.aspx)中，找到每個主要版本中所做變更的描述。

請注意，對於腳本的支援可能需要對文字堆疊元件進行某些變更，以及變更字型。 Windows 作業系統有許多文字堆疊元件： DirectWrite、GDI、Uniscribe、GDI +、WPF、RichEdit、Comctl32.dll 及其他。 提供的資訊主要適用于 GDI 和 DirectWrite。 它通常也適用于用於 Windows 8 存放區應用程式和轉譯 web 內容的 UI 架構，例如 RichEdit 或 MSHTML 轉譯代理程式，但這些元件可能會展現某些差異。

## <a name="best-practices"></a>最佳做法

**適用于開發人員的印刷樣式指引**

印刷樣式是 Microsoft 設計語言的核心。 每個 Microsoft 設計原則都強調印刷的重要性。 第一次，應用程式開發人員有一組支援先進印刷印刷功能的架構。 如需如何使用 JavaScript 和 HTML 來顯示和編輯 Windows Store 應用程式中文字的詳細資訊，請移至 [顯示和編輯文字](/previous-versions/windows/apps/hh465442(v=win.10)) 。

**字型計量**

字型計量是應用程式開發人員特定重要性的領域。 字型檔案包含與垂直和水準計量相關的各種值。 這些值記載于 [OpenType 規格](https://www.microsoft.com/typography/otspec/) 中，而且這些值會透過在 [DWRITE \_ 字型 \_ 計量結構](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) 和 [TEXTMETRIC 結構](/windows/win32/api/wingdi/ns-wingdi-textmetrica)中找到的各種 api 來公開。

## <a name="resources"></a>資源

-   [Windows 的腳本和字型支援](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [前往全球開發中心](https://msdn.microsoft.com/goglobal/default)
-   [顯示和編輯文字](/previous-versions/windows/apps/hh465442(v=win.10))
-   [OpenType 規格](https://www.microsoft.com/typography/otspec/)
-   [DWRITE \_ 字型 \_ 計量結構](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [TEXTMETRIC 結構](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 