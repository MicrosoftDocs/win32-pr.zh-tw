---
description: 這個類別是登錄事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Registry_V0_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9a72a0d6ddfe5e441b21dff4ba58fa3bb37457a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972188"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="d6331-104">Registry \_ V0 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="d6331-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="d6331-105">這個類別是登錄事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="d6331-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="d6331-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d6331-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6331-107">語法</span><span class="sxs-lookup"><span data-stu-id="d6331-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="d6331-108">成員</span><span class="sxs-lookup"><span data-stu-id="d6331-108">Members</span></span>

<span data-ttu-id="d6331-109">**Registry \_ V0 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d6331-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="d6331-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d6331-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6331-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d6331-111">Properties</span></span>

<span data-ttu-id="d6331-112">**Registry \_ V0 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d6331-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6331-113">經過時間</span><span class="sxs-lookup"><span data-stu-id="d6331-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6331-114">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="d6331-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="d6331-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6331-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6331-116">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="d6331-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="d6331-117">登錄作業的經過時間。</span><span class="sxs-lookup"><span data-stu-id="d6331-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6331-118">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="d6331-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6331-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d6331-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6331-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6331-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6331-121">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="d6331-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d6331-122">登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6331-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="d6331-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="d6331-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6331-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d6331-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6331-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6331-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6331-126">限定詞： WmiDataId (4) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="d6331-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="d6331-127">登錄機碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6331-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="d6331-128">狀態</span><span class="sxs-lookup"><span data-stu-id="d6331-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6331-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d6331-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6331-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d6331-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6331-131">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="d6331-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d6331-132">登錄作業的 NTSTATUS 值。</span><span class="sxs-lookup"><span data-stu-id="d6331-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6331-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6331-133">Requirements</span></span>



| <span data-ttu-id="d6331-134">需求</span><span class="sxs-lookup"><span data-stu-id="d6331-134">Requirement</span></span> | <span data-ttu-id="d6331-135">值</span><span class="sxs-lookup"><span data-stu-id="d6331-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6331-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6331-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d6331-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6331-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d6331-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6331-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d6331-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6331-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6331-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6331-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6331-141">**登錄 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="d6331-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 




