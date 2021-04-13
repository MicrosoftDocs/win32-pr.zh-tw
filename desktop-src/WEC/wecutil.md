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
# <a name="wecutilexe"></a><span data-ttu-id="998c3-104">Wecutil.exe</span><span class="sxs-lookup"><span data-stu-id="998c3-104">Wecutil.exe</span></span>

<span data-ttu-id="998c3-105">Wecutil.exe 是 Windows 事件收集器公用程式，可讓系統管理員建立和管理從支援 WS-Management 通訊協定的遠端事件來源轉送的事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-105">Wecutil.exe is a Windows Event Collector utility that enables an administrator to create and manage subscriptions to events forwarded from remote event sources that support the WS-Management protocol.</span></span> <span data-ttu-id="998c3-106">此公用程式的命令、選項和選項值不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="998c3-106">Commands, options, and option values are case-insensitive for this utility.</span></span>

<span data-ttu-id="998c3-107">如果您在嘗試執行 >wecutil 時收到指出「RPC 伺服器無法使用」或「介面不明」的訊息，則需要啟動 Windows 事件收集器服務 (wecsvc) 。</span><span class="sxs-lookup"><span data-stu-id="998c3-107">If you receive a message that says "The RPC server is unavailable" or "The interface is unknown" when you try to run wecutil, then you need to start the Windows Event Collector service (wecsvc).</span></span> <span data-ttu-id="998c3-108">若要開始 wecsvc，請在提升許可權的命令提示字元下輸入 **net start wecsvc**。</span><span class="sxs-lookup"><span data-stu-id="998c3-108">To start wecsvc, at an elevated command prompt type **net start wecsvc**.</span></span>

## <a name="list-existing-subscriptions"></a><span data-ttu-id="998c3-109">列出現有的訂閱</span><span class="sxs-lookup"><span data-stu-id="998c3-109">List existing subscriptions</span></span>

<span data-ttu-id="998c3-110">下列語法用來列出現有的遠端事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-110">The following syntax is used to list existing remote event subscriptions.</span></span>

``` syntax
wecutil { es | enum-subscription }
```

<span data-ttu-id="998c3-111">如果您使用腳本從輸出取得訂用帳戶的名稱，您將需要在輸出的第一行中略過 UTF-8 BOM 字元。</span><span class="sxs-lookup"><span data-stu-id="998c3-111">If you use a script to get the names of the subscriptions from the output, you will need to bypass the UTF-8 BOM characters in the first line of the output.</span></span> <span data-ttu-id="998c3-112">下列腳本顯示如何略過 BOM 字元的範例。</span><span class="sxs-lookup"><span data-stu-id="998c3-112">The following script shows an example of how you might skip the BOM characters.</span></span>

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

## <a name="get-subscription-configuration"></a><span data-ttu-id="998c3-113">取得訂用帳戶設定</span><span class="sxs-lookup"><span data-stu-id="998c3-113">Get subscription configuration</span></span>

<span data-ttu-id="998c3-114">下列語法用來顯示遠端事件訂閱設定資料。</span><span class="sxs-lookup"><span data-stu-id="998c3-114">The following syntax is used to display remote event subscription configuration data.</span></span>

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a><span data-ttu-id="998c3-115">取得設定參數</span><span class="sxs-lookup"><span data-stu-id="998c3-115">Get Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998c3-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="998c3-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-117">可唯一識別訂閱的字串。</span><span class="sxs-lookup"><span data-stu-id="998c3-117">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="998c3-118">此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="998c3-118">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f： \* 值**\*</span><span class="sxs-lookup"><span data-stu-id="998c3-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:\*VALUE**\*</span></span>
</dt> <dd>

<span data-ttu-id="998c3-120">值，指定訂用帳戶設定資料的輸出。</span><span class="sxs-lookup"><span data-stu-id="998c3-120">A value that specifies the output of the subscription configuration data.</span></span> <span data-ttu-id="998c3-121">*值* 可以是 "XML" 或 "簡易"，而預設值為 "簡易"。</span><span class="sxs-lookup"><span data-stu-id="998c3-121">*VALUE* can be "XML" or "Terse", and the default is "Terse".</span></span> <span data-ttu-id="998c3-122">如果 *值* 為 "xml"，則輸出會以 "xml" 格式列印。</span><span class="sxs-lookup"><span data-stu-id="998c3-122">If *VALUE* is "XML", then the output is printed in "XML" format.</span></span> <span data-ttu-id="998c3-123">如果 *值* 為 "簡易"，則輸出會以成對的名稱/值進行列印。</span><span class="sxs-lookup"><span data-stu-id="998c3-123">If *VALUE* is "Terse", then the output is printed in name-value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u： *值***</span><span class="sxs-lookup"><span data-stu-id="998c3-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-125">值，指定輸出是否為 Unicode 格式。</span><span class="sxs-lookup"><span data-stu-id="998c3-125">A value that specifies whether the output is in Unicode format.</span></span> <span data-ttu-id="998c3-126">*值* 可以是 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="998c3-126">*VALUE* can be "true" or "false".</span></span> <span data-ttu-id="998c3-127">如果 *值* 為 "true"，則輸出為 unicode 格式，如果 *值* 為 "false"，則輸出不是 unicode 格式。</span><span class="sxs-lookup"><span data-stu-id="998c3-127">If *VALUE* is "true", then the output is in Unicode format, and if *VALUE* is "false", then the output is not in Unicode format.</span></span>

