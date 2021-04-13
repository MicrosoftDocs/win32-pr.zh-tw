---
title: Wecutil.exe
description: Wecutil.exe 是 Windows 事件收集器公用程式，可讓系統管理員建立和管理從支援 WS-Management 通訊協定的遠端事件來源轉送的事件訂閱。
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104322568"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe 是 Windows 事件收集器公用程式，可讓系統管理員建立和管理從支援 WS-Management 通訊協定的遠端事件來源轉送的事件訂閱。 此公用程式的命令、選項和選項值不區分大小寫。

如果您在嘗試執行 >wecutil 時收到指出「RPC 伺服器無法使用」或「介面不明」的訊息，則需要啟動 Windows 事件收集器服務 (wecsvc) 。 若要開始 wecsvc，請在提升許可權的命令提示字元下輸入 **net start wecsvc**。

## <a name="list-existing-subscriptions"></a>列出現有的訂閱

下列語法用來列出現有的遠端事件訂閱。

``` syntax
wecutil { es | enum-subscription }
```

如果您使用腳本從輸出取得訂用帳戶的名稱，您將需要在輸出的第一行中略過 UTF-8 BOM 字元。 下列腳本顯示如何略過 BOM 字元的範例。

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a>取得訂用帳戶設定

下列語法用來顯示遠端事件訂閱設定資料。

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>取得設定參數

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**
</dt> <dd>

可唯一識別訂閱的字串。 此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f： * 值***
</dt> <dd>

值，指定訂用帳戶設定資料的輸出。 *值* 可以是 "XML" 或 "簡易"，而預設值為 "簡易"。 如果 *值* 為 "xml"，則輸出會以 "xml" 格式列印。 如果 *值* 為 "簡易"，則輸出會以成對的名稱/值進行列印。

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u： *值***
</dt> <dd>

值，指定輸出是否為 Unicode 格式。 *值* 可以是 "true" 或 "false"。 如果 *值* 為 "true"，則輸出為 unicode 格式，如果 *值* 為 "false"，則輸出不是 unicode 格式。

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>取得訂用帳戶執行時間狀態

下列語法用來顯示訂用帳戶執行時間狀態。

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>取得狀態參數

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**
</dt> <dd>

可唯一識別訂閱的字串。 此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**事件 \_ 來源**
</dt> <dd>

值，這個值會識別屬於事件訂閱之事件來源的電腦。 此值可以是電腦的完整功能變數名稱、NetBIOS 名稱或 IP 位址。

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>設定訂用帳戶設定資訊

下列語法可透過從命令列變更訂用帳戶參數或使用 XML 設定檔來設定訂閱設定資料。

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a>備註

當 **>wecutil ss** 命令中指定了不正確的使用者名稱或密碼時，除非您使用 **>wecutil gr** 命令來查看訂用帳戶的執行時間狀態，否則不會報告錯誤。

## <a name="set-configuration-parameters"></a>設定設定參數

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**
</dt> <dd>

可唯一識別訂閱的字串。 此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c： *CONGIG \_* 檔案**
</dt> <dd>

值，指定包含訂閱設定資訊之 XML 檔案的路徑。 路徑可以是目前目錄的絕對路徑或相對路徑。 這個參數只能搭配選用的/cus 和/cup 參數使用，而且與所有其他參數互斥。

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e： *值***
</dt> <dd>

值，決定是否要啟用或停用訂閱。 值可以是 true 或 false。 預設值為 true，可啟用訂用帳戶。

> [!Note]  
> 當您停用收集器起始的訂用帳戶時，事件來源會變成非使用中，而非停用。 在收集器起始的訂用帳戶中，您可以停用與訂用帳戶無關的事件來源。

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d： *描述***
</dt> <dd>

值，指定事件訂閱的描述。

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex： *日期 \_ 時間***
</dt> <dd>

