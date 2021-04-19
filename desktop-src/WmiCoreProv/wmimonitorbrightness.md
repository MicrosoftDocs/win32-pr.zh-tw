---
description: 代表電腦監視器的亮度參數。
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: WmiMonitorBrightness 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983870"
---
# <a name="wmimonitorbrightness-class"></a><span data-ttu-id="10798-103">WmiMonitorBrightness 類別</span><span class="sxs-lookup"><span data-stu-id="10798-103">WmiMonitorBrightness class</span></span>

<span data-ttu-id="10798-104">**WmiMonitorBrightness** WMI 類別代表電腦監視器的亮度參數。</span><span class="sxs-lookup"><span data-stu-id="10798-104">The **WmiMonitorBrightness** WMI class represents the brightness parameters of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="10798-105">語法</span><span class="sxs-lookup"><span data-stu-id="10798-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a><span data-ttu-id="10798-106">成員</span><span class="sxs-lookup"><span data-stu-id="10798-106">Members</span></span>

<span data-ttu-id="10798-107">**WmiMonitorBrightness** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="10798-107">The **WmiMonitorBrightness** class has these types of members:</span></span>

-   [<span data-ttu-id="10798-108">屬性</span><span class="sxs-lookup"><span data-stu-id="10798-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10798-109">屬性</span><span class="sxs-lookup"><span data-stu-id="10798-109">Properties</span></span>

<span data-ttu-id="10798-110">**WmiMonitorBrightness** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="10798-110">The **WmiMonitorBrightness** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10798-111">**使用中**</span><span class="sxs-lookup"><span data-stu-id="10798-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10798-112">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10798-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10798-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10798-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10798-114">指出目標監視器是否為作用中。</span><span class="sxs-lookup"><span data-stu-id="10798-114">Indicates if the target monitor is active.</span></span>

</dd> <dt>

<span data-ttu-id="10798-115">**CurrentBrightness**</span><span class="sxs-lookup"><span data-stu-id="10798-115">**CurrentBrightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10798-116">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="10798-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="10798-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10798-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10798-118">目前的亮度。</span><span class="sxs-lookup"><span data-stu-id="10798-118">Current brightness.</span></span> <span data-ttu-id="10798-119">此值必須是從 *層級* 取得的值。</span><span class="sxs-lookup"><span data-stu-id="10798-119">This value must be a value taken from *Levels*.</span></span>

<span data-ttu-id="10798-120">範例: 100</span><span class="sxs-lookup"><span data-stu-id="10798-120">Example: 100</span></span>

</dd> <dt>

<span data-ttu-id="10798-121">InstanceName</span><span class="sxs-lookup"><span data-stu-id="10798-121">InstanceName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10798-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10798-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10798-123">限定詞：索引鍵</span><span class="sxs-lookup"><span data-stu-id="10798-123">Qualifiers: Key</span></span>
</dt> </dl>

<span data-ttu-id="10798-124">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="10798-124">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="10798-125">**Level**</span><span class="sxs-lookup"><span data-stu-id="10798-125">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10798-126">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="10798-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="10798-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10798-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10798-128">包含可能的亮度層級的陣列。</span><span class="sxs-lookup"><span data-stu-id="10798-128">Array containing the possible brightness levels.</span></span>

<span data-ttu-id="10798-129">範例： \[ 0，1，2，...，100 \] 。</span><span class="sxs-lookup"><span data-stu-id="10798-129">Example: \[0, 1, 2, ..., 100\].</span></span>

</dd> <dt>

<span data-ttu-id="10798-130">**層級**</span><span class="sxs-lookup"><span data-stu-id="10798-130">**Levels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10798-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10798-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10798-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10798-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10798-133">監視器支援的亮度等級總數，如 *層級* 所述。</span><span class="sxs-lookup"><span data-stu-id="10798-133">The total number of brightness levels the monitor supports, as described in *Level*.</span></span>

<span data-ttu-id="10798-134">範例：101</span><span class="sxs-lookup"><span data-stu-id="10798-134">Example: 101</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="10798-135">範例</span><span class="sxs-lookup"><span data-stu-id="10798-135">Examples</span></span>

<span data-ttu-id="10798-136">如需在 PowerShell 中使用此類別的詳細資訊和程式碼範例，請參閱 [使用 Powershell 報告和設定監視亮度](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx)。</span><span class="sxs-lookup"><span data-stu-id="10798-136">For more information and code samples on using this class in PowerShell, see [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="10798-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="10798-137">Requirements</span></span>



| <span data-ttu-id="10798-138">需求</span><span class="sxs-lookup"><span data-stu-id="10798-138">Requirement</span></span> | <span data-ttu-id="10798-139">值</span><span class="sxs-lookup"><span data-stu-id="10798-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10798-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10798-140">Minimum supported client</span></span><br/> | <span data-ttu-id="10798-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10798-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="10798-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10798-142">Minimum supported server</span></span><br/> | <span data-ttu-id="10798-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10798-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="10798-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="10798-144">Namespace</span></span><br/>                | <span data-ttu-id="10798-145">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="10798-145">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="10798-146">MOF</span><span class="sxs-lookup"><span data-stu-id="10798-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10798-147"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="10798-147"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="10798-148">DLL</span><span class="sxs-lookup"><span data-stu-id="10798-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10798-149"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10798-149"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10798-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10798-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10798-151">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="10798-151">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




