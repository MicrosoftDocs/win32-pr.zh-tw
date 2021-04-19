---
description: 列出監視器所支援的頻率範圍。
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: WmiMonitorListedFrequencyRanges 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976967"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a><span data-ttu-id="7e046-103">WmiMonitorListedFrequencyRanges 類別</span><span class="sxs-lookup"><span data-stu-id="7e046-103">WmiMonitorListedFrequencyRanges class</span></span>

<span data-ttu-id="7e046-104">**WmiMonitorListedFrequencyRanges** WMI 類別會列出監視器所支援的頻率範圍。</span><span class="sxs-lookup"><span data-stu-id="7e046-104">The **WmiMonitorListedFrequencyRanges** WMI class lists the frequency ranges supported by the monitor.</span></span> <span data-ttu-id="7e046-105">您可以在視頻電子郵件標準關聯的影片輸入定義中找到這些範圍 (VESA) 增強的擴充顯示器識別資料 (E EDID) 區塊，或包含設備磁碟機資料的 Windows INF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="7e046-105">These ranges are found in Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) block or in the Windows INF file that contains device driver data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e046-106">語法</span><span class="sxs-lookup"><span data-stu-id="7e046-106">Syntax</span></span>

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a><span data-ttu-id="7e046-107">成員</span><span class="sxs-lookup"><span data-stu-id="7e046-107">Members</span></span>

<span data-ttu-id="7e046-108">**WmiMonitorListedFrequencyRanges** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7e046-108">The **WmiMonitorListedFrequencyRanges** class has these types of members:</span></span>

-   [<span data-ttu-id="7e046-109">屬性</span><span class="sxs-lookup"><span data-stu-id="7e046-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e046-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7e046-110">Properties</span></span>

<span data-ttu-id="7e046-111">**WmiMonitorListedFrequencyRanges** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7e046-111">The **WmiMonitorListedFrequencyRanges** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e046-112">**使用中**</span><span class="sxs-lookup"><span data-stu-id="7e046-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e046-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7e046-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e046-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e046-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e046-115">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="7e046-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7e046-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="7e046-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e046-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7e046-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e046-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e046-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e046-119">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="7e046-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7e046-120">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e046-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="7e046-121">**MonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="7e046-121">**MonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e046-122">資料類型： **FrequencyRangeDescriptor** 陣列</span><span class="sxs-lookup"><span data-stu-id="7e046-122">Data type: **FrequencyRangeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="7e046-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e046-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e046-124">由 [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) 類別的實例所表示的監視器頻率範圍清單。</span><span class="sxs-lookup"><span data-stu-id="7e046-124">List of monitor frequency ranges represented by instances of the [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7e046-125">**NumOfMonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="7e046-125">**NumOfMonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e046-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7e046-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e046-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7e046-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e046-128">所列支援的監視器頻率範圍數目。</span><span class="sxs-lookup"><span data-stu-id="7e046-128">Number of listed supported monitor frequency ranges.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e046-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e046-129">Requirements</span></span>



| <span data-ttu-id="7e046-130">需求</span><span class="sxs-lookup"><span data-stu-id="7e046-130">Requirement</span></span> | <span data-ttu-id="7e046-131">值</span><span class="sxs-lookup"><span data-stu-id="7e046-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e046-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e046-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7e046-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e046-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7e046-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e046-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7e046-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e046-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7e046-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="7e046-136">Namespace</span></span><br/>                | <span data-ttu-id="7e046-137">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="7e046-137">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7e046-138">MOF</span><span class="sxs-lookup"><span data-stu-id="7e046-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e046-139"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e046-139"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e046-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7e046-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e046-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e046-141"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e046-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e046-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e046-143">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="7e046-143">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




