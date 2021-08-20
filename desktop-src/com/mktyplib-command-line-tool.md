---
title: Mktyplib.exe Command-Line 工具
description: Mktyplib.exe 是一種命令列應用程式，可處理 IDL 檔案以產生類型程式庫。 它也可以用來產生 C 或 c + + 標頭檔。
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b712ed8220dd609dd3ba189bdac6b5ee11d2805f26ff5a1f146c20f17c1f8ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047936"
---
# <a name="mktyplib-command-line-tool"></a>Mktyplib.exe Command-Line 工具

\[Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。 如果您需要與舊有 Automation 程式的回溯相容性，請使用 MIDL 編譯器搭配 **/mktyplib203** 選項。\]

Mktyplib.exe 是一種命令列應用程式，可處理 IDL 檔案以產生類型程式庫。 它也可以用來產生 C 或 c + + 標頭檔。

若要從 ODL 檔產生類型程式庫：

-   從命令提示字元中，執行下列命令：

    * * mktyplibÂ * *_檔案名_

    其中 *filename* 是 ODL 檔案的名稱。

Mktyplib.exe 也支援數個選擇性參數。 如需完整清單，請執行下列命令列：

**mktyplib.exe/？**

由於 Mktyplib.exe 是過時的應用程式，因此無法剖析 IDL 檔案或具有在連結 [**庫**](/windows/desktop/Midl/library) 語句之外定義之介面的檔案。 如需詳細資訊，請參閱 [MIDL 與 Mktyplib.exe 之間的差異](/windows/desktop/Midl/differences-between-midl-and-mktyplib)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換成 c + +](translating-to-c--.md)
</dt> </dl>

 

 