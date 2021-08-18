---
title: 標頭檔
description: 介面標頭檔 (名稱 .h) 包含以目前 IDL 檔案中的介面定義為基礎的型別定義和函式宣告，以及包含在 \ include 指示詞中的檔案中宣告的所有資料類型和作業。
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- 標頭檔 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac9bc5e8b5edd091450af670fd51d251326029f13e1f88a6d5a9116faa5b4447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013516"
---
# <a name="the-header-files"></a>標頭檔

介面標頭檔 (名稱 .h) 包含以目前 IDL 檔案中的介面定義為基礎的類型定義和函式宣告，以及包含在 include 指示詞內含之檔案中宣告的所有資料類型和作業 \# 。 使用匯入指示詞彙入之檔案中的資料類型不會複寫至標頭檔;相反地，所產生的標頭檔會包含自匯入檔案所產生之 H 檔案的包含行。

將這個檔案包含在 proxy DLL 的來源檔案中，以及使用該介面的用戶端應用程式。

從檔案產生的標頭檔的預設名稱。 .idl 是 File .h。 [**/Header**](-header.md) MIDL 編譯器參數會覆寫介面標頭檔案的預設名稱。

 

 




