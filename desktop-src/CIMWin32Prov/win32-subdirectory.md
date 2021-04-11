---
description: Win32 \_ 子目錄關聯 WMI 類別會將目錄 (資料夾) 與其子目錄中的其中一個 () 的子資料夾建立關聯。
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Win32_SubDirectory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111200"
---
# <a name="win32_subdirectory-class"></a><span data-ttu-id="4e2e2-103">Win32 \_ 子目錄類別</span><span class="sxs-lookup"><span data-stu-id="4e2e2-103">Win32\_SubDirectory class</span></span>

<span data-ttu-id="4e2e2-104">**Win32 \_ 子目錄** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將目錄 (資料夾) 與其子目錄中的其中一個 () 的子資料夾建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-104">The **Win32\_SubDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a directory (folder) and one of its subdirectories (subfolders).</span></span>

<span data-ttu-id="4e2e2-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4e2e2-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e2e2-107">語法</span><span class="sxs-lookup"><span data-stu-id="4e2e2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4e2e2-108">成員</span><span class="sxs-lookup"><span data-stu-id="4e2e2-108">Members</span></span>

<span data-ttu-id="4e2e2-109">**Win32 \_ 子目錄** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4e2e2-109">The **Win32\_SubDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="4e2e2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4e2e2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e2e2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4e2e2-111">Properties</span></span>

<span data-ttu-id="4e2e2-112">**Win32 \_ 子目錄** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-112">The **Win32\_SubDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e2e2-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4e2e2-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e2e2-114">資料類型： **Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="4e2e2-114">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="4e2e2-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4e2e2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e2e2-116">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Directory" ) </span><span class="sxs-lookup"><span data-stu-id="4e2e2-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="4e2e2-117">代表此關聯中)  (資料夾的父目錄屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-117">Reference to the instance representing the properties of the parent directory (folder) in this association.</span></span>

</dd> <dt>

<span data-ttu-id="4e2e2-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4e2e2-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e2e2-119">資料類型： **Win32 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="4e2e2-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="4e2e2-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4e2e2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e2e2-121">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Directory" ) </span><span class="sxs-lookup"><span data-stu-id="4e2e2-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="4e2e2-122">此實例的參考，代表關聯) 部分 (子資料夾的子目錄。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-122">Reference to the instance representing the subdirectory (subfolder) part of the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e2e2-123">備註</span><span class="sxs-lookup"><span data-stu-id="4e2e2-123">Remarks</span></span>

<span data-ttu-id="4e2e2-124">**Win32 \_ 子目錄** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-124">The **Win32\_SubDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="4e2e2-125">若要傳回資料夾的子資料夾集合，請建立將 *ResultRole* 設定為 *PartComponent* 的關聯查詢。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-125">To return a collection of subfolders for a folder, create an association query that sets the *ResultRole* to *PartComponent*.</span></span> <span data-ttu-id="4e2e2-126">這表示傳回集合中的所有專案都必須扮演資料夾物件的 PartComponent 或子資料夾的角色。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-126">This indicates that all the items in the returned collection must play the role of a PartComponent, or subfolder, of the folder object.</span></span> <span data-ttu-id="4e2e2-127">若要傳回資料夾的父資料夾，請將 *ResultRole* 設定為 *GroupComponent*。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-127">To return the parent folder for a folder, set the *ResultRole* to *GroupComponent*.</span></span>

<span data-ttu-id="4e2e2-128">**Win32 \_ 子目錄** 類別只適用于緊接在指定資料夾正上方或正下方的檔案系統層級。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-128">The **Win32\_SubDirectory** class works only on the file system level immediately above or immediately below the specified folder.</span></span>

## <a name="examples"></a><span data-ttu-id="4e2e2-129">範例</span><span class="sxs-lookup"><span data-stu-id="4e2e2-129">Examples</span></span>

<span data-ttu-id="4e2e2-130">下列 VBScript 範例會傳回資料夾 C：腳本中所有子資料夾的清單 \\ 。</span><span class="sxs-lookup"><span data-stu-id="4e2e2-130">The following VBScript sample returns a list of all subfolders within the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="4e2e2-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e2e2-131">Requirements</span></span>



| <span data-ttu-id="4e2e2-132">需求</span><span class="sxs-lookup"><span data-stu-id="4e2e2-132">Requirement</span></span> | <span data-ttu-id="4e2e2-133">值</span><span class="sxs-lookup"><span data-stu-id="4e2e2-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2e2-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e2e2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2e2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e2e2-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e2e2-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e2e2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2e2-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e2e2-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e2e2-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="4e2e2-138">Namespace</span></span><br/>                | <span data-ttu-id="4e2e2-139">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4e2e2-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e2e2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4e2e2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e2e2-141"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e2e2-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e2e2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4e2e2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e2e2-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e2e2-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e2e2-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e2e2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e2e2-145">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="4e2e2-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="4e2e2-146">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="4e2e2-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
