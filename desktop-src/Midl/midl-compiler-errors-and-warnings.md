---
title: MIDL 編譯器錯誤和警告
description: 使用 MIDL 編譯器時，錯誤和警告可能是因為命令列參數不當使用或 IDL 和 ACF 檔的內容所造成。
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft 介面定義語言 MIDL，參考
- MIDL 編譯器 MIDL，錯誤
- 編譯器 MIDL，錯誤
- 錯誤 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f6c2dfd830a1240e2af107eb4a3f1799eafcd0de35ccec7f3756b3e9de5bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146401"
---
# <a name="midl-compiler-errors-and-warnings"></a>MIDL 編譯器錯誤和警告

使用 MIDL 編譯器時，錯誤和警告可能是因為命令列參數不當使用或 IDL 和 ACF 檔的內容所造成。 如果錯誤是因為不正確地輸入命令列參數，則錯誤或警告訊息可能會指定一或多個 MIDL 編譯器模式參數的名稱。 例如，當您使用/應用程式設定參數時，您可以在 IDL 檔案中包含某些 ACF 屬性，但如果您在不使用/**應用程式 \_** 設定參數的情況下編譯，則該 idl 檔案將會產生錯誤。**\_**

IDL 和 ACF 檔案中的錯誤可以分為兩類：預處理器所攔截到的錯誤，以及編譯器所辨識出的錯誤。 本節列出 MIDL 預處理器和編譯器錯誤訊息。 它也會描述其格式和原因。

-   [錯誤和警告訊息格式](error-and-warning-message-formats.md)
-   [預處理器錯誤](preprocessor-errors.md)
-   [編譯器錯誤](compiler-errors.md)

 

 




