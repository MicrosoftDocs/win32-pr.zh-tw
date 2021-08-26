---
description: 代理和補充字元
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: 代理和補充字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b1dc4743627297962c7279449c06cc1ff967ac35f931a6e945b4577c937b59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130048"
---
# <a name="surrogates-and-supplementary-characters"></a>代理和補充字元

Windows 的應用程式通常會使用 utf-16 來代表[Unicode](unicode.md)字元資料。 使用16個位可直接表示65536的唯一字元，但這個基本多語系平面 (BMP) 幾乎不足以涵蓋人類語言中使用的所有符號。 Unicode 4.1 版包含超過97000個字元，且僅適用于中文的超過70000個字元。

Unicode 標準已建立16個字元的額外「平面」，每個字元的大小都與 BMP 相同。 當然，除了 BMP 以外的大部分程式碼點尚未指派字元給它們，但平面的定義讓 Unicode 有可能定義1114112字元 (也就是在程式 \* 代碼點範圍 u + 0000 到 u + 10FFFF 內，2¹⁶17個) 字元。 若為 UTF-16 以表示這組較大的字元組，Unicode 標準會定義「增補字元」。

## <a name="about-supplementary-characters"></a>關於補充字元

補充字元是位在 BMP 以外的字元，而「代理」是 UTF-16 程式碼值。 若為 UTF-16，則需要「代理配對」以表示單一補充字元。 第一個 (high) 代理是16位的代碼值，範圍 U + D800 到 U + DBFF。 第二個 (低) 代理是16位的代碼值（範圍 U + DC00 到 U + DFFF）。 使用代理機制，UTF-16 可以支援所有1114112可能的 Unicode 字元。 如需有關增補字元、代理程式和代理組的詳細資訊，請參閱 [Unicode 標準](https://www.unicode.org/standard/standard.html)。

> [!Note]  
> Windows 2000 引進了基本輸入、輸出，以及補充字元的簡單排序支援。 不過，並非所有系統元件都與補充字元相容。

 

作業系統可透過下列方式支援補充字元：

-   OpenType 字型 cmap 資料表的格式12直接支援4位元組字元碼。 如需詳細資訊，請參閱 [OpenType 字型規格](/typography/opentype/spec/)。
-   Windows 支援已啟用代理功能的[輸入方法編輯器 (ime) ](../dxtecharts/installing-and-using-input-method-editors.md)。
-   [Windows GDI](../gdi/windows-gdi.md) API 支援在字型中格式化12個 cmap 資料表，讓代理程式可以正確顯示。
-   [Uniscribe](uniscribe.md) API 支援補充字元。
-   [Windows 控制項](../controls/window-controls.md)（包括[編輯](../controls/edit-controls.md)和[Rich edit](../controls/rich-edit-controls.md)）支援補充字元。
-   html 引擎支援包含補充字元的 html 網頁，可透過 Outlook Express) 和表單提交來顯示、編輯 (。
-   作業系統排序表支援補充字元。

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>使用補充字元進行軟體發展的一般指導方針

UTF-16 會將補充字元處理為代理組。 作業系統會以類似于處理非 [間距標記](using-nonspacing-characters-and-diacritics.md)的方式來處理代理配對。 在顯示時間，代理字組會透過 Unicode 標準所規定，以 Uniscribe 的方式顯示為一個圖像。

WindowsVista 引進了三個新宏，可協助您識別 UTF-16 字串中的代理和代理配對。 這些都 [**是 \_ 高 \_ 代理**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate)、 [**\_ 低 \_ 代理**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)和 [**\_ 代理 \_ 配對**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair)。

如果應用程式支援 Unicode 並使用系統控制項和標準 API 函式（例如 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) 和 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)），則會自動支援補充字元。 因此，如果您的應用程式使用標準系統控制項，或使用一般 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)類型呼叫來顯示，補充字元應該可以運作，而不需要任何特殊的編碼。

以自訂方式來處理圖像位置的應用程式，可以使用 Uniscribe 進行所有文字處理，藉此實現自己的編輯支援。 Uniscribe 有不同的函式來處理複雜的腳本處理，例如文字顯示、點擊測試和資料指標移動。 應用程式必須專門呼叫 Uniscribe 函式，才能取得這些先進的功能。 請注意，使用 Uniscribe 函式的應用程式完全是多語系的，但這會造成效能上的負面影響。 因此，有些應用程式應該自行處理補充字元。

因為代表補充字元的代理機制是妥善定義的，所以您的應用程式可以包含程式碼來處理 UTF-16 代理文字處理。 當應用程式從較低的保留代理範圍 (低代理) 或較高的保留代理範圍（ (高代理) ）遇到分隔的 UTF-16 值時，此值必須是代理配對的一半。 因此，應用程式可以藉由執行簡單的範圍檢查，來偵測代理程式配對。 如果它在較低或上限的範圍內遇到 UTF-16 值，它必須向前或向後再追蹤 1 16 位的寬度，才能取得字元的其餘部分。 撰寫您的應用程式時，請記住， [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) 和 [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) 是由16位程式碼點移動，而不是由代理配對所移動。

> [!Note]  
> 獨立代理程式碼點具有高代理（沒有連續的低代理），反之亦然。 這些程式碼點無效，且不受支援。 它們的行為未定義。

 

如果您正在開發字型或 IME 提供者，請注意預先 Windows XP 作業系統預設會停用補充字元支援。 WindowsXP 和更新版本預設會啟用補充字元。 如果您提供的字型和 IME 套件需要補充字元，則您的應用程式必須設定下列登錄值：


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\LanguagePack]
SURROGATE=(REG_DWORD)0x00000002

[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\International\Scripts\42]
IEFixedFontName=[Surrogate Font Face Name]
IEPropFontName=[Surrogate Font Face Name]
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[字元集](character-sets.md)
</dt> </dl>

 

 
