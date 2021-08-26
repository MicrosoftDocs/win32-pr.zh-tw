---
title: IDL 和 ACF 檔案
description: Microsoft 介面定義語言 (MIDL) 的語法是以 C 程式設計語言的語法為基礎。 當這項 MIDL 描述中的語言概念未完整定義時，就會隱含該詞彙的 C 語言定義。
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- 遠端程序呼叫 RPC、描述、IDL 和 ACF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788756c6762575d2366950f1b6412a76c03d14518acb1707dfdaf109ba2b5fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017098"
---
# <a name="the-idl-and-acf-files"></a>IDL 和 ACF 檔案

Microsoft 介面定義語言 (MIDL) 的語法是以 C 程式設計語言的語法為基礎。 當這項 MIDL 描述中的語言概念未完整定義時，就會隱含該詞彙的 C 語言定義。

MIDL 設計會指定兩個不同的檔案：介面定義語言 (IDL) 檔和應用程式佈建檔 (ACF) 。 這些檔案包含的屬性，會將管理遠端程序呼叫的 C 語言存根檔案的產生導向 (RPC) 。 IDL 檔案包含用戶端與伺服器程式之間的介面描述。 RPC 應用程式會使用 ACF 檔來描述組成特定作業環境之硬體和作業系統的特定介面特性。 將此資訊分割成兩個檔案的目的，是要讓軟體介面與只影響操作環境的特性分開。

IDL 檔案會指定用戶端與伺服器之間的網路合約，也就是 IDL 檔案會指定在用戶端與伺服器之間傳輸的內容。 將此資訊與作業環境相關的資訊保持不變，可將 IDL 檔案移植到其他環境。 IDL 檔案是由兩個部分所組成： [介面標頭](the-idl-interface-header.md) 和 [介面主體](the-idl-interface-body.md)。

ACF 所指定的屬性只會影響本機效能，而不會影響網路合約。 Microsoft RPC 允許您合併單一 IDL 檔案中的 ACF 和 IDL 屬性。 您也可以在單一 IDL 檔案中結合多個介面 (及其 ACF) 。

本節摘要說明 IDL 和 ACF 檔案中所指定的屬性。 它的目的只是要提供總覽。 如需詳細資訊，請參閱 [Midl 語言參考](/windows/desktop/Midl/midl-language-reference)，以及 [midl Command-Line 參考](/windows/desktop/Midl/midl-command-line-reference)。 本章節中的討論內容將在下列主題中顯示：

-   [介面定義語言 (IDL) 檔](the-interface-definition-language-idl-file.md)
-   [應用程式佈建檔 (ACF) ](the-application-configuration-file-acf-.md)
-   [MIDL 編譯器輸出](midl-compiler-output.md)

 

 