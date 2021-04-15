---
title: Application-Allocated 緩衝區
description: ACF 屬性 \ 位元組 \_ 計數 \ 會將存根導向至用戶端支援常式未配置或釋放的預先配置緩衝區。
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463544"
---
# <a name="application-allocated-buffer"></a>Application-Allocated 緩衝區

ACF 屬性 \[ [**位元組 \_ 計數**](/windows/desktop/Midl/byte-count) \] 會將存根導向至用戶端支援常式未配置或釋放的預先配置緩衝區。 \[ **Byte \_ count** \] 屬性會套用至指向緩衝區的指標或陣列參數。 它需要指定緩衝區大小的參數（以位元組為單位）。

用戶端配置的記憶體區域可以包含具有多個指標的複雜資料結構。 因為記憶體區域是連續的，所以應用程式不需要進行數個呼叫來個別釋放每個指標和結構。 當使用 [ \[ [**配置 (所有 \_ 節點)**](/windows/desktop/Midl/allocate) ] \] 屬性時，只要呼叫記憶體配置常式或免費的常式，就可以配置或釋放記憶體區域。 不過，與使用 [ \[ **配置 (所有 \_ 節點)** \] 屬性不同的是，緩衝區參數不是由用戶端 stub 所管理，而是由用戶端應用程式所管理。

緩衝區必須是 \[ [**out**](/windows/desktop/Midl/out-idl) \] 參數，而緩衝區長度（以位元組為單位）必須是僅供使用的 \[ [](/windows/desktop/Midl/in) \] 參數。 \[ [**Byte \_ count**](/windows/desktop/Midl/byte-count) \] 屬性只能套用至指標類型。 \[ **Byte \_ count** \] ACF 屬性是適用于 DCE IDL 的 Microsoft 擴充功能，因此，如果您使用 MIDL [**/osf**](/windows/desktop/Midl/-osf)參數進行編譯，就無法使用此屬性。

在下列範例中，參數 *pRoot* 使用 byte count：

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

[ \[ [**位元組 \_ 計數**](/windows/desktop/Midl/byte-count)] \] 屬性會顯示在 ACF 中，如下所示：

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

從這些 IDL 和 ACF 檔產生的用戶端 stub 不會配置或釋放此緩衝區的記憶體。 伺服器 stub 會使用提供的大小參數，在單一呼叫中配置和釋出緩衝區。 如果資料太大而無法使用指定的緩衝區大小，則會引發例外狀況。

 

 