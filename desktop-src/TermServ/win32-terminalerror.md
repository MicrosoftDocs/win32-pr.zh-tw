---
title: Win32_TerminalError 類別
description: 表示終端機錯誤。
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Win32_TerminalError 類別遠端桌面服務
- Win32_TerminalError 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094095"
---
# <a name="win32_terminalerror-class"></a><span data-ttu-id="7fce7-105">Win32 \_ TerminalError 類別</span><span class="sxs-lookup"><span data-stu-id="7fce7-105">Win32\_TerminalError class</span></span>

<span data-ttu-id="7fce7-106">表示終端機錯誤。</span><span class="sxs-lookup"><span data-stu-id="7fce7-106">Represents a terminal error.</span></span>

<span data-ttu-id="7fce7-107">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7fce7-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fce7-108">語法</span><span class="sxs-lookup"><span data-stu-id="7fce7-108">Syntax</span></span>

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="7fce7-109">成員</span><span class="sxs-lookup"><span data-stu-id="7fce7-109">Members</span></span>

<span data-ttu-id="7fce7-110">**Win32 \_ TerminalError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7fce7-110">The **Win32\_TerminalError** class has these types of members:</span></span>

-   [<span data-ttu-id="7fce7-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7fce7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fce7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7fce7-112">Properties</span></span>

<span data-ttu-id="7fce7-113">**Win32 \_ TerminalError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7fce7-113">The **Win32\_TerminalError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fce7-114">**說明**</span><span class="sxs-lookup"><span data-stu-id="7fce7-114">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fce7-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7fce7-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fce7-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fce7-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fce7-117">描述錯誤或操作狀態的任何使用者定義字串。</span><span class="sxs-lookup"><span data-stu-id="7fce7-117">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="7fce7-118">這個屬性繼承自 [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)。</span><span class="sxs-lookup"><span data-stu-id="7fce7-118">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="7fce7-119">**運算**</span><span class="sxs-lookup"><span data-stu-id="7fce7-119">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fce7-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7fce7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fce7-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fce7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fce7-122">發生失敗或異常時所發生的作業。</span><span class="sxs-lookup"><span data-stu-id="7fce7-122">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="7fce7-123">一般而言，WMI 會將此屬性設定為 WMI 方法的 COM API 名稱，如下所示： [**IWbemServices：： CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum)。</span><span class="sxs-lookup"><span data-stu-id="7fce7-123">Typically, WMI sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="7fce7-124">這個屬性繼承自 [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)。</span><span class="sxs-lookup"><span data-stu-id="7fce7-124">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="7fce7-125">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="7fce7-125">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fce7-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7fce7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fce7-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fce7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fce7-128">錯誤或狀態變更所涉及的參數。</span><span class="sxs-lookup"><span data-stu-id="7fce7-128">Parameters involved in an error or status change.</span></span> <span data-ttu-id="7fce7-129">例如，如果應用程式嘗試取得不存在的類別，這個屬性會設定為違規的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="7fce7-129">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="7fce7-130">這個屬性繼承自 [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)。</span><span class="sxs-lookup"><span data-stu-id="7fce7-130">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="7fce7-131">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="7fce7-131">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fce7-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7fce7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fce7-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fce7-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fce7-134">識別導致或報告錯誤或狀態變更的提供者。</span><span class="sxs-lookup"><span data-stu-id="7fce7-134">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="7fce7-135">如果不牽涉到提供者，此字串會設定為「Windows 管理」。</span><span class="sxs-lookup"><span data-stu-id="7fce7-135">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="7fce7-136">這個屬性繼承自 [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)。</span><span class="sxs-lookup"><span data-stu-id="7fce7-136">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="7fce7-137">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="7fce7-137">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fce7-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7fce7-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7fce7-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fce7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fce7-140">包含作業的錯誤或資訊代碼。</span><span class="sxs-lookup"><span data-stu-id="7fce7-140">Contains an error or information code for an operation.</span></span> <span data-ttu-id="7fce7-141">這可以是提供者所定義的任何值，但值 0 (零) 通常會保留以表示成功。</span><span class="sxs-lookup"><span data-stu-id="7fce7-141">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="7fce7-142">這個屬性繼承自 [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus)。</span><span class="sxs-lookup"><span data-stu-id="7fce7-142">This property is inherited from [**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span></span>

</dd> <dt>

<span data-ttu-id="7fce7-143">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="7fce7-143">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fce7-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7fce7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fce7-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7fce7-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fce7-146">發生錯誤之終端機 sin 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fce7-146">The name of the terminal sin which the error occurred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fce7-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fce7-147">Requirements</span></span>



| <span data-ttu-id="7fce7-148">需求</span><span class="sxs-lookup"><span data-stu-id="7fce7-148">Requirement</span></span> | <span data-ttu-id="7fce7-149">值</span><span class="sxs-lookup"><span data-stu-id="7fce7-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fce7-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fce7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7fce7-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fce7-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fce7-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fce7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7fce7-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fce7-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fce7-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="7fce7-154">Namespace</span></span><br/>                | <span data-ttu-id="7fce7-155">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="7fce7-155">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7fce7-156">MOF</span><span class="sxs-lookup"><span data-stu-id="7fce7-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fce7-157"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fce7-157"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fce7-158">DLL</span><span class="sxs-lookup"><span data-stu-id="7fce7-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fce7-159"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fce7-159"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fce7-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fce7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fce7-161">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="7fce7-161">**\_\_ExtendedStatus**</span></span>](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

