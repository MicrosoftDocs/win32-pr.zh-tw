---
title: 解析。CPP
description: 在範例提供者元件中，目錄服務路徑剖析器的程式碼範例位於 Parse. .cpp 中。
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- 剖析 .cpp ADSI
- 路徑剖析器 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518db6857f9b7018a0dbf3e1e97ac60ed654447d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880285"
---
# <a name="parsecpp"></a>解析。CPP

在範例提供者元件中，目錄服務路徑剖析器的程式碼範例位於 Parse. .cpp 中。 路徑剖析器是 ADs 提供者元件中的重要元件。 它會驗證傳遞給此提供者的 ADs 路徑語法是否有效。 如果語法有效，則會建立 **OBJECTINFO** 結構，其中包含這個物件之 ADspath 的元件化版本。

請注意，這只是語法驗證。 所有路徑驗證都必須符合剖析器所建立的文法規則，而不是特殊案例的每個新反復專案。

下表列出在 Parse 中實作為函式和方法。



| 項目                      | 說明                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | 剖析傳遞給它的 ADspath。 此函數會遵循下列文法規則： &lt; ADsObject &gt;  ->  &lt; ProviderName &gt; &lt; SampleDSObject&gt;<br/>     |
| **SampleDSObject**        | 剖析下列文法規則： &lt; SampleDSObject &gt; -> " \\ \\ " &lt; identifier &gt; " \\ " &lt; 路徑名稱&gt;<br/>                                            |
| **ProviderName**          | 在語法正確的提供者名稱中加入（如果沒有的話）。                                                                                                          |
| **PathName**              | 剖析下列文法規則： &lt; pathname &gt;  ->  &lt; 元件 &gt; " \\ \\ " &lt; 路徑名稱 &gt; 或<br/> &lt;Pathname &gt;  ->  &lt; 元件&gt;<br/> |
| **元件**             | 剖析下列文法規則： &lt; 識別碼 &gt; 或<br/> &lt;識別碼 &gt; "=" &lt; 識別碼&gt;<br/>                                              |
| **CLexer::CLexer**        | 標準的函式。                                                                                                                                                  |
| **CLexer：： ~ CLexer**       | 標準的函式。                                                                                                                                                   |
| **CLexer::GetNextToken**  | 權杖化工具。                                                                                                                                                             |
| **CLexer::NextChar**      | 抓取下一個單一字元。                                                                                                                                       |
| **CLexer：:P ushBackToken** | 備份到最後一個 token 的開頭。                                                                                                                               |
| **CLexer：:P ushbackChar**  | 備份一個字元。                                                                                                                                                |
| **CLexer::IsKeyword**     | 驗證關鍵字清單。 在 Globals) 中定義。                                                                                                                          |
| **AddComponent**          | 將這個元件加入元件陣列中。                                                                                                                            |
| **AddProviderName**       | 將語法正確的提供者名稱加入至 **OBJECTINFO** 結構。                                                                                            |
| **AddRootRDN**            | 將語法正確的根相對辨別名稱 (RDN) 名稱加入至 **OBJECTINFO** 結構。                                                            |
| **>advanced.field.settype**               | 設定物件的類型。                                                                                                                                           |
| **類型**                  | 剖析類型-> "user" \| "group" 等等。                                                                                                                          |



 

 

 





