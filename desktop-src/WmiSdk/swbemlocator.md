---
description: 您可以使用 Wbemscripting.swbemlocator 物件的方法來取得 SWbemServices 物件，該物件代表本機電腦或遠端主機電腦上的命名空間連接。
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: 'Wbemscripting.swbemlocator 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984208"
---
# <a name="swbemlocator-object"></a>Wbemscripting.swbemlocator 物件

您可以使用 **wbemscripting.swbemlocator** 物件的方法來取得 [**SWbemServices**](swbemservices.md) 物件，該物件代表本機電腦或遠端主機電腦上的命名空間連接。 然後，您可以使用 **SWbemServices** 物件的方法來存取 WMI。 這個物件可以由 VBScript **CreateObject** 呼叫建立。

## <a name="members"></a>成員

**Wbemscripting.swbemlocator** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Wbemscripting.swbemlocator** 物件有這些方法。



| 方法                                              | 描述                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**ConnectServer**](swbemlocator-connectserver.md) | 連接到指定電腦上的 WMI。<br/> |



 

### <a name="properties"></a>屬性

**Wbemscripting.swbemlocator** 物件具有這些屬性。



| 屬性                                                | 存取類型          | Description                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**安全性\_**](swbemlocator-security-.md)<br/> | 唯讀<br/> | 用來讀取或變更安全性設定。<br/> |



 

## <a name="remarks"></a>備註

WMI 腳本程式庫物件模型的頂端是 Wbemscripting.swbemlocator 物件。 Wbemscripting.swbemlocator 是用來建立與 WMI 命名空間的已驗證連接，相當於 VBScript GetObject 函數和 WMI 名字 "winmgmts：" 用來建立與 WMI 的已驗證連線。 不過，Wbemscripting.swbemlocator 的設計目的是要解決兩個無法使用 GetObject 和 WMI 標記來執行的特定腳本案例。 如果需要的話，您必須使用 Wbemscripting.swbemlocator：

-   提供使用者和密碼認證，以連接到遠端電腦上的 WMI。 與 GetObject 函數搭配使用的 WMI 標記不包含用來指定認證的機制。 大部分的 WMI 活動 (包括在遠端電腦上執行的所有作業) 都需要系統管理員許可權。 如果您通常使用一般使用者帳戶而非系統管理員帳戶登入，除非您在 [其他認證] 下執行腳本，否則無法執行大部分的 WMI 工作。
-   如果您是從網頁內執行 WMI 腳本，請連接至 WMI。 當您執行內嵌于 HTML 網頁中的腳本時，不能使用 GetObject 函式，因為基於安全考慮，Internet Explorer 不允許使用 GetObject。

此外，如果您發現與 GetObject 混淆或很難使用的 WMI 連接字串，您可能會想要使用 Wbemscripting.swbemlocator 連接到 WMI。

您可以使用 CreateObject 而非 GetObject 來建立 Wbemscripting.swbemlocator 的參考。 若要建立參考，您必須將 Wbemscripting.swbemlocator 程式設計識別碼 (ProgID) "WbemScripting. Wbemscripting.swbemlocator" 傳遞給 CreateObject 函式，如下列腳本範例的第2行所示。 取得 Wbemscripting.swbemlocator 物件的參考之後，您可以呼叫 ConnectServer 方法來連接至 WMI，並取得 SWbemServices 物件的參考。 這會在下列腳本的第3行上示範。


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



若要在替代認證下執行腳本，請將使用者名稱和密碼納入為傳遞給 ConnectServer 的其他參數。 例如，此腳本會使用名為 kenmyer 之使用者的認證來執行，並具有密碼 homerj。


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



您也可以使用網域 \\ 使用者名稱格式來指定使用者名稱。 例如：

`" fabrikam\kenmyer"`

## <a name="examples"></a>範例

下列 PowerShell 範例會使用 **wbemscripting.swbemlocator** 來連接到伺服器。


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ wbemscripting.swbemlocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




