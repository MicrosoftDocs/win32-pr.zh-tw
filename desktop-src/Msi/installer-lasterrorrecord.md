---
description: 安裝程式物件的 LastErrorRecord 方法會傳回記錄物件，其中包含產生錯誤記錄之函式的最新錯誤的錯誤參數。
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: LastErrorRecord 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bb9dad1962cace623a4a52991d3650451a0a6d5f660aad88e46c4fe393ce4e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142107"
---
# <a name="installerlasterrorrecord-method"></a>LastErrorRecord 方法

[**安裝程式**](installer-object.md)物件的 **LastErrorRecord** 方法會傳回 [**記錄**](record-object.md)物件，其中包含產生錯誤記錄之函式的最新錯誤的錯誤參數。

## <a name="syntax"></a>語法


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在任何產生錯誤記錄的函式執行此函數之後，會重設 [**記錄**](record-object.md) 物件。

只有下列指定的函式會產生錯誤記錄：

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [**認可**](database-commit.md)
-   [**OpenView**](database-openview.md)
-   [**匯入**](database-import.md)
-   [**匯出**](database-export.md)
-   [**合併**](database-merge.md)
-   [**基表**](database-generatetransform.md)
-   [**ApplyTransform**](database-applytransform.md)
-   [**執行**](view-execute.md)
-   [**Modify**](view-modify.md)
-   [**SetStream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**SourcePath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**ComponentCurrentState**](session-componentcurrentstate.md)
-   [**ComponentRequestState**](session-componentrequeststate.md)
-   [**FeatureCurrentState**](session-featurecurrentstate.md)
-   [**FeatureRequestState**](session-featurerequeststate.md)
-   [**FeatureCost**](session-featurecost.md)
-   [**FeatureValidStates**](session-featurevalidstates.md)
-   [**SetInstallLevel**](session-setinstalllevel.md)

VBScript 中的下列範例會使用 [**OpenDatabase**](installer-opendatabase.md) 的呼叫，以示範如何從支援 **LastErrorRecord** 方法的其中一個方法或屬性取得擴充的錯誤資訊。 當 **OpenDatabase** 方法失敗時，此範例會建立錯誤訊息。 **Err** 物件是用來判斷是否發生錯誤。


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




