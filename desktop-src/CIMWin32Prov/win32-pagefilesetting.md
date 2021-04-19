---
description: Win32 \_ PageFileSetting&\# 8194;WMI 類別代表分頁檔的設定。
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Win32_PageFileSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985590"
---
# <a name="win32_pagefilesetting-class"></a><span data-ttu-id="03a67-103">Win32 \_ PageFileSetting 類別</span><span class="sxs-lookup"><span data-stu-id="03a67-103">Win32\_PageFileSetting class</span></span>

<span data-ttu-id="03a67-104">**Win32 \_ PageFileSetting** [WMI 類別](../wmisdk/retrieving-a-class.md)代表分頁檔的設定。</span><span class="sxs-lookup"><span data-stu-id="03a67-104">The **Win32\_PageFileSetting** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings of a page file.</span></span> <span data-ttu-id="03a67-105">從這個類別所具現化的物件內所包含的資訊會指定在系統啟動時建立檔案時所使用的分頁檔參數。</span><span class="sxs-lookup"><span data-stu-id="03a67-105">Information contained within objects instantiated from this class specify the page file parameters used when the file is created at system startup.</span></span> <span data-ttu-id="03a67-106">此類別中的屬性可以修改並延後到啟動。</span><span class="sxs-lookup"><span data-stu-id="03a67-106">The properties in this class can be modified and deferred until startup.</span></span> <span data-ttu-id="03a67-107">這些設定與透過相關類別 [**Win32 \_ PageFileUsage**](win32-pagefileusage.md)表示之分頁檔的執行時間狀態不同。</span><span class="sxs-lookup"><span data-stu-id="03a67-107">These settings are different from the run-time state of a page file expressed through the associated class [**Win32\_PageFileUsage**](win32-pagefileusage.md).</span></span>

<span data-ttu-id="03a67-108">若要建立這個類別的實例，請啟用 **SeCreatePagefilePrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="03a67-108">To create an instance of this class, enable the **SeCreatePagefilePrivilege** privilege.</span></span> <span data-ttu-id="03a67-109">如需詳細資訊，請參閱 [**許可權常數**](../wmisdk/privilege-constants.md) 和 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="03a67-109">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="03a67-110">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="03a67-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="03a67-111">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="03a67-111">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a67-112">語法</span><span class="sxs-lookup"><span data-stu-id="03a67-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="03a67-113">成員</span><span class="sxs-lookup"><span data-stu-id="03a67-113">Members</span></span>

<span data-ttu-id="03a67-114">**Win32 \_ PageFileSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="03a67-114">The **Win32\_PageFileSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="03a67-115">屬性</span><span class="sxs-lookup"><span data-stu-id="03a67-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03a67-116">屬性</span><span class="sxs-lookup"><span data-stu-id="03a67-116">Properties</span></span>

<span data-ttu-id="03a67-117">**Win32 \_ PageFileSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="03a67-117">The **Win32\_PageFileSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03a67-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="03a67-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a67-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03a67-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a67-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03a67-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a67-121">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="03a67-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="03a67-122">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="03a67-122">Short textual description of the current object.</span></span>

<span data-ttu-id="03a67-123">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="03a67-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="03a67-124">**說明**</span><span class="sxs-lookup"><span data-stu-id="03a67-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a67-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03a67-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a67-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03a67-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a67-127">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="03a67-127">Textual description of the current object.</span></span>

<span data-ttu-id="03a67-128">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="03a67-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="03a67-129">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="03a67-129">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a67-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="03a67-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03a67-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="03a67-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03a67-132">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="03a67-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="03a67-133">分頁檔案的初始大小。</span><span class="sxs-lookup"><span data-stu-id="03a67-133">Initial size of the page file.</span></span>

<span data-ttu-id="03a67-134">範例：139</span><span class="sxs-lookup"><span data-stu-id="03a67-134">Example: 139</span></span>

</dd> <dt>

<span data-ttu-id="03a67-135">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="03a67-135">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a67-136">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="03a67-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03a67-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="03a67-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03a67-138">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="03a67-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="03a67-139">分頁檔案的大小上限。</span><span class="sxs-lookup"><span data-stu-id="03a67-139">Maximum size of the page file.</span></span>

<span data-ttu-id="03a67-140">範例：178</span><span class="sxs-lookup"><span data-stu-id="03a67-140">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="03a67-141">**名稱**</span><span class="sxs-lookup"><span data-stu-id="03a67-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a67-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03a67-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a67-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="03a67-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03a67-144">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="03a67-144">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="03a67-145">分頁檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="03a67-145">Path and file name of the page file.</span></span>

<span data-ttu-id="03a67-146">範例： "C： \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="03a67-146">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="03a67-147">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="03a67-147">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a67-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="03a67-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a67-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="03a67-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a67-150">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="03a67-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03a67-151">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03a67-151">Identifier by which the current object is known.</span></span>

<span data-ttu-id="03a67-152">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="03a67-152">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03a67-153">備註</span><span class="sxs-lookup"><span data-stu-id="03a67-153">Remarks</span></span>

<span data-ttu-id="03a67-154">**Win32 \_ PageFileSetting** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="03a67-154">The **Win32\_PageFileSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03a67-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="03a67-155">Requirements</span></span>



| <span data-ttu-id="03a67-156">需求</span><span class="sxs-lookup"><span data-stu-id="03a67-156">Requirement</span></span> | <span data-ttu-id="03a67-157">值</span><span class="sxs-lookup"><span data-stu-id="03a67-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03a67-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03a67-158">Minimum supported client</span></span><br/> | <span data-ttu-id="03a67-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03a67-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03a67-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03a67-160">Minimum supported server</span></span><br/> | <span data-ttu-id="03a67-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03a67-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03a67-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="03a67-162">Namespace</span></span><br/>                | <span data-ttu-id="03a67-163">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="03a67-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03a67-164">MOF</span><span class="sxs-lookup"><span data-stu-id="03a67-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03a67-165"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="03a67-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03a67-166">DLL</span><span class="sxs-lookup"><span data-stu-id="03a67-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a67-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03a67-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a67-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03a67-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a67-169">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="03a67-169">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="03a67-170">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="03a67-170">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
