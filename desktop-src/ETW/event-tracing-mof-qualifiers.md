---
description: 建立提供者 MOF 類別、事件 MOF 類別、事件種類 MOF 類別，以及事件種類 MOF 類別的屬性時，請使用本節中定義的限定詞。
ms.assetid: 3bc82074-05a7-411f-884f-5da1fd08112b
title: 事件追蹤 MOF 限定詞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7b4250b73e84d46a19dab307d0c263ab1cc7782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852547"
---
# <a name="event-tracing-mof-qualifiers"></a><span data-ttu-id="c7dfe-103">事件追蹤 MOF 限定詞</span><span class="sxs-lookup"><span data-stu-id="c7dfe-103">Event Tracing MOF Qualifiers</span></span>

<span data-ttu-id="c7dfe-104">建立 [提供者 mof 類別](#provider-mof-class-qualifiers)、事件 [MOF 類別](#event-mof-class-qualifiers)、 [事件種類 mof 類別](#event-type-mof-class-qualifiers)，以及 [事件種類 mof 類別的屬性](#property-qualifiers)時，請使用本節中定義的限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-104">Use the qualifiers defined in this section when creating your [provider MOF class](#provider-mof-class-qualifiers), [event MOF class](#event-mof-class-qualifiers), [event type MOF class](#event-type-mof-class-qualifiers), and [the properties of the event type MOF class](#property-qualifiers).</span></span> <span data-ttu-id="c7dfe-105">如需包含其中一些限定詞的範例，請參閱 [發行您的事件架構](publishing-your-event-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-105">For an example that includes some of these qualifiers, see [Publishing Your Event Schema](publishing-your-event-schema.md).</span></span>

## <a name="provider-mof-class-qualifiers"></a><span data-ttu-id="c7dfe-106">提供者 MOF 類別限定詞</span><span class="sxs-lookup"><span data-stu-id="c7dfe-106">Provider MOF class qualifiers</span></span>

<span data-ttu-id="c7dfe-107">下表列出您可以在提供者 MOF 類別上指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-107">The following table lists the qualifiers you can specify on a provider MOF class.</span></span>



| <span data-ttu-id="c7dfe-108">Qualifier</span><span class="sxs-lookup"><span data-stu-id="c7dfe-108">Qualifier</span></span> | <span data-ttu-id="c7dfe-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="c7dfe-109">Data type</span></span>  | <span data-ttu-id="c7dfe-110">描述</span><span class="sxs-lookup"><span data-stu-id="c7dfe-110">Description</span></span>                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7dfe-111">**Guid**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-111">**Guid**</span></span>  | <span data-ttu-id="c7dfe-112">**String**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-112">**String**</span></span> | <span data-ttu-id="c7dfe-113">必要。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-113">Required.</span></span> <span data-ttu-id="c7dfe-114">可唯一識別提供者的字串 Guid。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-114">String Guid that uniquely identifies a provider.</span></span> <span data-ttu-id="c7dfe-115">例如，Guid ( "{3F92E6E0-9886-434e-85DB-0D11D3904C0A}" ) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-115">For example, Guid("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}").</span></span> <span data-ttu-id="c7dfe-116">這與您在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函式來註冊提供者時所使用的 GUID 相同。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-116">This is the same GUID you use when you call the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register your provider.</span></span> |



 

## <a name="event-mof-class-qualifiers"></a><span data-ttu-id="c7dfe-117">事件 MOF 類別限定詞</span><span class="sxs-lookup"><span data-stu-id="c7dfe-117">Event MOF class qualifiers</span></span>

<span data-ttu-id="c7dfe-118">下表列出您可以在事件類別上指定的限定詞， (父類別，將相關的事件種類類別分組) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-118">The following table lists the qualifiers you can specify on an event class (the parent class that groups related event type classes).</span></span>

