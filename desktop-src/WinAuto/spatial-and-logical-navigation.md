---
title: 空間和邏輯導覽
description: 用戶端會藉由呼叫 IAccessible accNavigate 並指定其中一個導覽常數，來抓取在相同容器內空間或邏輯上接近另一個物件之物件的相關資訊。
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e49772a267e49d723a04005dcbc8a369510b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965859"
---
# <a name="spatial-and-logical-navigation"></a>空間和邏輯導覽

用戶端會藉由呼叫 [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 並指定其中一個 [導覽常數](navigation-constants.md)，來抓取在相同容器內空間或邏輯上接近另一個物件之物件的相關資訊。

使用 *空間導覽* 用戶端時，會根據其在畫面上的位置來流覽至物件。 用戶端會從目前的物件向上、向下、向左或向右導覽，以取得相同容器內另一個物件的相關資訊。

使用 *邏輯導覽* 用戶端時，流覽至邏輯上或緊接在另一個物件（由伺服器決定）上的物件。 用戶端會以兩種方式流覽至物件的所有子系：

-   使用 [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md)開始導覽，然後使用 NAVDIR 重複呼叫方法。 [**\_**](navigation-constants.md)
-   使用 [**NAVDIR \_ LASTCHILD**](navigation-constants.md) 開始導覽，並使用 [**\_ 先前的 NAVDIR**](navigation-constants.md)重複呼叫方法。

不論方向為何，導覽都會造訪屬於父物件的每個可見的子系。 隱藏的子系可能會略過邏輯導覽。 此外，每個子系只會造訪一次，而流覽不會進行迴圈。 也就是說，如果用戶端嘗試在第一個物件之前或最後一個物件之後流覽，則方法會失敗。

空間和邏輯導覽是相關的。 例如，在水準工具列中，使用 [**NAVDIR \_ RIGHT**](navigation-constants.md) 呼叫方法應該會產生與使用 NAVDIR 來呼叫方法相同的結果 [**\_**](navigation-constants.md)。

除非指定了 [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md)或 [**NAVDIR \_ LASTCHILD**](navigation-constants.md) ，否則導覽的起始物件是它本身 **或其中一個物件的子** 物件; 在此情況下，流覽必須從物件本身開始。

如果用戶端從可存取的物件流覽至同級使用者介面專案，或如果 *varStart* 的 **LVal** 成員是 **CHILDID \_ SELF** ，而 *navDir* 中指定的旗標是 [**navDir \_ FIRSTCHILD**](navigation-constants.md)或 [**navDir \_ LASTCHILD**](navigation-constants.md)以外的任何導覽旗標，則 *pvarEnd* 中的結果會是子識別碼或 [**IDispatch**](idispatch-interface.md)介面。 如果 *pvarEnd* 包含子識別碼，用戶端必須先取得父系的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，才能從這個使用者介面專案進行流覽，或取得其相關的詳細資訊。 為了取得父物件，用戶端會呼叫該物件的 [**IAccessible：： get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 屬性或導覽的起始物件。

請注意，用戶端必須透過呼叫 [**EnumChildWindows**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) 函式來取得所有浮動物件的相關資訊。 由於浮動物件不會裁剪至其父系，因此用戶端不會有兩個物件之間的階層式關聯性相關資訊（在畫面上彼此接近）

下圖是未裁剪至其父系的浮動物件範例。

![浮動在較大型 microsoft developer studio 視窗上方之開啟視窗的螢幕擷取畫面](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>在邏輯導覽中建立順序

在邏輯導覽中，設計物件的開發人員會建立它們之間的關聯性。 邏輯導覽比空間導覽更主觀。 此外，邏輯導覽中的順序與子識別碼搭配使用的順序不同。

對於具有螢幕位置的物件，伺服器開發人員應以大部分使用者認為邏輯的方式來建立導覽順序。 比方說，在英文的國家/地區中，這表示由左至右、由上到下的順序。

邏輯流覽順序必須平行鍵盤導覽順序。 例如，對話方塊包含 **[確定]** 和 [ **取消** ] 按鈕，以及一些編輯控制項。 當用戶端呼叫 [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) ，以流覽至該對話方塊中的下一個或上一個物件時，會以使用者按下 TAB 或 SHIFT + tab 的相同順序移動專案之間的焦點。

針對沒有定義螢幕位置的物件，邏輯順序是由伺服器開發人員決定，而且用戶端開發人員不應該對其進行任何假設。 比方說，不可見的物件（例如只會暫時隱藏的物件）可以接受，以與可見的物件交錯。

 

 