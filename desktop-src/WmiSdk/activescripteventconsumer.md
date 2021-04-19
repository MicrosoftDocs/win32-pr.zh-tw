---
description: 當事件傳遞給它時，以任意指令碼語言執行預先定義的腳本。
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: ActiveScriptEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997892"
---
# <a name="activescripteventconsumer-class"></a><span data-ttu-id="fba47-103">ActiveScriptEventConsumer 類別</span><span class="sxs-lookup"><span data-stu-id="fba47-103">ActiveScriptEventConsumer class</span></span>

<span data-ttu-id="fba47-104">當事件傳遞給它時， **ActiveScriptEventConsumer** 類別會以任意指令碼語言執行預先定義的腳本。</span><span class="sxs-lookup"><span data-stu-id="fba47-104">The **ActiveScriptEventConsumer** class runs a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span> <span data-ttu-id="fba47-105">此類別是 WMI 提供的其中一個標準事件取用者。</span><span class="sxs-lookup"><span data-stu-id="fba47-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="fba47-106">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="fba47-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



<span data-ttu-id="fba47-107">您可以在 **ScriptingStandardConsumerSetting** 的單一實例中設定 [**Timeout**](scriptingstandardconsumersetting.md)或 **MaximumScripts** 屬性的值，以設定系統上所有 **ActiveScriptEventConsumer** 實例的效能。</span><span class="sxs-lookup"><span data-stu-id="fba47-107">You can configure the performance of all instances of **ActiveScriptEventConsumer** on a system by setting the values of either the [**Timeout**](scriptingstandardconsumersetting.md) or **MaximumScripts** property in the single instance of **ScriptingStandardConsumerSetting**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba47-108">語法</span><span class="sxs-lookup"><span data-stu-id="fba47-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a><span data-ttu-id="fba47-109">成員</span><span class="sxs-lookup"><span data-stu-id="fba47-109">Members</span></span>

<span data-ttu-id="fba47-110">**ActiveScriptEventConsumer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fba47-110">The **ActiveScriptEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="fba47-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fba47-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fba47-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fba47-112">Properties</span></span>

<span data-ttu-id="fba47-113">**ActiveScriptEventConsumer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fba47-113">The **ActiveScriptEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fba47-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="fba47-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba47-115">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="fba47-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fba47-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fba47-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fba47-117">陣列，代表 (SID) 的安全識別碼，該識別碼可唯一識別作用中腳本事件取用者的建立者。</span><span class="sxs-lookup"><span data-stu-id="fba47-117">Array that represents the security identifier (SID), which uniquely identifies the creator of the Active Script Event consumer.</span></span> <span data-ttu-id="fba47-118">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="fba47-118">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fba47-119">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="fba47-119">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba47-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fba47-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fba47-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fba47-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fba47-122">允許腳本執行的數目（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="fba47-122">Number, in seconds, that the script is allowed to run.</span></span> <span data-ttu-id="fba47-123">如果 0 (零) （預設值），則腳本不會終止。</span><span class="sxs-lookup"><span data-stu-id="fba47-123">If 0 (zero), which is the default, the script is not terminated.</span></span>

</dd> <dt>

<span data-ttu-id="fba47-124">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="fba47-124">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba47-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fba47-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba47-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fba47-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fba47-127">WMI 傳送事件的目標電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="fba47-127">Name of the computer to which WMI sends events.</span></span> <span data-ttu-id="fba47-128">依照 Microsoft 標準取用者的慣例，腳本取用者無法從遠端執行。</span><span class="sxs-lookup"><span data-stu-id="fba47-128">By convention of Microsoft standard consumers, the script consumer cannot be run remotely.</span></span> <span data-ttu-id="fba47-129">協力廠商取用者也可以使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="fba47-129">Third-party consumers can also use this property.</span></span> <span data-ttu-id="fba47-130">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="fba47-130">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fba47-131">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="fba47-131">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba47-132">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fba47-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fba47-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fba47-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fba47-134">動態指令碼事件取用者的最大佇列（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fba47-134">Maximum queue, in bytes, for the Active Script Event consumer.</span></span> <span data-ttu-id="fba47-135">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="fba47-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="fba47-136">**名稱**</span><span class="sxs-lookup"><span data-stu-id="fba47-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba47-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fba47-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba47-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fba47-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fba47-139">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fba47-139">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fba47-140">事件取用者的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fba47-140">Unique identifier for the event consumer.</span></span> <span data-ttu-id="fba47-141">如果您重新命名取用者，結果會是兩個具有不同名稱的相同取用者。</span><span class="sxs-lookup"><span data-stu-id="fba47-141">If you rename the consumer, the result is two equal consumers that have different names.</span></span>

