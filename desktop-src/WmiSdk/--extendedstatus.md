---
description: 用來報告詳細的狀態和錯誤資訊。
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: __ExtendedStatus 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975334"
---
# <a name="__extendedstatus-class"></a><span data-ttu-id="88967-103">\_\_ExtendedStatus 類別</span><span class="sxs-lookup"><span data-stu-id="88967-103">\_\_ExtendedStatus class</span></span>

<span data-ttu-id="88967-104">**\_ \_ ExtendedStatus** 系統類別可用來報告詳細的狀態和錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="88967-104">The **\_\_ExtendedStatus** system class is used to report detailed status and error information.</span></span>

<span data-ttu-id="88967-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="88967-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="88967-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="88967-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88967-107">語法</span><span class="sxs-lookup"><span data-stu-id="88967-107">Syntax</span></span>

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="88967-108">成員</span><span class="sxs-lookup"><span data-stu-id="88967-108">Members</span></span>

<span data-ttu-id="88967-109">**\_ \_ ExtendedStatus** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="88967-109">The **\_\_ExtendedStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="88967-110">屬性</span><span class="sxs-lookup"><span data-stu-id="88967-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88967-111">屬性</span><span class="sxs-lookup"><span data-stu-id="88967-111">Properties</span></span>

<span data-ttu-id="88967-112">**\_ \_ ExtendedStatus** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="88967-112">The **\_\_ExtendedStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88967-113">**說明**</span><span class="sxs-lookup"><span data-stu-id="88967-113">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88967-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88967-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88967-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88967-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88967-116">描述錯誤或操作狀態的任何使用者定義字串。</span><span class="sxs-lookup"><span data-stu-id="88967-116">Any user-defined string that describes an error or operational status.</span></span>

</dd> <dt>

<span data-ttu-id="88967-117">**運算**</span><span class="sxs-lookup"><span data-stu-id="88967-117">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88967-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88967-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88967-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88967-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88967-120">發生失敗或異常時所發生的作業。</span><span class="sxs-lookup"><span data-stu-id="88967-120">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="88967-121">一般來說，Windows Management Instrumentation (WMI) 會將這個屬性設定為 WMI 方法的 COM API 名稱，如下所示： [**IWbemServices：： CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)。</span><span class="sxs-lookup"><span data-stu-id="88967-121">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

</dd> <dt>

<span data-ttu-id="88967-122">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="88967-122">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88967-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88967-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88967-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88967-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88967-125">錯誤或狀態變更所涉及的參數。</span><span class="sxs-lookup"><span data-stu-id="88967-125">Parameters involved in an error or status change.</span></span> <span data-ttu-id="88967-126">例如，如果應用程式嘗試取得不存在的類別，這個屬性會設定為違規的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="88967-126">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

</dd> <dt>

<span data-ttu-id="88967-127">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="88967-127">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88967-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88967-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88967-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88967-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88967-130">識別導致或報告錯誤或狀態變更的提供者。</span><span class="sxs-lookup"><span data-stu-id="88967-130">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="88967-131">如果不牽涉到提供者，此字串會設定為「Windows 管理」。</span><span class="sxs-lookup"><span data-stu-id="88967-131">If a provider is not involved, this string is set to "Windows Management".</span></span>

</dd> <dt>

<span data-ttu-id="88967-132">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="88967-132">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88967-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88967-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88967-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88967-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88967-135">包含作業的錯誤或資訊代碼。</span><span class="sxs-lookup"><span data-stu-id="88967-135">Contains an error or information code for an operation.</span></span> <span data-ttu-id="88967-136">這可以是提供者所定義的任何值，但值 0 (零) 通常會保留以表示成功。</span><span class="sxs-lookup"><span data-stu-id="88967-136">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="88967-137">這個屬性繼承自 [**\_ \_ NotifyStatus**](--notifystatus.md)。</span><span class="sxs-lookup"><span data-stu-id="88967-137">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88967-138">備註</span><span class="sxs-lookup"><span data-stu-id="88967-138">Remarks</span></span>

<span data-ttu-id="88967-139">**\_ \_ ExtendedStatus** 類別衍生自 [**\_ \_ NotifyStatus**](--notifystatus.md)類別。</span><span class="sxs-lookup"><span data-stu-id="88967-139">The **\_\_ExtendedStatus** class is derived from the [**\_\_NotifyStatus**](--notifystatus.md) class.</span></span>

<span data-ttu-id="88967-140">您可以使用 **\_ \_ ExtendedStatus** 類別來報告比簡單的結果碼更複雜的資訊。</span><span class="sxs-lookup"><span data-stu-id="88967-140">Use the **\_\_ExtendedStatus** class to report information that is more complex than a simple result code.</span></span> <span data-ttu-id="88967-141">如果提供者需要更多屬性來描述錯誤，則可以從 **\_ \_ ExtendedStatus** 衍生自己的類別。</span><span class="sxs-lookup"><span data-stu-id="88967-141">Providers can derive their own classes from **\_\_ExtendedStatus** if they require more properties to describe the errors.</span></span>

<span data-ttu-id="88967-142">**StatusCode** 屬性（繼承自 [**\_ \_ NotifyStatus**](--notifystatus.md)父類別）是一個不帶正負號的整數，代表錯誤或狀態值。</span><span class="sxs-lookup"><span data-stu-id="88967-142">The **StatusCode** property, inherited from the [**\_\_NotifyStatus**](--notifystatus.md) parent class, is an unsigned integer that represents the error or status value.</span></span> <span data-ttu-id="88967-143">當動態提供者從方法傳回這個類別的實例時， **StatusCode** 和 **Description** 屬性是由提供者設定，而其他屬性則由 WMI 設定。</span><span class="sxs-lookup"><span data-stu-id="88967-143">When instances of this class are returned from a method by a dynamic provider, the **StatusCode** and **Description** properties are set by the provider, and the other properties are set by WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="88967-144">範例</span><span class="sxs-lookup"><span data-stu-id="88967-144">Examples</span></span>

<span data-ttu-id="88967-145">下列程式碼範例（取自 [FND：如何使用](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa)TechNet 資源庫上的 WMI VBScript 程式碼範例處理設定管理員非同步錯誤）說明如何使用 **\_ \_ ExtendedStatus** 來取得錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="88967-145">The following code sample, taken from the [FND:How to Handle Configuration Manager Asynchronous Errors by Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example on TechNet Gallery, describes using **\_\_ExtendedStatus** to retrieve error information.</span></span>


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a><span data-ttu-id="88967-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="88967-146">Requirements</span></span>



| <span data-ttu-id="88967-147">需求</span><span class="sxs-lookup"><span data-stu-id="88967-147">Requirement</span></span> | <span data-ttu-id="88967-148">值</span><span class="sxs-lookup"><span data-stu-id="88967-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="88967-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88967-149">Minimum supported client</span></span><br/> | <span data-ttu-id="88967-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88967-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="88967-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88967-151">Minimum supported server</span></span><br/> | <span data-ttu-id="88967-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88967-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="88967-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="88967-153">Namespace</span></span><br/>                | <span data-ttu-id="88967-154">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="88967-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="88967-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88967-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88967-156">**\_\_NotifyStatus**</span><span class="sxs-lookup"><span data-stu-id="88967-156">**\_\_NotifyStatus**</span></span>](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[<span data-ttu-id="88967-157">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="88967-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

