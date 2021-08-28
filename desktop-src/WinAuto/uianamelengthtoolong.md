---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- UIA_NamePropertyId 識別碼 AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec235897680cde3b024a67745b923e989cfc68db3b154be260c9dcd3510ba10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993968"
---
# <a name="uianamelengthtoolong"></a>UiaNameLengthTooLong

## <a name="text"></a>Text

元素的名稱不應傳回長度超過字元的字串 {0}

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素名稱包含太多字元。 例如，用來取出專案之 UIA 名稱的 [**IUIAutomationElement：： CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) 方法會傳回大於限制的字串。

這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為元素可能有 unpronounceable、非直覺的名稱。

## <a name="possible-causes"></a>可能的原因

元素或其父系有不正確指派的名稱或標籤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