</dd> <dt>

<span data-ttu-id="fba47-142">**ScriptFileName**</span><span class="sxs-lookup"><span data-stu-id="fba47-142">**ScriptFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba47-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fba47-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba47-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fba47-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fba47-145">用來讀取腳本文字之檔案的名稱，目的是在 **ScriptText** 屬性中指定腳本文字的替代方案。</span><span class="sxs-lookup"><span data-stu-id="fba47-145">Name of the file from which the script text is read, intended as an alternative to specifying the text of the script in the **ScriptText** property.</span></span> <span data-ttu-id="fba47-146">如果 **ScriptText** 屬性不是 **null**，則這個屬性必須是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="fba47-146">This property must be **NULL** if the **ScriptText** property is not **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="fba47-147">當您指定 **ScriptFileName** 時，請務必保護您正在啟動的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="fba47-147">When you specify the **ScriptFileName**, it is important to secure the executable that you are launching.</span></span> <span data-ttu-id="fba47-148">如果可執行檔不在安全的位置，或使用強式存取控制清單來保護 (ACL) ，任何人都可以使用不同的可執行檔來取代該可執行檔。</span><span class="sxs-lookup"><span data-stu-id="fba47-148">If the executable is not in a secure location or secured with a strong access control list (ACL), anyone can replace the executable with a different one.</span></span> <span data-ttu-id="fba47-149">如需 Acl 的詳細資訊，請參閱 [在 c + + 中為新物件建立安全描述項 (SD) ](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="fba47-149">For more information about ACLs, see [Creating a Security Descriptor (SD) for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="fba47-150">**ScriptingEngine**</span><span class="sxs-lookup"><span data-stu-id="fba47-150">**ScriptingEngine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba47-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fba47-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba47-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fba47-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fba47-153">要使用的腳本引擎名稱，例如「VBScript」。</span><span class="sxs-lookup"><span data-stu-id="fba47-153">Name of the scripting engine to use, for example, "VBScript".</span></span> <span data-ttu-id="fba47-154">這個屬性不能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fba47-154">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fba47-155">**ScriptText**</span><span class="sxs-lookup"><span data-stu-id="fba47-155">**ScriptText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba47-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fba47-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba47-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fba47-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fba47-158">腳本的文字，以腳本引擎已知的語言表示。</span><span class="sxs-lookup"><span data-stu-id="fba47-158">Text of the script that is expressed in a language known to the scripting engine.</span></span> <span data-ttu-id="fba47-159">如果 **ScriptFileName** 屬性不是 **null**，則這個屬性必須是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="fba47-159">This property must be **NULL** if the **ScriptFileName** property is not **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fba47-160">備註</span><span class="sxs-lookup"><span data-stu-id="fba47-160">Remarks</span></span>

<span data-ttu-id="fba47-161">這個類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。</span><span class="sxs-lookup"><span data-stu-id="fba47-161">This class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span> <span data-ttu-id="fba47-162">它位於根訂用帳戶 \\ 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="fba47-162">It is located in the root\\subscription namespace.</span></span>

<span data-ttu-id="fba47-163">當「事件取用者」實例中指定腳本的文字時，腳本就可以存取腳本環境變數 **TargetEvent** 中的事件實例。</span><span class="sxs-lookup"><span data-stu-id="fba47-163">When the text of a script is specified in the event consumer instance, the script has access to the event instance in the script environment variable **TargetEvent**.</span></span>

<span data-ttu-id="fba47-164">腳本會在 LocalSystem 安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="fba47-164">The scripts run in the LocalSystem security context.</span></span> <span data-ttu-id="fba47-165">做為安全性措施，只有本機系統管理員或網域系統管理員可以設定腳本取用者。</span><span class="sxs-lookup"><span data-stu-id="fba47-165">As a security measure, only a local system administrator or a domain administrator can configure the scripting consumer.</span></span> <span data-ttu-id="fba47-166">在執行時間之前不會檢查存取權限。</span><span class="sxs-lookup"><span data-stu-id="fba47-166">Access rights are not checked until run time.</span></span> <span data-ttu-id="fba47-167">當取用者設定好之後，任何使用者都可以觸發引發腳本的事件。</span><span class="sxs-lookup"><span data-stu-id="fba47-167">After the consumer is configured, any user can trigger the event that causes the script to .</span></span>

