---
title: 使用 C/c + +-預處理器與 MIDL
description: MIDL 編譯器不會將來源檔案前置處理。
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL 編譯器 MIDL，C-預處理器
- C-預處理器 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300660"
---
# <a name="using-cc-preprocessor-with-midl"></a>使用 C/c + +-預處理器與 MIDL

MIDL 編譯器不會將來源檔案前置處理。 相反地，MIDL 編譯器會使用可用的預處理器來準備要剖析的輸入資料流程。 根據預設，MIDL 會使用 Microsoft C/c + + 編譯器的預處理器，從與 MIDL 相同的建立環境。 如果有需要，使用者可以指定 MIDL 要使用的不同預處理器。

MIDL 會為最上層 IDL 和 ACF 檔案，以及每個以 MIDL import 指示詞彙入的檔案，產生個別的預處理器回合。 **\# Include** 指示詞隨附的檔案是由預處理器直接處理。

下列主題描述 MIDL-預處理器互動的各個層面：

-   [C-MIDL 的預處理器需求](c-preprocessor-requirements-for-midl.md)
-   [驗證預處理器選項](verifying-preprocessor-options.md)
-   [正在儲存預處理器輸出](saving-preprocessor-output.md)
-   [處理 \# IDL 檔案中的定義](dealing-with-defines-in-idl-files-2.md)

 

 




