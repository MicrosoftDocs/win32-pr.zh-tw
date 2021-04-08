---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839723"
---
# <a name="uianameshouldnotcontaincontroltype"></a>UiaNameShouldNotContainControlType

## <a name="text"></a>Text

元素的名稱 ({0}) 不應包含 ControlType (的文字 {1}) 

## <a name="type"></a>類型

警告

## <a name="description"></a>描述

元素的名稱會併入其 UIA 控制項類型。 例如，如果具有按鈕控制項類型之專案的 [UIA Name] 屬性設定為 [我的按鈕]，就會發生這個警告。

這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為控制項類型將會讀取兩次，或是使用者可能 unpronounceable 或非直覺。

## <a name="possible-causes"></a>可能的原因

-   元素或其父系有不正確指派的名稱或標籤。
-   元素或其父系具有尚未修改為易記名稱的預設名稱。 例如，button1。
-   開發人員並不知道螢幕讀取器會讀取名稱和控制項類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




