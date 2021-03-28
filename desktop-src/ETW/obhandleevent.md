---
description: 表示處理建立或關閉事件的事件種類類別。
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: ObHandleEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae293684bd09322c7193035d374e5e2bad21447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973429"
---
# <a name="obhandleevent-class"></a><span data-ttu-id="4bdb1-103">ObHandleEvent 類別</span><span class="sxs-lookup"><span data-stu-id="4bdb1-103">ObHandleEvent class</span></span>

<span data-ttu-id="4bdb1-104">表示處理建立或關閉事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="4bdb1-104">Represents the event type class for handle creation or closure events.</span></span>

<span data-ttu-id="4bdb1-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4bdb1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bdb1-106">語法</span><span class="sxs-lookup"><span data-stu-id="4bdb1-106">Syntax</span></span>

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a><span data-ttu-id="4bdb1-107">成員</span><span class="sxs-lookup"><span data-stu-id="4bdb1-107">Members</span></span>

<span data-ttu-id="4bdb1-108">**ObHandleEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4bdb1-108">The **ObHandleEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="4bdb1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="4bdb1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bdb1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4bdb1-110">Properties</span></span>

<span data-ttu-id="4bdb1-111">**ObHandleEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4bdb1-111">The **ObHandleEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4bdb1-112">**Handle**</span><span class="sxs-lookup"><span data-stu-id="4bdb1-112">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bdb1-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4bdb1-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bdb1-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4bdb1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bdb1-115">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) </span><span class="sxs-lookup"><span data-stu-id="4bdb1-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="4bdb1-116">物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="4bdb1-116">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="4bdb1-117">**Object**</span><span class="sxs-lookup"><span data-stu-id="4bdb1-117">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bdb1-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4bdb1-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bdb1-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4bdb1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bdb1-120">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "x" ) ， [**指標**](event-tracing-mof-qualifiers.md)， [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) </span><span class="sxs-lookup"><span data-stu-id="4bdb1-120">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4bdb1-121">物件。</span><span class="sxs-lookup"><span data-stu-id="4bdb1-121">The object.</span></span>

</dd> <dt>

<span data-ttu-id="4bdb1-122">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="4bdb1-122">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bdb1-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4bdb1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bdb1-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4bdb1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bdb1-125">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "w" ) 、 [**StringTermination**](event-tracing-mof-qualifiers.md) ( "NullTerminated" ) 、 [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) </span><span class="sxs-lookup"><span data-stu-id="4bdb1-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="4bdb1-126">物件名稱。</span><span class="sxs-lookup"><span data-stu-id="4bdb1-126">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="4bdb1-127">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="4bdb1-127">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bdb1-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4bdb1-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4bdb1-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4bdb1-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bdb1-130">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) </span><span class="sxs-lookup"><span data-stu-id="4bdb1-130">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="4bdb1-131">物件類型。</span><span class="sxs-lookup"><span data-stu-id="4bdb1-131">The object type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bdb1-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bdb1-132">Requirements</span></span>



| <span data-ttu-id="4bdb1-133">需求</span><span class="sxs-lookup"><span data-stu-id="4bdb1-133">Requirement</span></span> | <span data-ttu-id="4bdb1-134">值</span><span class="sxs-lookup"><span data-stu-id="4bdb1-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bdb1-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bdb1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4bdb1-136">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bdb1-136">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4bdb1-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bdb1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4bdb1-138">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bdb1-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4bdb1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4bdb1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bdb1-140"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bdb1-140"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




