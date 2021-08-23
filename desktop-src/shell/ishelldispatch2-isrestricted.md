---
description: IShellDispatch2. IsRestricted 方法-從登錄中抓取群組的限制設定。
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: 'IShellDispatch2. IsRestricted 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 73bbaaefbe12e178a8ef5818665f97d29cc105e45c20c010a6c02254ab897b11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710378"
---
# <a name="ishelldispatch2isrestricted-method"></a>IShellDispatch2. IsRestricted 方法

從登錄抓取群組的限制設定。

## <a name="syntax"></a>語法


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a>參數

<dl> <dt>

*sGroup* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

包含組名的 **字串** 。 此值是用來檢查限制的登錄子機碼名稱。

</dd> <dt>

*sRestriction* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**字串**，包含要取出其值的限制。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型：**整數 \***

限制的值。 如果找不到指定的限制，則傳回值為0。

### <a name="vb"></a>VB

類型：**整數 \***

限制的值。 如果找不到指定的限制，則傳回值為0。

## <a name="remarks"></a>備註

這個方法是透過 [**IsRestricted**](./shell-isrestricted.md) 方法來執行和存取。

**IsRestricted** 會先尋找符合下列索引鍵之 *sGroup* 的子機碼名稱。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

限制會宣告為個別原則子機碼的值。 如果在 *sGroup* 中名為的子機碼中找到名為 *sRestriction* 的限制，則 **IsRestricted** 會傳回限制的目前值。 如果在 **HKEY \_ 本機 \_ 電腦** 下找不到限制，則會在 [ **HKEY 目前的 \_ \_ 使用者**] 底下檢查相同的子機碼。

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例示範如何使用 **IsRestricted** 從 **系統** 子機碼取出 **undockwithoutlogon** 限制的資料值。 JScript 和 VBScript 都會顯示使用方式。

JScript：


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
