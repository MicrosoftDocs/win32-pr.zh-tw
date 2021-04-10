---
description: Win32 \_ LogicalProgramGroupItemDataFile 關聯 WMI 類別會將 [開始] 功能表的程式群組專案和儲存這些專案的檔案產生關聯。
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItemDataFile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: beec7074104482e4c6bc91ba7efeaea89104a011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111601"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a><span data-ttu-id="f2a04-103">Win32 \_ LogicalProgramGroupItemDataFile 類別</span><span class="sxs-lookup"><span data-stu-id="f2a04-103">Win32\_LogicalProgramGroupItemDataFile class</span></span>

<span data-ttu-id="f2a04-104">**Win32 \_ LogicalProgramGroupItemDataFile** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯 [**開始**] 功能表的程式群組專案和儲存這些專案的檔案。</span><span class="sxs-lookup"><span data-stu-id="f2a04-104">The **Win32\_LogicalProgramGroupItemDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the program group items of the **Start** menu and the files in which they are stored.</span></span>

<span data-ttu-id="f2a04-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2a04-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f2a04-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="f2a04-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a04-107">語法</span><span class="sxs-lookup"><span data-stu-id="f2a04-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f2a04-108">成員</span><span class="sxs-lookup"><span data-stu-id="f2a04-108">Members</span></span>

<span data-ttu-id="f2a04-109">**Win32 \_ LogicalProgramGroupItemDataFile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f2a04-109">The **Win32\_LogicalProgramGroupItemDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="f2a04-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f2a04-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2a04-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f2a04-111">Properties</span></span>

<span data-ttu-id="f2a04-112">**Win32 \_ LogicalProgramGroupItemDataFile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f2a04-112">The **Win32\_LogicalProgramGroupItemDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2a04-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="f2a04-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a04-114">資料類型： **Win32 \_ LogicalProgramGroupItem**</span><span class="sxs-lookup"><span data-stu-id="f2a04-114">Data type: **Win32\_LogicalProgramGroupItem**</span></span>
</dt> <dt>

<span data-ttu-id="f2a04-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2a04-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a04-116">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ LogicalProgramGroupItem" ) </span><span class="sxs-lookup"><span data-stu-id="f2a04-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroupItem")</span></span>
</dt> </dl>

<span data-ttu-id="f2a04-117">代表 [ **開始** ] 功能表中程式群組的實例參考。</span><span class="sxs-lookup"><span data-stu-id="f2a04-117">Reference to the instance representing the program groupings in the **Start** menu.</span></span>

</dd> <dt>

<span data-ttu-id="f2a04-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="f2a04-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a04-119">資料類型： **CIM 資料 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="f2a04-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="f2a04-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2a04-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a04-121">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| cim \_ 資料檔案」 ) </span><span class="sxs-lookup"><span data-stu-id="f2a04-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="f2a04-122">代表與程式群組相關聯之類別的實例參考。</span><span class="sxs-lookup"><span data-stu-id="f2a04-122">Reference to the instance representing the class associated with the program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2a04-123">備註</span><span class="sxs-lookup"><span data-stu-id="f2a04-123">Remarks</span></span>

<span data-ttu-id="f2a04-124">**Win32 \_ LogicalProgramGroupItemDataFile** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="f2a04-124">The **Win32\_LogicalProgramGroupItemDataFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f2a04-125">使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="f2a04-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="f2a04-126">例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="f2a04-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="f2a04-127">如需詳細資訊，請參閱 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="f2a04-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2a04-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2a04-128">Requirements</span></span>



| <span data-ttu-id="f2a04-129">需求</span><span class="sxs-lookup"><span data-stu-id="f2a04-129">Requirement</span></span> | <span data-ttu-id="f2a04-130">值</span><span class="sxs-lookup"><span data-stu-id="f2a04-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a04-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2a04-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f2a04-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2a04-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2a04-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2a04-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f2a04-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2a04-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2a04-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="f2a04-135">Namespace</span></span><br/>                | <span data-ttu-id="f2a04-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f2a04-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2a04-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f2a04-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2a04-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2a04-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2a04-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f2a04-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2a04-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2a04-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2a04-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2a04-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a04-142">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="f2a04-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="f2a04-143">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2a04-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

