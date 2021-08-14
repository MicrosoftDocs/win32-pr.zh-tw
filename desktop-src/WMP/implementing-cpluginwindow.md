---
title: 執行 CPluginWindow
description: 執行 CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Windows Media Player 外掛程式、CPluginWindow 類別
- 外掛程式，CPluginWindow 類別
- 使用者介面外掛程式、CPluginWindow 類別
- UI 外掛程式、CPluginWindow 類別
- CPluginWindow 類別
- 程式設計指南，使用者介面外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6364d991fb219678d4f64b09ae4cd3df2526e77797093dcfff3a8dbce7f36101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748133"
---
# <a name="implementing-cpluginwindow"></a>執行 CPluginWindow

CPluginWindow 類別會提供使用者介面給外掛程式。 在搜尋 UI 外掛程式的案例中，這個類別包含 [ **搜尋** ] 按鈕的程式碼，以及按一下按鈕時啟動搜尋頁面的程式碼。

Wizard 在 CPluginWindow .h 標頭檔中提供 CPluginWindow 的基本執行。 為了簡單起見，搜尋 UI 外掛程式會直接修改這個檔案，雖然通常會在個別的 CPluginWindow .cpp 檔案中放置廣泛的新增專案。

下列各節說明執行 CPluginWindow 所需執行的動作：

-   [訊息對應](the-message-map.md)
-   [函數](the-constructor.md)
-   [OnPaint 方法](the-onpaint-method.md)
-   [>oncreate 方法](the-oncreate-method.md)
-   [OnSearch 方法](the-onsearch-method.md)
-   [LaunchPage 方法](the-launchpage-method.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**消費者介面外掛程式程式設計指南**](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




