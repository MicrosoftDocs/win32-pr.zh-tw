---
description: Win32 \_ PrivilegesStatus &\# 8194;WMI 類別會報告完成作業所需許可權的相關資訊。 當作業失敗或已傳回部分填入的實例時，可能會傳回它。
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: " (WMI) 的 Win32_PrivilegesStatus 類別"
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
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 658803be4e70849531bf52e7368e4e9cbcc2f0a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195217"
---
# <a name="win32_privilegesstatus-class-wmi"></a><span data-ttu-id="50245-104"> (WMI) 的 Win32_PrivilegesStatus 類別</span><span class="sxs-lookup"><span data-stu-id="50245-104">Win32_PrivilegesStatus class (WMI)</span></span>

<span data-ttu-id="50245-105">**Win32 \_ PrivilegesStatus**[WMI 類別](retrieving-a-class.md)會報告完成作業所需許可權的相關資訊。   </span><span class="sxs-lookup"><span data-stu-id="50245-105">The **Win32\_PrivilegesStatus**   [WMI class](retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="50245-106">當作業失敗或已傳回部分填入的實例時，可能會傳回它。</span><span class="sxs-lookup"><span data-stu-id="50245-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="50245-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="50245-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="50245-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="50245-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="50245-109">語法</span><span class="sxs-lookup"><span data-stu-id="50245-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
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

## <a name="members"></a><span data-ttu-id="50245-110">成員</span><span class="sxs-lookup"><span data-stu-id="50245-110">Members</span></span>

<span data-ttu-id="50245-111">**Win32 \_ PrivilegesStatus** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="50245-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="50245-112">屬性</span><span class="sxs-lookup"><span data-stu-id="50245-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50245-113">屬性</span><span class="sxs-lookup"><span data-stu-id="50245-113">Properties</span></span>

<span data-ttu-id="50245-114">**Win32 \_ PrivilegesStatus** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="50245-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50245-115">**說明**</span><span class="sxs-lookup"><span data-stu-id="50245-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50245-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50245-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50245-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50245-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50245-118">描述錯誤或操作狀態的任何使用者定義字串。</span><span class="sxs-lookup"><span data-stu-id="50245-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="50245-119">這個屬性繼承自 [**\_ \_ ExtendedStatus**](--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="50245-119">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="50245-120">**運算**</span><span class="sxs-lookup"><span data-stu-id="50245-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50245-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50245-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50245-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50245-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50245-123">發生失敗或異常時所發生的作業。</span><span class="sxs-lookup"><span data-stu-id="50245-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="50245-124">一般來說，Windows Management Instrumentation (WMI) 會將這個屬性設定為 WMI 方法的 COM API 名稱，如下所示： [**IWbemServices：： CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)。</span><span class="sxs-lookup"><span data-stu-id="50245-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="50245-125">這個屬性繼承自 [**\_ \_ ExtendedStatus**](--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="50245-125">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="50245-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="50245-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50245-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50245-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50245-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50245-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50245-129">錯誤或狀態變更所涉及的參數。</span><span class="sxs-lookup"><span data-stu-id="50245-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="50245-130">例如，如果應用程式嘗試取得不存在的類別，這個屬性會設定為違規的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="50245-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="50245-131">這個屬性繼承自 [**\_ \_ ExtendedStatus**](--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="50245-131">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="50245-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="50245-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50245-133">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="50245-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="50245-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50245-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50245-135">列出完成操作所缺少的必要存取權限。</span><span class="sxs-lookup"><span data-stu-id="50245-135">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="50245-136">您可以在 Windows 許可權下找到存取權限的類型。</span><span class="sxs-lookup"><span data-stu-id="50245-136">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="50245-137">範例：「SE \_ 關機 \_ 名稱」</span><span class="sxs-lookup"><span data-stu-id="50245-137">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="50245-138">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="50245-138">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50245-139">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="50245-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="50245-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50245-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50245-141">列出執行作業所需的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="50245-141">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="50245-142">這包括 **PrivilegesNotHeld** 屬性中的值。</span><span class="sxs-lookup"><span data-stu-id="50245-142">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="50245-143">範例：「SE \_ 關機 \_ 名稱」</span><span class="sxs-lookup"><span data-stu-id="50245-143">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="50245-144">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="50245-144">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50245-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50245-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50245-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50245-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50245-147">識別導致或報告錯誤或狀態變更的提供者。</span><span class="sxs-lookup"><span data-stu-id="50245-147">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="50245-148">如果不牽涉到提供者，此字串會設定為「Windows 管理」。</span><span class="sxs-lookup"><span data-stu-id="50245-148">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="50245-149">這個屬性繼承自 [**\_ \_ ExtendedStatus**](--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="50245-149">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="50245-150">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="50245-150">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50245-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="50245-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50245-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50245-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50245-153">包含作業的錯誤或資訊代碼。</span><span class="sxs-lookup"><span data-stu-id="50245-153">Contains an error or information code for an operation.</span></span> <span data-ttu-id="50245-154">這可以是提供者所定義的任何值，但值 0 (零) 通常會保留以表示成功。</span><span class="sxs-lookup"><span data-stu-id="50245-154">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="50245-155">這個屬性繼承自 [**\_ \_ NotifyStatus**](--notifystatus.md)。</span><span class="sxs-lookup"><span data-stu-id="50245-155">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50245-156">備註</span><span class="sxs-lookup"><span data-stu-id="50245-156">Remarks</span></span>

<span data-ttu-id="50245-157">**Win32 \_ PrivilegesStatus** 類別衍生自 [**\_ \_ ExtendedStatus**](--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="50245-157">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50245-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="50245-158">Requirements</span></span>



| <span data-ttu-id="50245-159">需求</span><span class="sxs-lookup"><span data-stu-id="50245-159">Requirement</span></span> | <span data-ttu-id="50245-160">值</span><span class="sxs-lookup"><span data-stu-id="50245-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50245-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50245-161">Minimum supported client</span></span><br/> | <span data-ttu-id="50245-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50245-162">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="50245-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50245-163">Minimum supported server</span></span><br/> | <span data-ttu-id="50245-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50245-164">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="50245-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="50245-165">Namespace</span></span><br/>                | <span data-ttu-id="50245-166">根 \\ WMI</span><span class="sxs-lookup"><span data-stu-id="50245-166">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="50245-167">MOF</span><span class="sxs-lookup"><span data-stu-id="50245-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50245-168"><dt>Wmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50245-168"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50245-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50245-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50245-170">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="50245-170">**\_\_ExtendedStatus**</span></span>](--extendedstatus.md)
</dt> </dl>

 

 




