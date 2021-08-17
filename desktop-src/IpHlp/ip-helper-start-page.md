---
description: 網際網路通訊協定協助程式 (IP 協助程式) API 可讓您對本機電腦的網路設定進行抓取和修改。
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: IP 協助程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6262543d1644fbe62858f2c90064f42d2c1348b2f3c56033813f453d33470ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146771"
---
# <a name="ip-helper"></a>IP 協助程式

## <a name="purpose"></a>目的

網際網路通訊協定協助程式 (IP 協助程式) API 可讓您對本機電腦的網路設定進行抓取和修改。

## <a name="where-applicable"></a>適用時

IP 協助程式 API 適用于任何以程式設計方式操作網路和 TCP/IP 設定的計算環境。 一般的應用程式包括 IP 路由通訊協定，以及簡單的網路管理通訊協定 (SNMP) 代理程式。

## <a name="developer-audience"></a>開發人員對象

IP Helper API 是設計來供 C/c + + 程式設計人員使用。 程式設計人員也應該熟悉 Windows 網路和 tcp/ip 網路概念。

## <a name="run-time-requirements"></a>執行階段需求求

IP 協助程式 API 可在所有 Windows 平臺上使用。 並非所有的作業系統都支援所有功能。 當 Windows 通訊端2平臺限制的特定實作為或功能存在時，就會在檔中清楚注明它們。 如果在不支援函數的平臺上呼叫 IP Helper 函式， \_ \_ 則會傳回不支援的錯誤。 如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的需求一節。

## <a name="in-this-section"></a>本節內容



| 主題                                                              | 描述                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IP Helper 的新功能](what-s-new-in-ip-helper.md)<br/>  | IP Helper 的新功能相關資訊。<br/>                                                                                                                                                             |
| [關於 IP Helper](about-ip-helper.md)<br/>                  | 適用于開發人員的 IP 協助程式程式設計考慮和功能的一般資訊。<br/>                                                                                               |
| [使用 IP Helper](using-ip-helper.md)<br/>                  | 搭配 IP Helper 使用的程式和程式設計技術。 本節包含基本 IP 協助程式程式設計技術，例如 [開始使用與 ip 協助程式的關聯](getting-started-with-ip-helper.md)。<br/> |
| [IP 協助程式參考](ip-helper-function-reference.md)<br/> | IP Helper 函數、結構和列舉的參考檔。<br/>                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows通訊端2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[路由及遠端存取服務](../rras/routing-start-page.md)
</dt> </dl>

 