</dd> </dl>

## <a name="get-subscription-runtime-status"></a><span data-ttu-id="998c3-128">取得訂用帳戶執行時間狀態</span><span class="sxs-lookup"><span data-stu-id="998c3-128">Get subscription runtime status</span></span>

<span data-ttu-id="998c3-129">下列語法用來顯示訂用帳戶執行時間狀態。</span><span class="sxs-lookup"><span data-stu-id="998c3-129">The following syntax is used to display the subscription runtime status.</span></span>

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a><span data-ttu-id="998c3-130">取得狀態參數</span><span class="sxs-lookup"><span data-stu-id="998c3-130">Get Status Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998c3-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="998c3-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-132">可唯一識別訂閱的字串。</span><span class="sxs-lookup"><span data-stu-id="998c3-132">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="998c3-133">此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="998c3-133">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**事件 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="998c3-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-135">值，這個值會識別屬於事件訂閱之事件來源的電腦。</span><span class="sxs-lookup"><span data-stu-id="998c3-135">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="998c3-136">此值可以是電腦的完整功能變數名稱、NetBIOS 名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="998c3-136">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="set-subscription-configuration-information"></a><span data-ttu-id="998c3-137">設定訂用帳戶設定資訊</span><span class="sxs-lookup"><span data-stu-id="998c3-137">Set Subscription Configuration Information</span></span>

<span data-ttu-id="998c3-138">下列語法可透過從命令列變更訂用帳戶參數或使用 XML 設定檔來設定訂閱設定資料。</span><span class="sxs-lookup"><span data-stu-id="998c3-138">The following syntax is used to set subscription configuration data by changing subscription parameters from the command line or using an XML configuration file.</span></span>

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

### <a name="remarks"></a><span data-ttu-id="998c3-139">備註</span><span class="sxs-lookup"><span data-stu-id="998c3-139">Remarks</span></span>

<span data-ttu-id="998c3-140">當 **>wecutil ss** 命令中指定了不正確的使用者名稱或密碼時，除非您使用 **>wecutil gr** 命令來查看訂用帳戶的執行時間狀態，否則不會報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="998c3-140">When an incorrect username or password is specified in the **wecutil ss** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="set-configuration-parameters"></a><span data-ttu-id="998c3-141">設定設定參數</span><span class="sxs-lookup"><span data-stu-id="998c3-141">Set Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998c3-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="998c3-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-143">可唯一識別訂閱的字串。</span><span class="sxs-lookup"><span data-stu-id="998c3-143">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="998c3-144">此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="998c3-144">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c： *CONGIG \_* 檔案**</span><span class="sxs-lookup"><span data-stu-id="998c3-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG\_FILE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-146">值，指定包含訂閱設定資訊之 XML 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="998c3-146">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="998c3-147">路徑可以是目前目錄的絕對路徑或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="998c3-147">The path can be absolute or relative to the current directory.</span></span> <span data-ttu-id="998c3-148">這個參數只能搭配選用的/cus 和/cup 參數使用，而且與所有其他參數互斥。</span><span class="sxs-lookup"><span data-stu-id="998c3-148">This parameter can only be used with the optional /cus and /cup parameters, and is mutually exclusive with all the other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e： *值***</span><span class="sxs-lookup"><span data-stu-id="998c3-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-150">值，決定是否要啟用或停用訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-150">A value that determines whether to enable or disable the subscription.</span></span> <span data-ttu-id="998c3-151">值可以是 true 或 false。</span><span class="sxs-lookup"><span data-stu-id="998c3-151">VALUE can be true or false.</span></span> <span data-ttu-id="998c3-152">預設值為 true，可啟用訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="998c3-152">The default value is true, which enables the subscription.</span></span>