指定訂閱到期時間的值。 *日期 \_TIME* 是標準 XML 或 ISO8601 日期時間格式所指定的值： "yyyy-mm-dd-ddThh： MM： ss \[ \] \[ Z \] "，其中 "T" 是時間分隔符號，而 "Z" 表示 UTC 時間。 例如，如果 *日期 \_ 時間* 為 "2007-01-12T01：20： 00"，則訂閱到期時間為2007年1月12日，01:20。

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri： *uri***
</dt> <dd>

值，指定訂閱所使用的事件種類。 事件來源電腦的位址和統一資源識別項 (URI) 唯一識別事件的來源。 URI 字串會用於訂用帳戶中的所有事件來源位址。

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm： *設定 \_ 模式***
</dt> <dd>

值，指定事件訂閱的設定模式。 *設定 \_模式* 可以是下列其中一個字串：「標準」、「自訂」、「MinLatency」或「MinBandwidth」。 EC 訂用帳戶設定 [**\_ \_ \_ 模式**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) 列舉會定義設定模式。 只有在設定模式設定為 [自訂] 時，才能指定/dm、/dmi、/hi 和/dmlt 參數。

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q： *查詢***
</dt> <dd>

值，指定訂閱的查詢字串。 這個字串的格式可以不同于不同的 URI 值，並套用至訂用帳戶中的所有事件來源。

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia： *方言***
</dt> <dd>

值，指定查詢字串使用的方言。

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf： *FORMAT***
</dt> <dd>

值，指定傳回之事件的格式。 *格式* 可以是 "Events" 或 "RenderedText"。 當值為 "RenderedText" 時，會傳回具有當地語系化字串的事件 (例如) 附加至事件的事件描述字串。 *FORMAT* 的預設值是 "RenderedText"。

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l：*地區* 設定**
</dt> <dd>

值，指定用來傳遞轉譯文字格式之當地語系化字串的地區設定。 *地區* 設定是語言/國家（地區）文化特性識別碼，例如 "en-us"。 只有當/cf 參數設定為 "RenderedText" 時，此參數才有效。

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree： \[ *值*\]**
</dt> <dd>

值，指定要傳遞給訂閱的事件。 *值* 可以是 true 或 false。 *當值* 為 true 時，會從訂用帳戶事件來源讀取所有現有的事件。 *當值* 為 false 時，僅會傳遞未來 (抵達) 事件。 如果指定/ree 時沒有值，預設值為 true; 如果未指定/ree，則預設值為 false。

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf： *FILENAME***
</dt> <dd>

值，指定用來儲存從事件訂閱接收之事件的本機事件記錄檔。

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn： *發行者***
</dt> <dd>

值，指定 (提供者) 名稱的事件發行者。 它必須是擁有或匯入/lf 參數所指定之記錄檔的發行者。

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm： *模式***
</dt> <dd>

指定訂閱傳遞模式的值。 *模式* 可以是 push 或 pull。 只有當/cm 參數設定為 Custom 時，此選項才有效。

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi： *NUMBER***
</dt> <dd>

值，指定事件訂用帳戶中批次處理傳遞的最大專案數。 只有當/cm 參數設定為 Custom 時，此選項才有效。

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt： *MS***
</dt> <dd>

值，指定傳遞事件批次所允許的最大延遲。 MS 是允許的毫秒數。 只有當/cm 參數設定為 Custom 時，此參數才有效。

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi： *MS***
</dt> <dd>

值，指定訂閱的心跳間隔。 *毫秒* 是間隔中使用的毫秒數。 只有當/cm 參數設定為 Custom 時，此參數才有效。

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn： *net-transportname***
</dt> <dd>

值，指定用來連接到遠端事件來源電腦的傳輸名稱。

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa： *事件 \_ 來源***
</dt> <dd>

值，指定事件來源電腦的位址。 *活動 \_來源* 是一種字串，可使用電腦的完整功能變數名稱、NetBIOS 名稱或 IP 位址來識別事件來源電腦。 這個參數可以與/ese、/aes、/res 或/un 和/up 參數搭配使用。

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese： *值***
</dt> <dd>

