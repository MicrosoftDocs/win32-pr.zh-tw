---
description: Registry_V1_TypeGroup1 類別-這個類別是登錄事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Registry_V1_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab0326f92d1b084f471f3dc1b57322f69aa645fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106156"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="c7e22-104">Registry \_ V1 \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="c7e22-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="c7e22-105">這個類別是登錄事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="c7e22-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="c7e22-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="c7e22-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e22-107">語法</span><span class="sxs-lookup"><span data-stu-id="c7e22-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="c7e22-108">成員</span><span class="sxs-lookup"><span data-stu-id="c7e22-108">Members</span></span>

<span data-ttu-id="c7e22-109">**Registry \_ V1 \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c7e22-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="c7e22-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c7e22-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7e22-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c7e22-111">Properties</span></span>

<span data-ttu-id="c7e22-112">**Registry \_ V1 \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c7e22-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7e22-113">經過時間</span><span class="sxs-lookup"><span data-stu-id="c7e22-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e22-114">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="c7e22-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7e22-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-116">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="c7e22-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="c7e22-117">登錄作業的經過時間。</span><span class="sxs-lookup"><span data-stu-id="c7e22-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="c7e22-118">索引</span><span class="sxs-lookup"><span data-stu-id="c7e22-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e22-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7e22-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7e22-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-121">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="c7e22-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c7e22-122">登錄作業 (的子機碼索引，例如 EnumerateKey) 。</span><span class="sxs-lookup"><span data-stu-id="c7e22-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="c7e22-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="c7e22-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e22-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7e22-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7e22-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-126">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="c7e22-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c7e22-127">登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c7e22-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="c7e22-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="c7e22-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e22-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7e22-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7e22-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-131">限定詞： WmiDataId (5) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="c7e22-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c7e22-132">登錄機碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7e22-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="c7e22-133">狀態</span><span class="sxs-lookup"><span data-stu-id="c7e22-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7e22-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7e22-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7e22-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7e22-136">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="c7e22-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c7e22-137">登錄作業的 NTSTATUS 值。</span><span class="sxs-lookup"><span data-stu-id="c7e22-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7e22-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7e22-138">Requirements</span></span>



| <span data-ttu-id="c7e22-139">需求</span><span class="sxs-lookup"><span data-stu-id="c7e22-139">Requirement</span></span> | <span data-ttu-id="c7e22-140">值</span><span class="sxs-lookup"><span data-stu-id="c7e22-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c7e22-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7e22-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e22-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7e22-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c7e22-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7e22-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e22-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7e22-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c7e22-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7e22-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e22-146">**登錄**</span><span class="sxs-lookup"><span data-stu-id="c7e22-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="c7e22-147">**登錄 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="c7e22-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 