> [!Note]  
> <span data-ttu-id="998c3-153">當您停用收集器起始的訂用帳戶時，事件來源會變成非使用中，而非停用。</span><span class="sxs-lookup"><span data-stu-id="998c3-153">When you disable a collector initiated subscription, the event source becomes inactive instead of disabled.</span></span> <span data-ttu-id="998c3-154">在收集器起始的訂用帳戶中，您可以停用與訂用帳戶無關的事件來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-154">In a collector initiated subscription, you can disable an event source independent of the subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="998c3-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d： *描述***</span><span class="sxs-lookup"><span data-stu-id="998c3-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-156">值，指定事件訂閱的描述。</span><span class="sxs-lookup"><span data-stu-id="998c3-156">A value that specifies a description for the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex： *日期 \_ 時間***</span><span class="sxs-lookup"><span data-stu-id="998c3-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE\_TIME***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-158">指定訂閱到期時間的值。</span><span class="sxs-lookup"><span data-stu-id="998c3-158">A value that specifies the subscription expiration time.</span></span> <span data-ttu-id="998c3-159">*日期 \_TIME* 是標準 XML 或 ISO8601 日期時間格式所指定的值： "yyyy-mm-dd-ddThh： MM： ss \[ \] \[ Z \] "，其中 "T" 是時間分隔符號，而 "Z" 表示 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="998c3-159">*DATE\_TIME* is a value specified in standard XML or ISO8601 date-time format: "yyyy-MM-ddThh:mm:ss\[.sss\]\[Z\]" where "T" is the time separator and "Z" indicates UTC time.</span></span> <span data-ttu-id="998c3-160">例如，如果 *日期 \_ 時間* 為 "2007-01-12T01：20： 00"，則訂閱到期時間為2007年1月12日，01:20。</span><span class="sxs-lookup"><span data-stu-id="998c3-160">For example, if *DATE\_TIME* is "2007-01-12T01:20:00", then the subscription expiration time is January 12th, 2007, 01:20.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri： *uri***</span><span class="sxs-lookup"><span data-stu-id="998c3-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-162">值，指定訂閱所使用的事件種類。</span><span class="sxs-lookup"><span data-stu-id="998c3-162">A value that specifies the type of events consumed by the subscription.</span></span> <span data-ttu-id="998c3-163">事件來源電腦的位址和統一資源識別項 (URI) 唯一識別事件的來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-163">The address of the event source computer along with the uniform resource identifier (URI) uniquely identifies the source of the events.</span></span> <span data-ttu-id="998c3-164">URI 字串會用於訂用帳戶中的所有事件來源位址。</span><span class="sxs-lookup"><span data-stu-id="998c3-164">The URI string is used for all event source addresses in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm： *設定 \_ 模式***</span><span class="sxs-lookup"><span data-stu-id="998c3-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *CONFIGURATION\_MODE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-166">值，指定事件訂閱的設定模式。</span><span class="sxs-lookup"><span data-stu-id="998c3-166">A value that specifies the configuration mode of the event subscription.</span></span> <span data-ttu-id="998c3-167">*設定 \_模式* 可以是下列其中一個字串：「標準」、「自訂」、「MinLatency」或「MinBandwidth」。</span><span class="sxs-lookup"><span data-stu-id="998c3-167">*CONFIGURATION\_MODE* can be one of the following strings: "Normal", "Custom", "MinLatency", or "MinBandwidth".</span></span> <span data-ttu-id="998c3-168">EC 訂用帳戶設定 [**\_ \_ \_ 模式**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) 列舉會定義設定模式。</span><span class="sxs-lookup"><span data-stu-id="998c3-168">The [**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) enumeration defines the configuration modes.</span></span> <span data-ttu-id="998c3-169">只有在設定模式設定為 [自訂] 時，才能指定/dm、/dmi、/hi 和/dmlt 參數。</span><span class="sxs-lookup"><span data-stu-id="998c3-169">The /dm, /dmi, /hi, and /dmlt parameters can only be specified if the configuration mode is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q： *查詢***</span><span class="sxs-lookup"><span data-stu-id="998c3-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-171">值，指定訂閱的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="998c3-171">A value that specifies the query string for the subscription.</span></span> <span data-ttu-id="998c3-172">這個字串的格式可以不同于不同的 URI 值，並套用至訂用帳戶中的所有事件來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-172">The format of this string can be different for different URI values and applies to all event sources in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia： *方言***</span><span class="sxs-lookup"><span data-stu-id="998c3-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-174">值，指定查詢字串使用的方言。</span><span class="sxs-lookup"><span data-stu-id="998c3-174">A value that specifies the dialect the query string uses.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf： *FORMAT***</span><span class="sxs-lookup"><span data-stu-id="998c3-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-176">值，指定傳回之事件的格式。</span><span class="sxs-lookup"><span data-stu-id="998c3-176">A value that specifies the format of the returned events.</span></span> <span data-ttu-id="998c3-177">*格式* 可以是 "Events" 或 "RenderedText"。</span><span class="sxs-lookup"><span data-stu-id="998c3-177">*FORMAT* can be "Events" or "RenderedText".</span></span> <span data-ttu-id="998c3-178">當值為 "RenderedText" 時，會傳回具有當地語系化字串的事件 (例如) 附加至事件的事件描述字串。</span><span class="sxs-lookup"><span data-stu-id="998c3-178">When the value is "RenderedText", the events are returned with the localized strings (such as event description strings) attached to the events.</span></span> <span data-ttu-id="998c3-179">*FORMAT* 的預設值是 "RenderedText"。</span><span class="sxs-lookup"><span data-stu-id="998c3-179">The default value of *FORMAT* is "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="998c3-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l：*地區\* 設定*\*</span><span class="sxs-lookup"><span data-stu-id="998c3-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-181">值，指定用來傳遞轉譯文字格式之當地語系化字串的地區設定。</span><span class="sxs-lookup"><span data-stu-id="998c3-181">A value that specifies the locale for delivery of the localized strings in rendered text format.</span></span> <span data-ttu-id="998c3-182">*地區* 設定是語言/國家（地區）文化特性識別碼，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="998c3-182">*LOCALE* is a language/country culture identifier, for example, "EN-us".</span></span> <span data-ttu-id="998c3-183">只有當/cf 參數設定為 "RenderedText" 時，此參數才有效。</span><span class="sxs-lookup"><span data-stu-id="998c3-183">This parameter is only valid when the /cf parameter is set to "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="998c3-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree： \[ *值*\]**</span><span class="sxs-lookup"><span data-stu-id="998c3-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree:\[*VALUE*\]**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-185">值，指定要傳遞給訂閱的事件。</span><span class="sxs-lookup"><span data-stu-id="998c3-185">A value that specifies which events are to be delivered for the subscription.</span></span> <span data-ttu-id="998c3-186">*值* 可以是 true 或 false。</span><span class="sxs-lookup"><span data-stu-id="998c3-186">*VALUE* can be true or false.</span></span> <span data-ttu-id="998c3-187">*當值* 為 true 時，會從訂用帳戶事件來源讀取所有現有的事件。</span><span class="sxs-lookup"><span data-stu-id="998c3-187">When *VALUE* is true, all existing events are read from the subscription event sources.</span></span> <span data-ttu-id="998c3-188">*當值* 為 false 時，僅會傳遞未來 (抵達) 事件。</span><span class="sxs-lookup"><span data-stu-id="998c3-188">When *VALUE* is false, only future (arriving) events are delivered.</span></span> <span data-ttu-id="998c3-189">如果指定/ree 時沒有值，預設值為 true; 如果未指定/ree，則預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="998c3-189">The default is true when /ree is specified without a value, and the default is false if /ree is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf： *FILENAME***</span><span class="sxs-lookup"><span data-stu-id="998c3-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-191">值，指定用來儲存從事件訂閱接收之事件的本機事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="998c3-191">A value that specifies the local event log that is used to store events received from the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn： *發行者***</span><span class="sxs-lookup"><span data-stu-id="998c3-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-193">值，指定 (提供者) 名稱的事件發行者。</span><span class="sxs-lookup"><span data-stu-id="998c3-193">A value that specifies the event publisher (provider) name.</span></span> <span data-ttu-id="998c3-194">它必須是擁有或匯入/lf 參數所指定之記錄檔的發行者。</span><span class="sxs-lookup"><span data-stu-id="998c3-194">It must be a publisher which owns or imports the log specified by the /lf parameter.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm： *模式***</span><span class="sxs-lookup"><span data-stu-id="998c3-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-196">指定訂閱傳遞模式的值。</span><span class="sxs-lookup"><span data-stu-id="998c3-196">A value that specifies the subscription delivery mode.</span></span> <span data-ttu-id="998c3-197">*模式* 可以是 push 或 pull。</span><span class="sxs-lookup"><span data-stu-id="998c3-197">*MODE* can be either push or pull.</span></span> <span data-ttu-id="998c3-198">只有當/cm 參數設定為 Custom 時，此選項才有效。</span><span class="sxs-lookup"><span data-stu-id="998c3-198">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi： *NUMBER***</span><span class="sxs-lookup"><span data-stu-id="998c3-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-200">值，指定事件訂用帳戶中批次處理傳遞的最大專案數。</span><span class="sxs-lookup"><span data-stu-id="998c3-200">A value that specifies the maximum number of items for batched delivery in the event subscription.</span></span> <span data-ttu-id="998c3-201">只有當/cm 參數設定為 Custom 時，此選項才有效。</span><span class="sxs-lookup"><span data-stu-id="998c3-201">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt： *MS***</span><span class="sxs-lookup"><span data-stu-id="998c3-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-203">值，指定傳遞事件批次所允許的最大延遲。</span><span class="sxs-lookup"><span data-stu-id="998c3-203">A value that specifies the maximum latency allowed in delivering a batch of events.</span></span> <span data-ttu-id="998c3-204">MS 是允許的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="998c3-204">MS is the number of milliseconds allowed.</span></span> <span data-ttu-id="998c3-205">只有當/cm 參數設定為 Custom 時，此參數才有效。</span><span class="sxs-lookup"><span data-stu-id="998c3-205">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi： *MS***</span><span class="sxs-lookup"><span data-stu-id="998c3-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-207">值，指定訂閱的心跳間隔。</span><span class="sxs-lookup"><span data-stu-id="998c3-207">A value that specifies the heartbeat interval for the subscription.</span></span> <span data-ttu-id="998c3-208">*毫秒* 是間隔中使用的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="998c3-208">*MS* is the number of milliseconds used in the interval.</span></span> <span data-ttu-id="998c3-209">只有當/cm 參數設定為 Custom 時，此參數才有效。</span><span class="sxs-lookup"><span data-stu-id="998c3-209">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn： *net-transportname***</span><span class="sxs-lookup"><span data-stu-id="998c3-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-211">值，指定用來連接到遠端事件來源電腦的傳輸名稱。</span><span class="sxs-lookup"><span data-stu-id="998c3-211">A value that specifies the name of the transport used to connect to the remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa： *事件 \_ 來源***</span><span class="sxs-lookup"><span data-stu-id="998c3-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *EVENT\_SOURCE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-213">值，指定事件來源電腦的位址。</span><span class="sxs-lookup"><span data-stu-id="998c3-213">A value that specifies the address of an event source computer.</span></span> <span data-ttu-id="998c3-214">*活動 \_來源* 是一種字串，可使用電腦的完整功能變數名稱、NetBIOS 名稱或 IP 位址來識別事件來源電腦。</span><span class="sxs-lookup"><span data-stu-id="998c3-214">*EVENT\_SOURCE* is a string that identifies an event source computer using the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span> <span data-ttu-id="998c3-215">這個參數可以與/ese、/aes、/res 或/un 和/up 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="998c3-215">This parameter can be used with the /ese, /aes, /res, or /un and /up parameters.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese： *值***</span><span class="sxs-lookup"><span data-stu-id="998c3-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-217">判斷是否要啟用或停用事件來源的值。</span><span class="sxs-lookup"><span data-stu-id="998c3-217">A value that determines whether to enable or disable an event source.</span></span> <span data-ttu-id="998c3-218">*值* 可以是 true 或 false。</span><span class="sxs-lookup"><span data-stu-id="998c3-218">*VALUE* can be true or false.</span></span> <span data-ttu-id="998c3-219">預設值為 true，這會啟用事件來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-219">The default value is true, which enables the event source.</span></span> <span data-ttu-id="998c3-220">只有在使用/esa 參數時，才會使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="998c3-220">This parameter is only used if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span><span class="sxs-lookup"><span data-stu-id="998c3-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-222">值，如果事件來源還不是事件訂閱的一部分，此值會加入/esa 參數所指定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-222">A value that adds the event source specified by the /esa parameter if the event source is not already part of the event subscription.</span></span> <span data-ttu-id="998c3-223">如果/esa 參數指定的電腦已經是訂用帳戶的一部分，則會顯示錯誤。</span><span class="sxs-lookup"><span data-stu-id="998c3-223">If the computer specified by the /esa parameter is already a part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="998c3-224">只有在使用/esa 參數時，才允許這個參數。</span><span class="sxs-lookup"><span data-stu-id="998c3-224">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-225"><span id="_res"></span><span id="_RES"></span>**/res**</span><span class="sxs-lookup"><span data-stu-id="998c3-225"><span id="_res"></span><span id="_RES"></span>**/res**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-226">如果事件來源已經是事件訂閱的一部分，則為移除/esa 參數所指定之事件來源的值。</span><span class="sxs-lookup"><span data-stu-id="998c3-226">A value that removes the event source specified by the /esa parameter if the event source is already part of the event subscription.</span></span> <span data-ttu-id="998c3-227">如果/esa 參數所指定的電腦不是訂用帳戶的一部分，則會顯示錯誤。</span><span class="sxs-lookup"><span data-stu-id="998c3-227">If the computer specified by the /esa parameter is not part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="998c3-228">只有在使用/esa 參數時，才允許這個參數。</span><span class="sxs-lookup"><span data-stu-id="998c3-228">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un： *USERNAME***</span><span class="sxs-lookup"><span data-stu-id="998c3-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-230">值，指定認證中所使用的使用者名稱，以連接到/esa 參數中指定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-230">A value that specifies the user name used in the credentials to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="998c3-231">只有在使用/esa 參數時，才允許這個參數。</span><span class="sxs-lookup"><span data-stu-id="998c3-231">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up： *密碼***</span><span class="sxs-lookup"><span data-stu-id="998c3-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-233">值，指定在/un 參數中指定之使用者名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="998c3-233">A value that specifies the password for the user name specified in the /un parameter.</span></span> <span data-ttu-id="998c3-234">使用者名稱和密碼認證是用來連接到/esa 參數中指定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-234">The user name and password credentials are used to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="998c3-235">只有在使用/un 參數時，才允許這個參數。</span><span class="sxs-lookup"><span data-stu-id="998c3-235">This parameter is allowed only if the /un parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp： *TRANSPORTPORT***</span><span class="sxs-lookup"><span data-stu-id="998c3-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-237">值，指定連接到遠端事件來源電腦時，傳輸所使用的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="998c3-237">A value that specifies the port number used by the transport when connecting to a remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn： *NAME***</span><span class="sxs-lookup"><span data-stu-id="998c3-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-239">值，指定本機電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="998c3-239">A value that specifies the DNS name of the local computer.</span></span> <span data-ttu-id="998c3-240">遠端事件來源會使用這個名稱來推送事件，而且必須只用于發送訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-240">This name is used by remote event sources to push back events and must be used for push subscriptions only.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct： *類型***</span><span class="sxs-lookup"><span data-stu-id="998c3-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-242">值，指定用來存取遠端事件來源的認證類型。</span><span class="sxs-lookup"><span data-stu-id="998c3-242">A value that specifies the credential type used for accessing remote event sources.</span></span> <span data-ttu-id="998c3-243">*類型* 可以是 "default"、"negotiate"、"digest"、"basic" 或 "localmachine"。</span><span class="sxs-lookup"><span data-stu-id="998c3-243">*TYPE* can be "default", "negotiate", "digest", "basic", or "localmachine".</span></span> <span data-ttu-id="998c3-244">預設值為 "default"。</span><span class="sxs-lookup"><span data-stu-id="998c3-244">The default is "default".</span></span> <span data-ttu-id="998c3-245">這些值定義于 [**EC \_ 訂閱 \_ 認證 \_ 類型**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="998c3-245">These values are defined in the [**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun： *USERNAME***</span><span class="sxs-lookup"><span data-stu-id="998c3-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-247">值，這個值會設定共用使用者認證，而這些認證用於沒有自己的使用者認證的事件來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-247">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span>

