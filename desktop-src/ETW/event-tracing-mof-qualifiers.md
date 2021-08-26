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
ms.openlocfilehash: abc5a2b884d9343e6c58737cacd259650952353a2fc5ad68ee843af2b30710e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901178"
---
# <a name="event-tracing-mof-qualifiers"></a>事件追蹤 MOF 限定詞

建立 [提供者 mof 類別](#provider-mof-class-qualifiers)、事件 [MOF 類別](#event-mof-class-qualifiers)、 [事件種類 mof 類別](#event-type-mof-class-qualifiers)，以及 [事件種類 mof 類別的屬性](#property-qualifiers)時，請使用本節中定義的限定詞。 如需包含其中一些限定詞的範例，請參閱 [發行您的事件架構](publishing-your-event-schema.md)。

## <a name="provider-mof-class-qualifiers"></a>提供者 MOF 類別限定詞

下表列出您可以在提供者 MOF 類別上指定的限定詞。



| Qualifier | 資料類型  | 描述                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**  | **String** | 必要。 可唯一識別提供者的字串 Guid。 例如，Guid ( "{3F92E6E0-9886-434e-85DB-0D11D3904C0A}" ) 。 這與您在呼叫 [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 函式來註冊提供者時所使用的 GUID 相同。 |



 

## <a name="event-mof-class-qualifiers"></a>事件 MOF 類別限定詞

下表列出您可以在事件類別上指定的限定詞， (父類別，將相關的事件種類類別分組) 。

| Qualifier        | 資料類型   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**         | **String**  | 必要。 識別事件類別的字串 Guid。 例如，Guid ( "{3F92E6E0-9886-434e-85DB-0D11D3904C0A}" ) 。 事件提供者會使用 Guid 來設定 [**事件 \_ 追蹤 \_ 標頭。Guid**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) 成員，讓取用者可以判斷它們所接收的事件類別。                                                                                                                                                                                                                                                                                  |
| **EventVersion** | **整數** | 針對最新版本的事件追蹤類別，此辨識符號是選擇性的，而且所有舊版的類別都需要此限定詞。 類別的最新版本不會指定 **EventVersion** 限定詞，也不會有最高的版本號碼。 版本號碼以0開頭，例如，EventVersion (0) 。一般來說，當您建立類別的新版本時，您也會將舊版重新命名為 <classname> \_ Vn，其中 n 是從0開始的遞增編號。 如需範例，請參閱 [**FileIo**](fileio.md) 和 [**FileIo \_ V0**](fileio-v0.md)。<br/> |



 

## <a name="event-type-mof-class-qualifiers"></a>事件種類 MOF 類別限定詞

下表列出您可以在事件種類類別上指定的限定詞， (定義事件屬性資料) 的類別。



| Qualifier         | 值       | 描述                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EventType**     | **整數** | 必要。 識別事件種類類別。 例如，「事件1」 (1) 。 事件提供者會使用相同的事件種類值來設定 [**事件 \_ 追蹤 \_ 標頭。類別。類型**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)。 如果有多個事件種類使用相同的 MOF 類別 (因為它們使用相同的事件資料) ，請將事件種類值指定為整數的陣列，例如，事件種類 {12,15} 。 |
| **EventTypeName** | **String**  | 選擇性。 描述事件種類。 例如，EventTypeName ( "Start" ) 。 如果多個事件種類使用相同的 MOF 類別 (因為它們使用相同的事件資料) ，請將事件種類名稱值指定為字串陣列，例如 EventTypeName {"Start"，"End"}。 EventTypeName 陣列的元素會直接對應至事件陣列。                 |



 

## <a name="property-qualifiers"></a>屬性限定詞

下表列出您可以在屬性上指定的限定詞。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Qualifier</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>點陣圖</strong></td>
<td>指定對應至字串值的位位置。 如果您指定這個辨識符號，您也必須指定 <strong>BitValues</strong> 限定詞。</td>
</tr>
<tr class="even">
<td><strong>BitValues</strong></td>
<td>字串值。 如果也指定了 <strong>點陣圖</strong> 辨識符號，字串就會直接對應到 <strong>點陣圖</strong> 辨識符號中的值。 否則，假設屬性值是值字串的單一索引， (位1對應至清單) 中的第一個字串。</td>
</tr>
<tr class="odd">
<td><strong>延伸模組</strong></td>
<td>提供有關如何使用 (解讀資料) 的其他資訊。 擴充值不區分大小寫。 以引號括住值，例如 (Guid) 的擴充功能 &quot; &quot; 。 可能的擴充值為： <dl> <dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Guid</dt> <dd> 指出屬性資料是 Guid。 MOF 資料類型必須是 <strong>object</strong>。 承載應為 <strong>GUID</strong> 結構。<br/> </dd> <dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>IPAddr 和 IPAddrV4</dt> <dd> 資料是 IP V4 位址。 MOF 資料類型必須是 <strong>object</strong>。 承載應為不帶正負號的 long。 不帶正負號的每個位元組都代表 IP 位址的四個部分中的其中一個（ (p1. p4) 。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。<br/> <strong>在 Windows Vista 之前：</strong>不支援 IPAddrV4 延伸模組。<br/> </dd> <dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> <dd> 資料是 IP V6 位址。 MOF 資料類型必須是 <strong>object</strong>。 承載應為 <strong>IN6_ADDR</strong> 結構。 <br/> <strong>在 Windows Vista 之前：</strong>不支援 IPAddrV6 延伸模組。<br/> </dd> <dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>NoPrint</dt> <dd> 指出取用者不應列印此資料。<br/> </dd> <dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>港口</dt> <dd> 資料會識別埠號碼。 MOF 資料類型必須是 <strong>object</strong>。 承載應為不帶正負號的簡短。<br/> </dd> <dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> <dd> 換行字元是以空格取代。 承載應為以 null 結束的 ANSI 字串。<br/> </dd> <dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>RWString</dt> <dd> 換行字元是以空格取代。 承載應為以 null 結尾的寬字元字串。<br/> </dd> <dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>希</dt> <dd> 資料代表二進位 blob SID。 MOF 資料類型必須是 <strong>object</strong>。 <br/> SID 的長度是可變的。 前4個位元組中包含的值 (<strong>ULONG</strong>) 指出 blob 是否包含 SID。 如果 blob 的前4個位元組 (<strong>ULONG</strong>) 為非零值，則 blob 會包含 SID。 Blob 的第一個部分包含 TOKEN_USER (結構在8個位元組的界限上對齊) ，而第二個部分則包含 SID。 若要處理 blob 的 SID 部分：<br/>
<ul>
<li>將位元組指標設定為 blob 的開頭</li>
<li>將事件記錄檔的指標大小乘以2，然後將產品加入至位元組指標， (<a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>包含指標大小值的<strong>PointerSize</strong>成員) </li>
</ul>
<br/> 您可以使用下列宏來判斷 SID 的長度。 <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> <dd> 指出屬性包含指標值。 指標值的大小取決於用來記錄事件的作業系統;承載會包含32位系統的4位元組值，或64位系統的8位元組值。 MOF 資料類型必須是 <strong>object</strong>。<br/> 如果屬性包含<strong>SizeT</strong>延伸模組，取用者應該忽略資料類型和<strong>格式</strong>限定詞。 若要判斷要為屬性讀取的資料大小，請使用：
<ul>
<li><a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>的<strong>PointerSize</strong>成員</li>
<li><a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a>的<strong>旗標</strong>成員</li>
</ul>
<br/> <strong>在 Windows Vista 之前：</strong><strong>PointerSize</strong>值可能不正確。 例如，在64位的電腦上，32位應用程式將會記錄4位元組指標;不過，會話會將 <strong>PointerSize</strong> 設定為8。<br/> </dd> <dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>變異</dt> <dd> 資料代表 blob。 前四個位元組 (uint32) 指出 blob 的大小。 MOF 資料類型必須是 <strong>object</strong>。 <br/> </dd> <dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>WmiTime</dt> <dd> 將時間戳記轉譯為系統時間。 MOF 資料類型必須是 <strong>object</strong>。 承載應為不帶正負號的64位整數。<br/> <strong>在 Windows Vista 之前：</strong>無法使用。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>格式</strong></td>
<td>定義屬性資料的格式。 例如，包含 &quot; 字串屬性 (w) 的格式， &quot; 表示字串為寬字元串。 可能的值包括：
<table>
<thead>
<tr class="header">
<th>詞彙</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="c"></span><span id="C"></span>C<br/></td>
<td>將屬性值顯示成 ASCII 字元。 您可以將此限定詞與 <strong>uint8</strong> 資料類型搭配使用。<br/></td>
</tr>
<tr class="even">
<td><span id="s"></span><span id="S"></span>！<br/></td>
<td>將字元陣列視為以 null 終止的字串。 如果資料類型為 <strong>char16</strong>，則字串是寬字元字串;否則，字串是 ASCII 字元字串。<br/></td>
</tr>
<tr class="odd">
<td><span id="w"></span><span id="W"></span>w<br/></td>
<td>屬性值是寬字元字串。 您可以使用此限定詞搭配 <strong>字串</strong> 資料類型。 <br/></td>
</tr>
<tr class="even">
<td><span id="x"></span><span id="X"></span>X<br/></td>
<td>將屬性值顯示為十六進位數位。 您可以將此限定詞與 16-、32-和64位整數資料類型搭配使用。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><strong>指標</strong></td>
<td><p>指出屬性包含指標值。 指標值的大小取決於用來記錄事件的作業系統;承載會包含32位系統的4位元組值，或64位系統的8位元組值。 MOF 資料類型必須是 <strong>object</strong>。</p>
<p>如果屬性包含<strong>SizeT</strong>延伸模組，取用者應該忽略資料類型和<strong>格式</strong>限定詞。 若要判斷要為屬性讀取的資料大小，請使用：</p>
<ul>
<li><a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a>的<strong>PointerSize</strong>成員</li>
<li><a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a>的<strong>旗標</strong>成員</li>
</ul>
<p><strong>在 Windows Vista 之前：</strong><strong>PointerSize</strong>值可能不正確。 例如，在64位的電腦上，32位應用程式將會記錄4位元組指標;不過，會話會將 <strong>PointerSize</strong> 設定為8。</p>
<p>請注意，有些事件會使用 <strong>PointerType</strong> 而非 <strong>指標</strong>;請勿使用 <strong>PointerType</strong>。</p></td>
</tr>
<tr class="even">
<td><strong>StringTermination</strong></td>
<td>指出如何終止字串屬性。 例如，StringTermination (&quot; NullTerminated &quot;) 表示字串屬性是以 null 結束。 可能的值包括：
<dl> <dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>數</strong></dt> <dd>
<p>字串的長度是以 <strong>USHORT</strong> 值的形式內嵌在字串開頭。</p>
</dd> <dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>NotCounted</strong></dt> <dd>
<p>字串不是以 null 終止，且字串的長度不會內嵌在字串開頭。 在此情況下，此字串應該是最後一個元素，並佔用事件資料結尾的所有空間。</p>
</dd> <dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> <dd>
<p>字串以 null 結束。 如果您未指定 <strong>StringTermination</strong> 限定詞，則會假設字串是以 null 結束。</p>
</dd> <dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>ReverseCounted</strong></dt> <dd>
<p>字串的長度內嵌在字串開頭，做為位元組由大到小格式的 <strong>USHORT</strong> 值。</p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ValueDescriptions</strong></td>
<td>提供 <strong>值</strong> 限定詞中每個值的描述。 當您嘗試取出關鍵字和層級資訊時， <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>TdhEnumerateProviderFieldInformation</strong></a> 和 <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>TdhQueryProviderFieldInformation</strong></a> 函數會傳回這些描述。 描述是選擇性的。 如果您未提供描述，函數會傳回 <strong>Null</strong>。 如需詳細資訊，請參閱針對 <a href="#specifying-level-and-enable-flags-values-for-a-provider">提供者指定層級和啟用旗標值</a> 。</td>
</tr>
<tr class="even">
<td><strong>ValueMap</strong></td>
<td>指定對應至字串值的整數索引或旗標值。 如果您指定此限定詞，您也必須指定 <strong>值</strong> 限定詞，以及選擇性地指定 <strong>ValueType</strong> 辨識符號。 請注意，ETW 不支援具有值對應值字串的 WMI 選項。
<p>下列範例示範如何使用 ValueMap、值和 ValueType 限定詞。</p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><strong>值</strong></td>
<td>字串值。 如果同時指定了 <strong>valuemap</strong> 辨識符號，字串就會直接對應到 <strong>valuemap</strong> 辨識符號中的值。 否則，假設屬性值是以零為基底的索引至值字串。</td>
</tr>
<tr class="even">
<td><strong>ValueType</strong></td>
<td>指出 <strong>ValueMap</strong> 值是否為整數索引值或位旗標值。 如果您未指定此辨識符號，則會假設為整數索引值。 若要指定值為整數索引值，請使用 ValueType (&quot; 索引 &quot;) 。 若要指定值為位旗標值，請使用 ValueType (&quot; 旗標 &quot;) 。</td>
</tr>
<tr class="odd">
<td><strong>WmiDataId</strong></td>
<td>每個屬性都必須包含 <strong>WmiDataId</strong> 限定詞。 <strong>WmiDataId</strong> 會定義取用者讀取事件資料的順序。 <strong>WmiDataId</strong>的值會從1開始，並針對類別中的每個屬性遞增。 例如，WmiDataId (1) 。</td>
</tr>
<tr class="even">
<td><strong>XMLFragment</strong></td>
<td>表示資料為 XML 格式，而且可以在不進一步格式化的情況下顯示。</td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a>指定提供者的層級和啟用旗標值

若要記錄層級，並啟用控制器將用來啟用您提供者的旗標，請在提供者 MOF 類別中包含「等級」和「旗標」屬性。 層級和旗標屬性名稱會區分大小寫。 屬性必須包含 **值** 和 **ValueMap** 限定詞，以指定可能的層級和啟用旗標值。 啟用旗標值的 **ValueMap** 必須是) 值的位 (旗標。 **ValueDescriptions** 限定詞是選擇性的，但您應該使用它來提供每個可能值的描述。 當有人呼叫 [**TdhEnumerateProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) 和 [**TdhQueryProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) 函式以取得可能的層級，並啟用 (關鍵字的旗標) 值給提供者時，就會使用這些描述。

下圖顯示指定可能層級和啟用旗標值的提供者類別。

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

 

 
