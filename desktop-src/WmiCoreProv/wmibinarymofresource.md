---
description: WDM 類別提供者會定義 \\ 根 wmi 命名空間中的 WMIBinaryMofResource 類別 \\ ，以支援追蹤 wmi 儲存機制中資料狀態的工作。
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: WMIBinaryMofResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848397"
---
# <a name="wmibinarymofresource-class"></a><span data-ttu-id="ac4c1-103">WMIBinaryMofResource 類別</span><span class="sxs-lookup"><span data-stu-id="ac4c1-103">WMIBinaryMofResource class</span></span>

<span data-ttu-id="ac4c1-104">WDM 類別提供者會定義 \\ 根 wmi 命名空間中的 WMIBinaryMofResource 類別 \\ ，以支援追蹤 wmi 儲存機制中資料狀態的工作。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-104">The WDM class provider defines the **WMIBinaryMofResource** class in the \\root\\wmi namespace to support the task of keeping track of the status of data in the WMI repository.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac4c1-105">Syntax</span></span>

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="ac4c1-106">成員</span><span class="sxs-lookup"><span data-stu-id="ac4c1-106">Members</span></span>

<span data-ttu-id="ac4c1-107">**WMIBinaryMofResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ac4c1-107">The **WMIBinaryMofResource** class has these types of members:</span></span>

-   [<span data-ttu-id="ac4c1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ac4c1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac4c1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ac4c1-109">Properties</span></span>

<span data-ttu-id="ac4c1-110">**WMIBinaryMofResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-110">The **WMIBinaryMofResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac4c1-111">**HighDateTime**</span><span class="sxs-lookup"><span data-stu-id="ac4c1-111">**HighDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac4c1-112">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ac4c1-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac4c1-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac4c1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac4c1-114">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ac4c1-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ac4c1-115">高一半的日期時間戳記。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-115">High half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="ac4c1-116">**LowDateTime**</span><span class="sxs-lookup"><span data-stu-id="ac4c1-116">**LowDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac4c1-117">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ac4c1-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac4c1-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac4c1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac4c1-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ac4c1-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ac4c1-120">日期時間戳記的下半部。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-120">Low half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="ac4c1-121">**MofProcessed**</span><span class="sxs-lookup"><span data-stu-id="ac4c1-121">**MofProcessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac4c1-122">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ac4c1-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac4c1-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac4c1-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ac4c1-124">指出是否已完整處理 mof 檔案的旗標。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-124">Flag indicating whether the .mof file was fully processed.</span></span>

</dd> <dt>

<span data-ttu-id="ac4c1-125">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ac4c1-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac4c1-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac4c1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac4c1-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac4c1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac4c1-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ac4c1-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ac4c1-129">已啟用 WDM 的驅動程式名稱，此驅動程式在 WMI 儲存機制中已成功編譯二進位 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-129">Name of the WDM enabled driver that has a binary MOF file successfully compiled in the WMI repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac4c1-130">備註</span><span class="sxs-lookup"><span data-stu-id="ac4c1-130">Remarks</span></span>

<span data-ttu-id="ac4c1-131">WDM 類別提供者會為每個提供二進位 MOF 檔案的 WDM 驅動程式建立 **WMIBinaryMofResource** 的實例。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-131">The WDM class provider creates an instance of **WMIBinaryMofResource** for each WDM driver that supplies a binary MOF file.</span></span>

<span data-ttu-id="ac4c1-132">每當 WMI 初始化提供者時，提供者會將時間戳記與驅動程式影像檔的時間戳記進行比較。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-132">Whenever WMI initializes the provider, the provider compares the timestamp with the timestamp of the driver image file.</span></span> <span data-ttu-id="ac4c1-133">如果時間戳記不同，WMI 會重新編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="ac4c1-133">If the timestamps differ, WMI re-compiles the MOF file.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac4c1-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac4c1-134">Requirements</span></span>



| <span data-ttu-id="ac4c1-135">需求</span><span class="sxs-lookup"><span data-stu-id="ac4c1-135">Requirement</span></span> | <span data-ttu-id="ac4c1-136">值</span><span class="sxs-lookup"><span data-stu-id="ac4c1-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4c1-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac4c1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ac4c1-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac4c1-138">Windows XP</span></span><br/>                                                              |
| <span data-ttu-id="ac4c1-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac4c1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ac4c1-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ac4c1-140">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="ac4c1-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac4c1-141">Namespace</span></span><br/>                | <span data-ttu-id="ac4c1-142">根 \\ WMI</span><span class="sxs-lookup"><span data-stu-id="ac4c1-142">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="ac4c1-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ac4c1-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac4c1-144"><dt>Wmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac4c1-144"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac4c1-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac4c1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4c1-146">WDM 提供者</span><span class="sxs-lookup"><span data-stu-id="ac4c1-146">WDM Provider</span></span>](wdm-provider.md)
</dt> </dl>

 

