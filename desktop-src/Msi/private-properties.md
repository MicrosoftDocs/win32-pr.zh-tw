---
description: 私用屬性是由安裝程式在內部使用，且其值必須由安裝封裝的作者在資料庫中輸入，或是由安裝程式在安裝期間由安裝程式設定為由作業環境決定的值。
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: 私用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d166f876bb953008a6920c3089fab5974ebbb05909c1b41db299212ee069dd8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558411"
---
# <a name="private-properties"></a>私用屬性

私用屬性是由安裝程式在內部使用，且其值必須由安裝封裝的作者在資料庫中輸入，或是由安裝程式在安裝期間由安裝程式設定為由作業環境決定的值。 使用者可以與私用屬性互動的唯一方式，是透過在套件撰寫的使用者介面中 [控制事件](control-events.md) 。 私用屬性名稱必須包含小寫字母。 請參閱 [屬性名稱的限制](restrictions-on-property-names.md)。

私用屬性通常會描述操作環境。 例如，如果是在 Windows 的平臺上執行安裝，安裝程式會將 [**WindowsFolder**](windowsfolder.md)屬性設定為屬性工作表中指定的值。

無法在命令列覆寫私用屬性值。 若要從安裝清除私用屬性，請將它保留在 [屬性工作表](property-table.md)中。 在 Windows XP 和 Windows 2000 中，您無法在安裝的使用者介面階段設定私用屬性，然後將值傳遞至執行階段。

如需安裝程式所使用之所有標準私用屬性的清單，請參閱 [屬性參考](property-reference.md)。 您可以藉由在屬性工作表中輸入屬性的名稱和初始值，來定義自訂私用屬性。 私用屬性名稱一律必須包含小寫字母。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[公用屬性](public-properties.md)
</dt> </dl>

 

 



