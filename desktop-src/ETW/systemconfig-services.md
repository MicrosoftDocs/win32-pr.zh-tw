---
description: SystemConfig_Services 類別-這個類別是服務設定事件的事件種類類別。
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: SystemConfig_Services 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106056"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="52f31-103">SystemConfig \_ 服務類別</span><span class="sxs-lookup"><span data-stu-id="52f31-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="52f31-104">此類別是服務設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="52f31-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="52f31-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="52f31-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f31-106">語法</span><span class="sxs-lookup"><span data-stu-id="52f31-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a><span data-ttu-id="52f31-107">成員</span><span class="sxs-lookup"><span data-stu-id="52f31-107">Members</span></span>

<span data-ttu-id="52f31-108">**SystemConfig \_ Services** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="52f31-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="52f31-109">屬性</span><span class="sxs-lookup"><span data-stu-id="52f31-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52f31-110">屬性</span><span class="sxs-lookup"><span data-stu-id="52f31-110">Properties</span></span>

<span data-ttu-id="52f31-111">**SystemConfig \_ Services** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="52f31-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52f31-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="52f31-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f31-113">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="52f31-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52f31-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="52f31-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f31-115">限定詞： **WmiDataId** (5) 、 **StringTermination ( "NullTerminated" )**、 **Format ( "w" )**</span><span class="sxs-lookup"><span data-stu-id="52f31-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="52f31-116">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="52f31-116">Display name of the service.</span></span> <span data-ttu-id="52f31-117">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="52f31-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="52f31-118">不過，顯示名稱比較一定不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="52f31-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="52f31-119">**進程**</span><span class="sxs-lookup"><span data-stu-id="52f31-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f31-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="52f31-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f31-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="52f31-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f31-122">限定詞： **WmiDataId** (1) ， **格式 ( "x" )**</span><span class="sxs-lookup"><span data-stu-id="52f31-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="52f31-123">服務執行所在進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="52f31-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="52f31-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="52f31-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f31-125">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="52f31-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52f31-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="52f31-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f31-127">限定詞： **WmiDataId** (6) 、 **StringTermination ( "NullTerminated" )**、 **Format ( "w" )**</span><span class="sxs-lookup"><span data-stu-id="52f31-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="52f31-128">服務執行所在進程的名稱。</span><span class="sxs-lookup"><span data-stu-id="52f31-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="52f31-129">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="52f31-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f31-130">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="52f31-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52f31-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="52f31-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f31-132">限定詞： **WmiDataId** (4) 、 **StringTermination ( "NullTerminated" )**、 **Format ( "w" )**</span><span class="sxs-lookup"><span data-stu-id="52f31-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="52f31-133">服務的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="52f31-133">Unique identifier of the service.</span></span> <span data-ttu-id="52f31-134">此識別碼提供服務所提供之功能的指示。</span><span class="sxs-lookup"><span data-stu-id="52f31-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="52f31-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="52f31-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f31-136">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="52f31-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f31-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="52f31-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f31-138">限定詞： **WmiDataId** (2) ， **格式 ( "x" )**</span><span class="sxs-lookup"><span data-stu-id="52f31-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="52f31-139">服務的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="52f31-139">Current state of the service.</span></span> <span data-ttu-id="52f31-140">如需可能的值，請參閱 **服務 \_ 狀態 \_ 進程** 的 **dwCurrentState** 成員。</span><span class="sxs-lookup"><span data-stu-id="52f31-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="52f31-141">**SubProcessTag**</span><span class="sxs-lookup"><span data-stu-id="52f31-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52f31-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="52f31-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52f31-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="52f31-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52f31-144">限定詞： **WmiDataId** (3) ， **格式 ( "x" )**</span><span class="sxs-lookup"><span data-stu-id="52f31-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="52f31-145">識別服務。</span><span class="sxs-lookup"><span data-stu-id="52f31-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52f31-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="52f31-146">Requirements</span></span>



| <span data-ttu-id="52f31-147">需求</span><span class="sxs-lookup"><span data-stu-id="52f31-147">Requirement</span></span> | <span data-ttu-id="52f31-148">值</span><span class="sxs-lookup"><span data-stu-id="52f31-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52f31-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52f31-149">Minimum supported client</span></span><br/> | <span data-ttu-id="52f31-150">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52f31-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52f31-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52f31-151">Minimum supported server</span></span><br/> | <span data-ttu-id="52f31-152">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52f31-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52f31-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52f31-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f31-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="52f31-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




