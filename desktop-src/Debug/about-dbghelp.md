---
description: 下列主題描述項號檔和 DbgHelp 函數所提供的功能。
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: 關於 DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 958a139a7dcbffb8ee1b3b3d030d170fc821e6022038cab6a704b3b04f820f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162696"
---
# <a name="about-dbghelp"></a>關於 DbgHelp

下列主題描述項號檔和 [DbgHelp 函數](dbghelp-functions.md)所提供的功能。

-   [DbgHelp 版本](dbghelp-versions.md)
-   [符號檔](symbol-files.md)
-   [符號處理](symbol-handling.md)
-   [符號伺服器和符號存放區](symbol-servers-and-symbol-stores.md)
-   [小型傾印檔案](minidump-files.md)
-   [來源伺服器](source-server-and-source-indexing.md)
-   [更新的平臺支援](updated-platform-support.md)

請注意，所有 [DbgHelp 函數](dbghelp-functions.md) 都是單一執行緒。 因此，從多個執行緒到此函式的呼叫可能會導致非預期的行為或記憶體損毀。 若要避免這種情況，您必須將多個執行緒的所有並行呼叫，同步處理至此函式。

 

 



