---
title: 'E (RPC) '
description: 從遠端程序呼叫中的 E 開始的單字 (RPC) 詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 76e35c3c-91dd-42e3-9699-6767e37b2699
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab198e0908ce27a1776b7f2655527140dea7af2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464017"
---
# <a name="e-rpc"></a>E (RPC) 

[](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) E [F](f-glos.md) G [](v-glos.md) H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) [N](n-glos.md) [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [](u-glos.md) [W](w-glos.md) X Y Z

<dl> <dt>

<span id="_rpc_embedded_pointer_glos"></span><span id="_RPC_EMBEDDED_POINTER_GLOS"></span>**內嵌指標**
</dt> <dd>

內嵌于參數中的指標，此參數是資料結構，例如陣列、結構或等位。 另請參閱 [*最上層指標*](t-glos.md)。

</dd> <dt>

<span id="_rpc_encoding_services_glos"></span><span id="_RPC_ENCODING_SERVICES_GLOS"></span>**編碼服務**
</dt> <dd>

MIDL 產生的存根常式，可支援資料編碼和解碼 (也稱為 *pickling* 或 *序列化*) 。 允許程式設計人員控制包含要封送處理和取消封送處理之資料的緩衝區。 另請參閱 [*類型序列化*](t-glos.md)和程式 [*序列化*](p-glos.md)。

</dd> <dt>

<span id="_rpc_endpoint_glos"></span><span id="_RPC_ENDPOINT_GLOS"></span>**端點**
</dt> <dd>

遠端程序呼叫之伺服器進程的網路特定位址。 端點的實際名稱取決於所使用的通訊協定順序。 另請參閱 [*動態端點*](d-glos.md) 和 [*已知端點*](w-glos.md)。

</dd> <dt>

<span id="_rpc_endpoint_mapper_glos"></span><span id="_RPC_ENDPOINT_MAPPER_GLOS"></span>**端點對應程式**
</dt> <dd>

RPC 子系統的一部分 (RPCSS) ，可讓執行時間程式庫以動態方式指派及解析端點。 另請參閱 [端點](/windows)。

</dd> <dt>

<span id="_rpc_encapsulated_union_glos"></span><span id="_RPC_ENCAPSULATED_UNION_GLOS"></span>**封裝聯集**
</dt> <dd>

MIDL 結構，可在判別為結構第一個欄位的結構中內嵌聯集，以便在遠端程序呼叫中傳遞等位，而且 union 是結構的第二個 (和最後一個) 欄位。 [*IDL*](i-glos.md)關鍵字 **參數** 指定封裝聯集。 另請參閱 [*nonencapsulated 聯集*](n-glos.md)。

</dd> <dt>

<span id="_rpc_epv_glos"></span><span id="_RPC_EPV_GLOS"></span>**進入點向量 (EPV)**
</dt> <dd>

函式的指標陣列，這些函式會執行介面中指定的作業。 陣列中的每個元素會對應至 IDL 檔案中定義的函式。 進入點向量可讓分散式應用程式支援 IDL 檔案中定義之函式的多個實作為。

</dd> </dl>

 

 
