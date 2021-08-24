---
description: GetSystemInformation 方法-捕獲系統資訊。
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: 'GetSystemInformation 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 23ad48c673fb0c5925e796f77bd43c77f3abd0afd4511864a5b840214861f792
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660648"
---
# <a name="shellgetsysteminformation-method"></a>GetSystemInformation 方法

捕獲系統資訊。

## <a name="syntax"></a>語法


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a>參數

<dl> <dt>

*sName* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**字串**，指定所要求的系統資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型： **Variant**

傳回所要求系統資訊的值。 傳回型別取決於所要求的系統資訊。 如需詳細資訊，請參閱＜備註＞一節。

### <a name="vb"></a>VB

類型： **Variant**

傳回所要求系統資訊的值。 傳回型別取決於所要求的系統資訊。 如需詳細資訊，請參閱＜備註＞一節。

## <a name="remarks"></a>備註

這個方法可以用來要求許多系統資訊值。 下表提供用來要求資訊的 *sName* 值，以及傳回值的相關聯類型。



*sName*

傳回類型

描述

DirectoryServiceAvailable

**布林值**

如果目錄服務可以使用，則設定為 **true** ;否則 **為 false**。

DoubleClickTime

**整數**

按兩下時間（以毫秒為單位）。

ProcessorLevel

**整數**

**Windows Vista 和更新版本**。 處理器層級。 分別針對 x386、x486 和 Pentium 層處理器傳回3、4或5。

>processorspeed

**整數**

處理器速度，以 MHz (MHz) 。

ProcessorArchitecture

**整數**

處理器架構。 如需詳細資訊，請參閱 [**系統 \_ 資訊**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)結構的 **wProcessorArchitecture** 成員討論。

PhysicalMemoryInstalled

**整數**

已安裝的實體記憶體數量（以位元組為單位）。

以下僅適用于 Windows XP。

Iso \_ Professional

**布林值**

如果作業系統是 Windows XP Professional Edition，則設定為 **true** ;否則 **為 false**。

Iso \_ 個人

**布林值**

如果作業系統是 Windows XP Home Edition，則設定為 **true** ;否則 **為 false**。

以下僅適用于 Windows XP 及更新版本。

Iso \_ DomainMember

**布林值**

如果電腦是網域的成員，則設定為 **true** ;否則 **為 false**。



 

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例顯示 JScript 和 VBScript 的 **GetSystemInformation** 用法。

JScript：


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

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



 

 
