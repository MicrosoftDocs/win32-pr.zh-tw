---
description: 作為提供者定義之錯誤類別的父類別。
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: __NotifyStatus 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694935"
---
# <a name="__notifystatus-class"></a><span data-ttu-id="a1d28-103">\_\_NotifyStatus 類別</span><span class="sxs-lookup"><span data-stu-id="a1d28-103">\_\_NotifyStatus class</span></span>

<span data-ttu-id="a1d28-104">**\_ \_ NotifyStatus** 抽象系統類別可作為提供者定義之錯誤類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a1d28-104">The **\_\_NotifyStatus** abstract system class serves as the parent class for provider-defined error classes.</span></span>

<span data-ttu-id="a1d28-105">下列語法簡化了受控物件格式 (MF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a1d28-105">The following syntax is simplified from Managed Object Format (MF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d28-106">語法</span><span class="sxs-lookup"><span data-stu-id="a1d28-106">Syntax</span></span>

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="a1d28-107">成員</span><span class="sxs-lookup"><span data-stu-id="a1d28-107">Members</span></span>

<span data-ttu-id="a1d28-108">**\_ \_ NotifyStatus** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a1d28-108">The **\_\_NotifyStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="a1d28-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a1d28-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1d28-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a1d28-110">Properties</span></span>

<span data-ttu-id="a1d28-111">**\_ \_ NotifyStatus** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a1d28-111">The **\_\_NotifyStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1d28-112">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="a1d28-112">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1d28-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a1d28-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1d28-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a1d28-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1d28-115">包含作業的錯誤或資訊代碼。</span><span class="sxs-lookup"><span data-stu-id="a1d28-115">Contains an error or information code for an operation.</span></span> <span data-ttu-id="a1d28-116">這可以是任何使用者定義的程式碼，但值 0 (零) 通常會保留以表示成功。</span><span class="sxs-lookup"><span data-stu-id="a1d28-116">This can be any user-defined code, but the value 0 (zero) is usually reserved to indicate success.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1d28-117">備註</span><span class="sxs-lookup"><span data-stu-id="a1d28-117">Remarks</span></span>

<span data-ttu-id="a1d28-118">雖然 **\_ \_ NotifyStatus** 類別可以是提供者定義之錯誤類別的父類別，但建議提供者改為從 [**\_ \_ ExtendedStatus**](--extendedstatus.md)衍生錯誤類別。</span><span class="sxs-lookup"><span data-stu-id="a1d28-118">Although the **\_\_NotifyStatus** class can be the parent class for provider-defined error classes, it is recommended that providers derive error classes from [**\_\_ExtendedStatus**](--extendedstatus.md) instead.</span></span> <span data-ttu-id="a1d28-119">使用 **\_ \_ ExtendedStatus** 可讓您更有效地標準化錯誤類別。</span><span class="sxs-lookup"><span data-stu-id="a1d28-119">Using **\_\_ExtendedStatus** allows for greater standardization of error classes.</span></span>

<span data-ttu-id="a1d28-120">提供者永遠不應直接建立 **\_ \_ NotifyStatus** 的實例，因為這些實例所傳達的資訊不會超過簡單的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="a1d28-120">Providers should never create instances of **\_\_NotifyStatus** directly, because these instances convey no more information than a simple return code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d28-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1d28-121">Requirements</span></span>



| <span data-ttu-id="a1d28-122">需求</span><span class="sxs-lookup"><span data-stu-id="a1d28-122">Requirement</span></span> | <span data-ttu-id="a1d28-123">值</span><span class="sxs-lookup"><span data-stu-id="a1d28-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a1d28-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1d28-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d28-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1d28-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a1d28-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1d28-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d28-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1d28-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a1d28-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1d28-128">Namespace</span></span><br/>                | <span data-ttu-id="a1d28-129">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="a1d28-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a1d28-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1d28-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d28-131">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="a1d28-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




