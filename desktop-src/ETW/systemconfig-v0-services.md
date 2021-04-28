---
description: SystemConfig_V0_Services 類別-這個類別是服務設定事件的事件種類類別。
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: SystemConfig_V0_Services 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: b69ca7cf4ee4e16a5fbcb6a5f10c659f713ab458
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105926"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="322ce-103">SystemConfig \_ V0 \_ 服務類別</span><span class="sxs-lookup"><span data-stu-id="322ce-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="322ce-104">此類別是服務設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="322ce-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="322ce-105">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="322ce-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="322ce-106">語法</span><span class="sxs-lookup"><span data-stu-id="322ce-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="322ce-107">成員</span><span class="sxs-lookup"><span data-stu-id="322ce-107">Members</span></span>

<span data-ttu-id="322ce-108">**SystemConfig \_ V0 \_ Services** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="322ce-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="322ce-109">屬性</span><span class="sxs-lookup"><span data-stu-id="322ce-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="322ce-110">屬性</span><span class="sxs-lookup"><span data-stu-id="322ce-110">Properties</span></span>

<span data-ttu-id="322ce-111">**SystemConfig \_ V0 \_ Services** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="322ce-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="322ce-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="322ce-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="322ce-113">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="322ce-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="322ce-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="322ce-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="322ce-115">限定詞： **WmiDataId** (2) ， **最大** (256) </span><span class="sxs-lookup"><span data-stu-id="322ce-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="322ce-116">服務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="322ce-116">Display name of the service.</span></span> <span data-ttu-id="322ce-117">服務控制管理員中的名稱會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="322ce-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="322ce-118">不過，顯示名稱比較一定不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="322ce-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="322ce-119">**進程**</span><span class="sxs-lookup"><span data-stu-id="322ce-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="322ce-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="322ce-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="322ce-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="322ce-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="322ce-122">限定詞： **WmiDataId** (4) </span><span class="sxs-lookup"><span data-stu-id="322ce-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="322ce-123">服務執行所在進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="322ce-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="322ce-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="322ce-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="322ce-125">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="322ce-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="322ce-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="322ce-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="322ce-127">限定詞： **WmiDataId** (3) ， **最大** (34) </span><span class="sxs-lookup"><span data-stu-id="322ce-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="322ce-128">服務執行所在進程的名稱。</span><span class="sxs-lookup"><span data-stu-id="322ce-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="322ce-129">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="322ce-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="322ce-130">資料類型： **char16** 陣列</span><span class="sxs-lookup"><span data-stu-id="322ce-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="322ce-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="322ce-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="322ce-132">限定詞： **WmiDataId** (1) ， **最大** (34) </span><span class="sxs-lookup"><span data-stu-id="322ce-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="322ce-133">服務的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="322ce-133">Unique identifier of the service.</span></span> <span data-ttu-id="322ce-134">此識別碼提供服務所提供之功能的指示。</span><span class="sxs-lookup"><span data-stu-id="322ce-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="322ce-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="322ce-135">Requirements</span></span>



| <span data-ttu-id="322ce-136">需求</span><span class="sxs-lookup"><span data-stu-id="322ce-136">Requirement</span></span> | <span data-ttu-id="322ce-137">值</span><span class="sxs-lookup"><span data-stu-id="322ce-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="322ce-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="322ce-138">Minimum supported client</span></span><br/> | <span data-ttu-id="322ce-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="322ce-139">None supported</span></span><br/>                            |
| <span data-ttu-id="322ce-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="322ce-140">Minimum supported server</span></span><br/> | <span data-ttu-id="322ce-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="322ce-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="322ce-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="322ce-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322ce-143">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="322ce-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




