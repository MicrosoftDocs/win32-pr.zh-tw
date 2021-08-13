---
description: 使用安全通訊端延伸模組的 Advanced Winsock 範例
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: 使用安全通訊端延伸模組的 Advanced Winsock 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ead38a7e62be527e91474ac921803327647ca6cefd1ec68778d03e1c68c1bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412168"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>使用安全通訊端延伸模組的 Advanced Winsock 範例

## <a name="secure-tcp-client-and-server-sample"></a>保護 TCP 用戶端和伺服器範例

Microsoft Windows 軟體開發套件 (SDK) 包含更先進的 Winsock 範例，示範如何使用安全通訊端延伸模組。 此範例包含使用 Winsock 和安全通訊端擴充功能安全地連接的 TCP 用戶端和伺服器。

根據預設，Winsock 範例原始程式碼會安裝在下列目錄中：

*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ 範例 \\ NetDs \\ winsock*

範例位於下列資料夾底下：

*securesocket*

範例程式碼會分割成不同的目錄，如下所述：

-   stcpclient-包含安全 TCP 用戶端程式代碼的資料夾。
-   stcpcommon-包含安全 TCP 用戶端與伺服器之間共用之通用程式庫程式碼的資料夾。
-   stcpserver-包含安全 TCP 伺服器程式碼的資料夾。

請注意，這些範例是要在執行 Windows Vista 或更新版本的兩部不同電腦上執行。 此外，您必須在兩部電腦上布建 IPsec 認證，才能讓連線成功，因為此範例使用 IPsec 保護其流量。 如需有關設定 IPsec 認證的詳細資訊，請參閱 [IPsec](/windows/desktop/FWP/ipsec-configuration) 設定的相關檔。

建立範例將會產生兩個可執行檔：

*stcpclient.exe* 和 *stcpserver.exe*。

將 *stcpclient.exe* 複製到電腦 A，然後將 *stcpserver.exe* 複製到電腦 B。在電腦 B 上，在命令提示字元中執行下列命令，以啟動 TCP 伺服器：

**stcpserver.exe**

執行下列命令以取得伺服器的其他使用方式選項：

**stcpserver.exe/？**

然後在電腦 A 上，在命令提示字元中執行下列命令，以啟動 TCP 用戶端：

**stcpclient.exe <的完整 DNS------------------->a**

此時，應該會安全地建立連接。

執行下列命令以取得用戶端的更多使用方式選項：

**stcpclient.exe/？**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 篩選平台](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[應用層強制 (ALE) ](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[IPsec 設定](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[IPsec 功能](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[使用安全通訊端擴充功能](using-secure-socket-extensions.md)
</dt> <dt>

[安全性支援提供者介面 (SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Windows 篩選平台](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Windows篩選平臺 API 函數](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Winsock 安全通訊端擴充功能](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
