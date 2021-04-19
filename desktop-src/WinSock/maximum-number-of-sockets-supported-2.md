---
description: 特定 Windows 通訊端服務提供者支援的通訊端數目上限是特定的實值。
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: 支援的通訊端數目上限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972410"
---
# <a name="maximum-number-of-sockets-supported"></a>支援的通訊端數目上限

特定 Windows 通訊端服務提供者支援的通訊端數目上限是特定的實值。 Microsoft Winsock 提供者會限制只能由本機電腦上的可用記憶體支援的通訊端數目上限。 不過，協力廠商 Winsock 提供者可能會限制支援的通訊端數目。 應用程式不應對特定數量的通訊端提供任何假設。 如需有關此主題的詳細資訊，請參閱 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)。

## <a name="fd_set-and-select"></a>FD \_ 設定並選取

\_從 UNIX 環境將應用程式移植到 Windows 時，會在 *Winsock2* 標頭檔中定義一些 FD XXX 宏。 這些宏會搭配 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 和 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函式使用，以將應用程式移植到 Windows。 Windows 通訊端應用程式可使用的通訊端數目上限不受資訊清單常數 FD SETSIZE 所影響 \_ 。 此值定義于 *Winsock2* 標頭檔中，用來建立與 **select** 函數搭配使用的 [**FD \_ 集**](/windows/desktop/api/winsock/nf-winsock-fd_set)結構。 Winsock2 中的預設值是64。 如果應用程式的設計目的是要使用 **select** 和 **WSAPoll** 函式來處理超過64通訊端，實作項應該先定義每個原始程式檔中的資訊清單 FD \_ SETSIZE，然後再包含 *Winsock2. h* 標頭檔。 執行這項操作的其中一種方法，就是將定義包含在 makefile 的編譯器選項中。 例如，您可以將 "-DFD \_ SETSIZE = 128" 新增為 Microsoft c + + 編譯器命令列的選項。 您必須強調，將 FD \_ SETSIZE 定義為特定值，並不會影響 Windows 通訊端服務提供者所提供的實際通訊端數目。 此值只會影響 \_ **Select** 和 **WSAPoll** 函數所使用的 FD XXX 宏。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**FD \_ 設定**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**選擇**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
