---
description: 適用于 WMI 的腳本 API 包含旗標、通用值和錯誤碼。
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: 腳本 API 常數
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997112"
---
# <a name="scripting-api-constants"></a><span data-ttu-id="cb20b-103">腳本 API 常數</span><span class="sxs-lookup"><span data-stu-id="cb20b-103">Scripting API Constants</span></span>

<span data-ttu-id="cb20b-104">WMI 會在 [wmi 的腳本 API](scripting-api-for-wmi.md)中，于方法呼叫的 *iflags* 參數中使用數種類型的常數。</span><span class="sxs-lookup"><span data-stu-id="cb20b-104">WMI uses several types of constants in the *iflags* parameter of method calls in the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="cb20b-105">Visual Basic 應用程式可包含腳本 API 的類型程式庫 >wbemdisp.tlb .tlb。</span><span class="sxs-lookup"><span data-stu-id="cb20b-105">Visual Basic applications can include the type library for the scripting API, Wbemdisp.tlb.</span></span> <span data-ttu-id="cb20b-106">腳本無法存取類型程式庫中的常數，除非它們使用 <REFERENCE> <OBJECT> Windows Script Host 中的或標記 (WSH) XML 檔案格式，如 [使用 WMI 腳本類型程式庫](using-the-wmi-scripting-type-library.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="cb20b-106">Scripts are unable to access constants in the type library unless they use the <REFERENCE> or <OBJECT> tags from the Windows Script Host (WSH) XML file format as described in [Using the WMI Scripting Type Library](using-the-wmi-scripting-type-library.md).</span></span> <span data-ttu-id="cb20b-107">否則，腳本必須使用常數的值。</span><span class="sxs-lookup"><span data-stu-id="cb20b-107">Otherwise, a script must use the value of the constant.</span></span>

## <a name="constants"></a><span data-ttu-id="cb20b-108">常數</span><span class="sxs-lookup"><span data-stu-id="cb20b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cb20b-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-110">定義安全性驗證等級。</span><span class="sxs-lookup"><span data-stu-id="cb20b-110">Define the security authentication levels.</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-112">定義如何執行對類別或實例的寫入操作。</span><span class="sxs-lookup"><span data-stu-id="cb20b-112">Define how a write operation to a class or an instance is carried out.</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-114">定義屬性值的有效 CIM 類型。</span><span class="sxs-lookup"><span data-stu-id="cb20b-114">Define the valid CIM types of a property value.</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-116">定義物件比較的設定，並由 [**SWbemObject. CompareTo \_**](swbemobject-compareto-.md)使用。</span><span class="sxs-lookup"><span data-stu-id="cb20b-116">Define the settings for object comparison and are used by [**SWbemObject.CompareTo\_**](swbemobject-compareto-.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-118">定義安全性旗標，當遠端電腦上的 WMI 連線失敗時，此旗標會用來做為呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 方法的參數。</span><span class="sxs-lookup"><span data-stu-id="cb20b-118">Defines a security flag that is used as a parameter in calls to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method when a connection to WMI on a remote machine is failing.</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-120">定義 [腳本 API 針對 WMI](scripting-api-for-wmi.md) 呼叫可能傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb20b-120">Define the errors that may be returned by [Scripting API for WMI](scripting-api-for-wmi.md) calls.</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-122">定義 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)、 [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)、 [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)和 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="cb20b-122">Defines constants that are used by [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md), and [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-124">定義安全性模擬等級。</span><span class="sxs-lookup"><span data-stu-id="cb20b-124">Define the security impersonation levels.</span></span> <span data-ttu-id="cb20b-125">這些常數會與 [**SWbemSecurity**](swbemsecurity.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="cb20b-125">These constants are used with [**SWbemSecurity**](swbemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-127">定義 [**SWbemObjectEx GetText \_**](swbemobjectex-gettext-.md)所要使用的有效物件文字格式。</span><span class="sxs-lookup"><span data-stu-id="cb20b-127">Define the valid object text formats to be used by [**SWbemObjectEx.GetText\_**](swbemobjectex-gettext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-129">定義許可權。</span><span class="sxs-lookup"><span data-stu-id="cb20b-129">Define privileges.</span></span> <span data-ttu-id="cb20b-130">這些常數會與 [**SWbemSecurity**](swbemsecurity.md) 搭配使用，以授與某些作業所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="cb20b-130">These constants are used with [**SWbemSecurity**](swbemsecurity.md) to grant the privileges required for some operations.</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-132">定義列舉或查詢的深度，以決定呼叫所傳回的物件數目。</span><span class="sxs-lookup"><span data-stu-id="cb20b-132">Define the depth of enumeration or query, which determines how many objects are returned by a call.</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span><span class="sxs-lookup"><span data-stu-id="cb20b-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-134">定義產生之物件文字的內容，並由 [**SWbemObject. GetObjectText \_**](swbemobject-getobjecttext-.md)使用。</span><span class="sxs-lookup"><span data-stu-id="cb20b-134">Defines the content of generated object text and is used by [**SWbemObject.GetObjectText\_**](swbemobject-getobjecttext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb20b-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span><span class="sxs-lookup"><span data-stu-id="cb20b-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span></span>
</dt> <dd>

<span data-ttu-id="cb20b-136">定義超時常數。</span><span class="sxs-lookup"><span data-stu-id="cb20b-136">Defines the time-out constants.</span></span> <span data-ttu-id="cb20b-137">[**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md)會使用這個常數。</span><span class="sxs-lookup"><span data-stu-id="cb20b-137">This constant is used by [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md).</span></span>

</dd> </dl>

## <a name="combining-flags"></a><span data-ttu-id="cb20b-138">組合旗標</span><span class="sxs-lookup"><span data-stu-id="cb20b-138">Combining Flags</span></span>

<span data-ttu-id="cb20b-139">您可以結合旗標來影響 API 呼叫的多個層面。</span><span class="sxs-lookup"><span data-stu-id="cb20b-139">You can combine flags to affect more than one aspect of the API call.</span></span>

<span data-ttu-id="cb20b-140">例如，若要建立 [*半同步*](gloss-s.md)呼叫， [**SWbemServices.Exe\_ CQuery**](swbemservices-execquery.md)呼叫中的 *iFlags* 參數必須包含兩個旗標： **WbemFlagReturnImmediately** 和 **WbemFlagForwardOnly**。</span><span class="sxs-lookup"><span data-stu-id="cb20b-140">For example, to create a [*semisynchronous*](gloss-s.md) call, the *iFlags* parameter in an [**SWbemServices.ExecQuery\_**](swbemservices-execquery.md) call must contain two flags: **WbemFlagReturnImmediately** and **WbemFlagForwardOnly**.</span></span> <span data-ttu-id="cb20b-141">**WbemFlagReturnImmediately** 的值為16，而 **WbemFlagForwardOnly** 的值為32。</span><span class="sxs-lookup"><span data-stu-id="cb20b-141">The value of **WbemFlagReturnImmediately** is 16 and the value of **WbemFlagForwardOnly** is 32.</span></span> <span data-ttu-id="cb20b-142">因為無法依名稱存取常數，所以會合並這些旗標的值，產生48的 *iFlags* 值。</span><span class="sxs-lookup"><span data-stu-id="cb20b-142">Because the constants cannot be accessed by name, the values of these flags are combined, producing an *iFlags* value of 48.</span></span>

<span data-ttu-id="cb20b-143">下列腳本範例顯示呼叫。</span><span class="sxs-lookup"><span data-stu-id="cb20b-143">The following script example shows the call.</span></span>


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



<span data-ttu-id="cb20b-144">並非所有旗標都可以合併，因為許多都互斥，而且可能會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="cb20b-144">Not all flags can be combined since many are mutually exclusive and may produce unpredictable results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb20b-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb20b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb20b-146">適用于 WMI 的腳本 API</span><span class="sxs-lookup"><span data-stu-id="cb20b-146">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 



