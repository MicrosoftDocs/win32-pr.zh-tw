---
description: 列出監視器描述項中影片監視器支援的來源模式（如果有的話）。
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: WmiMonitorListedSupportedSourceModes 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988265"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a><span data-ttu-id="19615-103">WmiMonitorListedSupportedSourceModes 類別</span><span class="sxs-lookup"><span data-stu-id="19615-103">WmiMonitorListedSupportedSourceModes class</span></span>

<span data-ttu-id="19615-104">**WmiMonitorListedSupportedSourceModes** 會在其監視描述項中列出影片監視器支援的來源模式（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="19615-104">The **WmiMonitorListedSupportedSourceModes** lists the supported source modes for a video monitor in its monitor descriptor, if any exist.</span></span> <span data-ttu-id="19615-105">針對沒有描述的監視器，此模式清單會根據監視器匯流排驅動程式所指定的監視器類型來產生。</span><span class="sxs-lookup"><span data-stu-id="19615-105">For monitors that have no description, this list of modes is generated based on the type of monitor, as specified by the monitor bus driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="19615-106">語法</span><span class="sxs-lookup"><span data-stu-id="19615-106">Syntax</span></span>

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a><span data-ttu-id="19615-107">成員</span><span class="sxs-lookup"><span data-stu-id="19615-107">Members</span></span>

<span data-ttu-id="19615-108">**WmiMonitorListedSupportedSourceModes** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="19615-108">The **WmiMonitorListedSupportedSourceModes** class has these types of members:</span></span>

-   [<span data-ttu-id="19615-109">屬性</span><span class="sxs-lookup"><span data-stu-id="19615-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19615-110">屬性</span><span class="sxs-lookup"><span data-stu-id="19615-110">Properties</span></span>

<span data-ttu-id="19615-111">**WmiMonitorListedSupportedSourceModes** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="19615-111">The **WmiMonitorListedSupportedSourceModes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19615-112">**使用中**</span><span class="sxs-lookup"><span data-stu-id="19615-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19615-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="19615-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19615-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19615-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19615-115">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="19615-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="19615-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="19615-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19615-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19615-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19615-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19615-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19615-119">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="19615-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="19615-120">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="19615-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="19615-121">**MonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="19615-121">**MonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19615-122">資料類型： **VideoModeDescriptor** 陣列</span><span class="sxs-lookup"><span data-stu-id="19615-122">Data type: **VideoModeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="19615-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19615-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19615-124">列出 [**VideoModeDescriptor**](videomodedescriptor.md) 類別的實例所代表的監視器來源模式。</span><span class="sxs-lookup"><span data-stu-id="19615-124">Lists monitor source modes represented by instances of the [**VideoModeDescriptor**](videomodedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="19615-125">**NumOfMonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="19615-125">**NumOfMonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19615-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="19615-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19615-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19615-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19615-128">所列支援的監視器來源模式數目。</span><span class="sxs-lookup"><span data-stu-id="19615-128">Number of listed supported monitor source mode.</span></span>

</dd> <dt>

<span data-ttu-id="19615-129">**PreferredMonitorSourceModeIndex**</span><span class="sxs-lookup"><span data-stu-id="19615-129">**PreferredMonitorSourceModeIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19615-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="19615-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="19615-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19615-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19615-132">慣用的監視器來源模式索引。</span><span class="sxs-lookup"><span data-stu-id="19615-132">Preferred monitor source mode index.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19615-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="19615-133">Requirements</span></span>



| <span data-ttu-id="19615-134">需求</span><span class="sxs-lookup"><span data-stu-id="19615-134">Requirement</span></span> | <span data-ttu-id="19615-135">值</span><span class="sxs-lookup"><span data-stu-id="19615-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19615-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19615-136">Minimum supported client</span></span><br/> | <span data-ttu-id="19615-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19615-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="19615-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19615-138">Minimum supported server</span></span><br/> | <span data-ttu-id="19615-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19615-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="19615-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="19615-140">Namespace</span></span><br/>                | <span data-ttu-id="19615-141">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="19615-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="19615-142">MOF</span><span class="sxs-lookup"><span data-stu-id="19615-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19615-143"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="19615-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="19615-144">DLL</span><span class="sxs-lookup"><span data-stu-id="19615-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19615-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19615-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19615-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19615-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19615-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="19615-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




