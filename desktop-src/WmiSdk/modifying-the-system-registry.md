---
description: 系統登錄包含作業系統、服務和應用程式所使用的設定資料。
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: 修改系統登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb274163999996267b5f1df62fb9352831763d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971986"
---
# <a name="modifying-the-system-registry"></a>修改系統登錄

系統登錄包含作業系統、服務和應用程式所使用的設定資料。 Windows Management Instrumentation (WMI) 具有 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 和 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 類別，其具有可用來監視或修改本機電腦或遠端電腦上登錄的方法。 [Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)支援 [**win32 \_ 登錄類別**](/windows/desktop/CIMWin32Prov/win32-registry)，其中包含有關登錄大小的靜態資料。

系統登錄提供者是與系統登錄介面互動的實例、屬性和事件提供者。 System Registry Provider 是具有 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面的標準提供者。 您可以使用系統登錄提供者來存取本機和遠端系統上的登錄機碼和資訊。 如需詳細資訊，請參閱 [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider)。

WMI 會將 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 放在根 \\ 預設命名空間中。 不過，您可以將 Regevent 的 mof 檔案編譯成其他命名空間，以供其他應用程式使用。

下表中所識別的主題可示範如何使用 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 類別和系統登錄提供者。



| 主題                                                                                              | 描述                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [取得登錄資料](obtaining-registry-data.md)                                             | 您可以透過 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 類別的方法取得或修改登錄資料，讓您可以在本機或遠端自動化登錄活動。                    |
| [變更登錄資料](changing-registry-data.md)                                               | 您可以新增或刪除金鑰，以及新增或變更機碼下的登錄專案值。                                                                                                                    |
| [使用系統登錄提供者進行程式設計](programming-with-the-system-registry-provider.md) | 您可以定義您自己的類別，讓系統登錄提供資料。                                                                                                                       |
| [註冊系統登錄事件](registering-for-system-registry-events.md)               | System Registry provider 可將事件傳送給取用者。 若要接收事件，您必須註冊您的取用者、建立查詢，然後確保提供者會正確地傳送事件給您。 |
| [註冊系統登錄提供者](registering-the-system-registry-provider.md)           | System Registry provider 會註冊為 WMI 安裝程式的一部分。                                                                                                                |



 

 

 
