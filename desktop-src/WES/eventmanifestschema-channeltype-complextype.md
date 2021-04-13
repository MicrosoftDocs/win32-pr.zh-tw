---
title: ChannelType 複雜類型
description: 定義提供者可以記錄事件的通道。
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- ChannelType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466260"
---
# <a name="channeltype-complex-type"></a><span data-ttu-id="af6df-104">ChannelType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="af6df-104">ChannelType Complex Type</span></span>

<span data-ttu-id="af6df-105">定義提供者可以記錄事件的通道。</span><span class="sxs-lookup"><span data-stu-id="af6df-105">Defines a channel to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="af6df-106">子元素</span><span class="sxs-lookup"><span data-stu-id="af6df-106">Child elements</span></span>



| <span data-ttu-id="af6df-107">元素</span><span class="sxs-lookup"><span data-stu-id="af6df-107">Element</span></span>                                                                  | <span data-ttu-id="af6df-108">類型</span><span class="sxs-lookup"><span data-stu-id="af6df-108">Type</span></span>                                                                                   | <span data-ttu-id="af6df-109">Description</span><span class="sxs-lookup"><span data-stu-id="af6df-109">Description</span></span>                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af6df-110">**測 井**</span><span class="sxs-lookup"><span data-stu-id="af6df-110">**logging**</span></span>](eventmanifestschema-logging-channeltype-element.md)       | [<span data-ttu-id="af6df-111">**ChannelLoggingType**</span><span class="sxs-lookup"><span data-stu-id="af6df-111">**ChannelLoggingType**</span></span>](eventmanifestschema-channelloggingtype-complextype.md)       | <span data-ttu-id="af6df-112">定義支援通道之記錄檔的屬性，例如其容量，以及記錄檔是否為連續或迴圈。</span><span class="sxs-lookup"><span data-stu-id="af6df-112">Defines the properties of the log file that backs the channel, such as its capacity and whether the log file is sequential or circular.</span></span><br/>                                                         |
| [<span data-ttu-id="af6df-113">**出版**</span><span class="sxs-lookup"><span data-stu-id="af6df-113">**publishing**</span></span>](eventmanifestschema-publishing-channeltype-element.md) | [<span data-ttu-id="af6df-114">**ChannelPublishingType**</span><span class="sxs-lookup"><span data-stu-id="af6df-114">**ChannelPublishingType**</span></span>](eventmanifestschema-channelpublishingtype-complextype.md) | <span data-ttu-id="af6df-115">為通道所使用的會話定義記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="af6df-115">Defines the logging properties for the session that the channel uses.</span></span> <span data-ttu-id="af6df-116">只有使用自訂隔離的 Debug 和分析通道和通道可以為其會話指定記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="af6df-116">Only Debug and Analytic channels and channels that use Custom isolation can specify logging properties for their session.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="af6df-117">屬性</span><span class="sxs-lookup"><span data-stu-id="af6df-117">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af6df-118">名稱</span><span class="sxs-lookup"><span data-stu-id="af6df-118">Name</span></span></th>
<th><span data-ttu-id="af6df-119">類型</span><span class="sxs-lookup"><span data-stu-id="af6df-119">Type</span></span></th>
<th><span data-ttu-id="af6df-120">Description</span><span class="sxs-lookup"><span data-stu-id="af6df-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af6df-121">access</span><span class="sxs-lookup"><span data-stu-id="af6df-121">access</span></span></td>
<td><span data-ttu-id="af6df-122">字串</span><span class="sxs-lookup"><span data-stu-id="af6df-122">string</span></span></td>
<td><span data-ttu-id="af6df-123"><a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">安全描述項定義語言</a> (SDDL) 存取描述項，可控制存取通道之記錄檔的存取權。</span><span class="sxs-lookup"><span data-stu-id="af6df-123">A <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL) access descriptor that controls access to the log file that backs the channel.</span></span> <span data-ttu-id="af6df-124">如果 [ <strong>隔離</strong> ] 屬性設定為 [應用程式] 或 [系統]，則存取描述項會控制檔案的讀取權限， (會忽略) 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="af6df-124">If the <strong>isolation</strong> attribute is set to Application or System, the access descriptor controls read access to the file (the write permissions are ignored).</span></span> <span data-ttu-id="af6df-125">如果 [ <strong>隔離</strong> ] 屬性設定為 [自訂]，則存取描述項會控制通道的寫入存取權，以及對該檔案的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="af6df-125">If the <strong>isolation</strong> attribute is set to Custom, the access descriptor controls write access to the channel and read access to the file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af6df-126">子</span><span class="sxs-lookup"><span data-stu-id="af6df-126">chid</span></span></td>
<td><span data-ttu-id="af6df-127">token</span><span class="sxs-lookup"><span data-stu-id="af6df-127">token</span></span></td>
<td><span data-ttu-id="af6df-128">此識別碼可唯一識別提供者所定義或匯入通道清單中的通道。</span><span class="sxs-lookup"><span data-stu-id="af6df-128">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="af6df-129">參考事件中的通道時，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="af6df-129">Use this value when referencing the channel in an event.</span></span> <span data-ttu-id="af6df-130">如果您未指定通道識別碼，請使用通道的名稱在事件定義中參考這個通道。</span><span class="sxs-lookup"><span data-stu-id="af6df-130">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af6df-131">已啟用</span><span class="sxs-lookup"><span data-stu-id="af6df-131">enabled</span></span></td>
<td><span data-ttu-id="af6df-132">boolean</span><span class="sxs-lookup"><span data-stu-id="af6df-132">boolean</span></span></td>
<td><span data-ttu-id="af6df-133">判斷是否已啟用通道。</span><span class="sxs-lookup"><span data-stu-id="af6df-133">Determines whether the channel is enabled.</span></span> <span data-ttu-id="af6df-134">設定為 <strong>true</strong> 以允許記錄至通道;否則 <strong>為 false</strong>。</span><span class="sxs-lookup"><span data-stu-id="af6df-134">Set to <strong>true</strong> to allow logging to the channel; otherwise, <strong>false</strong>.</span></span> <span data-ttu-id="af6df-135">預設值為 <strong>false</strong> () 停用記錄。</span><span class="sxs-lookup"><span data-stu-id="af6df-135">The default is <strong>false</strong> (logging is disabled).</span></span><br/> <span data-ttu-id="af6df-136">由於 Debug 和分析通道類型是大量的通道，因此您應該只在調查寫入該通道的元件發生問題時才啟用通道;否則，通道應該保持停用狀態。</span><span class="sxs-lookup"><span data-stu-id="af6df-136">Because Debug and Analytic channel types are high volume channels, you should enable the channel only when investigating an issue with a component that writes to that channel; otherwise, the channel should remain disabled.</span></span><br/> <span data-ttu-id="af6df-137">每次啟用 Debug 和分析通道時，服務都會清除通道中的事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-137">Each time you enable a Debug and Analytic channel, the service clears the events from the channel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af6df-138">隔離</span><span class="sxs-lookup"><span data-stu-id="af6df-138">isolation</span></span></td>
<td><span data-ttu-id="af6df-139">字串</span><span class="sxs-lookup"><span data-stu-id="af6df-139">string</span></span></td>
<td><span data-ttu-id="af6df-140">隔離值會定義通道的預設存取權限。</span><span class="sxs-lookup"><span data-stu-id="af6df-140">The isolation value defines the default access permissions for the channel.</span></span> <span data-ttu-id="af6df-141">您可以指定下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="af6df-141">You can specify one of the following values:</span></span>
<ul>
<li><span data-ttu-id="af6df-142"><strong>應用程式</strong></span><span class="sxs-lookup"><span data-stu-id="af6df-142"><strong>Application</strong></span></span></li>
<li><span data-ttu-id="af6df-143"><strong>系統</strong></span><span class="sxs-lookup"><span data-stu-id="af6df-143"><strong>System</strong></span></span></li>
<li><span data-ttu-id="af6df-144"><strong>Custom</strong></span><span class="sxs-lookup"><span data-stu-id="af6df-144"><strong>Custom</strong></span></span></li>
</ul>
<span data-ttu-id="af6df-145">預設隔離為 [ <strong>應用程式</strong>]。</span><span class="sxs-lookup"><span data-stu-id="af6df-145">The default isolation is <strong>Application</strong>.</span></span> <span data-ttu-id="af6df-146"><strong>應用程式</strong>的預設許可權 (使用 SDDL) 來顯示：</span><span class="sxs-lookup"><span data-stu-id="af6df-146">The default permissions for <strong>Application</strong> are (shown using SDDL):</span></span> <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af6df-147">Text</span><span class="sxs-lookup"><span data-stu-id="af6df-147">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="af6df-148"><strong>系統</strong>的預設許可權 (使用 SDDL) 來顯示：</span><span class="sxs-lookup"><span data-stu-id="af6df-148">The default permissions for <strong>System</strong> are (shown using SDDL):</span></span></p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af6df-149">Text</span><span class="sxs-lookup"><span data-stu-id="af6df-149">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="af6df-150"><strong>自訂</strong>隔離的預設許可權與應用程式相同。</span><span class="sxs-lookup"><span data-stu-id="af6df-150">The default permissions for <strong>Custom</strong> isolation is the same as Application.</span></span></p>
<p><span data-ttu-id="af6df-151">指定 <strong>應用程式</strong> 隔離的通道會使用相同的 ETW 會話。</span><span class="sxs-lookup"><span data-stu-id="af6df-151">Channels that specify <strong>Application</strong> isolation use the same ETW session.</span></span> <span data-ttu-id="af6df-152"><strong>系統</strong>隔離也是如此。</span><span class="sxs-lookup"><span data-stu-id="af6df-152">The same is true for <strong>System</strong> isolation.</span></span> <span data-ttu-id="af6df-153">但是，如果您指定 <strong>自訂</strong> 隔離，服務會為通道建立個別的 ETW 會話。</span><span class="sxs-lookup"><span data-stu-id="af6df-153">However, if you specify <strong>Custom</strong> isolation, the service creates a separate ETW session for the channel.</span></span> <span data-ttu-id="af6df-154">使用 <strong>自訂</strong> 隔離可讓您控制通道和備份檔案的存取權限。</span><span class="sxs-lookup"><span data-stu-id="af6df-154">Using <strong>Custom</strong> isolation lets you control the access permissions for the channel and backing file.</span></span> <span data-ttu-id="af6df-155">因為只有 64 ETW 會話可用，所以您應該限制使用 <strong>自訂</strong> 隔離。</span><span class="sxs-lookup"><span data-stu-id="af6df-155">Because there are only 64 ETW sessions available, you should limit your use of <strong>Custom</strong> isolation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af6df-156">message</span><span class="sxs-lookup"><span data-stu-id="af6df-156">message</span></span></td>
<td><span data-ttu-id="af6df-157">字串</span><span class="sxs-lookup"><span data-stu-id="af6df-157">string</span></span></td>
<td><p><span data-ttu-id="af6df-158">通道的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="af6df-158">The localized display name for the channel.</span></span> <span data-ttu-id="af6df-159">訊息字串會參考資訊清單之 <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="af6df-159">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af6df-160">NAME</span><span class="sxs-lookup"><span data-stu-id="af6df-160">name</span></span></td>
<td><span data-ttu-id="af6df-161">anyURI</span><span class="sxs-lookup"><span data-stu-id="af6df-161">anyURI</span></span></td>
<td><p><span data-ttu-id="af6df-162">通道的名稱。</span><span class="sxs-lookup"><span data-stu-id="af6df-162">The name of the channel.</span></span> <span data-ttu-id="af6df-163">在提供者所使用的通道清單中，此名稱必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="af6df-163">The name must be unique within the list of channels that the provider uses.</span></span> <span data-ttu-id="af6df-164">命名通道的慣例是將通道類型附加至提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="af6df-164">The convention for naming channels is to append the channel type to the provider's name.</span></span> <span data-ttu-id="af6df-165">例如，</span><span class="sxs-lookup"><span data-stu-id="af6df-165">For example.</span></span> <span data-ttu-id="af6df-166">如果提供者的名稱是公司產品元件，而您正在定義操作通道，則名稱會是公司產品元件/運作。</span><span class="sxs-lookup"><span data-stu-id="af6df-166">if the provider's name is Company-Product-Component and you are defining an operational channel, the name would be Company-Product-Component/Operational.</span></span></p>
<p><span data-ttu-id="af6df-167">通道名稱的長度必須少於255個字元，而且不能包含下列字元： ' > '，'</span><span class="sxs-lookup"><span data-stu-id="af6df-167">Channel names must be less that 255 characters and cannot contain the following characters: '>', '</span></span><', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af6df-168">符號</span><span class="sxs-lookup"><span data-stu-id="af6df-168">symbol</span></span></td>
<td><span data-ttu-id="af6df-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="af6df-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="af6df-170">用來參考應用程式中通道的符號。</span><span class="sxs-lookup"><span data-stu-id="af6df-170">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="af6df-171"><a href="message-compiler--mc-exe-.md"><strong>訊息編譯器 (MC.exe) </strong></a>會使用符號，在編譯器產生的標頭檔中建立通道的常數。</span><span class="sxs-lookup"><span data-stu-id="af6df-171">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="af6df-172">如果您未指定符號，編譯器會為您產生名稱。</span><span class="sxs-lookup"><span data-stu-id="af6df-172">If you do not specify a symbol, the compiler generates the name for you.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af6df-173">type</span><span class="sxs-lookup"><span data-stu-id="af6df-173">type</span></span></td>
<td><span data-ttu-id="af6df-174">字串</span><span class="sxs-lookup"><span data-stu-id="af6df-174">string</span></span></td>
<td><p><span data-ttu-id="af6df-175">識別通道的類型。</span><span class="sxs-lookup"><span data-stu-id="af6df-175">Identifies the channel's type.</span></span> <span data-ttu-id="af6df-176">您可以指定下列其中一種類型：</span><span class="sxs-lookup"><span data-stu-id="af6df-176">You can specify one of the following types:</span></span></p>
<ul>
<li><span data-ttu-id="af6df-177"><strong>管理員</strong></span><span class="sxs-lookup"><span data-stu-id="af6df-177"><strong>Admin</strong></span></span></li>
<li><span data-ttu-id="af6df-178"><strong>運作</strong></span><span class="sxs-lookup"><span data-stu-id="af6df-178"><strong>Operational</strong></span></span></li>
<li><span data-ttu-id="af6df-179"><strong>分析</strong></span><span class="sxs-lookup"><span data-stu-id="af6df-179"><strong>Analytic</strong></span></span></li>
<li><span data-ttu-id="af6df-180"><strong>偵錯</strong></span><span class="sxs-lookup"><span data-stu-id="af6df-180"><strong>Debug</strong></span></span></li>
</ul>
<p><span data-ttu-id="af6df-181">管理類型通道支援以終端使用者、系統管理員和支援人員為目標的事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-181">Admin type channels support events that target end users, administrators, and support personnel.</span></span> <span data-ttu-id="af6df-182">寫入管理通道的事件應該具有妥善定義的解決方案，系統管理員可以在其上採取行動。系統管理員事件的一個範例，就是當應用程式無法連接到印表機時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-182">Events written to the Admin channels should have a well-defined solution on which the administrator can act. An example of an admin event is an event that occurs when an application fails to connect to a printer.</span></span> <span data-ttu-id="af6df-183">這些事件都是妥善記載的，或是有相關聯的訊息，可提供讀者直接指示，說明必須完成才能修正問題。</span><span class="sxs-lookup"><span data-stu-id="af6df-183">These events are either well-documented or have a message associated with them that gives the reader direct instructions of what must be done to rectify the problem.</span></span></p>
<p><span data-ttu-id="af6df-184">作業類型通道支援用來分析及診斷問題或發生情況的事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-184">Operational type channels support events that are used for analyzing and diagnosing a problem or occurrence.</span></span> <span data-ttu-id="af6df-185">根據問題或發生的情況，它們可以用來觸發工具或工作。</span><span class="sxs-lookup"><span data-stu-id="af6df-185">They can be used to trigger tools or tasks based on the problem or occurrence.</span></span> <span data-ttu-id="af6df-186">舉例而言，在系統中新增或移除印表機時所發生的事件，就是作業事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-186">An example of an operational event is an event that occurs when a printer is added or removed from a system.</span></span></p>
<p><span data-ttu-id="af6df-187">分析類型通道支援在高磁片區中發佈的事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-187">Analytic type channels support events that are published in high volume.</span></span> <span data-ttu-id="af6df-188">它們會描述程式作業，並指出使用者操作所無法處理的問題。</span><span class="sxs-lookup"><span data-stu-id="af6df-188">They describe program operation and indicate problems that cannot be handled by user intervention.</span></span></p>
<p><span data-ttu-id="af6df-189">偵錯工具類型通道支援僅供開發人員用來診斷問題的事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-189">Debug type channels support events that are used solely by developers to diagnose a problem for debugging.</span></span></p>
<p><span data-ttu-id="af6df-190">分析和 debug 通道預設為停用，且只應啟用以判斷問題的原因。</span><span class="sxs-lookup"><span data-stu-id="af6df-190">Analytic and debug channels are disabled by default and should only enabled to determine the cause of an issue.</span></span> <span data-ttu-id="af6df-191">例如，您可以啟用通道、執行造成問題的案例、停用通道，然後查詢事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-191">For example, you would enable the channel, run the scenario that is causing the issue, disable the channel, and then query the events.</span></span> <span data-ttu-id="af6df-192">請注意，啟用通道會清除現有事件的通道。</span><span class="sxs-lookup"><span data-stu-id="af6df-192">Note that enabling the channel clears the channel of existing events.</span></span> <span data-ttu-id="af6df-193">如果分析和調試通道使用迴圈的支援檔案，您必須停用通道以查詢其事件。</span><span class="sxs-lookup"><span data-stu-id="af6df-193">If the analytic and debug channel uses a circular backing file, you must disable the channel to query its events.</span></span></p>
<p><span data-ttu-id="af6df-194">所有管理通道都使用相同的 ETW 會話;操作通道也是如此。</span><span class="sxs-lookup"><span data-stu-id="af6df-194">All Admin channels use the same ETW session; the same is true for Operational channels.</span></span> <span data-ttu-id="af6df-195">不過，每個分析和偵測通道都會使用個別的 ETW 會話，這是在需要時才啟用這些通道類型的另一個原因 () 可用的 ETW 會話數目有限。</span><span class="sxs-lookup"><span data-stu-id="af6df-195">However, each Analytic and Debug channel uses a separate ETW session, which is another reason to only enable these channel types when needed (there is a limited number of ETW sessions available).</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af6df-196">value</span><span class="sxs-lookup"><span data-stu-id="af6df-196">value</span></span></td>
<td><span data-ttu-id="af6df-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="af6df-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span></span></td>
<td><p><span data-ttu-id="af6df-198">可唯一識別提供者所定義通道清單內通道的數值識別碼。</span><span class="sxs-lookup"><span data-stu-id="af6df-198">A numeric identifier that uniquely identifies the channel within the list of channels that the provider defines.</span></span> <span data-ttu-id="af6df-199">如果未指定，訊息編譯器會指派值。</span><span class="sxs-lookup"><span data-stu-id="af6df-199">The message compiler assigns the value if not specified.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="af6df-200">備註</span><span class="sxs-lookup"><span data-stu-id="af6df-200">Remarks</span></span>

