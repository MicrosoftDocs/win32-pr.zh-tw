---
description: 表示處理重複事件的事件種類類別。
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: ObHandleDuplicateEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973716"
---
# <a name="obhandleduplicateevent-class"></a><span data-ttu-id="89208-103">ObHandleDuplicateEvent 類別</span><span class="sxs-lookup"><span data-stu-id="89208-103">ObHandleDuplicateEvent class</span></span>

<span data-ttu-id="89208-104">表示處理重複事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="89208-104">Represents the event type class for handle duplication events.</span></span>

<span data-ttu-id="89208-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="89208-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89208-106">語法</span><span class="sxs-lookup"><span data-stu-id="89208-106">Syntax</span></span>

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a><span data-ttu-id="89208-107">成員</span><span class="sxs-lookup"><span data-stu-id="89208-107">Members</span></span>

<span data-ttu-id="89208-108">**ObHandleDuplicateEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="89208-108">The **ObHandleDuplicateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="89208-109">屬性</span><span class="sxs-lookup"><span data-stu-id="89208-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89208-110">屬性</span><span class="sxs-lookup"><span data-stu-id="89208-110">Properties</span></span>

<span data-ttu-id="89208-111">**ObHandleDuplicateEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="89208-111">The **ObHandleDuplicateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89208-112">**Object**</span><span class="sxs-lookup"><span data-stu-id="89208-112">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89208-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="89208-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89208-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89208-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89208-115">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**指標**](event-tracing-mof-qualifiers.md)， [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) </span><span class="sxs-lookup"><span data-stu-id="89208-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="89208-116">物件。</span><span class="sxs-lookup"><span data-stu-id="89208-116">The object.</span></span>

</dd> <dt>

<span data-ttu-id="89208-117">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="89208-117">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89208-118">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89208-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89208-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89208-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89208-120">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (5) </span><span class="sxs-lookup"><span data-stu-id="89208-120">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="89208-121">物件類型。</span><span class="sxs-lookup"><span data-stu-id="89208-121">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="89208-122">**SourceHandle**</span><span class="sxs-lookup"><span data-stu-id="89208-122">**SourceHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89208-123">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="89208-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89208-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89208-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89208-125">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) </span><span class="sxs-lookup"><span data-stu-id="89208-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="89208-126">來源物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="89208-126">The handle of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="89208-127">**TargetHandle**</span><span class="sxs-lookup"><span data-stu-id="89208-127">**TargetHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89208-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="89208-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89208-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89208-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89208-130">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) </span><span class="sxs-lookup"><span data-stu-id="89208-130">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="89208-131">目標物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="89208-131">The handle of the target object.</span></span>

</dd> <dt>

<span data-ttu-id="89208-132">**TargetProcessId**</span><span class="sxs-lookup"><span data-stu-id="89208-132">**TargetProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89208-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="89208-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89208-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89208-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89208-135">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) </span><span class="sxs-lookup"><span data-stu-id="89208-135">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="89208-136">目標的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="89208-136">The process identifier of the target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89208-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="89208-137">Requirements</span></span>



| <span data-ttu-id="89208-138">需求</span><span class="sxs-lookup"><span data-stu-id="89208-138">Requirement</span></span> | <span data-ttu-id="89208-139">值</span><span class="sxs-lookup"><span data-stu-id="89208-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89208-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89208-140">Minimum supported client</span></span><br/> | <span data-ttu-id="89208-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89208-141">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="89208-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89208-142">Minimum supported server</span></span><br/> | <span data-ttu-id="89208-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89208-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="89208-144">MOF</span><span class="sxs-lookup"><span data-stu-id="89208-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89208-145"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="89208-145"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




