---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acecf91e90f93ccb1d220e9b2d91cbaa012b8d436b18a910daa73bf6ca3f1fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859998"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Text

從 get accRole 傳回的 int \_ 不是有效的角色常數，也就是 IE 角色 \_ 系統\_\*

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素報告了不正確 MSAA 角色。 例如， [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) 方法會傳回一個整數值，這個值不會對應到有效的物件角色常數 (例如角色 \_ 系統表示 \_) 。

這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為專案可能會不正確地識別給使用者。

## <a name="possible-causes"></a>可能的原因

元素或其父系的 MSAA 角色設定不當。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**物件角色**](object-roles.md)
</dt> </dl>

 

 




