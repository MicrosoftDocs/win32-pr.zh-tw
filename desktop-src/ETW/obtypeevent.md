---
description: 表示與資料收集開始和結束相關之物件類型事件的事件種類類別。
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: ObTypeEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115765"
---
# <a name="obtypeevent-class"></a><span data-ttu-id="e0f8a-103">ObTypeEvent 類別</span><span class="sxs-lookup"><span data-stu-id="e0f8a-103">ObTypeEvent class</span></span>

<span data-ttu-id="e0f8a-104">表示與資料收集開始和結束相關之物件類型事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="e0f8a-104">Represents the event type class for object type events related to the beginning and end of data collection.</span></span> <span data-ttu-id="e0f8a-105">此事件牽涉到型別索引值與型別名稱的對應。</span><span class="sxs-lookup"><span data-stu-id="e0f8a-105">This event involves the mapping of the type index values to the type names.</span></span>

<span data-ttu-id="e0f8a-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e0f8a-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f8a-107">語法</span><span class="sxs-lookup"><span data-stu-id="e0f8a-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a><span data-ttu-id="e0f8a-108">成員</span><span class="sxs-lookup"><span data-stu-id="e0f8a-108">Members</span></span>

<span data-ttu-id="e0f8a-109">**ObTypeEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e0f8a-109">The **ObTypeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e0f8a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e0f8a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0f8a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e0f8a-111">Properties</span></span>

<span data-ttu-id="e0f8a-112">**ObTypeEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e0f8a-112">The **ObTypeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0f8a-113">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="e0f8a-113">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f8a-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e0f8a-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0f8a-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0f8a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0f8a-116">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) </span><span class="sxs-lookup"><span data-stu-id="e0f8a-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e0f8a-117">物件類型。</span><span class="sxs-lookup"><span data-stu-id="e0f8a-117">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="e0f8a-118">**已保留**</span><span class="sxs-lookup"><span data-stu-id="e0f8a-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f8a-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e0f8a-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0f8a-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0f8a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0f8a-121">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) </span><span class="sxs-lookup"><span data-stu-id="e0f8a-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="e0f8a-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="e0f8a-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e0f8a-123">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="e0f8a-123">**TypeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f8a-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0f8a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f8a-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0f8a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0f8a-126">限定詞： [**Format**](event-tracing-mof-qualifiers.md) ( "w" ) 、 [**StringTermination**](event-tracing-mof-qualifiers.md) ( "NullTerminated" ) 、 [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) </span><span class="sxs-lookup"><span data-stu-id="e0f8a-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="e0f8a-127">類型名稱。</span><span class="sxs-lookup"><span data-stu-id="e0f8a-127">The type name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0f8a-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0f8a-128">Requirements</span></span>



| <span data-ttu-id="e0f8a-129">需求</span><span class="sxs-lookup"><span data-stu-id="e0f8a-129">Requirement</span></span> | <span data-ttu-id="e0f8a-130">值</span><span class="sxs-lookup"><span data-stu-id="e0f8a-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f8a-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0f8a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f8a-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0f8a-132">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e0f8a-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0f8a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f8a-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0f8a-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e0f8a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e0f8a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0f8a-136"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0f8a-136"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




