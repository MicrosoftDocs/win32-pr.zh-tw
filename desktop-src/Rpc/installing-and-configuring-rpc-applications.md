---
title: 安裝和設定 RPC 應用程式
description: 當伺服器或用戶端上安裝 Microsoft Windows 作業系統時，安裝程式會自動安裝 RPC 執行時間檔案。
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- 遠端程序呼叫 RPC、工作、安裝和設定應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5cf5d408e2b23042074031ce0307b3a13cf3461df31cc39899b0315f99e8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020438"
---
# <a name="installing-and-configuring-rpc-applications"></a>安裝和設定 RPC 應用程式

當伺服器或用戶端上安裝 Microsoft Windows 作業系統時，安裝程式會自動安裝 RPC 執行時間檔案。 不需要進一步的 RPC 安裝。 不過，您必須確定您安裝的 Windows 版本支援分散式應用程式中使用的所有功能。

當您在 Windows 3.x 或 Microsoft MS-DOS 作業系統上使用 rpc 應用程式時，您必須將 rpc 執行時間可執行檔案複製到將使用應用程式的 Windows 3.x 或 MS-DOS 電腦。 \\ \\ \_ 平臺軟體發展工具組上的 directory mstools RPC rt16 (SDK) CD 包含這些檔案的磁片映射，以及安裝程式來安裝檔案。 使用這個磁片映射來建立安裝磁片，以便與您的 RPC 應用程式一起散發。 您也可以在32位/64 位 Windows 作業系統上，使用以 MS-DOS 或 Windows 為目標的16位用戶端應用程式。 不過，您的應用程式安裝程式必須安裝此磁片映射中包含的可執行檔。

當您為 Macintosh 用戶端建立 RPC 應用程式時，您必須在組建階段將必要的檔案連結到應用程式。 不需要額外的 RPC 安裝。

如需可轉散發檔案和授權合約的詳細資訊，請參閱 \\ \\ \\ \\ Platform SDK CD 上的授權Redist.txt 和授權License.txt。

本節包含在各種不同的硬體和軟體平臺上設定 RPC 應用程式的相關資訊。 它會在下列各節中提供討論：

-   [設定名稱服務提供者](configuring-the-name-service-provider.md)
-   [登錄資訊](registry-information.md)
-   [使用 RPC 搭配 Winsock Proxy](using-rpc-with-winsock-proxy.md)
-   [SPX/IPX 安裝](spx-ipx-installation.md)
-   [設定安全性伺服器](configuring-the-security-server.md)

 

 




