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
ms.openlocfilehash: ebbfbc1061d8bca03f52dd8cb7583fbe23ebb33a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885243"
---
# <a name="scripting-api-constants"></a>腳本 API 常數

WMI 會在 [wmi 的腳本 API](scripting-api-for-wmi.md)中，于方法呼叫的 *iflags* 參數中使用數種類型的常數。

Visual Basic 應用程式可包含腳本 API 的類型程式庫 >wbemdisp.tlb .tlb。 腳本無法存取類型程式庫中的常數，除非使用 &lt; &gt; &lt; &gt; [WMI 腳本類型程式庫](using-the-wmi-scripting-type-library.md)中所述的 Windows 腳本主機 (WSH) XML 檔案格式的參考或物件標記。 否則，腳本必須使用常數的值。

## <a name="constants"></a>常數

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

定義安全性驗證等級。

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

定義如何執行對類別或實例的寫入操作。

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

定義屬性值的有效 CIM 類型。

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

定義物件比較的設定，並由 [**SWbemObject. CompareTo \_**](swbemobject-compareto-.md)使用。

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

定義安全性旗標，當遠端電腦上的 WMI 連線失敗時，此旗標會用來做為呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 方法的參數。

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

定義 [腳本 API 針對 WMI](scripting-api-for-wmi.md) 呼叫可能傳回的錯誤。

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

定義 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)、 [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)、 [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)和 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)所使用的常數。

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

定義安全性模擬等級。 這些常數會與 [**SWbemSecurity**](swbemsecurity.md)搭配使用。

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

定義 [**SWbemObjectEx GetText \_**](swbemobjectex-gettext-.md)所要使用的有效物件文字格式。

</dd> <dt>

<span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dd>

定義許可權。 這些常數會與 [**SWbemSecurity**](swbemsecurity.md) 搭配使用，以授與某些作業所需的許可權。

</dd> <dt>

<span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)
</dt> <dd>

定義列舉或查詢的深度，以決定呼叫所傳回的物件數目。

</dd> <dt>

<span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)
</dt> <dd>

定義產生之物件文字的內容，並由 [**SWbemObject. GetObjectText \_**](swbemobject-getobjecttext-.md)使用。

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

定義超時常數。 [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md)會使用這個常數。

</dd> </dl>

## <a name="combining-flags"></a>組合旗標

您可以結合旗標來影響 API 呼叫的多個層面。

例如，若要建立 [*半同步*](gloss-s.md)呼叫， [**SWbemServices.Exe\_ CQuery**](swbemservices-execquery.md)呼叫中的 *iFlags* 參數必須包含兩個旗標： **WbemFlagReturnImmediately** 和 **WbemFlagForwardOnly**。 **WbemFlagReturnImmediately** 的值為16，而 **WbemFlagForwardOnly** 的值為32。 因為無法依名稱存取常數，所以會合並這些旗標的值，產生48的 *iFlags* 值。

下列腳本範例顯示呼叫。


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



並非所有旗標都可以合併，因為許多都互斥，而且可能會產生無法預期的結果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)
</dt> </dl>

 

 