| <span data-ttu-id="c7dfe-119">Qualifier</span><span class="sxs-lookup"><span data-stu-id="c7dfe-119">Qualifier</span></span>        | <span data-ttu-id="c7dfe-120">資料類型</span><span class="sxs-lookup"><span data-stu-id="c7dfe-120">Data type</span></span>   | <span data-ttu-id="c7dfe-121">描述</span><span class="sxs-lookup"><span data-stu-id="c7dfe-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7dfe-122">**Guid**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-122">**Guid**</span></span>         | <span data-ttu-id="c7dfe-123">**String**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-123">**String**</span></span>  | <span data-ttu-id="c7dfe-124">必要。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-124">Required.</span></span> <span data-ttu-id="c7dfe-125">識別事件類別的字串 Guid。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-125">String Guid that identifies a class of events.</span></span> <span data-ttu-id="c7dfe-126">例如，Guid ( "{3F92E6E0-9886-434e-85DB-0D11D3904C0A}" ) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-126">For example, Guid("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}").</span></span> <span data-ttu-id="c7dfe-127">事件提供者會使用 Guid 來設定 [**事件 \_ 追蹤 \_ 標頭。Guid**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) 成員，讓取用者可以判斷它們所接收的事件類別。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-127">Event providers use the Guid to set the [**EVENT\_TRACE\_HEADER.Guid**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) member, so that consumers can determine the class of events they are receiving.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c7dfe-128">**EventVersion**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-128">**EventVersion**</span></span> | <span data-ttu-id="c7dfe-129">**整數**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-129">**Integer**</span></span> | <span data-ttu-id="c7dfe-130">針對最新版本的事件追蹤類別，此辨識符號是選擇性的，而且所有舊版的類別都需要此限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-130">This qualifier is optional for the latest version of an event trace class and is required for all older versions of the class.</span></span> <span data-ttu-id="c7dfe-131">類別的最新版本不會指定 **EventVersion** 限定詞，也不會有最高的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-131">The latest version of the class either does not specify the **EventVersion** qualifier or has the highest version number.</span></span> <span data-ttu-id="c7dfe-132">版本號碼以0開頭，例如，EventVersion (0) 。一般來說，當您建立類別的新版本時，您也會將舊版重新命名為 <classname> \_ Vn，其中 n 是從0開始的遞增編號。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-132">Version numbers begin with 0, for example, EventVersion(0).Typically, when you create a new version of the class, you also rename the previous version to <classname>\_Vn, where n is an incremental number starting at 0.</span></span> <span data-ttu-id="c7dfe-133">如需範例，請參閱 [**FileIo**](fileio.md) 和 [**FileIo \_ V0**](fileio-v0.md)。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-133">For an example, see [**FileIo**](fileio.md) and [**FileIo\_V0**](fileio-v0.md).</span></span><br/> |



 

## <a name="event-type-mof-class-qualifiers"></a><span data-ttu-id="c7dfe-134">事件種類 MOF 類別限定詞</span><span class="sxs-lookup"><span data-stu-id="c7dfe-134">Event type MOF class qualifiers</span></span>

<span data-ttu-id="c7dfe-135">下表列出您可以在事件種類類別上指定的限定詞， (定義事件屬性資料) 的類別。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-135">The following table lists the qualifiers you can specify on an event type class (the class that defines the event property data).</span></span>



