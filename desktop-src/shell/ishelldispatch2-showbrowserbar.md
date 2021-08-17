---
description: IShellDispatch2. ShowBrowserBar 方法-顯示瀏覽器列。
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: 'IShellDispatch2. ShowBrowserBar 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0b1380a44d2985b75e77dced43878c85e38d6a21b877fe06d9cdc7c10a8a2002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090328"
---
# <a name="ishelldispatch2showbrowserbar-method"></a>IShellDispatch2. ShowBrowserBar 方法

顯示瀏覽器列。

## <a name="syntax"></a>語法


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a>參數

<dl> <dt>

*sCLSID* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**字串**，包含要顯示的瀏覽器列之 CLSID 的字串形式。 物件必須註冊為具有 CATID \_ InfoBand 元件類別目錄的 Explorer Bar 物件。 如需詳細資訊，請參閱 [建立自訂的瀏覽器列、工具區和書桌等區](band-objects.md)。

</dd> <dt>

*vShow* \[在\]
</dt> <dd>

類型： **Variant**

設定為 **true** 會顯示流覽列，或設定為 **false** 以隱藏它。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型： **Variant \***

如果成功，則傳回 **true** ;否則 **為 false**。

### <a name="vb"></a>VB

類型： **Variant \***

如果成功，則傳回 **true** ;否則 **為 false**。

## <a name="remarks"></a>備註

這個方法是透過 [**ShowBrowserBar**](./shell-showbrowserbar.md) 方法來執行和存取。

您可以將 *sCLSID* 參數設定為該 explorer 列的 CLSID，以顯示其中一個標準 Explorer 列。 標準 Explorer 列和其 CLSID 字串如下所示：



| Explorer Bar | CLSID 字串                           |
|--------------|----------------------------------------|
| 我的最愛    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| 資料夾      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| 記錄      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| 搜尋       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例示範如何使用 **ShowBrowserBar** 來顯示 [我的最愛 **]** 瀏覽器列。 JScript 和 VBScript 都會顯示使用方式。

JScript：


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

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



 

 
