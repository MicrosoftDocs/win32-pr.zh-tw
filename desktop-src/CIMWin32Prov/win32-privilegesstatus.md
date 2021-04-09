---
description: Win32 \_ PrivilegesStatus&\# 8194;WMI 類別會報告完成作業所需許可權的相關資訊。 當作業失敗或已傳回部分填入的實例時，可能會傳回它。
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: 'Win32_PrivilegesStatus 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab399ce08374a954b3bbc015cfee7b4d20167b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847316"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a><span data-ttu-id="f9dd3-104">Win32_PrivilegesStatus 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="f9dd3-104">Win32_PrivilegesStatus class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f9dd3-105">**Win32 \_ PrivilegesStatus** [WMI 類別](../wmisdk/retrieving-a-class.md)會報告完成作業所需許可權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-105">The **Win32\_PrivilegesStatus** [WMI class](../wmisdk/retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="f9dd3-106">當作業失敗或已傳回部分填入的實例時，可能會傳回它。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="f9dd3-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f9dd3-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9dd3-109">語法</span><span class="sxs-lookup"><span data-stu-id="f9dd3-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a><span data-ttu-id="f9dd3-110">成員</span><span class="sxs-lookup"><span data-stu-id="f9dd3-110">Members</span></span>

<span data-ttu-id="f9dd3-111">**Win32 \_ PrivilegesStatus** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f9dd3-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="f9dd3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f9dd3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9dd3-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f9dd3-113">Properties</span></span>

<span data-ttu-id="f9dd3-114">**Win32 \_ PrivilegesStatus** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9dd3-115">**說明**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9dd3-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9dd3-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9dd3-118">描述錯誤或操作狀態的任何使用者定義字串。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="f9dd3-119">這個屬性繼承自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-119">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9dd3-120">**運算**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9dd3-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9dd3-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9dd3-123">發生失敗或異常時所發生的作業。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="f9dd3-124">一般來說，Windows Management Instrumentation (WMI) 會將這個屬性設定為 WMI 方法的 COM API 名稱，如下所示： [**IWbemServices：： CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum)。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="f9dd3-125">這個屬性繼承自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-125">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9dd3-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9dd3-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9dd3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9dd3-129">錯誤或狀態變更所涉及的參數。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="f9dd3-130">例如，如果應用程式嘗試取得不存在的類別，這個屬性會設定為違規的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="f9dd3-131">這個屬性繼承自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-131">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9dd3-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9dd3-133">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f9dd3-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9dd3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-135">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| AccessControl \| Windows NT 許可權" ) </span><span class="sxs-lookup"><span data-stu-id="f9dd3-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="f9dd3-136">列出完成操作所缺少的必要存取權限。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-136">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="f9dd3-137">您可以在 Windows 許可權下找到存取權限的類型。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-137">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="f9dd3-138">範例：「SE \_ 關機 \_ 名稱」</span><span class="sxs-lookup"><span data-stu-id="f9dd3-138">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="f9dd3-139">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-139">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9dd3-140">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f9dd3-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9dd3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-142">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| AccessControl \| Windows NT 許可權" ) </span><span class="sxs-lookup"><span data-stu-id="f9dd3-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="f9dd3-143">列出執行作業所需的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-143">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="f9dd3-144">這包括 **PrivilegesNotHeld** 屬性中的值。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-144">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="f9dd3-145">範例：「SE \_ 關機 \_ 名稱」</span><span class="sxs-lookup"><span data-stu-id="f9dd3-145">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="f9dd3-146">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-146">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9dd3-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9dd3-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9dd3-149">識別導致或報告錯誤或狀態變更的提供者。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-149">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="f9dd3-150">如果不牽涉到提供者，此字串會設定為「Windows 管理」。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-150">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="f9dd3-151">這個屬性繼承自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-151">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9dd3-152">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-152">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9dd3-153">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9dd3-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f9dd3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9dd3-155">包含作業的錯誤或資訊代碼。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-155">Contains an error or information code for an operation.</span></span> <span data-ttu-id="f9dd3-156">這可以是提供者所定義的任何值，但值 0 (零) 通常會保留以表示成功。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-156">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span>

<span data-ttu-id="f9dd3-157">這個屬性繼承自 [**\_ \_ NotifyStatus**](../wmisdk/--notifystatus.md)。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-157">This property is inherited from [**\_\_NotifyStatus**](../wmisdk/--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9dd3-158">備註</span><span class="sxs-lookup"><span data-stu-id="f9dd3-158">Remarks</span></span>

<span data-ttu-id="f9dd3-159">**Win32 \_ PrivilegesStatus** 類別衍生自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="f9dd3-159">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9dd3-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9dd3-160">Requirements</span></span>



| <span data-ttu-id="f9dd3-161">需求</span><span class="sxs-lookup"><span data-stu-id="f9dd3-161">Requirement</span></span> | <span data-ttu-id="f9dd3-162">值</span><span class="sxs-lookup"><span data-stu-id="f9dd3-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dd3-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9dd3-163">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dd3-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9dd3-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9dd3-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9dd3-165">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dd3-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9dd3-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9dd3-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="f9dd3-167">Namespace</span></span><br/>                | <span data-ttu-id="f9dd3-168">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f9dd3-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f9dd3-169">MOF</span><span class="sxs-lookup"><span data-stu-id="f9dd3-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9dd3-170"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9dd3-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9dd3-171">DLL</span><span class="sxs-lookup"><span data-stu-id="f9dd3-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9dd3-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9dd3-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9dd3-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9dd3-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9dd3-174">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="f9dd3-174">**\_\_ExtendedStatus**</span></span>](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