判斷是否要啟用或停用事件來源的值。 *值* 可以是 true 或 false。 預設值為 true，這會啟用事件來源。 只有在使用/esa 參數時，才會使用這個參數。

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

值，如果事件來源還不是事件訂閱的一部分，此值會加入/esa 參數所指定的事件來源。 如果/esa 參數指定的電腦已經是訂用帳戶的一部分，則會顯示錯誤。 只有在使用/esa 參數時，才允許這個參數。

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

如果事件來源已經是事件訂閱的一部分，則為移除/esa 參數所指定之事件來源的值。 如果/esa 參數所指定的電腦不是訂用帳戶的一部分，則會顯示錯誤。 只有在使用/esa 參數時，才允許這個參數。

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un： *USERNAME***
</dt> <dd>

值，指定認證中所使用的使用者名稱，以連接到/esa 參數中指定的事件來源。 只有在使用/esa 參數時，才允許這個參數。

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up： *密碼***
</dt> <dd>

值，指定在/un 參數中指定之使用者名稱的密碼。 使用者名稱和密碼認證是用來連接到/esa 參數中指定的事件來源。 只有在使用/un 參數時，才允許這個參數。

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp： *TRANSPORTPORT***
</dt> <dd>

值，指定連接到遠端事件來源電腦時，傳輸所使用的埠號碼。

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn： *NAME***
</dt> <dd>

值，指定本機電腦的 DNS 名稱。 遠端事件來源會使用這個名稱來推送事件，而且必須只用于發送訂閱。

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct： *類型***
</dt> <dd>

值，指定用來存取遠端事件來源的認證類型。 *類型* 可以是 "default"、"negotiate"、"digest"、"basic" 或 "localmachine"。 預設值為 "default"。 這些值定義于 [**EC \_ 訂閱 \_ 認證 \_ 類型**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) 列舉中。

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun： *USERNAME***
</dt> <dd>

值，這個值會設定共用使用者認證，而這些認證用於沒有自己的使用者認證的事件來源。

> [!Note]  
> 如果這個參數與/c 選項搭配使用，則會忽略設定檔案中個別事件來源的使用者名稱和密碼設定。 如果您想要針對特定事件來源使用不同的認證，您可以在另一個 set 訂用帳戶命令的命令列上，指定特定事件來源的/un 和/up 參數，以覆寫此值。

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup： *密碼***
</dt> <dd>

值，設定共用使用者認證的使用者密碼。 當 *密碼* 設定為 \* (星號) 時，會從主控台讀取密碼。 只有在指定/cun 參數時，這個選項才有效。

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica： *指紋***
</dt> <dd>

此值會以逗號分隔的清單，設定簽發者憑證 thumb 的清單。

> [!Note]  
> 此選項只適用于來源起始的訂閱。

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as： *允許***
</dt> <dd>

值，這個值會設定以逗號分隔的字串清單，指定允許起始訂用帳戶之非網域電腦的 DNS 名稱。 您可以使用萬用字元（例如 ". mydomain.com"）來指定名稱 \* 。 根據預設，此清單是空的。

> [!Note]  
> 此選項只適用于來源起始的訂閱。

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds： *拒絕***
</dt> <dd>

值，這個值會設定以逗號分隔的字串清單，指定不允許起始訂閱之非網域電腦的 DNS 名稱。 您可以使用萬用字元（例如 ". mydomain.com"）來指定名稱 \* 。 根據預設，此清單是空的。

> [!Note]  
> 此選項只適用于來源起始的訂閱。

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc： *SDDL***
</dt> <dd>

值，以 SDDL 格式設定字串，指定允許或不允許哪些網域電腦起始訂閱。 預設為允許所有網域電腦起始訂閱。

> [!Note]  
> 此選項只適用于來源起始的訂閱。

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>建立新的訂閱

