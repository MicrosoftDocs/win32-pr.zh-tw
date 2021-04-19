---
title: 使用安全陣列的最佳作法
description: Microsoft 消費者介面自動化的許多介面方法 \ 32;API 會將 SAFEARRAY 資料類型的引數稱為安全陣列。 本主題說明在消費者介面自動化應用程式中使用安全陣列的最佳作法。
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- 消費者介面自動化、安全陣列
- 消費者介面自動化，提供者
- 消費者介面自動化，用戶端
- 消費者介面自動化，在資料類型之間轉換
- 用戶端、安全陣列
- 提供者，消費者介面自動化
- 安全陣列
- 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969114"
---
# <a name="best-practices-for-using-safe-arrays"></a>使用安全陣列的最佳作法

Microsoft 消費者介面自動化 API 的許多介面方法都採用 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 資料類型的引數（稱為安全陣列）。 本主題說明在消費者介面自動化應用程式中使用安全陣列的最佳作法。

## <a name="clients"></a>用戶端

搭配消費者介面自動化用戶端 API 方法使用的所有安全陣列都是以零為基礎的一維陣列。 若要建立消費者介面自動化用戶端方法的安全陣列，請使用 [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) 函式，以及讀取和寫入安全陣列，使用 [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) 和 [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) 函數。 當您使用安全陣列完成時，請一律使用 [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) 函式來終結它，無論您建立的是安全陣列，還是從消費者介面自動化用戶端方法收到它。

數個消費者介面自動化的方法，包括屬性抓取方法（例如 [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)），可取得可以包含 [**POINT**](/previous-versions//dd162805(v=vs.85))或 [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)結構的 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)。 **點** 會封裝成 **VARIANT** 形式的安全陣列， (VT \_ R8) 與位於索引0的 **x** 成員，以及位於索引1的 **y** 成員。 同樣地， **UiaRect** 會封裝成 **VARIANT** 形式的安全陣列，其具有 **左方**、 **頂端**、 **寬度** 和 **高度** 成員（索引0到3）。 針對 **UiaRect** 結構的陣列，安全陣列針對每個 **UiaRect** 包含四個雙精度浮點數的連續陣列。 第一個 **UiaRect** 的 **左邊**、 **top**、 **width** 和 **height** 成員占索引0到3，第二個矩形的成員佔用索引4到7，依此類推。

[**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)介面包含下列方法，可在 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)和各種其他資料類型之間進行轉換。



| 方法                                                                                               | 描述                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | 將整數陣列轉換為 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)。                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | 將整數的 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 轉換成陣列。                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | 將包含矩形座標的 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 轉換成 **RECT** 類型的陣列。 |



 

## <a name="providers"></a>提供者

提供者必須執行一些介面方法，這些方法消費者介面自動化呼叫來從提供者取得資訊。 許多時候，這項資訊是由值陣列所組成。 若要將陣列傳回消費者介面自動化，提供者必須將陣列封裝成 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 結構。 陣列元素必須是預期的資料類型，而且必須以預期的順序顯示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> <dt>

[UI 自動化基礎](entry-uiautocore-overview.md)
</dt> </dl>

 

 