---
description: Singleton ScriptingStandardConsumerSetting 類別提供 ActiveScriptEventConsumer 標準取用者類別的所有實例通用的註冊資料。
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: ScriptingStandardConsumerSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192073"
---
# <a name="scriptingstandardconsumersetting-class"></a><span data-ttu-id="3b549-103">ScriptingStandardConsumerSetting 類別</span><span class="sxs-lookup"><span data-stu-id="3b549-103">ScriptingStandardConsumerSetting class</span></span>

<span data-ttu-id="3b549-104">Singleton **ScriptingStandardConsumerSetting** 類別提供 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 標準取用者類別的所有實例通用的註冊資料。</span><span class="sxs-lookup"><span data-stu-id="3b549-104">The singleton **ScriptingStandardConsumerSetting** class provides registration data that is common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) standard consumer class.</span></span> <span data-ttu-id="3b549-105">**ActiveScriptEventConsumer** 實例會使用 **MaximumScripts** 和 **Timeout** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3b549-105">An **ActiveScriptEventConsumer** instance uses the **MaximumScripts** and **Timeout** properties.</span></span> <span data-ttu-id="3b549-106">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="3b549-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="3b549-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b549-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3b549-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="3b549-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b549-109">語法</span><span class="sxs-lookup"><span data-stu-id="3b549-109">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a><span data-ttu-id="3b549-110">成員</span><span class="sxs-lookup"><span data-stu-id="3b549-110">Members</span></span>

<span data-ttu-id="3b549-111">**ScriptingStandardConsumerSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3b549-111">The **ScriptingStandardConsumerSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="3b549-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3b549-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b549-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3b549-113">Properties</span></span>

<span data-ttu-id="3b549-114">**ScriptingStandardConsumerSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3b549-114">The **ScriptingStandardConsumerSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b549-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="3b549-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b549-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b549-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b549-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b549-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b549-118">限定詞： [**MaxLen**](standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="3b549-118">Qualifiers: [**MaxLen**](standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3b549-119">物件的簡短描述（一行字串）。</span><span class="sxs-lookup"><span data-stu-id="3b549-119">A short description of an object a one line string.</span></span> <span data-ttu-id="3b549-120">包含字串 **ScriptingStandardConsumerSetting** ，因為這是單一類別。</span><span class="sxs-lookup"><span data-stu-id="3b549-120">Contains the string **ScriptingStandardConsumerSetting** because this is a singleton class.</span></span>

</dd> <dt>

<span data-ttu-id="3b549-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="3b549-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b549-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b549-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b549-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b549-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b549-124">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="3b549-124">A text description of an object.</span></span>

</dd> <dt>

<span data-ttu-id="3b549-125">**MaximumScripts**</span><span class="sxs-lookup"><span data-stu-id="3b549-125">**MaximumScripts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b549-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3b549-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b549-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3b549-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b549-128">取用者啟動新實例之前所執行的腳本數目上限。</span><span class="sxs-lookup"><span data-stu-id="3b549-128">Maximum number of scripts that are run before a consumer starts a new instance.</span></span> <span data-ttu-id="3b549-129">若要清除腳本的記憶體流失，請定期關閉取用者。</span><span class="sxs-lookup"><span data-stu-id="3b549-129">To clear out memory leaks from scripts, shut down the consumer regularly.</span></span> <span data-ttu-id="3b549-130">預設值為 300。</span><span class="sxs-lookup"><span data-stu-id="3b549-130">The default value is 300.</span></span>

</dd> <dt>

<span data-ttu-id="3b549-131">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="3b549-131">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b549-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b549-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b549-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b549-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b549-134">限定詞： [**MaxLen**](standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="3b549-134">Qualifiers: [**MaxLen**](standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3b549-135">設定物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b549-135">Identifier for the setting object.</span></span>

</dd> <dt>

<span data-ttu-id="3b549-136">**逾時**</span><span class="sxs-lookup"><span data-stu-id="3b549-136">**Timeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b549-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3b549-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b549-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3b549-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b549-139">限定詞： [**單位**](standard-qualifiers.md) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="3b549-139">Qualifiers: [**units**](standard-qualifiers.md) ("Minutes")</span></span>
</dt> </dl>

<span data-ttu-id="3b549-140">取用者啟動新實例之前的最大分鐘數。</span><span class="sxs-lookup"><span data-stu-id="3b549-140">Maximum number of minutes before a consumer starts a new instance.</span></span> <span data-ttu-id="3b549-141">如果 0 (零) ， **MaximumScripts** 屬性會控制取用者存留期。</span><span class="sxs-lookup"><span data-stu-id="3b549-141">If 0 (zero), the **MaximumScripts** property controls the consumer lifetime.</span></span> <span data-ttu-id="3b549-142">**Timeout** 的有效範圍是0到71000，預設值是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="3b549-142">The valid range for **Timeout** is 0 through 71,000 and the default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b549-143">備註</span><span class="sxs-lookup"><span data-stu-id="3b549-143">Remarks</span></span>

<span data-ttu-id="3b549-144">**ScriptingStandardConsumerSetting** 類別的單一實例位於根 \\ cimv2 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="3b549-144">The single instance of the **ScriptingStandardConsumerSetting** class resides in the root\\cimv2 namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b549-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b549-145">Requirements</span></span>



| <span data-ttu-id="3b549-146">需求</span><span class="sxs-lookup"><span data-stu-id="3b549-146">Requirement</span></span> | <span data-ttu-id="3b549-147">值</span><span class="sxs-lookup"><span data-stu-id="3b549-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b549-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b549-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3b549-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b549-149">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3b549-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b549-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3b549-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b549-151">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3b549-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b549-152">Namespace</span></span><br/>                | <span data-ttu-id="3b549-153">根 \\ 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="3b549-153">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="3b549-154">MOF</span><span class="sxs-lookup"><span data-stu-id="3b549-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b549-155"><dt>Scrcons mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b549-155"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b549-156">DLL</span><span class="sxs-lookup"><span data-stu-id="3b549-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b549-157"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b549-157"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b549-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b549-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b549-159">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="3b549-159">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[<span data-ttu-id="3b549-160">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="3b549-160">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="3b549-161">根據事件執行腳本</span><span class="sxs-lookup"><span data-stu-id="3b549-161">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="3b549-162">建立邏輯取用者</span><span class="sxs-lookup"><span data-stu-id="3b549-162">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="3b549-163">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="3b549-163">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="3b549-164">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="3b549-164">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

