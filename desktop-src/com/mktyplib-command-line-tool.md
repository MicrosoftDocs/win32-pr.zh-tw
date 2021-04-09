---
title: Mktyplib.exe Command-Line 工具
description: Mktyplib.exe 是一種命令列應用程式，可處理 IDL 檔案以產生類型程式庫。 它也可以用來產生 C 或 c + + 標頭檔。
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683192"
---
# <a name="mktyplib-command-line-tool"></a>Mktyplib.exe Command-Line 工具

\[Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。 如果您需要與舊有 Automation 程式的回溯相容性，請使用 MIDL 編譯器搭配 **/mktyplib203** 選項。\]

Mktyplib.exe 是一種命令列應用程式，可處理 IDL 檔案以產生類型程式庫。 它也可以用來產生 C 或 c + + 標頭檔。

若要從 ODL 檔產生類型程式庫：

-   從命令提示字元中，執行下列命令：

    **mktyplibÂ * * * 檔案名*

    其中 *filename* 是 ODL 檔案的名稱。

Mktyplib.exe 也支援數個選擇性參數。 如需完整清單，請執行下列命令列：

**mktyplib.exe/？**

由於 Mktyplib.exe 是過時的應用程式，因此無法剖析 IDL 檔案或具有在連結 [**庫**](/windows/desktop/Midl/library) 語句之外定義之介面的檔案。 如需詳細資訊，請參閱 [MIDL 與 Mktyplib.exe 之間的差異](/windows/desktop/Midl/differences-between-midl-and-mktyplib)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換成 c + +](translating-to-c--.md)
</dt> </dl>

 

 