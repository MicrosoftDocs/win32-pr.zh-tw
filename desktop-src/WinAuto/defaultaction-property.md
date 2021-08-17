---
title: DefaultAction 屬性
description: 物件的 DefaultAction 屬性會描述物件的主要操作方法，從使用者的觀點來看。 物件的 DefaultAction 屬性應該是動詞或簡短動詞片語。
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd5aa70e0c6c633aa5b0ca3fe5c40049dbeb8cf2496c7785eea513821e1d5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325752"
---
# <a name="defaultaction-property"></a>DefaultAction 屬性

物件的 **DefaultAction** 屬性會描述物件的主要操作方法，從使用者的觀點來看。 物件的 **DefaultAction** 屬性應該是動詞或簡短動詞片語。

藉由呼叫 [**IAccessible：： get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)，即可取出 **DefaultAction** 屬性。

用戶端會呼叫 [**IAccessible：： accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)來執行物件的預設動作。

並非所有物件都有預設動作，而某些物件具有與其 [**Value**](value-property.md) 屬性相關的預設動作，如下列範例所示：

-   選取的核取方塊具有預設動作「取消核取」和「已檢查」的值。
-   已清除的核取方塊具有預設動作 [檢查] 和 [未選取] 的值。
-   標示為「列印」的按鈕具有預設動作「按下」，沒有任何值。
-   顯示「印表機」的靜態文字控制項或編輯控制項沒有預設動作，但值為「印表機」。

 

 




