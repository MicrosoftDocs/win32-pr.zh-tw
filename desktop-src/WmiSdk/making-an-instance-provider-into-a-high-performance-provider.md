---
description: 不建議寫入 WMI 高效能提供者來建立效能計數器。
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: 讓執行個體提供者成為 High-Performance 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985659"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>讓執行個體提供者成為 High-Performance 提供者

不建議寫入 WMI 高效能提供者來建立效能計數器。 從 Windows Vista 開始，自動探索/AutoPurge (ADAP) 反向介面卡，不再將 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 遷移至 Windows 效能程式庫中。 若要建立效能計數器提供者，請使用 [效能計數器2.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。 建立效能程式庫物件之後， [WMIPerfClass 提供者](wmiperfclass-provider.md) 會剖析物件，並為每個效能物件建立或重新整理衍生自 [**WIN32 \_ performance 的**](/windows/desktop/CIMWin32Prov/win32-perf) WMI 類別。 然後， [WMIPerfInst 提供者](wmiperfinst-provider.md) 會動態地將原始和格式化的效能計數器資料提供給 WMI 效能類別。

下列高階程式提供建立高效能提供者所需的步驟。

**若要建立高效能提供者**

1.  向 WMI 註冊您的提供者。 如需詳細資訊，請參閱 [註冊 High-Performance 提供者](registering-a-high-performance-provider.md)。
2.  執行您的提供者。 如需詳細資訊，請參閱 [撰寫執行個體提供者](writing-an-instance-provider.md)。
3.  執行高效能介面。 如需詳細資訊，請參閱 [執行 High-Performance 介面](implementing-the-high-performance-interface.md)。
4.  受控物件格式 (MOF) 架構中衍生並撰寫您的，以取得原始效能資料。 如需詳細資訊，請參閱 [支援 Win32 \_ PerfRawData 類別](supporting-the-win32-perfrawdata-class.md)。
5.  衍生並撰寫您的 MOF 架構，以取得預先計算的資料。 藉由支援這個類別，就不需要提供者來執行計算。 這項資料會與在 Perfmon 中的系統監視器中顯示的資料相同。 如需詳細資訊，請參閱 [支援 Win32 \_ PerfFormattedData 類別](supporting-the-win32-perfformatteddata-class.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[效能程式庫和 WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