> [!Note]  
> <span data-ttu-id="998c3-248">如果這個參數與/c 選項搭配使用，則會忽略設定檔案中個別事件來源的使用者名稱和密碼設定。</span><span class="sxs-lookup"><span data-stu-id="998c3-248">If this parameter is used with the /c option, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="998c3-249">如果您想要針對特定事件來源使用不同的認證，您可以在另一個 set 訂用帳戶命令的命令列上，指定特定事件來源的/un 和/up 參數，以覆寫此值。</span><span class="sxs-lookup"><span data-stu-id="998c3-249">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="998c3-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup： *密碼***</span><span class="sxs-lookup"><span data-stu-id="998c3-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-251">值，設定共用使用者認證的使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="998c3-251">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="998c3-252">當 *密碼* 設定為 \* (星號) 時，會從主控台讀取密碼。</span><span class="sxs-lookup"><span data-stu-id="998c3-252">When *PASSWORD* is set to \* (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="998c3-253">只有在指定/cun 參數時，這個選項才有效。</span><span class="sxs-lookup"><span data-stu-id="998c3-253">This option is only valid when the /cun parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica： *指紋***</span><span class="sxs-lookup"><span data-stu-id="998c3-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *THUMBPRINTS***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-255">此值會以逗號分隔的清單，設定簽發者憑證 thumb 的清單。</span><span class="sxs-lookup"><span data-stu-id="998c3-255">A value that sets the list of issuer certificate thumb prints, in a comma-separated list.</span></span>