<span data-ttu-id="af6df-201">如果通道的名稱遵循通道命名慣例，Windows 事件檢視器將會使用反斜線後面的字串來列出通道。</span><span class="sxs-lookup"><span data-stu-id="af6df-201">If the channel's name follows the channel naming convention, the Windows Event Viewer will list the channel using the string that follows the backslash.</span></span> <span data-ttu-id="af6df-202">例如，如果通道名稱為公司產品元件/可運作，則事件檢視器會將通道列為公司產品元件提供者下的運作方式。</span><span class="sxs-lookup"><span data-stu-id="af6df-202">For example, if the channel name is Company-Product-Component/Operational, then the Event Viewer will list the channel as Operational under the Company-Product-Component provider.</span></span> <span data-ttu-id="af6df-203">否則，整個通道名稱會顯示在提供者底下。</span><span class="sxs-lookup"><span data-stu-id="af6df-203">Otherwise, the entire channel name is shown under the provider.</span></span> <span data-ttu-id="af6df-204">如果有提供，則會使用當地語系化的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="af6df-204">The localized display name is used if provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6df-205">規格需求</span><span class="sxs-lookup"><span data-stu-id="af6df-205">Requirements</span></span>



| <span data-ttu-id="af6df-206">需求</span><span class="sxs-lookup"><span data-stu-id="af6df-206">Requirement</span></span> | <span data-ttu-id="af6df-207">值</span><span class="sxs-lookup"><span data-stu-id="af6df-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af6df-208">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af6df-208">Minimum supported client</span></span><br/> | <span data-ttu-id="af6df-209">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af6df-209">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af6df-210">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af6df-210">Minimum supported server</span></span><br/> | <span data-ttu-id="af6df-211">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af6df-211">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




`
