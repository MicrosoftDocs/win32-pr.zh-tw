---
description: 表示與資料收集開始和結束相關之物件控制碼事件的事件種類類別。
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: ObHandleRundownEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973432"
---
# <a name="obhandlerundownevent-class"></a><span data-ttu-id="17392-103">ObHandleRundownEvent 類別</span><span class="sxs-lookup"><span data-stu-id="17392-103">ObHandleRundownEvent class</span></span>

<span data-ttu-id="17392-104">表示與資料收集開始和結束相關之物件控制碼事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="17392-104">Represents the event type class for object handle events related to the beginning and end of data collection.</span></span> <span data-ttu-id="17392-105">此事件涉及在執行取消時列舉所有控制碼。</span><span class="sxs-lookup"><span data-stu-id="17392-105">This event involves the enumerating of all handles when rundown is performed.</span></span>

<span data-ttu-id="17392-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="17392-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17392-107">語法</span><span class="sxs-lookup"><span data-stu-id="17392-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="17392-108">成員</span><span class="sxs-lookup"><span data-stu-id="17392-108">Members</span></span>

<span data-ttu-id="17392-109">**ObHandleRundownEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="17392-109">The **ObHandleRundownEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="17392-110">屬性</span><span class="sxs-lookup"><span data-stu-id="17392-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17392-111">屬性</span><span class="sxs-lookup"><span data-stu-id="17392-111">Properties</span></span>

<span data-ttu-id="17392-112">**ObHandleRundownEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="17392-112">The **ObHandleRundownEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17392-113">**Handle**</span><span class="sxs-lookup"><span data-stu-id="17392-113">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17392-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="17392-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17392-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17392-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17392-116">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) </span><span class="sxs-lookup"><span data-stu-id="17392-116">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="17392-117">物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="17392-117">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="17392-118">**Object**</span><span class="sxs-lookup"><span data-stu-id="17392-118">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17392-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="17392-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17392-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17392-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17392-121">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**指標**](event-tracing-mof-qualifiers.md)， [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) </span><span class="sxs-lookup"><span data-stu-id="17392-121">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="17392-122">物件。</span><span class="sxs-lookup"><span data-stu-id="17392-122">The object.</span></span>

</dd> <dt>

<span data-ttu-id="17392-123">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="17392-123">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17392-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17392-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17392-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17392-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17392-126">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "w" ) 、 [**StringTermination**](event-tracing-mof-qualifiers.md) ( "NullTerminated" ) 、 [**WmiDataId**](event-tracing-mof-qualifiers.md) (5) </span><span class="sxs-lookup"><span data-stu-id="17392-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="17392-127">物件名稱。</span><span class="sxs-lookup"><span data-stu-id="17392-127">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="17392-128">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="17392-128">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17392-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="17392-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17392-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17392-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17392-131">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) </span><span class="sxs-lookup"><span data-stu-id="17392-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="17392-132">物件類型。</span><span class="sxs-lookup"><span data-stu-id="17392-132">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="17392-133">**進程**</span><span class="sxs-lookup"><span data-stu-id="17392-133">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17392-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="17392-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17392-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17392-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17392-136">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) </span><span class="sxs-lookup"><span data-stu-id="17392-136">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="17392-137">處理序識別項。</span><span class="sxs-lookup"><span data-stu-id="17392-137">The process identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17392-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="17392-138">Requirements</span></span>



| <span data-ttu-id="17392-139">需求</span><span class="sxs-lookup"><span data-stu-id="17392-139">Requirement</span></span> | <span data-ttu-id="17392-140">值</span><span class="sxs-lookup"><span data-stu-id="17392-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17392-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17392-141">Minimum supported client</span></span><br/> | <span data-ttu-id="17392-142">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17392-142">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="17392-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17392-143">Minimum supported server</span></span><br/> | <span data-ttu-id="17392-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17392-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="17392-145">MOF</span><span class="sxs-lookup"><span data-stu-id="17392-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17392-146"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="17392-146"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




