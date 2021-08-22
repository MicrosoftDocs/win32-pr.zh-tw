---
description: 效能計數器提供者是一個高效能的提供者，可提供原始效能計數器資料給從 Win32 PerfRawData 衍生的 WMI 效能計數器類別 \_ 。 \_ \_ Win32Provider 實例名稱是 &\# 0034;NT5 \_ GenericPerfProvider \_ V1&\# 0034;。
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: 效能計數器提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c846d66cd183e866623004cacfbcb630ac68480fab8dd58eca2b5a4dc6d2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050526"
---
# <a name="performance-counter-provider"></a>效能計數器提供者

\[效能計數器提供者不再可供使用。 相反地，請使用 [WMIPerfInst](wmiperfinst-provider.md) 提供者。\]

效能計數器提供者是一個高效能的提供者，可提供原始效能計數器資料給從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)衍生的 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。 [**\_ \_ Win32Provider**](--win32provider.md)實例名稱為 "NT5 \_ GenericPerfProvider \_ V1"。

[**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別位於 WMI "Root \\ CIMv2" 命名空間中。 每個 WMI 效能類別都會對應到效能程式庫中的效能物件。 這些類別的屬性代表物件的計數器。 原始計數器物件的 WMI 類別名稱的格式為 **Win32 \_ \_ \_ PerfRawData* 服務 \_ 名稱 *\_* 物件 \_ 名稱 * * *。 例如，包含邏輯磁片計數器的 WMI 類別名稱是 [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)。

您可以使用對應的 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 類別，來取得 [*系統監視器*](gloss-s.md)中顯示的預先計算效能資料。 例如，使用 [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) 類別取得預先計算的磁片資料。

如需如何撰寫可存取原始效能資料之用戶端的詳細資訊，請參閱使用 [c + + 存取效能資料](accessing-performance-data-in-c--.md)。

效能計數器提供者是一個高效能的提供者，它會實作為標準 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 方法和下列 [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) 方法：

-   [**CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 提供者](wmi-providers.md)
</dt> </dl>

 

 
