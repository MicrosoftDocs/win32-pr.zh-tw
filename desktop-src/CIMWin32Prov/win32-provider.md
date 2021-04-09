---
description: Microsoft&\# 160;Win32 提供者會抓取和更新 Windows 系統&郵件的相關資料， \# 例如環境變數目前的設定和邏輯磁片的屬性。
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Win32 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688628"
---
# <a name="win32-provider"></a>Win32 提供者

Microsoft Win32 提供者會抓取和更新與 Windows 系統相關的資料—像是環境變數目前的設定和邏輯磁片的屬性。 使用 Win32 提供者時，管理應用程式可以使用 WMI 輕鬆地存取此資料。 Win32 提供者會藉由發出 Windows 函數呼叫和查詢系統登錄來抓取其資訊。

Win32 提供者會定義用來描述 Windows 系統上可用之硬體或軟體的類別，以及它們之間的關聯性。

Win32 提供者是實例和方法提供者，它會實作為標準 [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及下列 [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) 方法：

-   [**CreateInstanceEnumAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**DeleteInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ExecMethodAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

下表列出 Win32 提供者類別類別目錄。



| 類別                                                                             | Description                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [電腦系統硬體類別](computer-system-hardware-classes.md)<br/> | 與硬體相關的物件。<br/>                                      |
| [作業系統類別](operating-system-classes.md)<br/>                 | 作業系統相關物件。<br/>                              |
| [效能計數器類別](performance-counter-classes.md)<br/>           | 效能計數器中的原始和計算效能資料。<br/> |
| [WMI 服務管理類別](wmi-service-management-classes.md)<br/>     | WMI 的管理。<br/>                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CIMWin32 WMI 提供者](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
