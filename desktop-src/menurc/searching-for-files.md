---
title: 搜尋檔案
description: 根據預設，RC 會搜尋標頭檔和資源檔 (例如，圖示和游標檔案) 先在目前的目錄中，然後在 INCLUDE 環境變數所指定的目錄中。
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106995555"
---
# <a name="searching-for-files"></a>搜尋檔案

根據預設，RC 會搜尋標頭檔和資源檔 (例如，圖示和游標檔案) 先在目前的目錄中，然後在 INCLUDE 環境變數所指定的目錄中。  (PATH 環境變數不會影響哪些目錄 RC 搜尋。 ) 

## <a name="adding-a-directory-to-search"></a>新增要搜尋的目錄

您可以使用 **/i** 選項，將目錄新增至目錄 RC 搜尋清單。 然後編譯器會依下列順序搜尋目錄：

1.  目前的目錄
2.  使用 **/i** 選項指定的目錄或目錄（依它們出現在 RC 命令列上的順序）
3.  包含環境變數所指定的目錄清單（依變數列出的順序），除非您指定 **/x** 選項

下列範例會編譯資源定義檔案 MyApp .rc：

**rc/i c： \\ 來源 \\ 內容/i d： \\ 資源 myapp. rc**

在編譯 MyApp 的腳本時，RC 會先在目前的目錄中搜尋標頭檔和資源檔，然後在 C： \\ 來源 \\ 內容和 D： \\ 資源，然後在 INCLUDE 環境變數所指定的目錄中搜尋標頭檔和資源檔。

## <a name="ignoring-the-include-environment-variable"></a>忽略 INCLUDE 環境變數

您可以在決定要搜尋的目錄時，防止 RC 使用 INCLUDE 環境變數。 若要這樣做，請使用 **/x** 選項。 然後編譯器只會搜尋目前目錄中的檔案，以及使用 **/i** 選項指定的任何目錄中的檔案。

下列命令會編譯腳本檔案 MyApp .rc：

**rc/x/i c： \\ 來源專案 \\ myapp. rc**

在編譯 MyApp 的腳本時，RC 會先搜尋目前目錄中的標頭檔和資源檔，然後再搜尋 C： \\ 來源 \\ 內容。 它不會搜尋 INCLUDE 環境變數所指定的目錄。

 

 




