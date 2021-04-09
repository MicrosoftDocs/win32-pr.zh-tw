---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675663"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Text

元素的名稱 ({0}) 不應包含元素的角色 (的文字 {1}) 

## <a name="type"></a>類型

警告

## <a name="description"></a>描述

元素的名稱會併入其 MSAA 角色或 UIA 控制項類型。 例如，如果 [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)方法（用來抓取專案的 MSAA 名稱）傳回「角色 \_ 系統捲軸」，則可能會發生這個警告 \_ \_ \* 。

這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為角色會被讀取兩次，或是使用者可能 unpronounceable 或非直覺。

## <a name="possible-causes"></a>可能的原因

-   元素或其父系有不正確指派的名稱或標籤。
-   元素或其父系具有尚未修改為易記名稱的預設名稱。 例如，button1。
-   開發人員不知道螢幕讀取器會讀取名稱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name 屬性](name-property.md)
</dt> </dl>

 

 




