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
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672248"
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

 

 




