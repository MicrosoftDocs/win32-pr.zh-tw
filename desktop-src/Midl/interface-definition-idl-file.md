---
title: " (IDL) 檔案的介面定義"
description: 依照慣例，包含介面和型別程式庫定義的檔案稱為 IDL 檔案，且副檔名為 .idl。
ms.assetid: 4df87df8-3206-4845-b5ab-d77ea443b9e3
keywords:
- 介面 MIDL、IDL 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2666e02fc7812d9ecdc9a00e77400d5016ac627c9fcbd42d81be77bc41d487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383692"
---
# <a name="interface-definition-idl-file"></a> (IDL) 檔案的介面定義

依照慣例，包含介面和型別程式庫定義的檔案稱為 IDL 檔案，且副檔名為 .idl。 實際上，MIDL 編譯器會剖析介面定義檔，而不論它的副檔名為何。 介面是由關鍵字 [**介面**](interface.md)所識別。

每個介面都是由標頭和主體組成。 介面標頭包含適用于整個介面的屬性。 介面的主體包含其餘的介面定義。 如需介面和 IDL 檔案的總覽，請參閱 [介面定義語言 (IDL) ](/windows/desktop/Rpc/the-interface-definition-language-idl-file)檔。 如需可在介面標頭中使用之屬性的摘要，請參閱 [IDL 屬性](idl-attributes.md)。

 

 