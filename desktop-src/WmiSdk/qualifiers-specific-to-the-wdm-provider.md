---
description: 當從 WNODEs 中解壓縮資料以產生 WDM 驅動程式類別的實例時，設備磁碟機 MOF 檔案中的 WDM 提供者會使用下列限定詞。
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: WDM 提供者專用的限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993010"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a><span data-ttu-id="45733-103">WDM 提供者專用的限定詞</span><span class="sxs-lookup"><span data-stu-id="45733-103">Qualifiers Specific to the WDM Provider</span></span>

<span data-ttu-id="45733-104">當從 WNODEs 中解壓縮資料以產生 WDM 驅動程式類別的實例時，設備磁碟機 MOF 檔案中的 [WDM 提供者](/windows/desktop/WmiCoreProv/wdm-provider) 會使用下列限定詞。</span><span class="sxs-lookup"><span data-stu-id="45733-104">The following qualifiers are used by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) in device driver MOF files when they are extracting data from WNODEs to generate instances of WDM driver classes.</span></span>

<dt>

<span data-ttu-id="45733-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span><span class="sxs-lookup"><span data-stu-id="45733-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span></span>
</dt> <dd>

<span data-ttu-id="45733-106">資料類型： **DWORD、array、uint8、uint16、uint32、sint8、sint16 或 sint32。**</span><span class="sxs-lookup"><span data-stu-id="45733-106">Data type: **DWORD, array, uint8, uint16, uint32, sint8, sint16, or sint32.**</span></span>

<span data-ttu-id="45733-107">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="45733-107">Applies to: properties</span></span>

<span data-ttu-id="45733-108">這個屬性的遺漏值應該以 **Null** 表示，而不是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="45733-108">A missing value for this property should be represented by **NULL** rather than 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="45733-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span><span class="sxs-lookup"><span data-stu-id="45733-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span></span>
</dt> <dd>

<span data-ttu-id="45733-110">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="45733-110">Data type: **uint32**</span></span>

<span data-ttu-id="45733-111">適用物件：屬性</span><span class="sxs-lookup"><span data-stu-id="45733-111">Applies to: properties</span></span>

<span data-ttu-id="45733-112">屬性之資料 WNODE 中的索引。</span><span class="sxs-lookup"><span data-stu-id="45733-112">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="45733-113">WDM 提供者會使用此辨識符號來決定從 WNODE 中解壓縮資料並產生 WMI 類別時，如何格式化資料。</span><span class="sxs-lookup"><span data-stu-id="45733-113">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="45733-114">起始值為1。</span><span class="sxs-lookup"><span data-stu-id="45733-114">The starting value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="45733-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span><span class="sxs-lookup"><span data-stu-id="45733-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span></span>
</dt> <dd>

<span data-ttu-id="45733-116">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="45733-116">Data type: **uint32**</span></span>

<span data-ttu-id="45733-117">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="45733-117">Applies to: classes</span></span>

<span data-ttu-id="45733-118">指出存取資料區塊的資源成本。</span><span class="sxs-lookup"><span data-stu-id="45733-118">Indication of the resource cost to access the data block.</span></span> <span data-ttu-id="45733-119">例如，磁片幾何資訊不需要大量資源，因為它可在裝置延伸模組中取得。</span><span class="sxs-lookup"><span data-stu-id="45733-119">For example, disk geometry information does not require a lot of resources to obtain because it is available in the device extension.</span></span> <span data-ttu-id="45733-120">磁片讀取/寫入效能較需要大量資源，因為它需要對每個讀取/寫入作業進行額外的工作。</span><span class="sxs-lookup"><span data-stu-id="45733-120">Disk read/write performance is more resource-intensive because it requires extra work on each read/write operation.</span></span> <span data-ttu-id="45733-121">因此， **WMIExpense** 限定詞值會大於磁片讀取/寫入效能。</span><span class="sxs-lookup"><span data-stu-id="45733-121">Therefore, the **WMIExpense** qualifier value is larger for disk read/write performance.</span></span>

</dd> <dt>

<span data-ttu-id="45733-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span><span class="sxs-lookup"><span data-stu-id="45733-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span></span>
</dt> <dd>

<span data-ttu-id="45733-123">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="45733-123">Data type: **uint32**</span></span>

<span data-ttu-id="45733-124">適用于：方法</span><span class="sxs-lookup"><span data-stu-id="45733-124">Applies to: methods</span></span>

<span data-ttu-id="45733-125">屬性之資料 WNODE 中的索引。</span><span class="sxs-lookup"><span data-stu-id="45733-125">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="45733-126">WDM 提供者會使用此辨識符號來決定從 WNODE 中解壓縮資料並產生 WMI 類別時，如何格式化資料。</span><span class="sxs-lookup"><span data-stu-id="45733-126">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="45733-127">起始值為1。</span><span class="sxs-lookup"><span data-stu-id="45733-127">The starting value is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45733-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="45733-128">Requirements</span></span>



| <span data-ttu-id="45733-129">需求</span><span class="sxs-lookup"><span data-stu-id="45733-129">Requirement</span></span> | <span data-ttu-id="45733-130">值</span><span class="sxs-lookup"><span data-stu-id="45733-130">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="45733-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45733-131">Minimum supported client</span></span><br/> | <span data-ttu-id="45733-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45733-132">Windows Vista</span></span><br/>       |
| <span data-ttu-id="45733-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45733-133">Minimum supported server</span></span><br/> | <span data-ttu-id="45733-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45733-134">Windows Server 2008</span></span><br/> |



 

