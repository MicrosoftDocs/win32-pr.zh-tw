---
description: 以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [顯示視窗堆疊]。
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: 'IShellDispatch. TileHorizontally 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e83870abcec849b9e8bf5a2583b6e25d4e2a2280ead4df9c4979014149a643ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678442"
---
# <a name="ishelldispatchtilehorizontally-method"></a>IShellDispatch. TileHorizontally 方法

以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ **顯示視窗堆疊**]。

## <a name="syntax"></a>語法


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

這個方法不會傳回值。

### <a name="vb"></a>VB

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法是透過 [**TileHorizontally**](shell-tilehorizontally.md) 方法來執行和存取。

## <a name="examples"></a>範例

下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **TileHorizontally** 。

JScript：


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




