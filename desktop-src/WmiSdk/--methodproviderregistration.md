---
description: 使用 WMI 註冊方法提供者。
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: __MethodProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977096"
---
# <a name="__methodproviderregistration-class"></a><span data-ttu-id="5567c-103">\_\_MethodProviderRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="5567c-103">\_\_MethodProviderRegistration class</span></span>

<span data-ttu-id="5567c-104">**\_ \_ MethodProviderRegistration** 系統類別會向 WMI 註冊方法提供者。</span><span class="sxs-lookup"><span data-stu-id="5567c-104">The **\_\_MethodProviderRegistration** system class registers method providers with WMI.</span></span>

<span data-ttu-id="5567c-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5567c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5567c-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5567c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5567c-107">語法</span><span class="sxs-lookup"><span data-stu-id="5567c-107">Syntax</span></span>

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="5567c-108">成員</span><span class="sxs-lookup"><span data-stu-id="5567c-108">Members</span></span>

<span data-ttu-id="5567c-109">**\_ \_ MethodProviderRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5567c-109">The **\_\_MethodProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="5567c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5567c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5567c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5567c-111">Properties</span></span>

<span data-ttu-id="5567c-112">**\_ \_ MethodProviderRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5567c-112">The **\_\_MethodProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5567c-113">**供應商**</span><span class="sxs-lookup"><span data-stu-id="5567c-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5567c-114">資料類型： **\_ \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="5567c-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="5567c-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5567c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5567c-116">[**\_ \_ 提供者**](--provider.md)實例的參考，代表方法提供者的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="5567c-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the method provider.</span></span> <span data-ttu-id="5567c-117">這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="5567c-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5567c-118">備註</span><span class="sxs-lookup"><span data-stu-id="5567c-118">Remarks</span></span>

<span data-ttu-id="5567c-119">**\_ \_ MethodProviderRegistration** 類別衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="5567c-119">The **\_\_MethodProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="5567c-120">只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 **\_ \_ MethodProviderRegistration** 的實例來註冊或刪除方法提供者。</span><span class="sxs-lookup"><span data-stu-id="5567c-120">Only administrators can register or delete a method provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_MethodProviderRegistration**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5567c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5567c-121">Requirements</span></span>



| <span data-ttu-id="5567c-122">需求</span><span class="sxs-lookup"><span data-stu-id="5567c-122">Requirement</span></span> | <span data-ttu-id="5567c-123">值</span><span class="sxs-lookup"><span data-stu-id="5567c-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5567c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5567c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5567c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5567c-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5567c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5567c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5567c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5567c-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5567c-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="5567c-128">Namespace</span></span><br/>                | <span data-ttu-id="5567c-129">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="5567c-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5567c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5567c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5567c-131">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="5567c-131">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="5567c-132">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="5567c-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5567c-133">註冊方法提供者</span><span class="sxs-lookup"><span data-stu-id="5567c-133">Registering a Method Provider</span></span>](registering-a-method-provider.md)
</dt> </dl>

 

