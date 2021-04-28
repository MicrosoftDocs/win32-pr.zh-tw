---
description: ShellExecute 方法-在指定的檔案上執行指定的作業。
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Shell.ShellExecute 方法 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0fd31f0859fff5a1c94d5586f287e4a8980ddc02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104126"
---
# <a name="shellshellexecute-method"></a>ShellExecute 方法

在指定的檔案上執行指定的作業。

## <a name="syntax"></a>Syntax

Jscript：

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

VBScript

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

VB：

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a>參數

<dl> <dt>

*sFile* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**字串**，其中包含 **ShellExecute** 將執行 *vOperation* 所指定之動作的檔案名。

</dd> <dt>

*vArguments* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

包含作業參數值的字串。

</dd> <dt>

*vDirectory* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

目錄的完整路徑，其中包含 *sFile* 所指定的檔案。 如果未指定此參數，則會使用目前的工作目錄。

</dd> <dt>

*vOperation* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

要執行的作業。 此值會設定為檔案所支援的其中一個動詞字串。 如需動詞的討論，請參閱「備註」一節。 如果未指定此參數，則會執行預設作業。

</dd> <dt>

*vShow* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

一開始應該如何顯示應用程式視窗的建議。 應用程式可以忽略此建議。 此參數可以是下列其中一個值。 如果未指定此參數，應用程式會使用其預設值。



| 值                                                                                                                               | 意義                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0</dt> </dl>  | 使用隱藏視窗開啟應用程式。<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | 使用一般視窗開啟應用程式。 如果視窗最小化或最大化，系統會將其還原為其原始大小和位置。<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | 以最小化的視窗開啟應用程式。<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | 以最大化的視窗開啟應用程式。<br/>                                                                                                 |
| <dl> <dt></dt> <dt>4</dt> </dl>  | 以最新的大小和位置開啟應用程式的視窗。 使用中視窗仍維持使用中狀態。<br/>                                  |
| <dl> <dt></dt> <dt>5</dt> </dl>  | 以目前的大小和位置開啟應用程式的視窗。<br/>                                                                        |
| <dl> <dt></dt> <dt>7</dt> </dl>  | 以最小化的視窗開啟應用程式。 使用中視窗仍維持使用中狀態。<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | 使用應用程式所指定的預設狀態，以其視窗開啟應用程式。<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個方法相當於啟動與檔案的快捷方式功能表相關聯的其中一個命令。 每個命令都會以動詞字串表示。 一組支援的動詞會因檔案而異。 最常支援的動詞為 "open"，這通常也是預設動詞。 只有某些類型的檔案可能會支援其他動詞。 如需 Shell 動詞命令的進一步討論，請參閱 [啟動應用程式](launch.md) 或 [擴充快捷方式功能表](context.md)。

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例示範如何使用 **ShellExecute** 來開啟 [記事本]。 JScript 和 VBScript 會顯示使用方式。

Jscript：


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

VBScript

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