| <span data-ttu-id="c7dfe-136">Qualifier</span><span class="sxs-lookup"><span data-stu-id="c7dfe-136">Qualifier</span></span>         | <span data-ttu-id="c7dfe-137">值</span><span class="sxs-lookup"><span data-stu-id="c7dfe-137">Value</span></span>       | <span data-ttu-id="c7dfe-138">描述</span><span class="sxs-lookup"><span data-stu-id="c7dfe-138">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7dfe-139">**EventType**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-139">**EventType**</span></span>     | <span data-ttu-id="c7dfe-140">**整數**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-140">**Integer**</span></span> | <span data-ttu-id="c7dfe-141">必要。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-141">Required.</span></span> <span data-ttu-id="c7dfe-142">識別事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-142">Identifies the event type class.</span></span> <span data-ttu-id="c7dfe-143">例如，「事件1」 (1) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-143">For example, EventType(1).</span></span> <span data-ttu-id="c7dfe-144">事件提供者會使用相同的事件種類值來設定 [**事件 \_ 追蹤 \_ 標頭。類別。類型**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-144">The event provider uses the same event type value to set [**EVENT\_TRACE\_HEADER.Class.Type**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span></span> <span data-ttu-id="c7dfe-145">如果有多個事件種類使用相同的 MOF 類別 (因為它們使用相同的事件資料) ，請將事件種類值指定為整數的陣列，例如，事件種類 {12,15} 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-145">If the same MOF class is used for multiple event types (because they use the same event data), specify the event type value as an array of integers, for example, EventType{12,15}.</span></span> |
| <span data-ttu-id="c7dfe-146">**EventTypeName**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-146">**EventTypeName**</span></span> | <span data-ttu-id="c7dfe-147">**String**</span><span class="sxs-lookup"><span data-stu-id="c7dfe-147">**String**</span></span>  | <span data-ttu-id="c7dfe-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-148">Optional.</span></span> <span data-ttu-id="c7dfe-149">描述事件種類。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-149">Describes the event type.</span></span> <span data-ttu-id="c7dfe-150">例如，EventTypeName ( "Start" ) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-150">For example, EventTypeName("Start").</span></span> <span data-ttu-id="c7dfe-151">如果多個事件種類使用相同的 MOF 類別 (因為它們使用相同的事件資料) ，請將事件種類名稱值指定為字串陣列，例如 EventTypeName {"Start"，"End"}。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-151">If the same MOF class is used for multiple event types (because they use the same event data), specify the event type name value as an array of strings, for example, EventTypeName{"Start", "End"}.</span></span> <span data-ttu-id="c7dfe-152">EventTypeName 陣列的元素會直接對應至事件陣列。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-152">The elements of the EventTypeName array correspond directly to the EventType array.</span></span>                 |



 

## <a name="property-qualifiers"></a><span data-ttu-id="c7dfe-153">屬性限定詞</span><span class="sxs-lookup"><span data-stu-id="c7dfe-153">Property qualifiers</span></span>

<span data-ttu-id="c7dfe-154">下表列出您可以在屬性上指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-154">The following table lists the qualifiers you can specify on a property.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7dfe-155">Qualifier</span><span class="sxs-lookup"><span data-stu-id="c7dfe-155">Qualifier</span></span></th>
<th><span data-ttu-id="c7dfe-156">描述</span><span class="sxs-lookup"><span data-stu-id="c7dfe-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7dfe-157"><strong>點陣圖</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-157"><strong>BitMap</strong></span></span></td>
<td><span data-ttu-id="c7dfe-158">指定對應至字串值的位位置。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-158">Specifies the bit positions that map to string values.</span></span> <span data-ttu-id="c7dfe-159">如果您指定這個辨識符號，您也必須指定 <strong>BitValues</strong> 限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-159">If you specify this qualifier, you must also specify the <strong>BitValues</strong> qualifier.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7dfe-160"><strong>BitValues</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-160"><strong>BitValues</strong></span></span></td>
<td><span data-ttu-id="c7dfe-161">字串值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-161">String values.</span></span> <span data-ttu-id="c7dfe-162">如果也指定了 <strong>點陣圖</strong> 辨識符號，字串就會直接對應到 <strong>點陣圖</strong> 辨識符號中的值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-162">If the <strong>BitMap</strong> qualifier is also specified, the strings correspond directly to the values in the <strong>BitMap</strong> qualifier.</span></span> <span data-ttu-id="c7dfe-163">否則，假設屬性值是值字串的單一索引， (位1對應至清單) 中的第一個字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-163">Otherwise, assume the property value is a one-based index into the value strings (bit one corresponds to the first string in the list).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7dfe-164"><strong>分機</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-164"><strong>Extension</strong></span></span></td>
<td><span data-ttu-id="c7dfe-165">提供有關如何使用 (解讀資料) 的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-165">Provides additional information on how to consume (interpret) the data.</span></span> <span data-ttu-id="c7dfe-166">擴充值不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-166">The extension value is case-insensitive.</span></span> <span data-ttu-id="c7dfe-167">以引號括住值，例如 (Guid) 的擴充功能 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-167">Include the value in quotes, for example, Extension(&quot;Guid&quot;).</span></span> <span data-ttu-id="c7dfe-168">可能的擴充值為：</span><span class="sxs-lookup"><span data-stu-id="c7dfe-168">Possible extension values are:</span></span> <dl> <span data-ttu-id="c7dfe-169"><dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Guid</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-169"><dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Guid</dt> </span></span><dd> <span data-ttu-id="c7dfe-170">指出屬性資料是 Guid。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-170">Indicates the property data is a Guid.</span></span> <span data-ttu-id="c7dfe-171">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-171">The MOF data type must be <strong>object</strong>.</span></span> <span data-ttu-id="c7dfe-172">承載應為 <strong>GUID</strong> 結構。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-172">The payload is expected to be a <strong>GUID</strong> structure.</span></span><br/> </dd> <span data-ttu-id="c7dfe-173"><dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>IPAddr 和 IPAddrV4</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-173"><dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>IPAddr and IPAddrV4</dt> </span></span><dd> <span data-ttu-id="c7dfe-174">資料是 IP V4 位址。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-174">The data is an IP V4 address.</span></span> <span data-ttu-id="c7dfe-175">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-175">The MOF data type must be <strong>object</strong>.</span></span> <span data-ttu-id="c7dfe-176">承載應為不帶正負號的 long。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-176">The payload is expected to be an unsigned long.</span></span> <span data-ttu-id="c7dfe-177">不帶正負號的每個位元組都代表 IP 位址的四個部分中的其中一個（ (p1. p4) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-177">Each byte of the unsigned long represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="c7dfe-178">低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-178">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span><br/> <span data-ttu-id="c7dfe-179"><strong>在 Windows Vista 之前：</strong> 不支援 IPAddrV4 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-179"><strong>Prior to Windows Vista:</strong> The IPAddrV4 extension is not supported.</span></span><br/> </dd> <span data-ttu-id="c7dfe-180"><dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-180"><dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> </span></span><dd> <span data-ttu-id="c7dfe-181">資料是 IP V6 位址。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-181">The data is an IP V6 address.</span></span> <span data-ttu-id="c7dfe-182">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-182">The MOF data type must be <strong>object</strong>.</span></span> <span data-ttu-id="c7dfe-183">承載應為 <strong>IN6_ADDR</strong> 結構。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-183">The payload is expected to be an <strong>IN6_ADDR</strong> structure.</span></span> <br/> <span data-ttu-id="c7dfe-184"><strong>在 Windows Vista 之前：</strong> 不支援 IPAddrV6 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-184"><strong>Prior to Windows Vista:</strong> The IPAddrV6 extension is not supported.</span></span><br/> </dd> <span data-ttu-id="c7dfe-185"><dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>NoPrint</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-185"><dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>NoPrint</dt> </span></span><dd> <span data-ttu-id="c7dfe-186">指出取用者不應列印此資料。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-186">Indicates that the consumer should not print this data.</span></span><br/> </dd> <span data-ttu-id="c7dfe-187"><dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-187"><dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</dt> </span></span><dd> <span data-ttu-id="c7dfe-188">資料會識別埠號碼。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-188">The data identifies a port number.</span></span> <span data-ttu-id="c7dfe-189">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-189">The MOF data type must be <strong>object</strong>.</span></span> <span data-ttu-id="c7dfe-190">承載應為不帶正負號的簡短。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-190">The payload is expected to be an unsigned short.</span></span><br/> </dd> <span data-ttu-id="c7dfe-191"><dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-191"><dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> </span></span><dd> <span data-ttu-id="c7dfe-192">換行字元是以空格取代。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-192">Newline characters were replaced with spaces.</span></span> <span data-ttu-id="c7dfe-193">承載應為以 null 結束的 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-193">The payload is expected to be a null-terminated, ANSI string.</span></span><br/> </dd> <span data-ttu-id="c7dfe-194"><dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>RWString</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-194"><dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>RWString</dt> </span></span><dd> <span data-ttu-id="c7dfe-195">換行字元是以空格取代。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-195">Newline characters were replaced with spaces.</span></span> <span data-ttu-id="c7dfe-196">承載應為以 null 結尾的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-196">The payload is expected to be a null-terminated, wide-character string.</span></span><br/> </dd> <span data-ttu-id="c7dfe-197"><dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>希</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-197"><dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</dt> </span></span><dd> <span data-ttu-id="c7dfe-198">資料代表二進位 blob SID。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-198">The data represents a binary blob SID.</span></span> <span data-ttu-id="c7dfe-199">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-199">The MOF data type must be <strong>object</strong>.</span></span> <br/> <span data-ttu-id="c7dfe-200">SID 的長度是可變的。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-200">The SID is of a variable length.</span></span> <span data-ttu-id="c7dfe-201">前4個位元組中包含的值 (<strong>ULONG</strong>) 指出 blob 是否包含 SID。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-201">The value contained in the first 4-bytes (<strong>ULONG</strong>) indicates whether the blob contains a SID.</span></span> <span data-ttu-id="c7dfe-202">如果 blob 的前4個位元組 (<strong>ULONG</strong>) 為非零值，則 blob 會包含 SID。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-202">If the first 4-bytes (<strong>ULONG</strong>) of the blob is nonzero, the blob contains a SID.</span></span> <span data-ttu-id="c7dfe-203">Blob 的第一個部分包含 TOKEN_USER (結構在8個位元組的界限上對齊) ，而第二個部分則包含 SID。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-203">The first part of the blob contains the TOKEN_USER (the structure is aligned on an 8-byte boundary) and the second part contains the SID.</span></span> <span data-ttu-id="c7dfe-204">若要處理 blob 的 SID 部分：</span><span class="sxs-lookup"><span data-stu-id="c7dfe-204">To address the SID portion of the blob:</span></span><br/>
<ul>
<li><span data-ttu-id="c7dfe-205">將位元組指標設定為 blob 的開頭</span><span class="sxs-lookup"><span data-stu-id="c7dfe-205">Set a byte pointer to the beginning of the blob</span></span></li>
<li><span data-ttu-id="c7dfe-206">將事件記錄檔的指標大小乘以2，然後將產品加入至位元組指標， (<a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>包含指標大小值的<strong>PointerSize</strong>成員) </span><span class="sxs-lookup"><span data-stu-id="c7dfe-206">Multiply the pointer size for the event log by 2 and add the product to the byte pointer (the <strong>PointerSize</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> contains the pointer size value)</span></span></li>
</ul>
<br/> <span data-ttu-id="c7dfe-207">您可以使用下列宏來判斷 SID 的長度。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-207">You can use the following macro to determine the length of the SID.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <span data-ttu-id="c7dfe-208"><dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-208"><dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> </span></span><dd> <span data-ttu-id="c7dfe-209">指出屬性包含指標值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-209">Indicates that the property contains a pointer value.</span></span> <span data-ttu-id="c7dfe-210">指標值的大小取決於用來記錄事件的作業系統;承載會包含32位系統的4位元組值，或64位系統的8位元組值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-210">The size of the pointer value depends on the operating system used to log the event; the payload will contain a 4-byte value for 32-bit systems or an 8-byte value for 64-bit systems.</span></span> <span data-ttu-id="c7dfe-211">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-211">The MOF data type must be <strong>object</strong>.</span></span><br/> <span data-ttu-id="c7dfe-212">如果屬性包含<strong>SizeT</strong>延伸模組，取用者應該忽略資料類型和<strong>格式</strong>限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-212">Consumers should ignore the data type and <strong>Format</strong> qualifier if the property includes the <strong>SizeT</strong> extension.</span></span> <span data-ttu-id="c7dfe-213">若要判斷要為屬性讀取的資料大小，請使用：</span><span class="sxs-lookup"><span data-stu-id="c7dfe-213">To determine the size of data to read for the property, use:</span></span>
<ul>
<li><span data-ttu-id="c7dfe-214"><a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>的<strong>PointerSize</strong>成員</span><span class="sxs-lookup"><span data-stu-id="c7dfe-214">The <strong>PointerSize</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></span></span></li>
<li><span data-ttu-id="c7dfe-215"><a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a>的<strong>旗標</strong>成員</span><span class="sxs-lookup"><span data-stu-id="c7dfe-215">The <strong>Flags</strong> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="c7dfe-216"><strong>在 Windows Vista 之前：</strong><strong>PointerSize</strong>值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-216"><strong>Prior to Windows Vista:</strong> The <strong>PointerSize</strong> value may not be accurate.</span></span> <span data-ttu-id="c7dfe-217">例如，在64位的電腦上，32位應用程式將會記錄4位元組指標;不過，會話會將 <strong>PointerSize</strong> 設定為8。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-217">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set <strong>PointerSize</strong> to 8.</span></span><br/> </dd> <span data-ttu-id="c7dfe-218"><dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>變異</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-218"><dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>Variant</dt> </span></span><dd> <span data-ttu-id="c7dfe-219">資料代表 blob。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-219">The data represents a blob.</span></span> <span data-ttu-id="c7dfe-220">前四個位元組 (uint32) 指出 blob 的大小。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-220">The first four bytes (uint32) indicate the size of the blob.</span></span> <span data-ttu-id="c7dfe-221">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-221">The MOF data type must be <strong>object</strong>.</span></span> <br/> </dd> <span data-ttu-id="c7dfe-222"><dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>WmiTime</dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-222"><dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>WmiTime</dt> </span></span><dd> <span data-ttu-id="c7dfe-223">將時間戳記轉譯為系統時間。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-223">Translates the time stamp to system time.</span></span> <span data-ttu-id="c7dfe-224">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-224">The MOF data type must be <strong>object</strong>.</span></span> <span data-ttu-id="c7dfe-225">承載應為不帶正負號的64位整數。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-225">The payload is expected to be an unsigned 64-bit integer.</span></span><br/> <span data-ttu-id="c7dfe-226"><strong>在 Windows Vista 之前：</strong> 無法使用。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-226"><strong>Prior to Windows Vista:</strong> Not available.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7dfe-227"><strong>格式</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-227"><strong>Format</strong></span></span></td>
<td><span data-ttu-id="c7dfe-228">定義屬性資料的格式。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-228">Defines the format of the property data.</span></span> <span data-ttu-id="c7dfe-229">例如，包含 &quot; 字串屬性 (w) 的格式， &quot; 表示字串為寬字元串。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-229">For example, including Format(&quot;w&quot;) on a string property indicates the string is a wide string.</span></span> <span data-ttu-id="c7dfe-230">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="c7dfe-230">Possible values are:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c7dfe-231">詞彙</span><span class="sxs-lookup"><span data-stu-id="c7dfe-231">Term</span></span></th>
<th><span data-ttu-id="c7dfe-232">描述</span><span class="sxs-lookup"><span data-stu-id="c7dfe-232">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7dfe-233"><span id="c"></span><span id="C"></span>C</span><span class="sxs-lookup"><span data-stu-id="c7dfe-233"><span id="c"></span><span id="C"></span>c</span></span><br/></td>
<td><span data-ttu-id="c7dfe-234">將屬性值顯示成 ASCII 字元。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-234">Display the property value as an ASCII character.</span></span> <span data-ttu-id="c7dfe-235">您可以將此限定詞與 <strong>uint8</strong> 資料類型搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-235">You can use this qualifier with <strong>uint8</strong> data types.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7dfe-236"><span id="s"></span><span id="S"></span>！</span><span class="sxs-lookup"><span data-stu-id="c7dfe-236"><span id="s"></span><span id="S"></span>s</span></span><br/></td>
<td><span data-ttu-id="c7dfe-237">將字元陣列視為以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-237">Treat the array of characters as a null-terminated string.</span></span> <span data-ttu-id="c7dfe-238">如果資料類型為 <strong>char16</strong>，則字串是寬字元字串;否則，字串是 ASCII 字元字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-238">The string is a wide-character string if the data type is <strong>char16</strong>; otherwise, the string is an ASCII character string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7dfe-239"><span id="w"></span><span id="W"></span>w</span><span class="sxs-lookup"><span data-stu-id="c7dfe-239"><span id="w"></span><span id="W"></span>w</span></span><br/></td>
<td><span data-ttu-id="c7dfe-240">屬性值是寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-240">The property value is a wide-character string.</span></span> <span data-ttu-id="c7dfe-241">您可以使用此限定詞搭配 <strong>字串</strong> 資料類型。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-241">You can use this qualifier with <strong>string</strong> data types.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7dfe-242"><span id="x"></span><span id="X"></span>X</span><span class="sxs-lookup"><span data-stu-id="c7dfe-242"><span id="x"></span><span id="X"></span>x</span></span><br/></td>
<td><span data-ttu-id="c7dfe-243">將屬性值顯示為十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-243">Display the property value as a hexadecimal number.</span></span> <span data-ttu-id="c7dfe-244">您可以將此限定詞與 16-、32-和64位整數資料類型搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-244">You can use this qualifier with 16-, 32-, and 64-bit integer data types.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7dfe-245"><strong>指標</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-245"><strong>Pointer</strong></span></span></td>
<td><p><span data-ttu-id="c7dfe-246">指出屬性包含指標值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-246">Indicates that the property contains a pointer value.</span></span> <span data-ttu-id="c7dfe-247">指標值的大小取決於用來記錄事件的作業系統;承載會包含32位系統的4位元組值，或64位系統的8位元組值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-247">The size of the pointer value depends on the operating system used to log the event; the payload will contain a 4-byte value for 32-bit systems or an 8-byte value for 64-bit systems.</span></span> <span data-ttu-id="c7dfe-248">MOF 資料類型必須是 <strong>object</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-248">The MOF data type must be <strong>object</strong>.</span></span></p>
<p><span data-ttu-id="c7dfe-249">如果屬性包含<strong>SizeT</strong>延伸模組，取用者應該忽略資料類型和<strong>格式</strong>限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-249">Consumers should ignore the data type and <strong>Format</strong> qualifier if the property includes the <strong>SizeT</strong> extension.</span></span> <span data-ttu-id="c7dfe-250">若要判斷要為屬性讀取的資料大小，請使用：</span><span class="sxs-lookup"><span data-stu-id="c7dfe-250">To determine the size of data to read for the property, use:</span></span></p>
<ul>
<li><span data-ttu-id="c7dfe-251"><a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>的<strong>PointerSize</strong>成員</span><span class="sxs-lookup"><span data-stu-id="c7dfe-251">The <strong>PointerSize</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></span></span></li>
<li><span data-ttu-id="c7dfe-252"><a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a>的<strong>旗標</strong>成員</span><span class="sxs-lookup"><span data-stu-id="c7dfe-252">The <strong>Flags</strong> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></span></span></li>
</ul>
<p><span data-ttu-id="c7dfe-253"><strong>在 Windows Vista 之前：</strong><strong>PointerSize</strong>值可能不正確。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-253"><strong>Prior to Windows Vista:</strong> The <strong>PointerSize</strong> value may not be accurate.</span></span> <span data-ttu-id="c7dfe-254">例如，在64位的電腦上，32位應用程式將會記錄4位元組指標;不過，會話會將 <strong>PointerSize</strong> 設定為8。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-254">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set <strong>PointerSize</strong> to 8.</span></span></p>
<p><span data-ttu-id="c7dfe-255">請注意，有些事件會使用 <strong>PointerType</strong> 而非 <strong>指標</strong>;請勿使用 <strong>PointerType</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-255">Note that some events use <strong>PointerType</strong> instead of <strong>Pointer</strong>; do not use <strong>PointerType</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7dfe-256"><strong>StringTermination</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-256"><strong>StringTermination</strong></span></span></td>
<td><span data-ttu-id="c7dfe-257">指出如何終止字串屬性。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-257">Indicates how the string property is terminated.</span></span> <span data-ttu-id="c7dfe-258">例如，StringTermination (&quot; NullTerminated &quot;) 表示字串屬性是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-258">For example, StringTermination(&quot;NullTerminated&quot;) indicates the string property is null-terminated.</span></span> <span data-ttu-id="c7dfe-259">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="c7dfe-259">Possible values are:</span></span>
<dl> <span data-ttu-id="c7dfe-260"><dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>數</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-260"><dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>Counted</strong></dt> </span></span><dd>
<p><span data-ttu-id="c7dfe-261">字串的長度是以 <strong>USHORT</strong> 值的形式內嵌在字串開頭。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-261">The length of the string is embedded at the beginning of the string as a <strong>USHORT</strong> value.</span></span></p>
</dd> <span data-ttu-id="c7dfe-262"><dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>NotCounted</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-262"><dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>NotCounted</strong></dt> </span></span><dd>
<p><span data-ttu-id="c7dfe-263">字串不是以 null 終止，且字串的長度不會內嵌在字串開頭。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-263">The string is not null-terminated and the length of the string is not embedded at the beginning of the string.</span></span> <span data-ttu-id="c7dfe-264">在此情況下，此字串應該是最後一個元素，並佔用事件資料結尾的所有空間。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-264">In this case, the string should be the last element and occupy all the space to the end of the event data.</span></span></p>
</dd> <span data-ttu-id="c7dfe-265"><dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-265"><dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> </span></span><dd>
<p><span data-ttu-id="c7dfe-266">字串以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-266">The string is null-terminated.</span></span> <span data-ttu-id="c7dfe-267">如果您未指定 <strong>StringTermination</strong> 限定詞，則會假設字串是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-267">If you do not specify the <strong>StringTermination</strong> qualifier, the string is assumed to be null-terminated.</span></span></p>
</dd> <span data-ttu-id="c7dfe-268"><dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>ReverseCounted</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7dfe-268"><dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>ReverseCounted</strong></dt> </span></span><dd>
<p><span data-ttu-id="c7dfe-269">字串的長度內嵌在字串開頭，做為位元組由大到小格式的 <strong>USHORT</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-269">The length of the string is embedded at the beginning of the string as a <strong>USHORT</strong> value in big-endian format.</span></span></p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7dfe-270"><strong>ValueDescriptions</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-270"><strong>ValueDescriptions</strong></span></span></td>
<td><span data-ttu-id="c7dfe-271">提供 <strong>值</strong> 限定詞中每個值的描述。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-271">Provides descriptions for each value in the <strong>Values</strong> qualifier.</span></span> <span data-ttu-id="c7dfe-272">當您嘗試取出關鍵字和層級資訊時， <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>TdhEnumerateProviderFieldInformation</strong></a> 和 <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>TdhQueryProviderFieldInformation</strong></a> 函數會傳回這些描述。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-272">The <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>TdhEnumerateProviderFieldInformation</strong></a> and <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>TdhQueryProviderFieldInformation</strong></a> functions return these descriptions when you try to retrieve keyword and level information.</span></span> <span data-ttu-id="c7dfe-273">描述是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-273">The descriptions are optional.</span></span> <span data-ttu-id="c7dfe-274">如果您未提供描述，函數會傳回 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-274">If you do not provide the descriptions, the functions return <strong>NULL</strong>.</span></span> <span data-ttu-id="c7dfe-275">如需詳細資訊，請參閱針對 <a href="#specifying-level-and-enable-flags-values-for-a-provider">提供者指定層級和啟用旗標值</a> 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-275">See <a href="#specifying-level-and-enable-flags-values-for-a-provider">Specifying level and enable flags values for a provider</a> for more details.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7dfe-276"><strong>ValueMap</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-276"><strong>ValueMap</strong></span></span></td>
<td><span data-ttu-id="c7dfe-277">指定對應至字串值的整數索引或旗標值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-277">Specifies the integer index or flag values that map to string values.</span></span> <span data-ttu-id="c7dfe-278">如果您指定此限定詞，您也必須指定 <strong>值</strong> 限定詞，以及選擇性地指定 <strong>ValueType</strong> 辨識符號。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-278">If you specify this qualifier, you must also specify the <strong>Values</strong> qualifier, and optionally the <strong>ValueType</strong> qualifier.</span></span> <span data-ttu-id="c7dfe-279">請注意，ETW 不支援具有值對應值字串的 WMI 選項。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-279">Note that ETW does not support the WMI option of having strings for value map values.</span></span>
<p><span data-ttu-id="c7dfe-280">下列範例示範如何使用 ValueMap、值和 ValueType 限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-280">The following example shows how to use the ValueMap, Values, and ValueType qualifiers.</span></span></p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7dfe-281"><strong>值</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-281"><strong>Values</strong></span></span></td>
<td><span data-ttu-id="c7dfe-282">字串值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-282">String values.</span></span> <span data-ttu-id="c7dfe-283">如果同時指定了 <strong>valuemap</strong> 辨識符號，字串就會直接對應到 <strong>valuemap</strong> 辨識符號中的值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-283">If the <strong>ValueMap</strong> qualifier is also specified, the strings correspond directly to the values in the <strong>ValueMap</strong> qualifier.</span></span> <span data-ttu-id="c7dfe-284">否則，假設屬性值是以零為基底的索引至值字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-284">Otherwise, assume the property value is a zero-based index into the value strings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7dfe-285"><strong>ValueType</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-285"><strong>ValueType</strong></span></span></td>
<td><span data-ttu-id="c7dfe-286">指出 <strong>ValueMap</strong> 值是否為整數索引值或位旗標值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-286">Indicates if the <strong>ValueMap</strong> values are integer index values or bit flag values.</span></span> <span data-ttu-id="c7dfe-287">如果您未指定此辨識符號，則會假設為整數索引值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-287">If you do not specify this qualifier, integer index values are assumed.</span></span> <span data-ttu-id="c7dfe-288">若要指定值為整數索引值，請使用 ValueType (&quot; 索引 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-288">To specify that the values are integer index values, use ValueType(&quot;index&quot;).</span></span> <span data-ttu-id="c7dfe-289">若要指定值為位旗標值，請使用 ValueType (&quot; 旗標 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-289">To specify that the values are bit flag values, use ValueType(&quot;flag&quot;).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7dfe-290"><strong>WmiDataId</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-290"><strong>WmiDataId</strong></span></span></td>
<td><span data-ttu-id="c7dfe-291">每個屬性都必須包含 <strong>WmiDataId</strong> 限定詞。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-291">Each property must contain the <strong>WmiDataId</strong> qualifier.</span></span> <span data-ttu-id="c7dfe-292"><strong>WmiDataId</strong> 會定義取用者讀取事件資料的順序。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-292"><strong>WmiDataId</strong> defines the order in which the consumer reads the event data.</span></span> <span data-ttu-id="c7dfe-293"><strong>WmiDataId</strong>的值會從1開始，並針對類別中的每個屬性遞增。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-293">The value for <strong>WmiDataId</strong> starts at 1 and increments for each property in the class.</span></span> <span data-ttu-id="c7dfe-294">例如，WmiDataId (1) 。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-294">For example, WmiDataId(1).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7dfe-295"><strong>XMLFragment</strong></span><span class="sxs-lookup"><span data-stu-id="c7dfe-295"><strong>XMLFragment</strong></span></span></td>
<td><span data-ttu-id="c7dfe-296">表示資料為 XML 格式，而且可以在不進一步格式化的情況下顯示。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-296">Indicates that the data is in XML format and ready to display without further formatting.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a><span data-ttu-id="c7dfe-297">指定提供者的層級和啟用旗標值</span><span class="sxs-lookup"><span data-stu-id="c7dfe-297">Specifying level and enable flags values for a provider</span></span>

<span data-ttu-id="c7dfe-298">若要記錄層級，並啟用控制器將用來啟用您提供者的旗標，請在提供者 MOF 類別中包含「等級」和「旗標」屬性。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-298">To document the level and enable flags that a controller would use to enable your provider, include the "Level" and "Flags" properties in your provider MOF class.</span></span> <span data-ttu-id="c7dfe-299">層級和旗標屬性名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-299">The Level and Flags property names are case sensitive.</span></span> <span data-ttu-id="c7dfe-300">屬性必須包含 **值** 和 **ValueMap** 限定詞，以指定可能的層級和啟用旗標值。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-300">The properties must include the **Values** and **ValueMap** qualifiers, which specify the possible level and enable flag values.</span></span> <span data-ttu-id="c7dfe-301">啟用旗標值的 **ValueMap** 必須是) 值的位 (旗標。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-301">The **ValueMap** for the enable flag values must be bit (flag) values.</span></span> <span data-ttu-id="c7dfe-302">**ValueDescriptions** 限定詞是選擇性的，但您應該使用它來提供每個可能值的描述。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-302">The **ValueDescriptions** qualifier is optional but you should use it to provide descriptions for each possible value.</span></span> <span data-ttu-id="c7dfe-303">當有人呼叫 [**TdhEnumerateProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) 和 [**TdhQueryProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) 函式以取得可能的層級，並啟用 (關鍵字的旗標) 值給提供者時，就會使用這些描述。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-303">The descriptions are used when someone calls the [**TdhEnumerateProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) and [**TdhQueryProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) functions to get the possible level and enable flags (keywords) values for the provider.</span></span>

<span data-ttu-id="c7dfe-304">下圖顯示指定可能層級和啟用旗標值的提供者類別。</span><span class="sxs-lookup"><span data-stu-id="c7dfe-304">The following shows a provider class that specifies the possible level and enable flags values.</span></span>

``` syntax
[Dynamic,
 Description("IIS_Trace") : amended,
 guid("{3a2a4e84-4c21-4981-ae10-3fda0d9b0f83}"),
 locale("MS\\0x409")]
class IIS_Trace : EventTrace
{
    [Description ("Enable Flags") : amended,
        ValueDescriptions{
             "Allow_tracing_only_selected_requests ",
             "IIS_authentication_events ",
             "IIS_security_events ",
             "IIS_filter_events ",
             "IIS_static_file_events ",
             "IIS_CGI_events ",
             "IIS_compression_events ",
             "IIS_cache_events ",
             "IIS_request_notifications_events ",
             "IIS_module_events ",
             "IIS_FastCGI_events "},
        DefineValues{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        Values{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        ValueMap{
             "0x00000001",
             "0x00000002",
             "0x00000004",
             "0x00000008",
             "0x00000010",
             "0x00000020",
             "0x00000040",
             "0x00000080",
             "0x00000100",
             "0x00000200",
             "0x00001000"}: amended
    ]
    uint32 Flags;

    [Description ("Levels") : amended,
        ValueDescriptions{
            "Abnormal exit or termination",
            "Severe errors that need logging",
            "Warnings such as allocation failure",
            "Includes non-error cases",
            "Detailed traces from intermediate steps" } : amended,
         DefineValues{
            "TRACE_LEVEL_FATAL",
            "TRACE_LEVEL_ERROR",
            "TRACE_LEVEL_WARNING"
            "TRACE_LEVEL_INFORMATION",
            "TRACE_LEVEL_VERBOSE" },
        Values{
            "Fatal",
            "Error",
            "Warning",
            "Information",
            "Verbose" },
        ValueMap{
            "0x1",
            "0x2",
            "0x3",
            "0x4",
            "0x5" },
        ValueType("index")
    ]
    uint32 Level;
};
```

 

 
