---
description: 以下列出用來定義 View 提供者類別的限定詞。
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: 視圖提供者專用的限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194143"
---
# <a name="qualifiers-specific-to-the-view-provider"></a><span data-ttu-id="34572-103">視圖提供者專用的限定詞</span><span class="sxs-lookup"><span data-stu-id="34572-103">Qualifiers Specific to the View Provider</span></span>

<span data-ttu-id="34572-104">以下列出用來定義 View 提供者類別的限定詞。</span><span class="sxs-lookup"><span data-stu-id="34572-104">The following lists the qualifiers use to define View Provider classes.</span></span>

> [!Note]  
> <span data-ttu-id="34572-105">視圖提供者類別在使用遠端參考時，僅支援 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="34572-105">The View provider class only supports NetBIOS names when using remote references.</span></span> <span data-ttu-id="34572-106">如果您在遠端參考中使用 IP 位址或 DNS 名稱，則連線會失敗並出現0x800706ba 錯誤。</span><span class="sxs-lookup"><span data-stu-id="34572-106">If you use an IP address or a DNS name in a remote reference, then the connection fails with a 0x800706ba error.</span></span>

 

<dt>

<span data-ttu-id="34572-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**直接**</span><span class="sxs-lookup"><span data-stu-id="34572-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Direct**</span></span>
</dt> <dd>

<span data-ttu-id="34572-108">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="34572-108">Data type: **boolean**</span></span>

<span data-ttu-id="34572-109">與 view 關聯屬性一起使用，以防止關聯參考對應至 view 參考。</span><span class="sxs-lookup"><span data-stu-id="34572-109">Used with view association properties to prevent association references from being mapped to a view reference.</span></span>

<span data-ttu-id="34572-110">下列範例會將屬性 **GroupComponent** 定義為未在 view 參考中對應的關聯參考。</span><span class="sxs-lookup"><span data-stu-id="34572-110">The following example defines the property **GroupComponent** as an association reference that is not mapped in the view reference.</span></span>


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span data-ttu-id="34572-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span><span class="sxs-lookup"><span data-stu-id="34572-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span></span>
</dt> <dd>

<span data-ttu-id="34572-112">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="34572-112">Data type: **boolean**</span></span>

<span data-ttu-id="34572-113">根據具有不同預設值之來源類別屬性的視圖類別屬性預設值。</span><span class="sxs-lookup"><span data-stu-id="34572-113">Default value for a view class property based on a source class property with a different default value.</span></span> <span data-ttu-id="34572-114">基礎來源類別是由視圖隱含的。</span><span class="sxs-lookup"><span data-stu-id="34572-114">The underlying source class is implied by the view.</span></span>

<span data-ttu-id="34572-115">例如，來源類別 [**Win32 \_ register-scheduledjob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) 具有 [布林值](boolean.md) 屬性 **RunRepeatedly** ，指出是否要定期或只執行一次作業。</span><span class="sxs-lookup"><span data-stu-id="34572-115">For example, the source class [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) has a [boolean](boolean.md) property **RunRepeatedly** that indicates whether the job is to be carried out periodically or one time only.</span></span> <span data-ttu-id="34572-116">**Win32 \_ register-scheduledjob** 的預設值 **RunRepeatedly** 不是 true，但 view 類別的預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="34572-116">The default value of **RunRepeatedly** is not True for **Win32\_ScheduledJob**, but is True for the view class.</span></span>


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span data-ttu-id="34572-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span><span class="sxs-lookup"><span data-stu-id="34572-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span></span>
</dt> <dd>

<span data-ttu-id="34572-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="34572-118">Data type: **string**</span></span>

<span data-ttu-id="34572-119">定義在聯結視圖類別中聯結來源類別實例的方式。</span><span class="sxs-lookup"><span data-stu-id="34572-119">Defines how source class instances are joined in join view classes.</span></span> <span data-ttu-id="34572-120">下列範例顯示如何使用 **JoinOn** 限定詞來聯結兩個來源類別。</span><span class="sxs-lookup"><span data-stu-id="34572-120">The following example shows how to use the **JoinOn** qualifier to join two source classes.</span></span>


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span data-ttu-id="34572-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span><span class="sxs-lookup"><span data-stu-id="34572-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span></span>
</dt> <dd>

<span data-ttu-id="34572-122">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="34572-122">Data type: **string array**</span></span>

