---
description: Microsoft&\# 160;Win32 提供者會&\# 郵件、資料（例如環境變數目前的設定和邏輯磁片的屬性），來抓取和更新與 Windows 系統相關的資料。
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Win32 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca4426f849b59dfbfb5f667c32e8e3b9cd47ca7482fd3547d631592a080f968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118007771"
---
# <a name="win32-provider"></a>Win32 提供者

Microsoft Win32 提供者會抓取和更新與 Windows 系統相關的資料，例如環境變數目前的設定和邏輯磁片的屬性等資料。 使用 Win32 提供者時，管理應用程式可以使用 WMI 輕鬆地存取此資料。 Win32 提供者會藉由進行 Windows 函式呼叫和查詢系統登錄來抓取其資訊。

Win32 提供者會定義用來描述 Windows 系統上可用之硬體或軟體的類別，以及它們之間的關聯性。

Win32 提供者是實例和方法提供者，它會實作為標準 [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及下列 [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) 方法：

-   [**CreateInstanceEnumAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**DeleteInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ExecMethodAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

下表列出 Win32 提供者類別類別目錄。



| 類別                                                                             | 描述                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [電腦系統硬體類別](computer-system-hardware-classes.md)<br/> | 與硬體相關的物件。<br/>                                      |
| [作業系統類別](operating-system-classes.md)<br/>                 | 作業系統相關物件。<br/>                              |
| [效能計數器類別](performance-counter-classes.md)<br/>           | 效能計數器中的原始和計算效能資料。<br/> |
| [WMI 服務管理類別](wmi-service-management-classes.md)<br/>     | WMI 的管理。<br/>                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CIMWin32 WMI 提供者](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
