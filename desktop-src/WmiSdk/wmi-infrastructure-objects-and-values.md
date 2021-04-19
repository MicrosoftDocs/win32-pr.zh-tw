---
description: Wmi 辨識符號、受控物件格式 (MOF) 語法、效能計數器類型，以及 WMI 提供者、腳本和應用程式所使用之其他資料的相關資訊。
ms.assetid: 7f0e3ebb-ba10-4cf0-86a9-5fdec5ffc383
ms.tgt_platform: multiple
title: WMI 基礎結構物件和值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b39ac726a45b95a667a865ac26e0be937ff445
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979059"
---
# <a name="wmi-infrastructure-objects-and-values"></a><span data-ttu-id="e5b57-103">WMI 基礎結構物件和值</span><span class="sxs-lookup"><span data-stu-id="e5b57-103">WMI Infrastructure Objects and Values</span></span>

<span data-ttu-id="e5b57-104">本節包含 WMI 辨識符號、[*受控物件格式*](gloss-m.md) (MOF) 語法、效能計數器類型，[*以及 wmi 提供*](gloss-q.md)者、腳本和應用程式所使用之其他資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5b57-104">This section includes information about WMI [*qualifiers*](gloss-q.md), [*Managed Object Format*](gloss-m.md) (MOF) syntax, performance counter types, and other data used by WMI providers, scripts, and applications.</span></span>

<dl> <dt>

<span data-ttu-id="e5b57-105"><span id="CIMTYPE_ENUMERATION"></span><span id="cimtype_enumeration"></span>[**CIMTYPE \_ 列舉**](/windows/win32/api/wbemcli/ne-wbemcli-cimtype_enumeration)</span><span class="sxs-lookup"><span data-stu-id="e5b57-105"><span id="CIMTYPE_ENUMERATION"></span><span id="cimtype_enumeration"></span>[**CIMTYPE\_ENUMERATION**](/windows/win32/api/wbemcli/ne-wbemcli-cimtype_enumeration)</span></span>
</dt> <dd>

<span data-ttu-id="e5b57-106">定義指定不同 CIM 資料類型的值。</span><span class="sxs-lookup"><span data-stu-id="e5b57-106">Defines values that specify different CIM data types.</span></span>

</dd> <dt>