<span data-ttu-id="34572-123">要針對 view 方法執行的來源方法。</span><span class="sxs-lookup"><span data-stu-id="34572-123">Source method to execute for the view method.</span></span> <span data-ttu-id="34572-124">如需類似的語法，請參閱 [PropertySources 限定詞](propertysources-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="34572-124">For similar syntax, see [PropertySources Qualifier](propertysources-qualifier.md).</span></span> <span data-ttu-id="34572-125">方法的簽章必須完全符合來源類別的簽章。</span><span class="sxs-lookup"><span data-stu-id="34572-125">The signature of the method must match the signature of the source class exactly.</span></span> <span data-ttu-id="34572-126">從定義來源類別的 MOF 檔案複製方法簽章。</span><span class="sxs-lookup"><span data-stu-id="34572-126">Copy the method signature from the MOF file that defines the source class.</span></span> <span data-ttu-id="34572-127">下列範例會從 [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))的 [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile)方法定義方法：</span><span class="sxs-lookup"><span data-stu-id="34572-127">The example below defines a method from the [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) method of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span></span>


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



<span data-ttu-id="34572-128">只有在搭配聯集視圖使用時，此限定詞才有效。</span><span class="sxs-lookup"><span data-stu-id="34572-128">This qualifier is only valid when it is used with union views.</span></span>

</dd> <dt>

<span data-ttu-id="34572-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="34572-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="34572-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="34572-130">Data type: **string**</span></span>

<span data-ttu-id="34572-131">WQL 查詢在聯結類別聯結之後篩選實例。</span><span class="sxs-lookup"><span data-stu-id="34572-131">WQL query to filter instances after they have been joined in a join class.</span></span>

</dd> <dt>

<span data-ttu-id="34572-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="34572-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="34572-133">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="34572-133">Data type: **string array**</span></span>

<span data-ttu-id="34572-134">View 類別屬性從中取得資料的來源屬性。</span><span class="sxs-lookup"><span data-stu-id="34572-134">Source properties from which a view class property gets data.</span></span>

</dd> <dt>

<span data-ttu-id="34572-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**聯盟**</span><span class="sxs-lookup"><span data-stu-id="34572-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**</span></span>
</dt> <dd>

<span data-ttu-id="34572-136">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="34572-136">Data type: **boolean**</span></span>

<span data-ttu-id="34572-137">指出您是否要定義聯集類別。</span><span class="sxs-lookup"><span data-stu-id="34572-137">Indicates whether you are defining a union class.</span></span> <span data-ttu-id="34572-138">聯集視圖包含以來源實例聯集為基礎的實例。</span><span class="sxs-lookup"><span data-stu-id="34572-138">Union views contain instances based on the union of source instances.</span></span> <span data-ttu-id="34572-139">例如，您可以宣告下列各項：</span><span class="sxs-lookup"><span data-stu-id="34572-139">For example, you might declare the following:</span></span>


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span data-ttu-id="34572-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="34572-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="34572-141">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="34572-141">Data type: **string array**</span></span>

<span data-ttu-id="34572-142">WMI 查詢語言 (WQL) 查詢的集合，可定義特定視圖類別中所使用的來源實例和屬性。</span><span class="sxs-lookup"><span data-stu-id="34572-142">Set of WMI Query Language (WQL) queries that define the source instances and properties used in a specific view class.</span></span> <span data-ttu-id="34572-143">所有陣列限定詞的位置對應都很重要。</span><span class="sxs-lookup"><span data-stu-id="34572-143">Positional correspondence of all the array qualifiers is important.</span></span>

</dd> <dt>

<span data-ttu-id="34572-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="34572-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="34572-145">資料類型： **字串陣列**</span><span class="sxs-lookup"><span data-stu-id="34572-145">Data type: **string array**</span></span>

<span data-ttu-id="34572-146">來源實例所在的命名空間。</span><span class="sxs-lookup"><span data-stu-id="34572-146">Namespaces where the source instances are located.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34572-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="34572-147">Requirements</span></span>



| <span data-ttu-id="34572-148">需求</span><span class="sxs-lookup"><span data-stu-id="34572-148">Requirement</span></span> | <span data-ttu-id="34572-149">值</span><span class="sxs-lookup"><span data-stu-id="34572-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="34572-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34572-150">Minimum supported client</span></span><br/> | <span data-ttu-id="34572-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34572-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="34572-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34572-152">Minimum supported server</span></span><br/> | <span data-ttu-id="34572-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34572-153">Windows Server 2008</span></span><br/> |



 

