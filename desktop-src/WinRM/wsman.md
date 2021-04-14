---
title: 'WSMan 物件 (WSManDisp .h) '
description: 提供用來建立會話的方法和屬性，以會話物件表示。
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- WSMan 物件 Windows 遠端管理
- WSMan 物件 Windows 遠端管理，說明
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384002"
---
# <a name="wsman-object"></a>WSMan 物件

提供用來建立會話的方法和屬性，以 [**會話**](session.md) 物件表示。 任何 Windows 遠端管理作業都需要建立連接至遠端電腦、[*基礎管理控制器*](windows-remote-management-glossary.md) (BMC) 或本機電腦的 [**會話**](session.md)。 作業包括取得、寫入、列舉資料或叫用方法。

## <a name="members"></a>成員

**WSMan** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**WSMan** 物件有這些方法。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">方法</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></td>
<td style="text-align: left;">建立 <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> 物件，這個物件會指定建立遠端會話時使用的使用者名稱和密碼。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></td>
<td style="text-align: left;">建立可指定的 <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> 物件：<br/>
<ul>
<li><a href="windows-remote-management-glossary.md"><em>資源</em></a>的完整路徑或單一資料片段。</li>
<li>特定資源實例的 <a href="windows-remote-management-glossary.md"><em>選取器</em></a> 。</li>
<li>提供其他資料給資源提供者的 <a href="windows-remote-management-glossary.md"><em>選項</em></a> 。</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></td>
<td style="text-align: left;">建立可用於後續網路作業的 <a href="session.md"><strong>會話</strong></a> 物件。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></td>
<td style="text-align: left;">傳回列舉旗標<strong>EnumerationFlagHierarchyDeep</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></td>
<td style="text-align: left;">傳回列舉旗標<strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></td>
<td style="text-align: left;">傳回列舉旗標<strong>EnumerationFlagHierarchyShallow</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></td>
<td style="text-align: left;">傳回列舉常數 <strong>WSManFlagNonXmlText</strong> 的值，以用於 Session 的 <em>Flags</em> 參數。 <a href="session-enumerate.md"><strong>列舉</strong></a> 方法。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></td>
<td style="text-align: left;">傳回列舉旗標<strong>EnumerationFlagReturnEPR</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></td>
<td style="text-align: left;">傳回列舉旗標<strong>EnumerationFlagReturnObject</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></td>
<td style="text-align: left;">傳回列舉旗標<strong>EnumerationFlagReturnObjectAndEPR</strong>的值，以用於<a href="session-enumerate.md"><strong>Session</strong></a>的<em>flags</em>參數。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></td>
<td style="text-align: left;">傳回格式化的字串，其中包含錯誤號碼的文字。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagCredUsernamePassword</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagEnableSPNServerPort</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagNoEncryption</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></td>
<td style="text-align: left;">傳回<strong>WSManFlagSkipCACheck</strong> authentication 旗標的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagSkipCNCheck</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagUseBasic</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagUseDigest</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagUseKerberos</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagUseNegotiate</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagUseNoAuthentication</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></td>
<td style="text-align: left;">傳回驗證旗標<strong>WSManFlagUTF8</strong>的值，以便在<a href="wsman-createsession.md"><strong>CreateSession</strong></a>的<em>flags</em>參數中使用。<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>屬性

**WSMan** 物件具有這些屬性。



| 屬性                                            | 存取類型          | Description                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**CommandLine**](wsman-commandline.md)<br/> | 唯讀<br/> | 取得目前裝載進程未處理的命令列。<br/> |
| [**錯誤**](wsman-error.md)<br/>             | 唯讀<br/> | 取得錯誤資訊。<br/>                                            |



 

## <a name="remarks"></a>備註

**WSMan** 物件會對應至 [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)和 [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)介面。 **WSMan** 是唯一可以使用 [CreateObject](/previous-versions//xzysf6hc(v=vs.85))直接建立的物件。

## <a name="examples"></a>範例

下列程式碼範例示範如何將 **WSMan** 物件具現化。


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WinRM 腳本 API](winrm-scripting-api.md)
</dt> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)
</dt> <dt>

[從本機電腦取得資料](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[從遠端電腦取得資料](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

