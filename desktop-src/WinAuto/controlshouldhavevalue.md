---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183668"
---
# <a name="controlshouldhavevalue"></a>ControlShouldHaveValue

## <a name="text"></a>Text

角色為的控制項 {0} 應具有值，但未實 \_ accValue

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

根據指派的 MSAA 角色，元素不會如預期般提供值，這表示該元素未實作用 [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 方法。 例如，下列 MSAA 角色應該都提供一個值。

-   角色 \_ 系統 \_ COMBOBOX
-   角色 \_ 系統 \_ IPADDRESS
-   角色 \_ 系統 \_ 連結
-   角色 \_ 系統 \_ OUTLINEITEM
-   角色 \_ 系統 \_ PROGRESSBAR
-   角色 \_ 系統 \_ 滑杆
-   角色系統已進行數值 \_ \_ 調節
-   角色 \_ 系統 \_ 捲軸
-   角色 \_ 系統 \_ 文字

這個問題是因為有內建值的元素必須能夠將該值回報給使用者，所以依賴螢幕讀取器和鍵盤進行導覽的人會遇到問題。

## <a name="possible-causes"></a>可能的原因

元素或其父系的 MSAA 角色設定不當。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**物件角色**](object-roles.md)
</dt> </dl>

 

 




