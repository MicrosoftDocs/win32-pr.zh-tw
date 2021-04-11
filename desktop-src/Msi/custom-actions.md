---
description: Windows Installer 提供許多內建動作來執行安裝程式。 如需這些動作的清單，請參閱標準動作參考。
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: 自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026884"
---
# <a name="custom-actions"></a>自訂動作

Windows Installer 提供許多內建動作來執行安裝程式。 如需這些動作的清單，請參閱 [標準動作參考](standard-actions-reference.md)。

標準動作足以在大部分情況下執行安裝。 不過，在某些情況下，安裝套件的開發人員會發現需要撰寫自訂動作。 例如：

-   您想要在安裝期間啟動可執行檔（安裝在使用者電腦上，或與應用程式一起安裝時）。
-   您想要在安裝期間于動態連結程式庫 (DLL) 中定義的特殊函式進行呼叫。
-   在安裝期間，您想要使用 Microsoft Visual Basic Scripting Edition 或 Microsoft JScript 常值腳本文字所撰寫的函式。
-   您想要順延強制某些動作，直到執行安裝腳本的時間為止。
-   您想要將時間和進度資訊加入至 ProgressBar 控制項和 TimeRemaining 文字控制項。

下列各節說明自訂動作，以及如何將它們併入安裝套件：

-   [關於自訂動作](about-custom-actions.md)
-   [使用自訂動作](using-custom-actions.md)
-   [自訂動作參考](custom-action-reference.md)
-   [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md)

 

 



