---
title: " (RPC) 的帶正負號和不帶正負號的類型"
description: 瞭解 RPC 中的已簽署和不帶正負號的類型。 使用不同預設類型的編譯器可能會在您的分散式應用程式中造成軟體錯誤。
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17a2ccf28233bb14e0811e8015c83aede37d60c58fe9411f13806355fdb7f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017694"
---
# <a name="signed-and-unsigned-types-rpc"></a> (RPC) 的帶正負號和不帶正負號的類型

針對帶正負號和不帶正負號的類型使用不同預設值的編譯器可能會在分散式應用程式中造成軟體錯誤。 您可以明確地將您的字元類型宣告為 **帶正負** 號或不 **帶正負** 號，以避免這些問題。

MIDL 會定義要在目標 C 編譯器中採用與 **char** 類型相同之預設正負號的 [**小型**](/windows/desktop/Midl/small)型別。 如果編譯器假設 **char** 未簽署，則 **小小** 部分也會定義為未簽署。 許多 C 編譯器可讓您將預設值變更為命令列選項。 例如，Microsoft C 編譯器 **/j** 命令列選項會將預設的 **char** 符號從 sign 變更為未簽署。

您也可以使用 MIDL 編譯器命令列參數 [**/char**](/windows/desktop/Midl/-char)來控制 **char** 和 **small** 類型變數的正負號。 此參數可讓您指定編譯器所使用的預設符號。 MIDL 編譯器會在產生的標頭檔中明確宣告不符合 C 編譯器預設類型的所有 **char** 類型的正負號。

 

 
