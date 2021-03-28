---
description: 顯示 [尋找印表機] 對話方塊。
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: 'IShellDispatch2. FindPrinter 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191616"
---
# <a name="ishelldispatch2findprinter-method"></a>IShellDispatch2. FindPrinter 方法

顯示 [ **尋找印表機** ] 對話方塊。

## <a name="syntax"></a>語法


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a>參數

<dl> <dt>

*sName* \[在中，選擇性\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

包含印表機名稱的 **字串** 。

</dd> <dt>

*sLocation* \[在中，選擇性\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

包含印表機位置的 **字串** 。

</dd> <dt>

*sModel* \[在中，選擇性\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

包含印表機型號的 **字串** 。

</dd> </dl>

## <a name="remarks"></a>備註

這個方法是透過 [**FindPrinter**](./shell-findprinter.md) 方法來執行和存取。

如果您將字串指派給一或多個選擇性參數，當顯示 [ **尋找印表機** ] 對話方塊時，它們會在相關聯的編輯控制項中顯示為預設值。 使用者可以接受或覆寫這些值。 如果未指派任何值給參數，則相關聯的編輯方塊是空的，而且使用者必須輸入值。

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例示範如何使用 **FindPrinter** 來顯示特定應用程式的 [ **尋找印表機** ] 對話方塊。 JScript、VBScript 和 Visual Basic 會顯示使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
