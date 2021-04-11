---
description: 效能計數器類別可讓腳本和程式存取由現有高效能提供者計算的系統效能資料。
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: 效能計數器類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847605"
---
# <a name="performance-counter-classes"></a>效能計數器類別

效能計數器類別可讓腳本和程式存取由現有高效能提供者計算的系統效能資料。 這些類別是由原始效能計數器類別和格式化效能計數器類別所組成。

不同的提供者會透過 WMI 提供效能程式庫資料。 [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)和[WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)提供者會提供第1版和第2版[效能計數器](/windows/desktop/PerfCtrs/performance-counters-portal)的類別。 這些提供者會維持與舊版作業系統中可用類別的相容性。

此區段中的類別是用來建立效能計數器類別的抽象基類。 這不是您在作業系統上可能會發現的完整類別清單。 如需詳細資訊，請參閱 [效能程式庫和 WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi)。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**Win32 \_ 效能**](win32-perf.md)
</dt> <dd>

效能計數器類別 [**Win32 \_ PerfRawData**](win32-perfrawdata.md) 和 [**win32 \_ PerfFormattedData**](win32-perfformatteddata.md)的基類。

</dd> <dt>

[**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md)
</dt> <dd>

預先安裝的計算資料類別的抽象基類。

</dd> <dt>

[**Win32 \_ PerfRawData**](win32-perfrawdata.md)
</dt> <dd>

所有具體原始效能計數器類別的抽象基類。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Win32 類別](win32-provider.md)
</dt> </dl>

 

 