<span data-ttu-id="fba47-168">無法載入腳本引擎或剖析和驗證腳本會視為失敗。</span><span class="sxs-lookup"><span data-stu-id="fba47-168">Failure to load the scripting engine or parse and validate the script is considered a failure.</span></span> <span data-ttu-id="fba47-169">從腳本傳回錯誤碼，並使用超時來終止腳本，也會視為失敗。</span><span class="sxs-lookup"><span data-stu-id="fba47-169">Error return codes from the script and terminating the script by using a time-out are also considered failures.</span></span>

<span data-ttu-id="fba47-170">**ScriptText** 或 **ScriptFileName** 不能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fba47-170">Either **ScriptText** or **ScriptFileName** must be not **NULL**.</span></span> <span data-ttu-id="fba47-171">如果這兩個屬性都是 **null** 或 not **null**，則會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="fba47-171">If both properties are **NULL** or not **NULL**, an error is generated.</span></span>

<span data-ttu-id="fba47-172">當 WMI 以服務的形式執行時，由 **ActiveScriptEventConsumer** 執行的腳本不會產生螢幕輸出。</span><span class="sxs-lookup"><span data-stu-id="fba47-172">When WMI is run as a service, scripts run by **ActiveScriptEventConsumer** do not generate screen output.</span></span> <span data-ttu-id="fba47-173">使用 **MsgBox** 的腳本會執行，但不會在螢幕上顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="fba47-173">Scripts that use **MsgBox** do run, but they do not display information on the screen.</span></span> <span data-ttu-id="fba47-174">不支援執行 WMI 服務作為可執行檔，但 WMI 允許使用 **MsgBox** 函數的腳本顯示輸出或接受使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="fba47-174">Running the WMI service as an executable file is not supported, but WMI allows scripts that use the **MsgBox** function to display output or accept user input.</span></span> <span data-ttu-id="fba47-175">[Wscript.echo](/previous-versions//at5ydy31(v=vs.85))物件提供的方法都不能使用，因為 **ActiveScriptEventConsumer** 不會使用 WINDOWS Script Host (WSH) 。</span><span class="sxs-lookup"><span data-stu-id="fba47-175">None of the methods provided by the [WScript](/previous-versions//at5ydy31(v=vs.85)) object can be used because **ActiveScriptEventConsumer** does not use Windows Script Host (WSH).</span></span>

## <a name="examples"></a><span data-ttu-id="fba47-176">範例</span><span class="sxs-lookup"><span data-stu-id="fba47-176">Examples</span></span>

<span data-ttu-id="fba47-177">在 TechNet 資源庫上 [建立永久性 Wmi 事件註冊來監視](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) 檔案 PowerShell 範例使用 **ActiveScriptEventConsumer** 做為複雜字集的一部分，以設定永久的 wmi 事件註冊。</span><span class="sxs-lookup"><span data-stu-id="fba47-177">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **ActiveScriptEventConsumer** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba47-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="fba47-178">Requirements</span></span>



| <span data-ttu-id="fba47-179">需求</span><span class="sxs-lookup"><span data-stu-id="fba47-179">Requirement</span></span> | <span data-ttu-id="fba47-180">值</span><span class="sxs-lookup"><span data-stu-id="fba47-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fba47-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fba47-181">Minimum supported client</span></span><br/> | <span data-ttu-id="fba47-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fba47-182">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fba47-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fba47-183">Minimum supported server</span></span><br/> | <span data-ttu-id="fba47-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fba47-184">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fba47-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="fba47-185">Namespace</span></span><br/>                | <span data-ttu-id="fba47-186">根 \\ 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="fba47-186">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="fba47-187">MOF</span><span class="sxs-lookup"><span data-stu-id="fba47-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fba47-188"><dt>Scrcons mof</dt></span><span class="sxs-lookup"><span data-stu-id="fba47-188"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="fba47-189">DLL</span><span class="sxs-lookup"><span data-stu-id="fba47-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba47-190"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fba47-190"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba47-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fba47-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba47-192">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="fba47-192">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="fba47-193">根據事件執行腳本</span><span class="sxs-lookup"><span data-stu-id="fba47-193">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="fba47-194">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="fba47-194">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="fba47-195">建立邏輯取用者</span><span class="sxs-lookup"><span data-stu-id="fba47-195">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="fba47-196">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="fba47-196">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="fba47-197">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="fba47-197">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md)
</dt> </dl>

 