> [!Note]  
> <span data-ttu-id="998c3-256">此選項只適用于來源起始的訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-256">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="998c3-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as： *允許***</span><span class="sxs-lookup"><span data-stu-id="998c3-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ALLOWED***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-258">值，這個值會設定以逗號分隔的字串清單，指定允許起始訂用帳戶之非網域電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="998c3-258">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are allowed to initiate subscriptions.</span></span> <span data-ttu-id="998c3-259">您可以使用萬用字元（例如 ". mydomain.com"）來指定名稱 \* 。</span><span class="sxs-lookup"><span data-stu-id="998c3-259">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="998c3-260">根據預設，此清單是空的。</span><span class="sxs-lookup"><span data-stu-id="998c3-260">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="998c3-261">此選項只適用于來源起始的訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-261">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="998c3-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds： *拒絕***</span><span class="sxs-lookup"><span data-stu-id="998c3-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-263">值，這個值會設定以逗號分隔的字串清單，指定不允許起始訂閱之非網域電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="998c3-263">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are not allowed to initiate subscriptions.</span></span> <span data-ttu-id="998c3-264">您可以使用萬用字元（例如 ". mydomain.com"）來指定名稱 \* 。</span><span class="sxs-lookup"><span data-stu-id="998c3-264">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="998c3-265">根據預設，此清單是空的。</span><span class="sxs-lookup"><span data-stu-id="998c3-265">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="998c3-266">此選項只適用于來源起始的訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-266">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="998c3-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc： *SDDL***</span><span class="sxs-lookup"><span data-stu-id="998c3-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-268">值，以 SDDL 格式設定字串，指定允許或不允許哪些網域電腦起始訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-268">A value that sets a string, in SDDL format, that specifies which domain computers are allowed or not allowed to initiate subscriptions.</span></span> <span data-ttu-id="998c3-269">預設為允許所有網域電腦起始訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-269">The default is to allow all domain computers to initiate subscriptions.</span></span>

