---
description: 從 Windows Vista 開始，WmiPerfInst 提供者會將原始和格式化的效能計數器資料動態提供給衍生自 Win32 效能的 WMI 效能計數器類別 \_ 。
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: WmiPerfInst 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983425"
---
# <a name="wmiperfinst-provider"></a><span data-ttu-id="b2b33-103">WmiPerfInst 提供者</span><span class="sxs-lookup"><span data-stu-id="b2b33-103">WmiPerfInst Provider</span></span>

<span data-ttu-id="b2b33-104">從 Windows Vista 開始，WmiPerfInst 提供者會將原始和格式化的效能計數器資料動態提供給衍生自 [**Win32 效能 \_**](/windows/desktop/CIMWin32Prov/win32-perf)的 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。</span><span class="sxs-lookup"><span data-stu-id="b2b33-104">Starting with Windows Vista, the WmiPerfInst provider supplies raw and formatted performance counter data dynamically to WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span> <span data-ttu-id="b2b33-105">此提供者會取代 [格式化的效能 Data Provider](formatted-performance-data-provider.md)（也稱為「處理後計數器提供者」）和 [效能計數器提供者](performance-counter-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="b2b33-105">This provider replaces the [Formatted Performance Data Provider](formatted-performance-data-provider.md), also known as the "Cooked Counter Provider", and the [Performance Counter Provider](performance-counter-provider.md).</span></span>

<span data-ttu-id="b2b33-106">WmiPerfInst 提供者會提供資料給 [WMIPerfClass](wmiperfclass-provider.md) 提供者所提供的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="b2b33-106">The WmiPerfInst provider supplies data to the WMI classes that are provided by the [WMIPerfClass](wmiperfclass-provider.md) provider.</span></span> <span data-ttu-id="b2b33-107">此提供者是效能資料協助程式 (PDH) 實例與 WmiPerfClass 提供者所提供之 WMI 效能類別之間的橋樑。</span><span class="sxs-lookup"><span data-stu-id="b2b33-107">This provider is a bridge between Performance Data Helper (PDH) instances and the WMI performance classes supplied by the WmiPerfClass Provider.</span></span> <span data-ttu-id="b2b33-108">當 WmiPerfInst 收到資料的查詢時，它會載入類別，並使用類別和屬性 [限定詞](qualifiers-specific-to-wmi-performance-classes.md) 來找出 PDH 實例。</span><span class="sxs-lookup"><span data-stu-id="b2b33-108">When WmiPerfInst receives a query for data, it loads the class and uses the class and property [qualifiers](qualifiers-specific-to-wmi-performance-classes.md) to locate the PDH instances.</span></span> <span data-ttu-id="b2b33-109">如需詳細資訊，請參閱 [使用 PDH 函數來使用計數器資料](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)。</span><span class="sxs-lookup"><span data-stu-id="b2b33-109">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

<span data-ttu-id="b2b33-110">不建議您藉由建立 WMI 高效能提供者來開發新的效能物件，並相依于 [*ADAP 反向介面卡*](gloss-r.md) 程式以將資料傳輸至效能程式庫。</span><span class="sxs-lookup"><span data-stu-id="b2b33-110">It is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries.</span></span> <span data-ttu-id="b2b33-111">例外狀況是當您正在開發 Windows Driver Model 的驅動程式，而且想要提供效能資料時。</span><span class="sxs-lookup"><span data-stu-id="b2b33-111">The exception is when you are developing a Windows Driver Model driver and want to supply performance data.</span></span> <span data-ttu-id="b2b33-112">雖然反向介面卡程式會繼續運作以提供回溯相容性，但建議的方法是使用 [效能計數器6.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="b2b33-112">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="b2b33-113">此提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例名稱為 "WmiPerfInst"。</span><span class="sxs-lookup"><span data-stu-id="b2b33-113">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfInst".</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2b33-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2b33-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2b33-115">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="b2b33-115">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="b2b33-116">效能程式庫和 WMI</span><span class="sxs-lookup"><span data-stu-id="b2b33-116">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="b2b33-117">監視效能資料</span><span class="sxs-lookup"><span data-stu-id="b2b33-117">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
