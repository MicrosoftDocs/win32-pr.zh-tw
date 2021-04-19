---
description: 必須在系統上正確安裝傳輸通訊協定，並向 Windows 通訊端註冊，應用程式才能存取。
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: 同時存取多個傳輸通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989314"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a>同時存取多個傳輸通訊協定

必須在系統上正確安裝傳輸通訊協定，並向 Windows 通訊端註冊，應用程式才能存取。 Ws2 \_32.dll 程式庫會匯出一組函式來加速註冊程式。 這包括建立新的註冊，以及移除現有的註冊。

建立新的註冊時，呼叫者 (亦即，堆疊廠商的安裝腳本) 會提供一或多個填入 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構，其中包含一組完整的通訊協定資訊。 如需詳細資訊，請參閱 [Windows 通訊端 2 SPI](about-the-winsock-spi.md)。 以這種方式安裝的任何傳輸堆疊都稱為 Windows 通訊端服務提供者。

在 Windows XP Service Pack 2 (SP2) 、Windows Server 2003 （含 Service Pack 1） (SP1) ，以及 Windows Vista 和更新版本。 您可以使用下列命令，在命令提示字元中顯示包含已安裝的傳輸和命名空間提供者清單的 Winsock 目錄：

**netsh winsock show catalog**

Microsoft Windows 軟體開發套件 (SDK) 包含 *Sporder.exe*，可讓使用者查看和修改服務提供者的列舉順序。 使用 *Sporder.exe*，如果有一個以上的這類堆疊存在，使用者就可以手動建立特定的 tcp/ip 通訊協定堆疊作為預設 tcp/ip 提供者。

*Sporder.exe* 應用程式會使用 *Sporder.dll* 中匯出的函式，來重新排序服務提供者。 因此，安裝應用程式可以使用 *Sporder.dll* 所提供的介面，以程式設計方式重新排序服務提供者。

-   [多層通訊協定和通訊協定鏈](layered-protocols-and-protocol-chains-2.md)
-   [使用多個通訊協定](using-multiple-protocols-2.md)
-   [Select 上有多個提供者限制](multiple-provider-restrictions-on-select-2.md)

 

 
