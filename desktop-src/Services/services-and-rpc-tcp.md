---
description: 從 Windows Vista 開始，服務控制管理員 (SCM) 支援使用傳輸控制)  (通訊協定的遠端程序呼叫， (RPC/NP) 的具名管道。
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: 服務和 RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fdb2ef3b21f280ba4e5078d302813de41a5a43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987355"
---
# <a name="services-and-rpctcp"></a>服務和 RPC/TCP

從 Windows Vista 開始，服務控制管理員 (SCM) 支援使用傳輸控制)  (通訊協定的遠端程序呼叫， (RPC/NP) 的具名管道。 用戶端 SCM 函式預設會使用 RPC/TCP。

RPC/TCP 適用于從遠端使用 SCM 功能的大部分應用程式，例如遠端系統管理或監視工具。 不過，針對相容性和效能，有些應用程式可能需要藉由設定本主題中所述的登錄值來停用 RPC/TCP。

當服務呼叫遠端 SCM 函數時，用戶端 SCM 會先嘗試使用 RPC/TCP 來與伺服器端 SCM 通訊。 如果伺服器執行的是支援 RPC/TCP 的 Windows 版本，並允許 RPC/TCP 流量，RPC/TCPP 連接將會成功。 如果伺服器執行的 Windows 版本不支援 RPC/TCP，或支援 RPC/TCP，但在只允許具名管道流量的防火牆後方運作，則 RPC/TCP 連接逾時，且 SCM 會重試與 RPC/NP 的連接。 最後，這將會成功，但可能需要一些時間 (通常超過20秒的) ，導致 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式顯示為封鎖。

TCP 不包含使用 **net use** 命令指定的使用者認證。 因此，如果啟用了 RPC/TCP，並使用 **sc.exe** 來嘗試存取指定的服務，則命令可能會失敗並拒絕存取。 在用戶端上停用 RPC/TCP 會導致 **sc.exe** 命令使用具有使用者認證的具名管道，因此命令將會成功。 如需 sc.exe 的詳細資訊，請參閱 [使用 SC 控制服務](controlling-a-service-using-sc.md)。

> [!Note]  
> 服務不應該將明確的認證提供給 **net use** 命令，因為這些認證可能會在服務界限之外不慎共用。 相反地，服務應該使用 [用戶端](/windows/desktop/SecAuthZ/client-impersonation) 模擬來模擬使用者。

 

### <a name="rpctcp-registry-values"></a>RPC/TCP 登錄值

RPC/TCP 是由 **SCMApiConnectionParam**、 **DisableRPCOverTCP** 和 **DisableRemoteScmEndpoints** 登錄值所控制，這些值全都位於 **HKEY \_ 本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **Control** 機碼下。 所有這些值都有 REG \_ DWORD 資料類型。 下列程式示範如何使用這些登錄值來控制 RPC/TCP。

下列程式描述如何在用戶端上停用 RPC/TCP。

**若要在用戶端上停用 RPC/TCP**

1.  將 **SCMApiConnectionParam** 登錄值與 mask 值0x80000000 合併。
2.  重新開機呼叫 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式的應用程式。

下列程式描述如何在伺服器端停用 TCP。

**若要在伺服器端停用 TCP**

1.  將 **DisableRPCOverTCP** 登錄值設定為1。
2.  重新啟動伺服器。

下列程式說明如何在伺服器上停用 RPC/TCP 和 RPC/NP (例如，以減少受攻擊面) 。

**若要在伺服器上停用 RPC/TCP 和 RPC/NP**

1.  將 **DisableRemoteScmEndpoints** 登錄值設定為1。
2.  重新啟動伺服器。

**SCMApiConnectionParam** 登錄值也可以用來指定 RPC/TCP 逾時間隔（以毫秒為單位）。 例如，值為30000時，會指定30秒的逾時間隔。 預設值為 21000 (21 秒) 。

 

 
