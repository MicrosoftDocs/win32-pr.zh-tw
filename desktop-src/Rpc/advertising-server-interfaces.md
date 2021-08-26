---
title: 廣告伺服器介面
description: 使用自動控制碼的應用程式的伺服器端必須呼叫函式 RpcNsBindingExport，以將伺服器的相關系結資訊提供給用戶端使用。
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f81ec4b494c9ce2abd18031e3bf0ed3dd25d55908238ebc7bba96bce57e88f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073598"
---
# <a name="advertising-server-interfaces"></a>廣告伺服器介面

使用自動控制碼的應用程式的伺服器端必須呼叫函式 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) ，以將伺服器的相關系結資訊提供給用戶端使用。 自動系結控制碼需要在可供用戶端存取的伺服器上執行名稱服務。 Microsoft 的名稱服務（Microsoft 定位器）的實作為管理自動控點。 使用隱含和明確系結控制碼的伺服器應用程式，也可以在名稱服務資料庫中通告其存在。

一般來說，伺服器會呼叫下列執行時間函數：

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

呼叫此程式碼片段中的前兩個函式，類似于 [Hello，World 範例](tutorial.md)。 這些函式會將可用系結的相關資訊提供給用戶端。 [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)和 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)的呼叫會將資訊放入名稱服務資料庫中。 在將控制碼匯出至名稱服務之前，對 [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 的呼叫會以有效的系結控制碼填滿系結向量。 在伺服器程式將控制碼匯出至資料庫之後，用戶端 (或用戶端存根) 可以呼叫 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) 和 [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) 來取得此資訊。 如需詳細資訊，請參閱 [尋找伺服器主機系統](finding-server-host-systems.md)。

[**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)和 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)的呼叫和其相關聯的資料結構看起來會像下面這樣：

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

請注意， [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) 參數 *PBindingVector* 是指向 RPC 系結 [**\_ \_ 向量**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector)指標的指標。 也請記住，每次呼叫 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) 時，都必須接著呼叫 [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)。

若要從名稱服務資料庫中移除匯出的介面，伺服器會呼叫 [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) ，如下所示：

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

只有在永久移除服務時，才應該使用 [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) 函數。 暫時停用服務時，不應使用此服務，例如當伺服器關閉進行維護時。 伺服器程式可以向名稱服務資料庫登錄，但因為伺服器暫時離線，所以無法使用。 用戶端應用程式應包含這類條件的例外狀況處理常式代碼。

如需名稱服務資料庫的內容和格式的詳細資訊，請參閱 [RPC 名稱服務資料庫](the-rpc-name-service-database.md)。

如果用戶端和伺服器程式都是在 Windows 2000 下執行，應用程式就可以利用 Active Directory 服務。 執行用戶端和伺服器程式的電腦，都必須是 Windows 2000 網域的成員。

若要使用 Active Directory 服務通告其存在，伺服器程式應在網域系統管理員的安全性內容中執行。 如果它是在網域使用者的內容中執行，則網域系統管理員必須修改 RPC 服務容器 (ACL) 的存取控制清單。 如需詳細資訊，請參閱 Active Directory 檔。

 

 




