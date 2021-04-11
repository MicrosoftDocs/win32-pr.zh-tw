---
description: Win32 \_ LoadOrderGroupServiceDependencies 關聯 WMI 類別會將服務相依的基底服務和載入順序群組關聯至開始執行。
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Win32_LoadOrderGroupServiceDependencies 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111365"
---
# <a name="win32_loadordergroupservicedependencies-class"></a><span data-ttu-id="ae45e-103">Win32 \_ LoadOrderGroupServiceDependencies 類別</span><span class="sxs-lookup"><span data-stu-id="ae45e-103">Win32\_LoadOrderGroupServiceDependencies class</span></span>

<span data-ttu-id="ae45e-104">**Win32 \_ LoadOrderGroupServiceDependencies** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將服務相依的基底服務和載入順序群組關聯至開始執行。</span><span class="sxs-lookup"><span data-stu-id="ae45e-104">The **Win32\_LoadOrderGroupServiceDependencies** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a base service and a load order group that the service depends on to start running.</span></span>

<span data-ttu-id="ae45e-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae45e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ae45e-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ae45e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae45e-107">語法</span><span class="sxs-lookup"><span data-stu-id="ae45e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ae45e-108">成員</span><span class="sxs-lookup"><span data-stu-id="ae45e-108">Members</span></span>

<span data-ttu-id="ae45e-109">**Win32 \_ LoadOrderGroupServiceDependencies** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ae45e-109">The **Win32\_LoadOrderGroupServiceDependencies** class has these types of members:</span></span>

-   [<span data-ttu-id="ae45e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ae45e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae45e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ae45e-111">Properties</span></span>

<span data-ttu-id="ae45e-112">**Win32 \_ LoadOrderGroupServiceDependencies** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ae45e-112">The **Win32\_LoadOrderGroupServiceDependencies** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae45e-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="ae45e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae45e-114">資料類型： **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="ae45e-114">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="ae45e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ae45e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae45e-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ LoadOrderGroup" ) </span><span class="sxs-lookup"><span data-stu-id="ae45e-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="ae45e-117">代表載入順序群組之屬性的實例的參考，該群組必須在這個類別的相依基底服務可以啟動之前啟動。</span><span class="sxs-lookup"><span data-stu-id="ae45e-117">Reference to the instance representing the properties of the load order group that must start before the dependent base service of this class can start.</span></span>

</dd> <dt>

<span data-ttu-id="ae45e-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="ae45e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae45e-119">資料類型： **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="ae45e-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="ae45e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ae45e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae45e-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 BaseService」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="ae45e-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="ae45e-122">此實例的參考，代表相依于載入順序群組以開始執行的基底服務屬性。</span><span class="sxs-lookup"><span data-stu-id="ae45e-122">Reference to the instance representing the properties of the base service that is dependent upon the load order group to start running.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae45e-123">備註</span><span class="sxs-lookup"><span data-stu-id="ae45e-123">Remarks</span></span>

<span data-ttu-id="ae45e-124">**Win32 \_ LoadOrderGroupServiceDependencies** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="ae45e-124">The **Win32\_LoadOrderGroupServiceDependencies** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae45e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae45e-125">Requirements</span></span>



| <span data-ttu-id="ae45e-126">需求</span><span class="sxs-lookup"><span data-stu-id="ae45e-126">Requirement</span></span> | <span data-ttu-id="ae45e-127">值</span><span class="sxs-lookup"><span data-stu-id="ae45e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae45e-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae45e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ae45e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae45e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae45e-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae45e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ae45e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae45e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae45e-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="ae45e-132">Namespace</span></span><br/>                | <span data-ttu-id="ae45e-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ae45e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae45e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ae45e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae45e-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae45e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae45e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ae45e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae45e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae45e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae45e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae45e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae45e-139">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="ae45e-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="ae45e-140">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae45e-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

