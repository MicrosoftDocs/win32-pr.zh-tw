---
title: Macos textedit 控制項模式
description: 介紹執行 ITextEditProvider 的指導方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- 消費者介面自動化，執行 Macos textedit 控制項模式
- 消費者介面自動化，Macos textedit 控制項模式
- 控制項模式，Macos textedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8512db4f676a263bf46bdbdfea7b6b7eaba11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316348"
---
# <a name="textedit-control-pattern"></a>Macos textedit 控制項模式

介紹執行 [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider)的指導方針和慣例，包括屬性和方法的相關資訊。 **Macos textedit** 控制項模式用於以程式設計方式存取修改文字的控制項，例如執行自動校正或啟用輸入組合的控制項。

> [!Note]  
> 本主題中的「執行附注」指的是來自文字服務架構 (TSF) 的 Api。 如需 TSF 和 API 參考的詳細資訊，請參閱 [文字服務架構](/windows/desktop/TSF/text-services-framework)。

 

## <a name="required-members-for-itexteditprovider"></a>**ITextEditProvider** 的必要成員

執行 [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) 介面時需要這些屬性和方法。



| 必要成員                                                              | 成員類型 | 備註                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetActiveComposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | 方法      | 傳回目前轉換的範圍 (無（如果沒有轉換) ）。 傳回 TSF 中的使用中複合 (，這是由 GUID 成分 **\_ \_ 組成**) 標記的範圍。 例如，使用 Microsoft 日文輸入法編輯器 (IME) ，這會是完整加底線的文字。 |
| [**GetConversionTarget**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | 方法      | 如果沒有轉換) ，則傳回目前的轉換目標範圍 (無。 在 TSF 中，這是標示為 **tf \_ attr \_ Target \_ NOTCONVERTED** 或 **tf \_ attr \_ target \_** （從 **tf \_ DISPLAYATTRIBUTE** 結構轉換）的字元範圍。                                               |



 

**TextEditTextChanged** 和 **ConversionTargetChanged** 事件必須由支援 **macos textedit** 模式的 Microsoft 消費者介面自動化元素所引發。

### <a name="textedittextchanged"></a>**TextEditTextChanged**

-   使用 [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) 函數來引發 **TextEditTextChanged** 事件。
-   下表列出您應該引發事件的案例，以及要使用的 [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) 參數。



| TextEditChangeType                                            | 事件裝載                                | 備註                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**校正**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | 新增的更正字串                         | 當控制項進行自動校正時引發。 或每次透過 TSF 進行取代，而且範圍具有已套用之 **TKB \_ 替代 \_ 自動校正 \_** 的 **GUID 內容 \_ \_ TKB \_ 替換** 值。<br/>                                                                                                                                                                   |
| [**Composition**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | 更新的字串                           | 承載必須只包含變更的字元 (不會傳送整個撰寫字串) 。 每次進行組合取代時引發。 在 TSF 中，會將組合取代定義為已設定 **GUID \_ \_ 組成** 旗標的取代。 執行 TSF 的編輯控制項可以透過 **OnEndEdit** 通知來監視這些變更。<br/>         |
| [**CompositionFinalized**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | 完成的組合字元串 (查看附注)  | 在 TSF 中，要完成的轉換字串是由從組合中移除的 **GUID \_ \_ 組成** 旗標所定義。 執行 TSF 的編輯控制項應從 **EndComposition** 判斷已完成的字串，並在呼叫 **OnEndEdit** 時引發事件。<br/> 如果組合已取消或刪除，則完成的組合字元串可能是空的。<br/> |



 

### <a name="conversiontargetchanged"></a>**ConversionTargetChanged**

-   當轉換目標從某個目標變更為另一個目標時，就會發生 **ConversionTargetChanged** 。
-   您可以使用 [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) 函數來引發 **ConversionTargetChanged** 事件， (傳遞 [**UIA \_ macos textedit \_ ConversionTargetChangedEventId**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**) 事件識別碼) 。
-   當目標的內容變更時，不應引發 **ConversionTargetChanged** 。 如果目標變更同時與組合變更發生，則必須在引發任何組合事件之後引發目標變更事件。
-   在 TSF 中，轉換目標是由從 **tf \_ DISPLAYATTRIBUTE** 結構 **\_ \_ \_ 轉換成設定的 tf ATTR 目標** 值所定義。 您可以使用 **OnEndEdit** 來監視變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

