---
description: 本節將討論如何建立快捷方式 (內容) 功能表，以及如何 (動詞) 處理常式來執行快捷方式功能表。
title: 快捷方式 (內容) 功能表和快捷方式功能表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191181"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a>快捷方式 (內容) 功能表和快捷方式功能表處理常式

本節將討論如何建立快捷方式 (內容) 功能表，以及如何 (動詞) 處理常式來執行快捷方式功能表。

這一節的檔案類型和檔案關聯的組織方式如下：

-   [動詞和檔案關聯](fa-verbs.md)
-   [選擇靜態或動態快捷方式功能表方法](shortcut-choose-method.md)
-   [快速鍵功能表處理常式和多個動詞的最佳作法](verbs-best-practices.md)
-   [建立快捷方式功能表處理常式](context-menu-handlers.md)
-   [建立靜態串聯功能表](creating-static-cascading-menus.md)
-   [如何隱藏和控制動詞可見度](how-to-suppress-and-control-visibility.md)
-   [如何使用動詞選取模型](how-to-employ-the-verb-selection-model.md)
-   [如何使用專案屬性](how-to-use-item-attributes.md)
-   [如何透過 Desktop.ini為資料夾執行自訂動詞 ](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)
-   [如何執行 ICoNtextMenu 介面](how-to-implement-the-icontextmenu-interface.md)
-   [快速鍵功能表參考](context-menu-reference.md)

## <a name="additional-resources"></a>其他資源

如需相關的概念背景，請參閱下列主題：

-   檔案[關聯簡介](fa-intro.md)。
-   若要使用檔案類型處理常式來擴充 Shell，請參閱 [建立 Shell 擴充處理常式](handlers.md)。
-   若要建立 Shell 資料存放區，請參閱 [執行基本資料夾物件介面](nse-implement.md)。

如需相關的參考檔，請參閱下列主題：

-   若要在 Shell 專案上執行動詞命令，請參閱 [**InvokeVerb**](folderitem-invokeverb.md) 方法。
-   若要取得可在 Shell 專案上執行的動詞集合，請參閱 [**動詞**](folderitem-verbs.md) 方法。
-   若要在指定的檔案上執行作業，請參閱 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 函數。

 

 



