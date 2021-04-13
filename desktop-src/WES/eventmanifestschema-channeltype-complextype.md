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
# <a name="channeltype-complex-type"></a>ChannelType 複雜類型

定義提供者可以記錄事件的通道。

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

## <a name="child-elements"></a>子元素



| 元素                                                                  | 類型                                                                                   | Description                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**測 井**](eventmanifestschema-logging-channeltype-element.md)       | [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)       | 定義支援通道之記錄檔的屬性，例如其容量，以及記錄檔是否為連續或迴圈。<br/>                                                         |
| [**出版**](eventmanifestschema-publishing-channeltype-element.md) | [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) | 為通道所使用的會話定義記錄屬性。 只有使用自訂隔離的 Debug 和分析通道和通道可以為其會話指定記錄屬性。<br/> |



## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>名稱</th>
<th>類型</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>access</td>
<td>字串</td>
<td><a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">安全描述項定義語言</a> (SDDL) 存取描述項，可控制存取通道之記錄檔的存取權。 如果 [ <strong>隔離</strong> ] 屬性設定為 [應用程式] 或 [系統]，則存取描述項會控制檔案的讀取權限， (會忽略) 的寫入權限。 如果 [ <strong>隔離</strong> ] 屬性設定為 [自訂]，則存取描述項會控制通道的寫入存取權，以及對該檔案的讀取權限。<br/></td>
</tr>
<tr class="even">
<td>子</td>
<td>token</td>
<td>此識別碼可唯一識別提供者所定義或匯入通道清單中的通道。 參考事件中的通道時，請使用此值。 如果您未指定通道識別碼，請使用通道的名稱在事件定義中參考這個通道。<br/></td>
</tr>
<tr class="odd">
<td>已啟用</td>
<td>boolean</td>
<td>判斷是否已啟用通道。 設定為 <strong>true</strong> 以允許記錄至通道;否則 <strong>為 false</strong>。 預設值為 <strong>false</strong> () 停用記錄。<br/> 由於 Debug 和分析通道類型是大量的通道，因此您應該只在調查寫入該通道的元件發生問題時才啟用通道;否則，通道應該保持停用狀態。<br/> 每次啟用 Debug 和分析通道時，服務都會清除通道中的事件。<br/></td>
</tr>
<tr class="even">
<td>隔離</td>
<td>字串</td>
<td>隔離值會定義通道的預設存取權限。 您可以指定下列其中一個值：
<ul>
<li><strong>應用程式</strong></li>
<li><strong>系統</strong></li>
<li><strong>Custom</strong></li>
</ul>
預設隔離為 [ <strong>應用程式</strong>]。 <strong>應用程式</strong>的預設許可權 (使用 SDDL) 來顯示： <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Text</th>
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

<p><strong>系統</strong>的預設許可權 (使用 SDDL) 來顯示：</p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Text</th>
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
<p><strong>自訂</strong>隔離的預設許可權與應用程式相同。</p>
<p>指定 <strong>應用程式</strong> 隔離的通道會使用相同的 ETW 會話。 <strong>系統</strong>隔離也是如此。 但是，如果您指定 <strong>自訂</strong> 隔離，服務會為通道建立個別的 ETW 會話。 使用 <strong>自訂</strong> 隔離可讓您控制通道和備份檔案的存取權限。 因為只有 64 ETW 會話可用，所以您應該限制使用 <strong>自訂</strong> 隔離。</p></td>
</tr>
<tr class="odd">
<td>message</td>
<td>字串</td>
<td><p>通道的當地語系化顯示名稱。 訊息字串會參考資訊清單之 <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> 區段中的當地語系化字串。</p></td>
</tr>
<tr class="even">
<td>NAME</td>
<td>anyURI</td>
<td><p>通道的名稱。 在提供者所使用的通道清單中，此名稱必須是唯一的。 命名通道的慣例是將通道類型附加至提供者的名稱。 例如， 如果提供者的名稱是公司產品元件，而您正在定義操作通道，則名稱會是公司產品元件/運作。</p>
<p>通道名稱的長度必須少於255個字元，而且不能包含下列字元： ' > '，'<', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td>符號</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td><p>用來參考應用程式中通道的符號。 <a href="message-compiler--mc-exe-.md"><strong>訊息編譯器 (MC.exe) </strong></a>會使用符號，在編譯器產生的標頭檔中建立通道的常數。 如果您未指定符號，編譯器會為您產生名稱。</p></td>
</tr>
<tr class="even">
<td>type</td>
<td>字串</td>
<td><p>識別通道的類型。 您可以指定下列其中一種類型：</p>
<ul>
<li><strong>管理員</strong></li>
<li><strong>運作</strong></li>
<li><strong>分析</strong></li>
<li><strong>偵錯</strong></li>
</ul>
<p>管理類型通道支援以終端使用者、系統管理員和支援人員為目標的事件。 寫入管理通道的事件應該具有妥善定義的解決方案，系統管理員可以在其上採取行動。系統管理員事件的一個範例，就是當應用程式無法連接到印表機時，就會發生此事件。 這些事件都是妥善記載的，或是有相關聯的訊息，可提供讀者直接指示，說明必須完成才能修正問題。</p>
<p>作業類型通道支援用來分析及診斷問題或發生情況的事件。 根據問題或發生的情況，它們可以用來觸發工具或工作。 舉例而言，在系統中新增或移除印表機時所發生的事件，就是作業事件。</p>
<p>分析類型通道支援在高磁片區中發佈的事件。 它們會描述程式作業，並指出使用者操作所無法處理的問題。</p>
<p>偵錯工具類型通道支援僅供開發人員用來診斷問題的事件。</p>
<p>分析和 debug 通道預設為停用，且只應啟用以判斷問題的原因。 例如，您可以啟用通道、執行造成問題的案例、停用通道，然後查詢事件。 請注意，啟用通道會清除現有事件的通道。 如果分析和調試通道使用迴圈的支援檔案，您必須停用通道以查詢其事件。</p>
<p>所有管理通道都使用相同的 ETW 會話;操作通道也是如此。 不過，每個分析和偵測通道都會使用個別的 ETW 會話，這是在需要時才啟用這些通道類型的另一個原因 () 可用的 ETW 會話數目有限。</p></td>
</tr>
<tr class="odd">
<td>value</td>
<td><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></td>
<td><p>可唯一識別提供者所定義通道清單內通道的數值識別碼。 如果未指定，訊息編譯器會指派值。</p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

如果通道的名稱遵循通道命名慣例，Windows 事件檢視器將會使用反斜線後面的字串來列出通道。 例如，如果通道名稱為公司產品元件/可運作，則事件檢視器會將通道列為公司產品元件提供者下的運作方式。 否則，整個通道名稱會顯示在提供者底下。 如果有提供，則會使用當地語系化的顯示名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 




`
