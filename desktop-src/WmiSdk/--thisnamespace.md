---
description: 以安全描述項的形式保存命名空間的安全性許可權。
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: __thisNAMESPACE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996905"
---
# <a name="__thisnamespace-class"></a><span data-ttu-id="e5a07-103">\_\_thisNAMESPACE 類別</span><span class="sxs-lookup"><span data-stu-id="e5a07-103">\_\_thisNAMESPACE class</span></span>

<span data-ttu-id="e5a07-104">**\_ \_ ThisNAMESPACE** 系統類別會以安全描述項的形式保存命名空間的安全性許可權。</span><span class="sxs-lookup"><span data-stu-id="e5a07-104">The **\_\_thisNAMESPACE** system class holds the security rights for the namespace in the form of a security descriptor.</span></span> <span data-ttu-id="e5a07-105">在所有命名空間中都可以找到這個類別和單一實例。</span><span class="sxs-lookup"><span data-stu-id="e5a07-105">This class and a single instance is found in all namespaces.</span></span>

<span data-ttu-id="e5a07-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e5a07-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e5a07-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e5a07-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a07-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5a07-108">Syntax</span></span>

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a><span data-ttu-id="e5a07-109">成員</span><span class="sxs-lookup"><span data-stu-id="e5a07-109">Members</span></span>

<span data-ttu-id="e5a07-110">**\_ \_ ThisNAMESPACE** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e5a07-110">The **\_\_thisNAMESPACE** class has these types of members:</span></span>

-   [<span data-ttu-id="e5a07-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e5a07-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5a07-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e5a07-112">Properties</span></span>

<span data-ttu-id="e5a07-113">**\_ \_ ThisNAMESPACE** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e5a07-113">The **\_\_thisNAMESPACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5a07-114">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="e5a07-114">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5a07-115">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5a07-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e5a07-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5a07-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5a07-117">安全描述項，描述誰可以存取命名空間，以及誰可以讀取或寫入命名空間。</span><span class="sxs-lookup"><span data-stu-id="e5a07-117">Security descriptor describing who can access the namespace and who can read from or write to the namespace.</span></span> <span data-ttu-id="e5a07-118">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="e5a07-118">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="e5a07-119">如需安全描述項格式的詳細資訊，請參閱 Windows SDK 的安全性一節中的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors) 。</span><span class="sxs-lookup"><span data-stu-id="e5a07-119">For more information about the format of security descriptors, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors) in the Security section of the Windows SDK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5a07-120">備註</span><span class="sxs-lookup"><span data-stu-id="e5a07-120">Remarks</span></span>

<span data-ttu-id="e5a07-121">**\_ \_ ThisNAMESPACE** 的單一實例是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e5a07-121">The singleton instance of **\_\_thisNAMESPACE** is read-only.</span></span> <span data-ttu-id="e5a07-122">若要變更安全描述項屬性的設定，請使用 [**\_ \_ SystemSecurity**](--systemsecurity.md)類別的方法。</span><span class="sxs-lookup"><span data-stu-id="e5a07-122">To change the settings of the security descriptor property, use the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span> <span data-ttu-id="e5a07-123">**\_ \_ ThisNAMESPACE** 類別衍生自 [**\_ \_ SystemClass**](--systemclass.md)。</span><span class="sxs-lookup"><span data-stu-id="e5a07-123">The **\_\_thisNAMESPACE** class derives from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a07-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5a07-124">Requirements</span></span>



| <span data-ttu-id="e5a07-125">需求</span><span class="sxs-lookup"><span data-stu-id="e5a07-125">Requirement</span></span> | <span data-ttu-id="e5a07-126">值</span><span class="sxs-lookup"><span data-stu-id="e5a07-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e5a07-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5a07-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a07-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5a07-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e5a07-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5a07-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a07-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5a07-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e5a07-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5a07-131">Namespace</span></span><br/>                | <span data-ttu-id="e5a07-132">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="e5a07-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e5a07-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5a07-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a07-134">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="e5a07-134">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="e5a07-135">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="e5a07-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

