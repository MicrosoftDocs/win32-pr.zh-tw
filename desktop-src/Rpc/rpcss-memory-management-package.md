---
title: RpcSs 記憶體管理套件
description: 在代表應用程式佈建記憶體時，存根和執行時間所使用的預設配置器/釋放器組是 midl \_ 使用者 \_ 配置/midl \_ 使用者 \_ 免費。
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463536"
---
# <a name="rpcss-memory-management-package"></a>RpcSs 記憶體管理套件

在代表應用程式佈建記憶體時，存根和執行時間所使用的預設配置器/釋放器組是 **midl \_ 使用者 \_** / **\_ \_ 免費配置 midl 使用者**。 不過，您可以使用 ACF 屬性 **\[ 啟用 \_ 配置 \]** 來選擇 RpcSs 封裝，而不是預設值。 此 RpcSs 封裝包含以首碼 **RpcSs** 或 **RPCSM** 開頭的 RPC 函數。 Windows 應用程式不建議使用此 RpcSs 套件。

> [!Note]  
> Rpcss 記憶體管理套件已過時。 建議您在其位置使用 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Midl/midl-user-allocate-1) 和 [**midl \_ 使用者 \_ 免費**](/windows/desktop/Midl/midl-user-free-1) 。

 

在 **/osf** 模式中，使用完整的指標時，會自動啟用 MIDL 產生的存根、引數需要記憶體配置，或做為使用 [ **\[ 啟用 \_ 配置 \]** ] 屬性的結果。 在預設 (Microsoft 擴充) 模式下，只有在使用 [ **\[ 啟用 \_ 配置 \]** ] 屬性時，才會啟用 RpcSs 套件。 [ **\[ 啟用 \_ 配置 \]** ] 屬性會依伺服器端的存根啟用 RpcSs 環境。 用戶端會收到可能啟用 RpcSs 封裝的警示。 在 **/osf** 模式中，用戶端不會受到影響。

啟用 RpcSs 封裝之後，就會使用私用的 RpcSs 記憶體管理配置器和釋放器配對來完成伺服器端的記憶體配置。 您可以使用相同的機制來配置記憶體，方法是呼叫 [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (或 [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)) 。 從伺服器 stub 傳回時，會自動釋放由 RpcSs 封裝配置的所有記憶體。 下列範例顯示如何啟用 RpcSs 套件：

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

您的應用程式可以藉由叫用 [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) 或 [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) 函式來明確釋放記憶體。 請注意，這些函數實際上並不會釋出記憶體。 他們將其標示為刪除。 當您的程式呼叫 [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) 或 [**RPCSSDISABLEALLOCATE**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate)時，RPC 程式庫會釋放記憶體。

您也可以藉由呼叫 [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) 常式 (為您的應用程式啟用記憶體管理環境，也可以藉由呼叫 [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) 常式) 來停用它。 啟用之後，應用程式程式碼就可以從 RpcSs 封裝呼叫函式，以配置和解除配置記憶體。

 

 