---
description: 表示 WMI 命名空間。
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852020"
---
# <a name="__namespace-class"></a><span data-ttu-id="2bddd-103">\_\_Namespace 類別</span><span class="sxs-lookup"><span data-stu-id="2bddd-103">\_\_Namespace class</span></span>

<span data-ttu-id="2bddd-104">**\_ \_ Namespace** 系統類別代表 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="2bddd-104">The **\_\_Namespace** system class represents a WMI namespace.</span></span>

<span data-ttu-id="2bddd-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2bddd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2bddd-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2bddd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bddd-107">語法</span><span class="sxs-lookup"><span data-stu-id="2bddd-107">Syntax</span></span>

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="2bddd-108">成員</span><span class="sxs-lookup"><span data-stu-id="2bddd-108">Members</span></span>

<span data-ttu-id="2bddd-109">**\_ \_ Namespace** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2bddd-109">The **\_\_Namespace** class has these types of members:</span></span>

-   [<span data-ttu-id="2bddd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2bddd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bddd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2bddd-111">Properties</span></span>

<span data-ttu-id="2bddd-112">**\_ \_ Namespace** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2bddd-112">The **\_\_Namespace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bddd-113">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2bddd-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bddd-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2bddd-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bddd-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2bddd-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2bddd-116">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2bddd-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2bddd-117">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="2bddd-117">Namespace name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bddd-118">備註</span><span class="sxs-lookup"><span data-stu-id="2bddd-118">Remarks</span></span>

<span data-ttu-id="2bddd-119">**\_ \_ 命名空間** 類別衍生自沒有屬性的 [**\_ \_ SystemClass**](--systemclass.md)。</span><span class="sxs-lookup"><span data-stu-id="2bddd-119">The **\_\_Namespace** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="2bddd-120">您可以使用 **\_ \_ 命名空間** 來識別、建立及刪除您擁有 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)物件之目前工作命名空間內的子命名空間。</span><span class="sxs-lookup"><span data-stu-id="2bddd-120">You can use **\_\_Namespace** to identify, create, and delete child namespaces within the current working namespace for which you have an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) object.</span></span> <span data-ttu-id="2bddd-121">在任何工作的命名空間內建立 **\_ \_ 命名空間** 的新實例，會在工作的命名空間內建立子命名空間。</span><span class="sxs-lookup"><span data-stu-id="2bddd-121">Creating a new instance of **\_\_Namespace** within any working namespace creates a child namespace within the working namespace.</span></span> <span data-ttu-id="2bddd-122">相反地，刪除 **\_ \_ 命名空間** 的實例會從工作命名空間移除子命名空間。</span><span class="sxs-lookup"><span data-stu-id="2bddd-122">Conversely, deleting an instance of **\_\_Namespace** removes the child namespace from the working namespace.</span></span> <span data-ttu-id="2bddd-123">請注意，刪除子命名空間時，也會刪除其所有的類別和實例。</span><span class="sxs-lookup"><span data-stu-id="2bddd-123">Note that deleting a child namespace also deletes all of its classes and instances.</span></span>

<span data-ttu-id="2bddd-124">在任何工作的命名空間內列舉此類別的實例會提供可用的子命名空間。</span><span class="sxs-lookup"><span data-stu-id="2bddd-124">Enumerating instances of this class within any working namespace gives the available child namespaces.</span></span>

<span data-ttu-id="2bddd-125">例如，在 \\ 根命名空間內是 **\_ \_ 命名空間** 的兩個實例。</span><span class="sxs-lookup"><span data-stu-id="2bddd-125">For example, within the \\root namespace are two instances of **\_\_Namespace**.</span></span> <span data-ttu-id="2bddd-126">其中一個屬性設定為 "Default"，另 **一個名稱屬性** 設 **為** "Cimv2"。</span><span class="sxs-lookup"><span data-stu-id="2bddd-126">One has its **Name** property set to "Default," the other has **Name** set to "Cimv2."</span></span> <span data-ttu-id="2bddd-127">這些實例分別代表 \\ 根 \\ 預設值和 \\ 根 \\ cimv2 命名空間。</span><span class="sxs-lookup"><span data-stu-id="2bddd-127">These instances represent the \\root\\default, and \\root\\cimv2 namespaces, respectively.</span></span>

## <a name="examples"></a><span data-ttu-id="2bddd-128">範例</span><span class="sxs-lookup"><span data-stu-id="2bddd-128">Examples</span></span>

<span data-ttu-id="2bddd-129">TechNet 資源庫上的[所有 WMI 命名空間](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257)VBScript 範例都會使用遞迴呼叫來列出 \_ \_ 系統上命名空間類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="2bddd-129">The [List All WMI Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript example on the TechNet Gallery uses a recursive call to list all instances of the \_\_Namespace class on a system.</span></span>

<span data-ttu-id="2bddd-130">下列程式碼範例會取出 PowerShell 中的所有命名空間。</span><span class="sxs-lookup"><span data-stu-id="2bddd-130">The following code sample retrieves all namespaces in PowerShell.</span></span>


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



<span data-ttu-id="2bddd-131">下列程式碼範例會改善先前的範例，並新增其他資訊。</span><span class="sxs-lookup"><span data-stu-id="2bddd-131">The following code sample improves on the previous sample, and adds in additional information.</span></span>


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a><span data-ttu-id="2bddd-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bddd-132">Requirements</span></span>



| <span data-ttu-id="2bddd-133">需求</span><span class="sxs-lookup"><span data-stu-id="2bddd-133">Requirement</span></span> | <span data-ttu-id="2bddd-134">值</span><span class="sxs-lookup"><span data-stu-id="2bddd-134">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2bddd-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bddd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2bddd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bddd-136">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2bddd-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bddd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2bddd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bddd-138">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2bddd-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="2bddd-139">Namespace</span></span><br/>                | <span data-ttu-id="2bddd-140">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="2bddd-140">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2bddd-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bddd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bddd-142">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="2bddd-142">**\_\_SystemClass**</span></span>](--systemclass.md)
</dt> <dt>

[<span data-ttu-id="2bddd-143">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="2bddd-143">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




