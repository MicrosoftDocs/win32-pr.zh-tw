---
description: 傳統提供者應該使用受控物件格式 (MOF) 來發佈其事件資料的配置。 接著，取用者可以在執行時間從 WMI 讀取已發佈的配置，並用它來讀取事件資料。
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: 發佈傳統提供者的事件架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318528"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a><span data-ttu-id="8a06f-104">發佈傳統提供者的事件架構</span><span class="sxs-lookup"><span data-stu-id="8a06f-104">Publishing Your Event Schema for a Classic Provider</span></span>

<span data-ttu-id="8a06f-105">[傳統](about-event-tracing.md) 提供者應該使用 [受控物件格式](../wmisdk/managed-object-format--mof-.md) (MOF) 來發佈其事件資料的配置。</span><span class="sxs-lookup"><span data-stu-id="8a06f-105">[Classic](about-event-tracing.md) providers should use [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) to publish the layout of their event data.</span></span> <span data-ttu-id="8a06f-106">接著，取用者可以在執行時間從 WMI 讀取已發佈的配置，並用它來讀取事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a06f-106">Consumers can then read the published layout from WMI at runtime and use it to read the event data.</span></span>

<span data-ttu-id="8a06f-107">如果您使用 MOF 來發佈 WMI 中的事件資料版面配置，通常會在根 WMI 命名空間中建立下列三種類型的 MOF 類別 \\ ：</span><span class="sxs-lookup"><span data-stu-id="8a06f-107">If you use MOF to publish the layout of your event data in WMI, you typically create the following three types of MOF classes in the root\\wmi namespace:</span></span>

