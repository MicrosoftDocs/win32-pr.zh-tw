---
title: UI 自動化文字單位
description: 本主題說明 Microsoft 消費者介面自動化 \ 32 所支援的文字單位;TextRange 控制項模式。 消費者介面自動化提供者和用戶端會使用文字單位來指定移動或變更文字範圍大小所依據的數量。
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- 消費者介面自動化，文字單位
- 文字單位，關於
- 消費者介面自動化，文字單位清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff4257c70b34cea01a149b30dff2bf2fbe691a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315268"
---
# <a name="ui-automation-text-units"></a>消費者介面自動化文字單位

本主題說明 Microsoft 消費者介面自動化 [TextRange](uiauto-implementingtextandtextrange.md) 控制項模式所支援的文字單位。 消費者介面自動化提供者和用戶端會使用文字單位來指定移動或變更文字範圍大小所依據的數量。

-   [文字單位 API 元素](#text-unit-api-elements)
-   [文字單位描述](#text-unit-descriptions)
    -   [字元](#character)
    -   [格式](#format)
    -   [Word](#word)
    -   [線條](#line)
    -   [Paragraph](#paragraph)
    -   [頁面](#page)
    -   [文件](#document)
-   [其他可能的範圍](#other-potential-ranges)
-   [相關主題](#related-topics)

## <a name="text-unit-api-elements"></a>文字單位 API 元素

消費者介面自動化 API 包含下列需要指定文字單位的方法：

-   [**ITextRangeProvider：： Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**IUIAutomationTextRange：： Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**IUIAutomationTextRange::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

[**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)列舉會定義消費者介面自動化文字範圍所支援的文字單位。 若要指定文字單位， [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 列舉的成員是在 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) 或 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) 方法的呼叫中指定。 文字單位（從最小到最大）如下所示：

-   [**TextUnit \_ 字元**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ 格式**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ 行**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ 段落**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ 頁面**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ 檔**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

如果特定以文字為基礎的控制項不支援指定的文字單位，則提供者應該以控制項所支援的下一個較大文字單位來回應。 例如，如果指定了 [**TextUnit \_ 段落**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ，但不支援，則方法可以替代 [**TextUnit \_ 頁面**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 或 [**TextUnit \_ 檔**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)。

來源文字的語言特性可讓提供者難以根據指定的文字單位來判斷文字界限。 為了協助判斷文字界限，提供者可以使用 Uniscribe API 函式，例如 [**ScriptBreak**](/windows/desktop/api/usp10/nf-usp10-scriptbreak)。 如需詳細資訊，請參閱 MSDN 網站上的 [Uniscribe](/windows/desktop/Intl/uniscribe) 。

## <a name="endpoint-inclusivity"></a>端點包容性

文字單位端點可以作為相同類型之相鄰文字範圍的 [起始](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) 端點和 [端點](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) 端點。 如果某個文字單位的結尾也是另一個文字單位的開頭，則包含 [結束](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) 端點的範圍不會共用包含 [開始](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) 端點之相鄰範圍的任何屬性或物件。

例如，文字資料流程 "Hello **world**" 包含兩個字型粗細屬性不同的文字單位 (一般和粗體) 。 在此情況下，文字單位 "Hello" 的 [結束](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)端點和單字單位 "**World**" 的 [開始](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)端點是相同的，因此會產生下列結果：

- "Hello" 的範圍不會共用字組 "world" 的粗體字屬性，也不會傳回字型粗細文字屬性的 mixed 屬性值。
- "**World**" 的範圍具有單一字型粗細 (粗體) ，且不會共用上述字組 "Hello" 的字型粗細。

以下是另一個範例，其中的文字資料流程包含兩個單字單元，其中一個是連結： `[Foo]() Bar` 。 在此情況下，單字單元的 [結束](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) 端點 `[Foo]()` 和單字單位 "Bar" 的 [開始](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) 端點是相同的，因此會產生下列結果：

- 連結屬於包含 "Foo" 的文字範圍。
- 連結是文字範圍 "Foo" 的子系，並以 [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)括住。
- 文字範圍 "Bar" 沒有子系，而且會以 [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)括住。

**其他注意事項：**

> 在具有相同類型之文字範圍的文字單位界限上，退化 (空白) 範圍會假設立即相鄰文字單位的屬性。
>
> 在具有相同類型之文字範圍的文字單位界限上，對一個退化範圍呼叫 [IUIAutomationTextRange：： ExpandToEnclosingUnit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) 時，會將退化範圍展開至下列文字單位。

## <a name="text-unit-descriptions"></a>文字單位描述

本節說明消費者介面自動化所支援的每個文字單位。

### <a name="character"></a>字元

[**TextUnit \_字元**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 是代表單一字元之文字的語言單位。 字元的語言定義會依語言而有所不同。 若是美式英文，字元通常會以空格或其他字元（例如標點符號、數位或字母）來加上邊框。

像是換行字元的控制字元，以及 Unicode 的左到右標示 (LTM) 不應視為字元，但可以包含在根據字元文字單位正規化的文字範圍中。

標點符號和斷字字元（例如空格）應該視為字元。

### <a name="format"></a>格式

[**TextUnit \_格式**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 是用來根據文字的格式化屬性，來定位文字範圍的界限。 例如，如果文字範圍目前定位於單字的單一字元，則在 [**IUIAutomationTextRange：： ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)的呼叫中指定 **TextUnit \_ 格式** 會展開文字範圍，以包含所有與單一字元共用所有相同屬性的文字。 產生的文字範圍不一定會包含整個單字。 此外，使用格式文字單位並不會在内嵌物件（例如影像或超連結）的界限上展開文字範圍。

不同于其他文字單位（包含小於自身的文字單位）， [**TextUnit \_ 格式**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 可以比其他單位小或大。 例如，如果整份檔共用相同的 text 屬性，且不包含任何内嵌物件，依 **TextUnit \_ 格式** 展開文字範圍將會建立包含整份檔的新範圍，而依 [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 展開文字範圍會建立較小的範圍。

### <a name="word"></a>Word

[**TextUnit \_Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 是代表單一單字的文字語言單位。 單字的語言定義會因語言而異。 針對美式英文，單字通常會以空格或標點符號字元分隔。

當 [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 用來設定文字範圍的界限時，產生的文字範圍應包含出現在單字結尾，但在下一個單字開頭之前的任何斷詞字元。

### <a name="line"></a>線條

[**TextUnit \_線條**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 是一種文字單位，代表控制項的各方面所呈現的單一文字行。 使用 **TextUnit \_ 線** 設定文字範圍的界限時，提供者應該在控制字元中斷該行的點之後立即設定界限，或讓控制項的視口將文字換行至新行。 界限應該在新行開始時設定。

### <a name="paragraph"></a>Paragraph

[**TextUnit \_段落**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 是表示完整段落的語言文字。 段落應該在段落的第一個字元之前開始，而且通常會在最後一個字元之後結束。 段落後面的任何空白行都應該合併到段落中，除非文字來源中的某些內容表示其他。 通常，段落的結束界限也會標示 [**TextUnit \_ 線**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 文字單位的結束界限。

### <a name="page"></a>頁面

[**TextUnit \_頁面**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 代表檔的完整文字頁面。 頁面的界限應該在頁面開始和結束的立即點設定。

### <a name="document"></a>文件

[**TextUnit \_檔**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 代表 [文字](uiauto-implementingtextandtextrange.md) 控制項模式所支援之檔的整個內容。 包含檔的文字範圍之外不應有任何文字。 插入檔中的任何物件（例如跨頁面界限的注釋附注），都應該視為檔的内嵌物件，而不是檔文字內容的一部分。

## <a name="other-potential-ranges"></a>其他可能的範圍

目前的 [TextRange](uiauto-implementingtextandtextrange.md) 控制項模式規格不允許將新的文字單位值新增至 [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 列舉，也不允許重新定義現有的文字單位值。 若要公開其他可能的範圍，例如標頭和注釋，提供者應該將這些範圍公開為具有相關聯文字範圍的内嵌物件。 如此一來，您也可以新增適當控制項模式的支援。 此解決方案比定義新的文字單位更有彈性且可擴充。

## <a name="related-topics"></a>相關主題

### <a name="reference"></a>參考

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider：： GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>概念

[消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)

[使用以文字為基礎的控制項](uiauto-workingwithtextbasedcontrols.md)