下列語法用來為遠端電腦上的事件建立事件訂閱。

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>備註

當 **>wecutil cs** 命令中指定了不正確的使用者名稱或密碼時，除非您使用 **>wecutil gr** 命令來查看訂用帳戶的執行時間狀態，否則不會報告錯誤。

## <a name="creation-parameters"></a>建立參數

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**配置 \_ 檔**
</dt> <dd>

值，指定包含訂閱設定資訊之 XML 檔案的路徑。 路徑可以是目前目錄的絕對路徑或相對路徑。

下列 XML 是訂用帳戶設定檔的範例，此檔案會建立收集器起始的訂用帳戶，以將遠端電腦的應用程式事件記錄檔中的事件轉送至 ForwardedEvents 記錄檔。


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



下列 XML 是訂用帳戶設定檔的範例，它會建立來源起始的訂用帳戶，以將遠端電腦的應用程式事件記錄檔中的事件轉送至 ForwardedEvents 記錄檔。


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> 建立來源起始的訂閱時，如果 **AllowedSourceDomainComputers**、 **AllowedSourceNonDomainComputers** / **IssuerCAList**、 **AllowedSubjectList** 和 **DeniedSubjectList** 都是空的，則會提供 **AllowedSourceDomainComputers** 的預設值： O:NSG： NSD： (a;;GA;;;DC)  (A;;GA;;;NS) 」。 此 SDDL 預設會授與網域電腦網域群組的成員，以及本機轉寄站) 的局域網路服務群組 (，這是為此訂用帳戶引發事件的能力。

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun： *USERNAME***
</dt> <dd>

值，這個值會設定共用使用者認證，而這些認證用於沒有自己的使用者認證的事件來源。 此值僅適用于收集器起始的訂閱。

> [!Note]  
> 如果指定這個參數，則會忽略設定檔案中個別事件來源的使用者名稱和密碼設定。 如果您想要針對特定事件來源使用不同的認證，您可以在另一個 set 訂用帳戶命令的命令列上，指定特定事件來源的/un 和/up 參數，以覆寫此值。

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup： *密碼***
</dt> <dd>

值，設定共用使用者認證的使用者密碼。 當 *密碼* 設定為 " \* " (星號) ，則會從主控台讀取密碼。 只有在指定/cun 參數時，這個選項才有效。

</dd> </dl>

## <a name="delete-a-subscription"></a>刪除訂用帳戶

下列語法用來刪除事件訂閱。

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>刪除參數

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**
</dt> <dd>

可唯一識別訂閱的字串。 此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。 將會刪除此參數中識別的訂用帳戶。

</dd> </dl>

## <a name="retry-a-subscription"></a>重試訂用帳戶

下列語法用來重試非使用中的訂閱，方法是藉由建立每個事件來源的連接，並將遠端訂閱要求傳送至事件來源，藉以重試非使用中的訂閱。 停用的事件來源不會重試。

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>重試參數

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**
</dt> <dd>

可唯一識別訂閱的字串。 此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。 將會重試此參數中識別的訂用帳戶。

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**事件 \_ 來源**
</dt> <dd>

值，這個值會識別屬於事件訂閱之事件來源的電腦。 此值可以是電腦的完整功能變數名稱、NetBIOS 名稱或 IP 位址。

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>設定 Windows 事件收集器服務

下列語法是用來設定 Windows 事件收集器服務，以確保可以在電腦重新開機時建立和持續事件訂閱。 這包括下列程式：

**設定 Windows 事件收集器服務**

1.  如果已停用，請啟用 ForwardedEvents 通道。
2.  延遲 Windows 事件收集器服務的啟動。
3.  如果 Windows 事件收集器服務未執行，請加以啟動。

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>設定事件收集器參數

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q： *值***
</dt> <dd>

值，這個值會決定快速設定命令是否會提示確認。 值可以是 true 或 false。 如果值為 true，則命令會提示您進行確認。 預設值為 false。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



 

 





