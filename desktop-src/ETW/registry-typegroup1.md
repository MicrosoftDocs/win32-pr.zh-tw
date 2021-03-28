---
description: 這個類別是登錄事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Registry_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_TypeGroup1
- Registry_TypeGroup1.InitialTime
- Registry_TypeGroup1.Status
- Registry_TypeGroup1.Index
- Registry_TypeGroup1.KeyHandle
- Registry_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bfbf0157141473be4cc2460659912dc662ef7c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972280"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="5db80-104">登錄 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="5db80-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="5db80-105">這個類別是登錄事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="5db80-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="5db80-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="5db80-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db80-107">語法</span><span class="sxs-lookup"><span data-stu-id="5db80-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "KCBCreate", "KCBDelete", "KCBRundownBegin", "KCBRundownEnd", "Virtualize", "Close"}]
class Registry_TypeGroup1 : Registry
{
  sint64 InitialTime;
  uint32 Status;
  uint32 Index;
  uint32 KeyHandle;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="5db80-108">成員</span><span class="sxs-lookup"><span data-stu-id="5db80-108">Members</span></span>

<span data-ttu-id="5db80-109">登錄 **\_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5db80-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="5db80-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5db80-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5db80-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5db80-111">Properties</span></span>

<span data-ttu-id="5db80-112">登錄 **\_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5db80-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5db80-113">索引</span><span class="sxs-lookup"><span data-stu-id="5db80-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db80-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5db80-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5db80-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5db80-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5db80-116">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="5db80-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="5db80-117">登錄作業 (的子機碼索引，例如 EnumerateKey) 。</span><span class="sxs-lookup"><span data-stu-id="5db80-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="5db80-118">InitialTime</span><span class="sxs-lookup"><span data-stu-id="5db80-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db80-119">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="5db80-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="5db80-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5db80-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5db80-121">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="5db80-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="5db80-122">登錄操作的初始時間。</span><span class="sxs-lookup"><span data-stu-id="5db80-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="5db80-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="5db80-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db80-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5db80-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5db80-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5db80-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5db80-126">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="5db80-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5db80-127">登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5db80-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="5db80-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="5db80-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db80-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5db80-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5db80-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5db80-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5db80-131">限定詞： WmiDataId (5) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="5db80-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5db80-132">登錄機碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="5db80-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="5db80-133">狀態</span><span class="sxs-lookup"><span data-stu-id="5db80-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5db80-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5db80-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5db80-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5db80-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5db80-136">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="5db80-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5db80-137">登錄作業的 NTSTATUS 值。</span><span class="sxs-lookup"><span data-stu-id="5db80-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5db80-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="5db80-138">Requirements</span></span>



| <span data-ttu-id="5db80-139">需求</span><span class="sxs-lookup"><span data-stu-id="5db80-139">Requirement</span></span> | <span data-ttu-id="5db80-140">值</span><span class="sxs-lookup"><span data-stu-id="5db80-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5db80-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5db80-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5db80-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5db80-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5db80-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5db80-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5db80-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5db80-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5db80-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5db80-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db80-146">**登錄**</span><span class="sxs-lookup"><span data-stu-id="5db80-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 




