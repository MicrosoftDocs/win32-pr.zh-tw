---
description: 列舉裝置和篩選器
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: 列舉裝置和篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53f4a36e2bf994cfeab34a49444d104b2213a839bb1fa8bd2aa4d70e0003b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401772"
---
# <a name="enumerating-devices-and-filters"></a>列舉裝置和篩選器

有時候，應用程式必須在使用者的系統上找出特定的篩選準則。 例如，影片捕獲應用程式可能會顯示可用的捕獲裝置清單。 因為 DirectShow 使用以元件為基礎的架構，所以您無法在設計階段得知使用者系統上安裝了哪些篩選器。 這特別適用于代表硬體裝置的篩選準則。 DirectShow 提供兩個元件來尋找已註冊的篩選準則：

-   [系統裝置列舉](system-device-enumerator.md)值會依類別目錄來尋找篩選。
-   [篩選器](filter-mapper.md)對應程式會根據應用程式所提供的搜尋條件來尋找篩選。

本節中所討論的列舉值會遵循 COM 列舉介面所使用的標準格式。 如需詳細資訊，請參閱 Microsoft 平臺軟體發展工具組 (SDK) 中的「IEnumXXXX」主題。

本節包含下列主題：

-   [使用系統裝置列舉值](using-the-system-device-enumerator.md)
-   [使用篩選器對應程式](using-the-filter-mapper.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本 DirectShow 工作](basic-directshow-tasks.md)
</dt> </dl>

 

 



