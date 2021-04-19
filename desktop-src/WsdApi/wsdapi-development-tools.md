---
description: Windows SDK 中包含的 WSDAPI 開發工具 (WSD CodeGen、WSD Debug 主控制項和 WSD Debug 用戶端) 讓開發人員建立及偵測 WSDAPI 用戶端與裝置。
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: WSDAPI 開發工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977824"
---
# <a name="wsdapi-development-tools"></a>WSDAPI 開發工具

Windows SDK 中包含的 WSDAPI 開發工具 (WSD CodeGen、WSD Debug 主控制項和 WSD Debug 用戶端) 讓開發人員建立及偵測 WSDAPI 用戶端與裝置。 無法使用這些工具的原始程式碼。 SDK 工具位於下列目錄： <Windows SDK Install Folder> \\ Bin。

WSD CodeGen (wsdcodegen.exe) 會將 WSDL 合約轉換成產生的 c + + 程式碼，讓開發人員可以直接呼叫。 它會處理資料序列化和線路標記法，讓開發人員可以專注于設計應用程式。 如需 WSD CodeGen 的詳細資訊，請參閱 [裝置上的 Web 服務程式碼](web-services-for-devices-code-generator.md)產生器。 這項工具適用于 Microsoft Windows 軟體開發套件 (SDK) 以及 Windows 驅動程式套件 (WDK) 。

WSD Debug Host (wsddebug \_host.exe) 和 WSD Debug 用戶端 (wsddebug \_client.exe) 工具可協助開發人員進行用戶端和主機的調試。 這些工具可用來驗證和檢查 WS-Discovery 和中繼資料交換流量。 如需 WSD Debug 主控制項和 WSD 偵錯工具用戶端的詳細資訊，請參閱 [調試](debugging-tools.md)程式。 這些工具僅適用于 Windows SDK。

有一個額外的開發工具，名為 [ [WSDAPI 基本互通性工具] (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx)，只會在 WDK 中提供。 這項工具是用來測試服務方法、訊息傳輸優化機制 (MTOM) 、附件或 WS-事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 上的 WSD 應用程式開發](wsd-application-development-on-windows.md)
</dt> <dt>

[裝置上的 Web 服務程式碼產生器](web-services-for-devices-code-generator.md)
</dt> <dt>

[WSDAPI 基本互通性工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[調試工具](debugging-tools.md)
</dt> </dl>

 

 



