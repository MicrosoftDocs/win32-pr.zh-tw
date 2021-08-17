---
title: 核心模式 SSL
description: 核心模式 SSL
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- 核心模式 SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9dcfeb87b1a98539d7bd6a3b8b82dcfd5ee41fc9ad4c4c306f4c399aebd18a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393916"
---
# <a name="kernel-mode-ssl"></a>核心模式 SSL

核心模式 SSL 是在 Windows Server 2003 Service Pack 1 (SP1) （支援有限）中引進。 針對 Windows Server 2003 SP1 上執行的電腦，必須將登錄機碼設定為啟用核心 SSL。 針對 Windows Server 2008 和 Windows Vista 上執行的電腦，會提供 SSL 的完整核心模式支援。

下列各節說明核心模式的 SSL 支援：

-   Windows Server 2003 SP1 中的核心模式 SSL
-   Windows Server 2008 和 Windows Vista 中的核心模式 SSL

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Windows Server 2003 SP1 中的核心模式 SSL

在 Windows server 2003 （含 SP1）中，HTTP 伺服器 API 可讓您選擇以核心模式執行 ssl 安全性 (使用者模式 SSL 是預設) 。 核心模式功能藉由將加密和解密作業移至核心來改善 SSL 效能，進而減少核心模式和使用者模式之間的轉換數目。

當 SSL 以核心模式執行時，不支援下列功能：

-   Client certificates
-   RC2 密碼
-   PCT 1.0 通訊協定
-   伺服器憑證設定變更需要重新開機 HTTP 服務
-   大量加密和卸載支援

## <a name="configuring-kernel-mode-ssl"></a>設定核心模式 SSL

核心模式 SSL 是由 **EnableKernelSSL** 登錄值所控制，並藉由將值設定為1來啟用。 啟用核心模式 SSL 將會停用使用者模式 SSL，且需要重新開機 HTTP 服務才會生效。 **EnableKernelSSL** 登錄機碼位於：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **HTTP** \\ **參數** \\ **EnableKernelSSL**

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>Windows Server 2008 和 Windows Vista 中的核心模式 SSL

針對 Windows Server 2008 和 Windows Vista 上執行的電腦，HTTP 伺服器 API 具備增強的 SSL 功能。

以下是支援的新功能：

-   核心模式 SSL 中的完整用戶端憑證支援
-   所有 HTTP SSL 交易的核心模式 SSL
-   大量加密和卸載支援
-   PCT 1.0 通訊協定
-   RC2 密碼
-   提高使用者模式 SSL 的效能

## <a name="configuration"></a>組態

核心模式 SSL 可透過下列兩個登錄值設定：位於下列位置的 HTTP 參數機碼：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

使用者必須擁有系統管理員/本機系統許可權，才能修改登錄值，以及查看或修改記錄檔以及包含它們的資料夾。

啟動 HTTP 伺服器 API 驅動程式時，會讀取登錄值中的設定資訊。 如此一來，如果設定已變更，則必須停止並重新啟動驅動程式，才能讀取新的值。 您可以使用下列主控台命令來完成這項作業：

**net stop HTTP**

**net start HTTP**

下表列出登錄設定值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>登錄值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EnableKernelSSL</td>
<td><strong>Windows Server 2008 和 Windows Vista：</strong>此登錄值已過時。<br/></td>
</tr>
<tr class="even">
<td>EnableSslCloseNotify</td>
<td>設定為<strong>TRUE</strong>以啟用關閉通知的<strong>DWORD</strong>值，否則為<strong>FALSE</strong>以停用關閉通知需求。 關閉-通知預設為停用。<br/> 當啟用 [關閉-通知] 時，用戶端應用程式必須在關閉 TCP 連接之前傳送「關閉通知」訊息。 HTTP 伺服器 API 也會在關閉連接之前傳送關閉通知。<br/> 當啟用 [關閉] 通知時，當用戶端傳送「關閉通知」訊息時，HTTP 伺服器 API 會在未來連線到用戶端時重複使用 SSL 會話。 如果用戶端未傳送關閉通知，HTTP 伺服器 API 將不會在未來的連接上重複使用相同的 SSL 會話。 因此，在新的連接上會觸發完整的 SSL 交握，因此會降低效能。 <br/>
<blockquote>
[!Note]<br />
啟用「關閉通知」有助於減輕對 HTTPS 要求和回應的截斷攻擊。
</blockquote>
<br/> <br/> 停用 [關閉通知] 時，HTTP 伺服器 API 會重複使用 SSL 會話，以供未來連接使用。<br/></td>
</tr>
<tr class="odd">
<td>DisableSslCertChainCacheOnlyUrlRetrieval</td>
<td>設定為<strong>TRUE</strong>的<strong>DWORD</strong>值，可讓 HTTP 伺服器 API 從網際網路或本機存放區取出中繼憑證，或使用<strong>FALSE</strong>從本機存放區取出中繼憑證。 預設的登錄值為 <strong>FALSE</strong>。<br/> 根據預設，HTTP 伺服器 API 會在本機電腦帳戶下，從中繼憑證授權單位單位存放區中取出中繼憑證，以建立用戶端憑證鏈。 將此值設定為 <strong>TRUE</strong> ，可讓 HTTP 伺服器 API 只從本機存放區取得中繼憑證，但也可從網際網路上的中繼憑證授權單位單位抓取。<br/></td>
</tr>
</tbody>
</table>



 

 

 





