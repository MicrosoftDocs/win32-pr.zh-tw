---
title: " (MIDL) 的帶正負號和不帶正負號類型"
description: 瞭解 MIDL 中的正負號和不帶正負號的類型。 使用不同預設類型的編譯器可能會在您的分散式應用程式中造成軟體錯誤。
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- 資料類型 MIDL、帶正負號和不帶正負號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407381"
---
# <a name="signed-and-unsigned-types-midl"></a> (MIDL) 的帶正負號和不帶正負號類型

針對帶正負號和不帶正負號的類型使用不同預設值的編譯器可能會在分散式應用程式中造成軟體錯誤。 您可以明確地將您的字元類型宣告為帶正負號或不帶正負號，以避免這些問題。 請注意，DCE IDL 編譯器無法辨識關鍵字 [**簽署**](signed.md)。 因此，當您使用 MIDL 編譯器/**憑證** 參數時，就無法使用這項功能。

MIDL 會定義要在目標 C 編譯器中採用與 [**char**](char-idl.md)類型相同之預設正負號的 [**小型**](small.md)型別。 如果編譯器假設 **char** 未簽署，則 **小小** 部分也會定義為未簽署。 許多 C 編譯器可讓您將預設值變更為命令列選項。 例如，在 Microsoft Visual C++ 開發環境中， **/j** 命令列選項會將預設的 **char** 符號從 [已簽署] 變更為 [未簽署]。

您也可以使用 MIDL 編譯器命令列參數 [**/char**](-char.md)來控制 [**char**](char-idl.md)和 [**small**](small.md)類型變數的正負號。 此參數可讓您指定編譯器所使用的預設符號。 MIDL 編譯器會在產生的標頭檔中明確宣告不符合 C 編譯器預設類型的所有 **char** 類型的正負號。

 

 




