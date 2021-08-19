---
title: 函數傳回值
description: 函數傳回值類似于僅限 \t 參數，因為它們的資料不是由用戶端應用程式所提供。
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525c63422b058da5267003711efa612814907eb91ced353bd78ee78a820a7377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020998"
---
# <a name="function-return-values"></a>函數傳回值

函式傳回值類似于 **\[ out \]** 參數，因為它們的資料不是由用戶端應用程式所提供。 不過，它們的管理方式不同。 不同于僅限 **\[ out \]** 參數，它們不需要是指標。 除了參考指標和 nonencapsulated 等位之外，遠端程式可以傳回任何有效的資料類型。

不過，建議使用 **\[ out \]** 參數，而不是複雜資料類型的傳回值。 當傳回復雜的資料類型時，MIDL 編譯器將會產生/Os 模式存根。 因此，/robust 所提供的所有最近的錯誤檢查資訊都會遺失。

指標類型的函式傳回值是由用戶端存根配置，並且會呼叫 [midl \_ 使用者 \_ 配置](/windows/desktop/Midl/midl-user-allocate-1)。 因此，只有 unique 或 full 指標屬性可以套用至指標函式的傳回型別。

 

 