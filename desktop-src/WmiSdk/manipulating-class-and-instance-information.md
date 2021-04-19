---
description: WMI 提供各種不同的技術，可讓您使用 Microsoft PowerShell、Visual&160，來取得和操作 WMI 類別和實例資訊 \# ;Basic 腳本撰寫版 (VBScript) 和 c + +。
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: 操作類別和實例資訊
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987774"
---
# <a name="manipulating-class-and-instance-information"></a>操作類別和實例資訊

WMI 提供各種不同的技術，可讓您使用 Microsoft PowerShell Visual Basic Scripting Edition (VBScript) 和 c + +，來取得和操作 WMI 類別和實例資訊。

下表列出的主題將討論取得和操作 WMI 類別和實例資訊的技術。



| 主題                                                                                  | 描述                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [正在抓取 WMI 類別或實例資料](retrieving-class-or-instance-data.md)         | 從 WMI 資訊儲存機制取出和設定資料。                                                                                                                 |
| [修改實例屬性](modifying-an-instance-property.md)                   | 在實例抓取之後變更其資訊。                                                                                                                     |
| [變更實例的繼承](changing-the-inheritance-of-an-instance.md) | 變更實例的父類別。                                                                                                                                           |
| [修改方法](modifying-a-method.md)                                           | 修改實例的參數。                                                                                                                                             |
| [列舉 WMI](enumerating-wmi.md)                                                 | 列舉 WMI 物件。                                                                                                                                                            |
| [查詢 WMI](querying-wmi.md)                                                       | 查詢 WMI 物件。                                                                                                                                                                |
| [呼叫方法](calling-a-method.md)                                               | 使用由 Microsoft 或其他協力廠商開發人員建立的相關方法來進一步操作 WMI 物件，否則會直接影響 WMI 物件所代表的物件。 |
| [存取集合](accessing-a-collection.md)                                   | 列舉腳本中的集合。                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a>使用 VBScript 運算元據

您可以直接在 [**SWbemObject**](swbemobject.md)上使用直接存取來存取 wmi 類別或實例的 wmi 屬性，而不是透過該物件的屬性 [集合](accessing-a-collection.md) 。 您也可以使用程式設計語言的原生樣式來執行該物件的方法，而不是使用 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) 呼叫。 例如， [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)中的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法在 windows 2000 中有三個參數，但是在 windows Server 2003 中有四個參數。

使用直接存取時，您可以將 WMI 屬性和方法視為 [**SWbemObject**](swbemobject.md)的自動化屬性和方法。

下列範例會顯示如何存取屬性。


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



下列範例顯示當您有直接存取權時，可以如何存取屬性。


```VB
VolumeName = MyDisk.VolumeName
```



物件的連結也是可接受的。

下列範例示範如何存取內嵌在另一個物件中之物件的屬性。


```VB
value = MyComputer.MyDisk.VolumeName
```



下列範例示範如何使用陣列注標標記法來存取屬性。


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



下列 VBScript 程式碼範例示範如何將輸入參數的實例產生到 [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process)類別中的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法做為 [**SWbemObject**](swbemobject.md)、填入輸入屬性，然後使用 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)來執行 **create** 方法。

[**SWbemObject 方法 \_**](swbemobject-methods-.md)屬性會傳回 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)方法的 [**SWbemMethodSet**](swbemmethodset.md)集合。 方法集合的成員是 [**SWbemMethod**](swbemmethod.md) 物件，而 [**SWbemMethod**](swbemmethod-inparameters.md) 則會傳回 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) 方法的輸入參數。 必要的 *命令列* 輸入參數設定為 "calc.exe"。 方法接著會由 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)執行，以產生 calc.exe 的進程。


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



下列程式碼範例示範如何使用直接存取來執行先前的作業。


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



如需詳細資訊，請參閱[使用 SWbemObject](scripting-with-swbemobject.md)[呼叫提供者方法](calling-a-provider-method.md)和腳本。

 

 
