---
description: 安裝程式會使用下列優先順序來設定屬性。 此清單中的屬性值可以覆寫在其後面的值，並由在清單中之前的值覆寫。
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: 屬性優先順序的順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980064"
---
# <a name="order-of-property-precedence"></a>屬性優先順序的順序

安裝程式會使用下列優先順序來設定屬性。 此清單中的屬性值可以覆寫在其後面的值，並由在清單中之前的值覆寫。

1.  作業環境所指定的屬性。
2.  在命令列上設定的[公用屬性](public-properties.md)。
3.  [**AdminProperties**](adminproperties.md) propertyset 在 [系統管理安裝](administrative-installation.md)期間列出的公用屬性。
4.  在應用程式 [*轉換*](t-gly.md)期間設定的公用或私用屬性。
5.  藉由撰寫 .msi 檔案的 [屬性工作表](property-table.md) 所設定的公用或私用屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於屬性](about-properties.md)
</dt> </dl>

 

 



