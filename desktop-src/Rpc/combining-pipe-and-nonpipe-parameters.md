---
title: 結合管道和 Nonpipe 參數
description: 將遠端程序呼叫中的管道和 nonpipe 參數結合 (RPC) 。
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76bc2f334325c87cbf8c4a09898cf0fe54153cd84f6f2809995e66cc08e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022668"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>結合管道和 Nonpipe 參數

當您在遠端程序呼叫中結合管道類型和其他類型時，會根據參數的方向來傳輸資料：

-   在 [ **\[ \] 方向]** 中，會先傳送所有 nonpipe 引數的資料，然後再傳送管線資料。
-   在 **\[ 輸出 \]** 方向中，伺服器會先傳送管線資料。 在管理員常式傳回之後，伺服器會傳送 nonpipe 的資料。
-   當 **\[ in、out \]** 管道引數與 **\[ in、out \]** 非管道引數合併時，會先將輸入資料完整傳輸（如先前所述）。 然後，輸出資料會如先前所述傳輸。

下列限制適用于此 (MIDL 3.0) 實作為管道：當您在單一遠端程序呼叫中結合管道類型和其他類型時，nonpipe 參數必須有妥善定義的大小，才能讓 MIDL 編譯器計算所需的緩衝區大小。 例如，您無法將管道參數與 \[ [唯一](/windows/desktop/Midl/unique) \] 指標或符合標準的結構結合，因為它們的大小無法在編譯時期決定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管道](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 