---
description: 提供計算 (&\# 0034; 處理後&\# 0034; ) 效能計數器資料。 提供動態資料給衍生自 Win32 PerfFormattedData 的 WMI 類別 \_ 。 也稱為處理後計數器提供者。
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: 格式化效能 Data Provider
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab8e931c3d03c619af5b1e37cadd8dacdccd21534513ed3a1aa1d7b9076acfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556611"
---
# <a name="formatted-performance-data-provider"></a>格式化效能 Data Provider

\[格式化的效能 Data Provider （也稱為「處理後計數器提供者」）不再適用于使用。 相反地，請使用 [WMIPerfInst](wmiperfinst-provider.md) 提供者。\]

高效能格式化的效能資料提供者提供計算 ( "處理後" ) 效能計數器資料，例如磁片花在寫入資料的時間百分比。 此提供者會將動態資料提供給衍生自 [**Win32 \_ PERFFORMATTEDDATA**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的 WMI 類別。 此提供者和 [效能計數器提供者](performance-counter-provider.md) 之間的差異在於效能計數器提供者會提供原始資料，而處理後計數器提供者會提供與 [*系統監視器*](gloss-s.md)完全一樣的效能資料。 [**\_ \_ Win32Provider**](--win32provider.md)實例名稱為 "HiPerfCooker \_ v1"。

計數器物件的 WMI 格式化類別名稱的格式為「Win32 \_ PerfFormattedData \_ *服務 \_ 名稱* \_ *物件 \_ 名稱*」。 例如，包含邏輯磁片計數器的 WMI 類別名稱是 **Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**。 這些類別位於「根 \\ CIMv2」命名空間中。

因為效能資料類別是在指定的系統上動態新增和修改，所以無法正式記錄所有已知效能物件的屬性。 若要判斷哪些類別可供您使用，以及識別這些類別具有哪些成員，請參閱抓取 [原始和格式化效能資料物件的檔](retrieving-raw-and-formatted-performance-data.md)。

[**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別會使用 [WMI 效能計數器類型](wmi-performance-counter-types.md)中的 **CookingType** 辨識符號來指定計算效能資料的公式。 此辨識符號與 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中的 **CounterType** 限定詞相同。

作為高效能的提供者，處理後計數器提供者會實作為標準 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及 [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 方法和下列 [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) 方法：

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

 

 
