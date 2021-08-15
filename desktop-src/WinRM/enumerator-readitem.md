---
title: 'ReadItem 方法 (WSManDisp .h) '
description: 從資源抓取專案，並傳回專案的 XML 表示。
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- ReadItem 方法 Windows 遠端管理
- ReadItem 方法 Windows 遠端管理，列舉值物件
- 列舉值物件 Windows 遠端管理，ReadItem 方法
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a24109d22c4fc114513c2113af48c62a7042cd90feb075718e57323ecf5238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993808"
---
# <a name="enumeratorreaditem-method"></a>ReadItem 方法

從資源抓取專案，並傳回專案的 XML 表示。

## <a name="syntax"></a>語法


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*資源* 
</dt> <dd>

專案的 URI。

</dd> </dl>

## <a name="return-value"></a>傳回值

專案的 XML 表示。

## <a name="remarks"></a>備註

若要限制讀取的專案數目，請設定 [**Session.BatchItems**](session-batchitems.md) ] 屬性。

請注意，釋出列舉物件會清除任何暫止的列舉要求。

[**Session**](session-enumerate.md)方法未取得集合的方式，與 [WMI 查詢](/windows/desktop/WmiSdk/querying-wmi)相同，例如，會傳回 `SELECT * from Win32_LogicalDisk` [**swbemobjectset 搭配使用**](/windows/desktop/WmiSdk/swbemobjectset)中的集合。 若要將檔案讀取為文字資料流程，您必須建立腳本 [TextStream](/previous-versions//312a5kbt(v=vs.85)) 物件，並呼叫 [TextStream](/previous-versions//h7se9d4f(v=vs.85)) 方法來讀取檔案的每一行。 以類似的方式，您可以呼叫 **Session。列舉** 方法以取得 [**列舉**](enumerator.md) 值物件，然後呼叫 **ReadItem** 方法。 如同從文字檔讀取一般，您可以檢查 [**AtEndOfStream**](enumerator-atendofstream.md) 屬性來檢查是否已到達資料項目的結尾。

## <a name="examples"></a>範例

下列 VBScript 範例會呼叫 [**Session。列舉**](session-enumerate.md) 方法可取得排程工作的清單。 DisplayOutput 副程式使用 Winrm 命令列工具 XML 轉換檔 (WsmTxt. xsl) 以表格格式輸出資料。


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉值**](enumerator.md)
</dt> <dt>

[列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

