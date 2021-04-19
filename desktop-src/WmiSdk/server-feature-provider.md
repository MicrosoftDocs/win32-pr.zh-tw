---
description: 從 Windows Server 2008 開始，伺服器功能提供者會提供在伺服器上安裝哪些伺服器功能的相關資訊。 此類別可讓系統管理員清查及管理其伺服器角色和功能。
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: 伺服器功能提供者
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977361"
---
# <a name="server-feature-provider"></a>伺服器功能提供者

從 Windows Server 2008 開始，伺服器功能提供者會提供在伺服器上安裝哪些伺服器功能的相關資訊。 此類別可讓系統管理員清查及管理其伺服器角色和功能。

伺服器角色定義為一組元件，可提供特定功能區域的函式，例如列印、檔案、網域控制項等等。 一般伺服器角色是檔案伺服器、郵件伺服器、DNS 伺服器、網域控制站、應用程式伺服器等等。

如果企業未執行報表伺服器角色的管理軟體（例如已安裝管理元件 Microsoft Operations Manager），則您可以藉由查詢 [**Win32 \_ ServerFeature**](win32-serverfeature.md) 類別來取得該資訊。 遠端電腦上的伺服器角色和功能資訊可透過一般的 WMI 遠端連線或使用 Windows 遠端管理 (WinRM) 服務來取得。 如需遠端 WMI DCOM 連接的詳細資訊，請參閱 [連接到遠端電腦上的 wmi](connecting-to-wmi-on-a-remote-computer.md)。 如需使用 [*ws-management*](/windows/desktop/WinRM/windows-remote-management-glossary) 通訊協定連接的詳細資訊，請參閱 [Windows 遠端管理](/windows/desktop/WinRM/portal)。

伺服器功能提供者支援下列 WMI 類別：

-   [**Win32 \_ ServerFeature**](win32-serverfeature.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 提供者](wmi-providers.md)
</dt> </dl>

 

 
