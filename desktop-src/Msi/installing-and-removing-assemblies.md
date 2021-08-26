---
description: 將元件安裝到特定應用程式的隔離位置時，必須在 MsiAssembly 資料表的 [檔案應用程式] 資料行中指定應用程式 \_ 。
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: 安裝和移除元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0117c29a9bcc49a549529a6e05f1124236cb845d9b7792d7bcbda143fd6d08e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043428"
---
# <a name="installing-and-removing-assemblies"></a>安裝和移除元件

將元件安裝到特定應用程式的隔離位置時，必須在 MsiAssembly 資料表的 [檔案應用程式] 資料行中指定應用程式 \_ 。 [](msiassembly-table.md) 此欄位是檔案 [資料表](file-table.md)中的索引鍵。 安裝程式會使用 [目錄資料表](directory-table.md) 中指定的目錄結構，將元件安裝到與包含這個檔案的元件相同的目錄中。

將元件安裝到全域組件快取時， \_ [MsiAssembly 資料表](msiassembly-table.md) 的 File Application 資料行中的值必須是 Null。

下列各節說明 Win32 和 common language runtime 元件的安裝：

-   [Win32 元件的安裝](installation-of-win32-assemblies.md)
-   [Common Language Runtime 元件的安裝](installation-of-common-language-runtime-assemblies.md)

 

 