-   [<span data-ttu-id="8a06f-108">提供者 MOF 類別</span><span class="sxs-lookup"><span data-stu-id="8a06f-108">A provider MOF class</span></span>](#provider-mof-classes)
-   [<span data-ttu-id="8a06f-109">一或多個事件 MOF 類別</span><span class="sxs-lookup"><span data-stu-id="8a06f-109">One or more event MOF classes</span></span>](#event-mof-classes)
-   [<span data-ttu-id="8a06f-110">一或多個事件種類 MOF 類別</span><span class="sxs-lookup"><span data-stu-id="8a06f-110">One or more event type MOF classes</span></span>](#event-type-mof-classes)

## <a name="provider-mof-classes"></a><span data-ttu-id="8a06f-111">提供者 MOF 類別</span><span class="sxs-lookup"><span data-stu-id="8a06f-111">Provider MOF classes</span></span>

<span data-ttu-id="8a06f-112">如果您發佈事件資料的配置，您必須建立識別提供者的 MOF 類別。</span><span class="sxs-lookup"><span data-stu-id="8a06f-112">If you publish the layout of your event data, you must create a MOF class that identifies your provider.</span></span> <span data-ttu-id="8a06f-113">此類別必須衍生自 **EventTrace** MOF 類別，而且必須是空的 (沒有任何屬性或方法) 。</span><span class="sxs-lookup"><span data-stu-id="8a06f-113">This class must derive from the **EventTrace** MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="8a06f-114">類別也必須包含可唯一識別提供者的 **Guid** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="8a06f-114">The class must also include the **Guid** qualifier which uniquely identifies the provider.</span></span> <span data-ttu-id="8a06f-115">這與您在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函式來註冊提供者時所使用的 GUID 相同。</span><span class="sxs-lookup"><span data-stu-id="8a06f-115">This is the same GUID you use when you calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register your provider.</span></span>

## <a name="event-mof-classes"></a><span data-ttu-id="8a06f-116">事件 MOF 類別</span><span class="sxs-lookup"><span data-stu-id="8a06f-116">Event MOF classes</span></span>

<span data-ttu-id="8a06f-117">事件 MOF 類別會定義提供者所提供之事件的類別。</span><span class="sxs-lookup"><span data-stu-id="8a06f-117">An event MOF class defines a class of events that the provider provides.</span></span> <span data-ttu-id="8a06f-118">這個類別衍生自提供者 MOF 類別，而且必須是空的 (沒有任何屬性或方法) 。</span><span class="sxs-lookup"><span data-stu-id="8a06f-118">This class derives from the provider MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="8a06f-119">類別也必須包含 **Guid** 辨識符號，以唯一識別其子類別所定義的事件類別。</span><span class="sxs-lookup"><span data-stu-id="8a06f-119">The class must also include the **Guid** qualifier which uniquely identifies the class of events that its child classes define.</span></span> <span data-ttu-id="8a06f-120">在設定 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **guid** 成員時，提供者會使用這個相同的 guid。</span><span class="sxs-lookup"><span data-stu-id="8a06f-120">The provider uses this same GUID when setting the **Guid** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="event-type-mof-classes"></a><span data-ttu-id="8a06f-121">事件種類 MOF 類別</span><span class="sxs-lookup"><span data-stu-id="8a06f-121">Event type MOF classes</span></span>

<span data-ttu-id="8a06f-122">事件種類 MOF 類別會定義實際的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a06f-122">An event type MOF class defines the actual event data.</span></span> <span data-ttu-id="8a06f-123">此類別衍生自其父事件 MOF 類別。</span><span class="sxs-lookup"><span data-stu-id="8a06f-123">This class derives from its parent event MOF class.</span></span> <span data-ttu-id="8a06f-124">為事件種類 MOF 類別命名時，慣例是在事件種類 MOF 類別名稱的開頭使用事件 MOF 類別名稱。</span><span class="sxs-lookup"><span data-stu-id="8a06f-124">When naming the event type MOF class, the convention is to use the event MOF class name at the beginning of the event type MOF class name.</span></span> <span data-ttu-id="8a06f-125">例如，如果事件 MOF 類別名稱是 HWConfig，而事件種類 MOF 類別代表 CPU 資訊，您應該將事件種類的 MOF 類別命名為 HWConfig \_ cpu。</span><span class="sxs-lookup"><span data-stu-id="8a06f-125">For example, if the event MOF class name is HWConfig and the event type MOF class represents CPU information, you should name the event type MOF class, HWConfig\_CPU.</span></span>

<span data-ttu-id="8a06f-126">使用事件種類 MOF 類別上 **的 [事件** 類型] 限定詞來識別事件種類。</span><span class="sxs-lookup"><span data-stu-id="8a06f-126">Use the **EventType** qualifier on the event type MOF class to identify the event type.</span></span> <span data-ttu-id="8a06f-127">如果多個事件種類使用相同的事件資料，則可以使用相同的 MOF 類別。</span><span class="sxs-lookup"><span data-stu-id="8a06f-127">If multiple event types use the same event data, they can use the same MOF class.</span></span> <span data-ttu-id="8a06f-128">在設定類別時，提供者會使用相同的事件種類值來識別事件。[**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="8a06f-128">The provider uses the same event type value to identify the event when setting the **Class.Type** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

<span data-ttu-id="8a06f-129">事件種類 MOF 類別包含屬性。</span><span class="sxs-lookup"><span data-stu-id="8a06f-129">The event type MOF class contains properties.</span></span> <span data-ttu-id="8a06f-130">這些屬性的順序會定義事件資料的版面配置。</span><span class="sxs-lookup"><span data-stu-id="8a06f-130">The order of these properties define the layout of the event data.</span></span> <span data-ttu-id="8a06f-131">下表指出您可以用來定義屬性的資料類型和限定詞。</span><span class="sxs-lookup"><span data-stu-id="8a06f-131">The following table identifies the data types and qualifiers you can use to define the properties.</span></span> <span data-ttu-id="8a06f-132">如需您可以使用的屬性和類別限定詞的詳細資訊，請參閱 [事件追蹤 MOF 限定詞](event-tracing-mof-qualifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="8a06f-132">For more information on the property and class qualifiers that you can use, see [Event Tracing MOF Qualifiers](event-tracing-mof-qualifiers.md).</span></span>



| <span data-ttu-id="8a06f-133">資料類型</span><span class="sxs-lookup"><span data-stu-id="8a06f-133">Data type</span></span>              | <span data-ttu-id="8a06f-134">限定詞</span><span class="sxs-lookup"><span data-stu-id="8a06f-134">Qualifiers</span></span>                        | <span data-ttu-id="8a06f-135">描述</span><span class="sxs-lookup"><span data-stu-id="8a06f-135">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a06f-136">**sint8**、 **uint8**</span><span class="sxs-lookup"><span data-stu-id="8a06f-136">**sint8**, **uint8**</span></span>   | <span data-ttu-id="8a06f-137">**格式**</span><span class="sxs-lookup"><span data-stu-id="8a06f-137">**Format**</span></span>                        | <span data-ttu-id="8a06f-138">宣告1位元組的十進位整數。</span><span class="sxs-lookup"><span data-stu-id="8a06f-138">Declares a 1-byte decimal integer.</span></span> <span data-ttu-id="8a06f-139">若要宣告 ANSI 字元，請使用 **格式** 辨識符號，並將其值設定為 "c"。</span><span class="sxs-lookup"><span data-stu-id="8a06f-139">To declare an ANSI character, use the **Format** qualifier and set its value to "c".</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="8a06f-140">**sint16**、 **uint16**</span><span class="sxs-lookup"><span data-stu-id="8a06f-140">**sint16**, **uint16**</span></span> | <span data-ttu-id="8a06f-141">**格式**</span><span class="sxs-lookup"><span data-stu-id="8a06f-141">**Format**</span></span>                        | <span data-ttu-id="8a06f-142">宣告2個位元組的十進位整數。</span><span class="sxs-lookup"><span data-stu-id="8a06f-142">Declares a 2-byte decimal integer.</span></span> <span data-ttu-id="8a06f-143">若要指示數位是十六進位數位，請使用 **格式** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="8a06f-143">To indicate the number is a hexadecimal number, use the **Format** qualifier.</span></span> <span data-ttu-id="8a06f-144">例如， ( "x" 格式 ) 。</span><span class="sxs-lookup"><span data-stu-id="8a06f-144">For example, format("x").</span></span>                                                                                                                                                                               |
| <span data-ttu-id="8a06f-145">**sint32**、 **uint32**</span><span class="sxs-lookup"><span data-stu-id="8a06f-145">**sint32**, **uint32**</span></span> | <span data-ttu-id="8a06f-146">**格式**</span><span class="sxs-lookup"><span data-stu-id="8a06f-146">**Format**</span></span>                        | <span data-ttu-id="8a06f-147">宣告4位元組的十進位整數。</span><span class="sxs-lookup"><span data-stu-id="8a06f-147">Declares a 4-byte decimal integer.</span></span> <span data-ttu-id="8a06f-148">若要指示數位是十六進位數位，請使用 **格式** 辨識符號，並將其值設定為 "x"。</span><span class="sxs-lookup"><span data-stu-id="8a06f-148">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="8a06f-149">**sint64**， **uint64**</span><span class="sxs-lookup"><span data-stu-id="8a06f-149">**sint64**, **uint64**</span></span> | <span data-ttu-id="8a06f-150">**格式**</span><span class="sxs-lookup"><span data-stu-id="8a06f-150">**Format**</span></span>                        | <span data-ttu-id="8a06f-151">宣告8位元組的十進位整數。</span><span class="sxs-lookup"><span data-stu-id="8a06f-151">Declares a 8-byte decimal integer.</span></span> <span data-ttu-id="8a06f-152">若要指示數位是十六進位數位，請使用 **格式** 辨識符號，並將其值設定為 "x"。</span><span class="sxs-lookup"><span data-stu-id="8a06f-152">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="8a06f-153">**boolean**</span><span class="sxs-lookup"><span data-stu-id="8a06f-153">**boolean**</span></span>            |                                   | <span data-ttu-id="8a06f-154">宣告布林值。</span><span class="sxs-lookup"><span data-stu-id="8a06f-154">Declares a Boolean value.</span></span> <span data-ttu-id="8a06f-155">事件取用者應該將值以 BOOL (4 位元組整數) 來解讀。</span><span class="sxs-lookup"><span data-stu-id="8a06f-155">The event consumer should interpret the value as BOOL (4-byte integer).</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="8a06f-156">**char16**</span><span class="sxs-lookup"><span data-stu-id="8a06f-156">**char16**</span></span>             |                                   | <span data-ttu-id="8a06f-157">宣告寬字元。</span><span class="sxs-lookup"><span data-stu-id="8a06f-157">Declares a wide character.</span></span> <span data-ttu-id="8a06f-158">事件取用者應該將核心事件中的 char16 陣列轉譯為寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="8a06f-158">The event consumer should interpret char16 arrays in kernel events as wide character strings.</span></span> <span data-ttu-id="8a06f-159"> (使用陣列大小來複製字串。</span><span class="sxs-lookup"><span data-stu-id="8a06f-159">(Use the array size to copy the string.</span></span> <span data-ttu-id="8a06f-160">某些字串可能會包含開頭的 Null 字元。 ) </span><span class="sxs-lookup"><span data-stu-id="8a06f-160">Some strings may contain leading NULL characters.)</span></span>                                                                                                      |
| <span data-ttu-id="8a06f-161">**object**</span><span class="sxs-lookup"><span data-stu-id="8a06f-161">**object**</span></span>             | <span data-ttu-id="8a06f-162">**分機**</span><span class="sxs-lookup"><span data-stu-id="8a06f-162">**Extension**</span></span>                     | <span data-ttu-id="8a06f-163">宣告二進位 blob。</span><span class="sxs-lookup"><span data-stu-id="8a06f-163">Declares a binary blob.</span></span> <span data-ttu-id="8a06f-164">**延伸** 模組辨識符號表示 blob 中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="8a06f-164">The **Extension** qualifier indicates the type of data in the blob.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="8a06f-165">**string**</span><span class="sxs-lookup"><span data-stu-id="8a06f-165">**string**</span></span>             | <span data-ttu-id="8a06f-166">**Format**、 **StringTermination**</span><span class="sxs-lookup"><span data-stu-id="8a06f-166">**Format**, **StringTermination**</span></span> | <span data-ttu-id="8a06f-167">宣告字串值。</span><span class="sxs-lookup"><span data-stu-id="8a06f-167">Declares a string value.</span></span> <span data-ttu-id="8a06f-168">若要指出字串是寬字元字串，請使用 **格式** 辨識符號，並將其值設定為 "w"。</span><span class="sxs-lookup"><span data-stu-id="8a06f-168">To indicate the string is a wide-character string use the **Format** qualifier and set its value to "w".</span></span> <span data-ttu-id="8a06f-169">如果您未指定 **格式** 辨識符號，則字串會被視為 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="8a06f-169">The string is considered an ANSI string if you do not specify the **Format** qualifier.</span></span> <span data-ttu-id="8a06f-170">若要指出字串的結束方式，請使用 **StringTermination** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="8a06f-170">To indicate how the string is terminated, use the **StringTermination** qualifier.</span></span> <br/> |



 

<span data-ttu-id="8a06f-171">若要指定陣列，您可以使用方括弧 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="8a06f-171">To specify an array, you can use square brackets, \[\].</span></span> <span data-ttu-id="8a06f-172">方括弧可以包含陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="8a06f-172">The square brackets can include the size of the array.</span></span> <span data-ttu-id="8a06f-173">例如：</span><span class="sxs-lookup"><span data-stu-id="8a06f-173">For example:</span></span>

`[WmiDataId(1), read] uint8 MyGuid[16];`

<span data-ttu-id="8a06f-174">您也可以使用 **Max** 辨識符號來指定陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="8a06f-174">You can also use the **Max** qualifier to specify the size of an array.</span></span> <span data-ttu-id="8a06f-175">例如：</span><span class="sxs-lookup"><span data-stu-id="8a06f-175">For example:</span></span>

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

<span data-ttu-id="8a06f-176">如果您在方括弧中包含陣列的大小，MOF 編譯器會為您產生最大限定詞。</span><span class="sxs-lookup"><span data-stu-id="8a06f-176">If you include the size of the array in the square brackets, the MOF compiler generates the Max qualifier for you.</span></span>

<span data-ttu-id="8a06f-177">請務必針對每個屬性使用 **描述** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="8a06f-177">It is important that you use the **Description** qualifier for each property.</span></span> <span data-ttu-id="8a06f-178">描述應該包含取用者顯示內容值時可使用的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8a06f-178">The description should contain a display name that the consumer can use when displaying the property values.</span></span>

<span data-ttu-id="8a06f-179">下列範例會顯示描述提供者、事件和事件種類 MOF 類別之 MOF 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="8a06f-179">The following example shows the contents of a MOF file that describes a provider, event, and event type MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

<span data-ttu-id="8a06f-180">請注意，提供者、事件和事件種類 MOF 類別名稱在整個命名空間中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8a06f-180">Note that the provider, event, and event type MOF class names must be unique within the entire namespace.</span></span> <span data-ttu-id="8a06f-181">若要避免命名衝突，您應該針對所有類別名稱使用唯一和描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="8a06f-181">To avoid naming conflicts, you should use unique and descriptive name for all class names.</span></span> <span data-ttu-id="8a06f-182">類別屬性在其類別階層中也應該具有描述性和唯一的，也就是包含與父類別相同屬性名稱的子類別，會覆寫父類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="8a06f-182">Class properties should also be descriptive and unique within its class hierarchy—a child class that contains the same property name as a parent class overwrites the property of the parent class.</span></span>

<span data-ttu-id="8a06f-183">定義您的 MOF 類別之後，請使用 MOF 編譯器來產生您的事件架構，並將它新增至 CIM 存放庫。</span><span class="sxs-lookup"><span data-stu-id="8a06f-183">After defining your MOF classes, use the MOF compiler to generate your event schema and add it to the CIM repository.</span></span> <span data-ttu-id="8a06f-184">接著，取用者可以從存放庫讀取架構，並以程式設計方式讀取事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a06f-184">Consumers can then read the schema from the repository and programmatically read the event data.</span></span> <span data-ttu-id="8a06f-185">如需 MOF 語法和使用 MOF 編譯器 (Mofcomp.exe) 將 MOF 類別新增至 CIM 存放庫的完整說明，請參閱 [受控物件格式](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="8a06f-185">For a complete description of the MOF syntax and using the MOF compiler (Mofcomp.exe) to add your MOF classes to the CIM repository, see [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span></span> <span data-ttu-id="8a06f-186">如需使用 Wbemtest.exe 來存取 CIM 存放庫的詳細資訊，請參閱 [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI) 。</span><span class="sxs-lookup"><span data-stu-id="8a06f-186">For information on using Wbemtest.exe to access the CIM repository, see [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).</span></span>

## <a name="versioning-mof-class"></a><span data-ttu-id="8a06f-187">版本設定 MOF 類別</span><span class="sxs-lookup"><span data-stu-id="8a06f-187">Versioning MOF class</span></span>

<span data-ttu-id="8a06f-188">如果您新增或變更事件種類 MOF 類別，則慣例是將事件 MOF 類別和其子事件種類 MOF 類別的版本設為版本。</span><span class="sxs-lookup"><span data-stu-id="8a06f-188">If you add or change an event type MOF class, the convention is to version both the event MOF class and its child event type MOF classes.</span></span> <span data-ttu-id="8a06f-189">若要將目前的事件 MOF 類別設為版本，請將 \_ Vn 附加至類別名稱，其中 n 是從0開始的遞增編號。</span><span class="sxs-lookup"><span data-stu-id="8a06f-189">To version the current event MOF class, append \_Vn to the class name, where n is an incremental number starting at 0.</span></span> <span data-ttu-id="8a06f-190">如果這是類別的第一個修訂，請將 \_ V0 附加至類別名稱。</span><span class="sxs-lookup"><span data-stu-id="8a06f-190">If this is the first revision to the class, append \_V0 to the class name.</span></span> <span data-ttu-id="8a06f-191">您也必須將 **EventVersion** 限定詞新增至類別。</span><span class="sxs-lookup"><span data-stu-id="8a06f-191">You must also add the **EventVersion** qualifier to the class.</span></span> <span data-ttu-id="8a06f-192">使用您在類別名稱中用來作為 **EventVersion** 限定詞值的相同版本號碼。</span><span class="sxs-lookup"><span data-stu-id="8a06f-192">Use the same version number you used in the class name for the value of the **EventVersion** qualifier.</span></span>

<span data-ttu-id="8a06f-193">新版本的事件 MOF 類別必須使用與原始類別相同的名稱和 **Guid** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="8a06f-193">The new version of the event MOF class must use the same name and **Guid** qualifier as the original class.</span></span> <span data-ttu-id="8a06f-194">新的類別可以選擇性地新增 **EventVersion** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="8a06f-194">The new class may optionally add the **EventVersion** qualifier.</span></span> <span data-ttu-id="8a06f-195">未包含 **EventVersion** 限定詞的事件 MOF 類別會被視為最新版本，或者，如果類別的所有版本都包含 **EventVersion** 辨識符號，則具有最高版本號碼的類別會被視為最新版本。</span><span class="sxs-lookup"><span data-stu-id="8a06f-195">The event MOF class that does not contain the **EventVersion** qualifier is considered the latest version, or if all the versions of the class contain an **EventVersion** qualifier, then the class with the highest version number is considered the latest version.</span></span> <span data-ttu-id="8a06f-196">提供者會使用 [**事件 \_ 追蹤 \_ 標頭**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)結構的 **類別. 版本** 成員，來識別追蹤中包含的事件版本。</span><span class="sxs-lookup"><span data-stu-id="8a06f-196">The provider uses the **Class.Version** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to identify the version of the event included in the trace.</span></span>

<span data-ttu-id="8a06f-197">下列範例示範如何為事件 MOF 類別的版本。</span><span class="sxs-lookup"><span data-stu-id="8a06f-197">The following example shows how to version an event MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