> [!Note]  
> <span data-ttu-id="998c3-270">此選項只適用于來源起始的訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-270">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> </dl>

## <a name="create-a-new-subscription"></a><span data-ttu-id="998c3-271">建立新的訂閱</span><span class="sxs-lookup"><span data-stu-id="998c3-271">Create a New Subscription</span></span>

<span data-ttu-id="998c3-272">下列語法用來為遠端電腦上的事件建立事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-272">The following syntax is used to create an event subscription for events on a remote computer.</span></span>

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a><span data-ttu-id="998c3-273">備註</span><span class="sxs-lookup"><span data-stu-id="998c3-273">Remarks</span></span>

<span data-ttu-id="998c3-274">當 **>wecutil cs** 命令中指定了不正確的使用者名稱或密碼時，除非您使用 **>wecutil gr** 命令來查看訂用帳戶的執行時間狀態，否則不會報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="998c3-274">When an incorrect username or password is specified in the **wecutil cs** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="creation-parameters"></a><span data-ttu-id="998c3-275">建立參數</span><span class="sxs-lookup"><span data-stu-id="998c3-275">Creation Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998c3-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**配置 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="998c3-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**CONFIGURATION\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-277">值，指定包含訂閱設定資訊之 XML 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="998c3-277">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="998c3-278">路徑可以是目前目錄的絕對路徑或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="998c3-278">The path can be absolute or relative to the current directory.</span></span>

