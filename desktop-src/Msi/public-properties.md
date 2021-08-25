---
description: 您可以用與私用屬性相同的方式，將公用屬性撰寫至安裝資料庫。
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: 公用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0138db2fcbe664ac9a4064379486c42c3d52a6896fc53a608b99192a8d70c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828428"
---
# <a name="public-properties"></a>公用屬性

您可以用與 [私用屬性](private-properties.md)相同的方式，將公用屬性撰寫至安裝資料庫。 此外，使用者或系統管理員可以藉由在命令列上設定屬性、套用轉換，或與撰寫的使用者介面互動，來變更公用屬性的值。 公用屬性名稱不能包含小寫字母。 請參閱 [屬性名稱的限制](restrictions-on-property-names.md)。

公用屬性通常會在安裝期間由使用者設定。 例如，您可以在用來啟動安裝的命令列或使用撰寫的使用者介面選擇的命令列中指定 public property [**INSTALLLEVEL**](installlevel.md) 屬性。

您可以在命令列使用 [標準](standard-actions.md) 或 [自訂](custom-actions.md) 動作、套用轉換，或讓使用者與撰寫的使用者介面進行互動，來覆寫公用屬性值。 若要清除屬性工作表中的公用屬性，請將它保留在資料表中。 在安裝期間要由使用者介面設定，然後傳遞至安裝的執行時間的屬性必須是公用的。

如需安裝程式所使用的標準公用屬性清單，請參閱 [屬性參考](property-reference.md)。 作者也可以藉由在 [屬性工作表](property-table.md)中輸入屬性的名稱和初始值，來定義自訂的公用屬性。 如果下列任何一個條件成立，則所有使用者都可以覆寫所有公用屬性。

-   使用者是系統管理員。
-   每一電腦的 EnableUserControl 原則設定為1。 請參閱 [系統原則](system-policy.md)。
-   [**EnableUserControl**](-enableusercontrol.md)屬性設定為1。
-   這是未以較高許可權執行的非受控安裝。

如果上述條件都不成立，則安裝程式會預設為限制不是系統管理員的使用者可覆寫哪些公用屬性。 請參閱 [**受限制的公用屬性**](restricted-public-properties.md)。

 

 



