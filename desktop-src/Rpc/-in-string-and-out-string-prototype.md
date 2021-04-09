---
title: " 在、字串和輸出中，字串原型"
description: 下列函式原型使用 \ in、string \ 參數和 out、string \ 參數的兩個參數。
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933554"
---
# <a name="in-string-and-out-string-prototype"></a>\[在、字串 \] 和 \[ 輸出中，字串 \] 原型

下列函數原型會使用兩個參數： \[ [**in**](/windows/desktop/Midl/in)、 [**string**](/windows/desktop/Midl/string) \] 參數和 \[ [**out**](/windows/desktop/Midl/out-idl)、 **string** \] 參數。

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

第一個參數只能 \[ [**是**](/windows/desktop/Midl/in) \] 。 此輸入字串只會從用戶端傳送到伺服器。 伺服器會使用它做為進一步處理的基礎。 字串不會經過修改，而且用戶端不需要再次使用，因此不需要將它傳回至用戶端。

第二個參數（代表醫生的回應）只是 \[ [**輸出**](/windows/desktop/Midl/out-idl) \] 。 這個回應字串只會從伺服器傳送到用戶端。 提供配置大小，讓伺服器存根可以為它配置記憶體。 因為 *pszOutput* 是 \[ [**ref**](/windows/desktop/Midl/ref) \] 指標，所以用戶端必須在呼叫之前配置足夠的記憶體給字串。 當遠端程式傳回時，回應字串會寫入此記憶體區域中。

 

 