<span data-ttu-id="e5b57-107"><span id="MOF_Data_Types"></span><span id="mof_data_types"></span><span id="MOF_DATA_TYPES"></span>[MOF 資料類型](mof-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="e5b57-107"><span id="MOF_Data_Types"></span><span id="mof_data_types"></span><span id="MOF_DATA_TYPES"></span>[MOF Data Types](mof-data-types.md)</span></span>
</dt> <dd>

<span data-ttu-id="e5b57-108">MOF 語言所支援的資料類型清單。</span><span class="sxs-lookup"><span data-stu-id="e5b57-108">A list of data types supported by the MOF language.</span></span>

</dd> <dt>

<span data-ttu-id="e5b57-109"><span id="WMI_Events"></span><span id="wmi_events"></span><span id="WMI_EVENTS"></span>[**WMI 事件**](wmi-events.md)</span><span class="sxs-lookup"><span data-stu-id="e5b57-109"><span id="WMI_Events"></span><span id="wmi_events"></span><span id="WMI_EVENTS"></span>[**WMI Events**](wmi-events.md)</span></span>
</dt> <dd>

<span data-ttu-id="e5b57-110">WMI 寫入至記錄檔的訊息清單。</span><span class="sxs-lookup"><span data-stu-id="e5b57-110">A list of messages WMI writes to logs.</span></span>

</dd> <dt>

<span data-ttu-id="e5b57-111"><span id="WMI_Performance_Counter_Types"></span><span id="wmi_performance_counter_types"></span><span id="WMI_PERFORMANCE_COUNTER_TYPES"></span>[WMI 效能計數器類型](wmi-performance-counter-types.md)</span><span class="sxs-lookup"><span data-stu-id="e5b57-111"><span id="WMI_Performance_Counter_Types"></span><span id="wmi_performance_counter_types"></span><span id="WMI_PERFORMANCE_COUNTER_TYPES"></span>[WMI Performance Counter Types](wmi-performance-counter-types.md)</span></span>
</dt> <dd>

<span data-ttu-id="e5b57-112">計數器類型的清單，指定取得計算的效能計數器所需的公式。</span><span class="sxs-lookup"><span data-stu-id="e5b57-112">A list of counter types that designate the formulas required to obtain calculated performance counters.</span></span>

</dd> <dt>

<span data-ttu-id="e5b57-113"><span id="WMI_Qualifiers"></span><span id="wmi_qualifiers"></span><span id="WMI_QUALIFIERS"></span>[WMI 限定詞](wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e5b57-113"><span id="WMI_Qualifiers"></span><span id="wmi_qualifiers"></span><span id="WMI_QUALIFIERS"></span>[WMI Qualifiers](wmi-qualifiers.md)</span></span>
</dt> <dd>

<span data-ttu-id="e5b57-114">WMI 所支援的 [*限定詞*](gloss-q.md) 清單。</span><span class="sxs-lookup"><span data-stu-id="e5b57-114">A list of the [*qualifiers*](gloss-q.md) supported by WMI.</span></span>

</dd> <dt>

<span data-ttu-id="e5b57-115"><span id="WMI_Return_Codes"></span><span id="wmi_return_codes"></span><span id="WMI_RETURN_CODES"></span>[WMI 傳回碼](wmi-return-codes.md)</span><span class="sxs-lookup"><span data-stu-id="e5b57-115"><span id="WMI_Return_Codes"></span><span id="wmi_return_codes"></span><span id="WMI_RETURN_CODES"></span>[WMI Return Codes](wmi-return-codes.md)</span></span>
</dt> <dd>

<span data-ttu-id="e5b57-116">以 **HRESULT** 的 WMI 傳回的符號常數、常值和描述的清單。</span><span class="sxs-lookup"><span data-stu-id="e5b57-116">A list of the symbolic constants, literal values, and descriptions returned by WMI in **HRESULT**.</span></span>

</dd> <dt>

<span data-ttu-id="e5b57-117"><span id="WMI_Security"></span><span id="wmi_security"></span><span id="WMI_SECURITY"></span>[WMI 安全性](wmi-security.md)</span><span class="sxs-lookup"><span data-stu-id="e5b57-117"><span id="WMI_Security"></span><span id="wmi_security"></span><span id="WMI_SECURITY"></span>[WMI Security](wmi-security.md)</span></span>
</dt> <dd>

<span data-ttu-id="e5b57-118">在用於操作安全描述項或許可權的方法中，用於安全描述項和常數的物件清單。</span><span class="sxs-lookup"><span data-stu-id="e5b57-118">A list of objects used in security descriptors and constants used in methods that manipulate security descriptors or privileges.</span></span>

</dd> <dt>

<span data-ttu-id="e5b57-119"><span id="WMI_System_Properties"></span><span id="wmi_system_properties"></span><span id="WMI_SYSTEM_PROPERTIES"></span>[WMI 系統屬性](wmi-system-properties.md)</span><span class="sxs-lookup"><span data-stu-id="e5b57-119"><span id="WMI_System_Properties"></span><span id="wmi_system_properties"></span><span id="WMI_SYSTEM_PROPERTIES"></span>[WMI System Properties](wmi-system-properties.md)</span></span>
</dt> <dd>

<span data-ttu-id="e5b57-120">用於 WMI 內部操作的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="e5b57-120">A list of properties used for the internal operations of WMI.</span></span> <span data-ttu-id="e5b57-121">類似于 WMI 系統類別，您可以辨識它們，因為名稱的開頭是雙底線 (\_ \_) 。</span><span class="sxs-lookup"><span data-stu-id="e5b57-121">Similar to the WMI system classes, you can recognize them because the name begins with a double underscore (\_\_).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="e5b57-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5b57-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5b57-123">WMI 參考</span><span class="sxs-lookup"><span data-stu-id="e5b57-123">WMI Reference</span></span>](wmi-reference.md)
</dt> </dl>

 

 