<span data-ttu-id="998c3-279">下列 XML 是訂用帳戶設定檔的範例，此檔案會建立收集器起始的訂用帳戶，以將遠端電腦的應用程式事件記錄檔中的事件轉送至 ForwardedEvents 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="998c3-279">The following XML is an example of a subscription configuration file that creates a collector initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


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



<span data-ttu-id="998c3-280">下列 XML 是訂用帳戶設定檔的範例，它會建立來源起始的訂用帳戶，以將遠端電腦的應用程式事件記錄檔中的事件轉送至 ForwardedEvents 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="998c3-280">The following XML is an example of a subscription configuration file that creates a source initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


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
> <span data-ttu-id="998c3-281">建立來源起始的訂閱時，如果 **AllowedSourceDomainComputers**、 **AllowedSourceNonDomainComputers** / **IssuerCAList**、 **AllowedSubjectList** 和 **DeniedSubjectList** 都是空的，則會提供 **AllowedSourceDomainComputers** 的預設值： O:NSG： NSD： (a;;GA;;;DC)  (A;;GA;;;NS) 」。</span><span class="sxs-lookup"><span data-stu-id="998c3-281">When creating a source initiated subscription, if **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers**/**IssuerCAList**, **AllowedSubjectList**, and **DeniedSubjectList** are all empty, then a default will be provided for **AllowedSourceDomainComputers** - "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)".</span></span> <span data-ttu-id="998c3-282">此 SDDL 預設會授與網域電腦網域群組的成員，以及本機轉寄站) 的局域網路服務群組 (，這是為此訂用帳戶引發事件的能力。</span><span class="sxs-lookup"><span data-stu-id="998c3-282">This SDDL default grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="998c3-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun： *USERNAME***</span><span class="sxs-lookup"><span data-stu-id="998c3-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-284">值，這個值會設定共用使用者認證，而這些認證用於沒有自己的使用者認證的事件來源。</span><span class="sxs-lookup"><span data-stu-id="998c3-284">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span> <span data-ttu-id="998c3-285">此值僅適用于收集器起始的訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-285">This value applies to collector initiated subscriptions only.</span></span>

> [!Note]  
> <span data-ttu-id="998c3-286">如果指定這個參數，則會忽略設定檔案中個別事件來源的使用者名稱和密碼設定。</span><span class="sxs-lookup"><span data-stu-id="998c3-286">If this parameter is specified, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="998c3-287">如果您想要針對特定事件來源使用不同的認證，您可以在另一個 set 訂用帳戶命令的命令列上，指定特定事件來源的/un 和/up 參數，以覆寫此值。</span><span class="sxs-lookup"><span data-stu-id="998c3-287">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="998c3-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup： *密碼***</span><span class="sxs-lookup"><span data-stu-id="998c3-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-289">值，設定共用使用者認證的使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="998c3-289">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="998c3-290">當 *密碼* 設定為 " \* " (星號) ，則會從主控台讀取密碼。</span><span class="sxs-lookup"><span data-stu-id="998c3-290">When *PASSWORD* is set to "\*" (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="998c3-291">只有在指定/cun 參數時，這個選項才有效。</span><span class="sxs-lookup"><span data-stu-id="998c3-291">This option is only valid when the /cun parameter is specified.</span></span>

</dd> </dl>

## <a name="delete-a-subscription"></a><span data-ttu-id="998c3-292">刪除訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="998c3-292">Delete a Subscription</span></span>

<span data-ttu-id="998c3-293">下列語法用來刪除事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-293">The following syntax is used to delete an event subscription.</span></span>

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a><span data-ttu-id="998c3-294">刪除參數</span><span class="sxs-lookup"><span data-stu-id="998c3-294">Deletion Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998c3-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="998c3-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-296">可唯一識別訂閱的字串。</span><span class="sxs-lookup"><span data-stu-id="998c3-296">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="998c3-297">此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="998c3-297">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="998c3-298">將會刪除此參數中識別的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="998c3-298">The subscription identified in this parameter will be deleted.</span></span>

</dd> </dl>

## <a name="retry-a-subscription"></a><span data-ttu-id="998c3-299">重試訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="998c3-299">Retry a subscription</span></span>

<span data-ttu-id="998c3-300">下列語法用來重試非使用中的訂閱，方法是藉由建立每個事件來源的連接，並將遠端訂閱要求傳送至事件來源，藉以重試非使用中的訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-300">The following syntax is used to retry an inactive subscription by attempting to reactivate all or specified event sources by establishing a connection to each event source and sending a remote subscription request to the event source.</span></span> <span data-ttu-id="998c3-301">停用的事件來源不會重試。</span><span class="sxs-lookup"><span data-stu-id="998c3-301">Disabled event sources are not retried.</span></span>

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a><span data-ttu-id="998c3-302">重試參數</span><span class="sxs-lookup"><span data-stu-id="998c3-302">Retry Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998c3-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**訂用帳戶 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="998c3-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-304">可唯一識別訂閱的字串。</span><span class="sxs-lookup"><span data-stu-id="998c3-304">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="998c3-305">此識別碼是在用來建立訂用帳戶的 XML 設定檔中的 **SubscriptionId** 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="998c3-305">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="998c3-306">將會重試此參數中識別的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="998c3-306">The subscription identified in this parameter will be retried.</span></span>

</dd> <dt>

<span data-ttu-id="998c3-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**事件 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="998c3-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="998c3-308">值，這個值會識別屬於事件訂閱之事件來源的電腦。</span><span class="sxs-lookup"><span data-stu-id="998c3-308">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="998c3-309">此值可以是電腦的完整功能變數名稱、NetBIOS 名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="998c3-309">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a><span data-ttu-id="998c3-310">設定 Windows 事件收集器服務</span><span class="sxs-lookup"><span data-stu-id="998c3-310">Configure the Windows Event Collector Service</span></span>

<span data-ttu-id="998c3-311">下列語法是用來設定 Windows 事件收集器服務，以確保可以在電腦重新開機時建立和持續事件訂閱。</span><span class="sxs-lookup"><span data-stu-id="998c3-311">The following syntax is used to configure the Windows Event Collector service to ensure event subscriptions can be created and sustained through computer restarts.</span></span> <span data-ttu-id="998c3-312">這包括下列程式：</span><span class="sxs-lookup"><span data-stu-id="998c3-312">This includes the following procedure:</span></span>

<span data-ttu-id="998c3-313">**設定 Windows 事件收集器服務**</span><span class="sxs-lookup"><span data-stu-id="998c3-313">**To configure the Windows Event Collector service**</span></span>

1.  <span data-ttu-id="998c3-314">如果已停用，請啟用 ForwardedEvents 通道。</span><span class="sxs-lookup"><span data-stu-id="998c3-314">Enable the ForwardedEvents channel if it is disabled.</span></span>
2.  <span data-ttu-id="998c3-315">延遲 Windows 事件收集器服務的啟動。</span><span class="sxs-lookup"><span data-stu-id="998c3-315">Delay the start of the Windows Event Collector service.</span></span>
3.  <span data-ttu-id="998c3-316">如果 Windows 事件收集器服務未執行，請加以啟動。</span><span class="sxs-lookup"><span data-stu-id="998c3-316">Start the Windows Event Collector service if it is not running.</span></span>

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a><span data-ttu-id="998c3-317">設定事件收集器參數</span><span class="sxs-lookup"><span data-stu-id="998c3-317">Configure Event Collector Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998c3-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q： *值***</span><span class="sxs-lookup"><span data-stu-id="998c3-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="998c3-319">值，這個值會決定快速設定命令是否會提示確認。</span><span class="sxs-lookup"><span data-stu-id="998c3-319">A value that determines whether the quick-config command will prompt for confirmation.</span></span> <span data-ttu-id="998c3-320">值可以是 true 或 false。</span><span class="sxs-lookup"><span data-stu-id="998c3-320">VALUE can be true or false.</span></span> <span data-ttu-id="998c3-321">如果值為 true，則命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="998c3-321">If VALUE is true, then the command will prompt for confirmation.</span></span> <span data-ttu-id="998c3-322">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="998c3-322">The default value is false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="998c3-323">規格需求</span><span class="sxs-lookup"><span data-stu-id="998c3-323">Requirements</span></span>



| <span data-ttu-id="998c3-324">需求</span><span class="sxs-lookup"><span data-stu-id="998c3-324">Requirement</span></span> | <span data-ttu-id="998c3-325">值</span><span class="sxs-lookup"><span data-stu-id="998c3-325">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="998c3-326">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="998c3-326">Minimum supported client</span></span><br/> | <span data-ttu-id="998c3-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="998c3-327">Windows Vista</span></span><br/>       |
| <span data-ttu-id="998c3-328">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="998c3-328">Minimum supported server</span></span><br/> | <span data-ttu-id="998c3-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="998c3-329">Windows Server 2008</span></span><br/> |



 

 





