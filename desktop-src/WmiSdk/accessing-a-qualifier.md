---
description: 辨識符號是一種標記，可提供 WMI 物件、方法或屬性的詳細資訊。
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: 存取 WMI 辨識符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45601de8e7b3f8ef7054742812c24f9a81dcedf5417f7b7ba501f2471adedc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820616"
---
# <a name="accessing-a-wmi-qualifier"></a>存取 WMI 辨識符號

辨識符號是一種標記，可提供 WMI 物件、方法或屬性的詳細資訊。 有時，您可能需要存取儲存在辨識符號中的資料。 例如，一般工作是藉由嘗試抓取該方法的已實限定詞來判斷提供者是否要 **執行** 方法。 如需詳細資訊，請參閱 [WMI 限定詞](wmi-qualifiers.md) 和 [新增限定詞](adding-a-qualifier.md)。

您可以先抓取物件，然後檢查限定詞，如同任何其他屬性一樣，在 PowerShell 中取出 WMI 物件的限定詞。

**使用 PowerShell 取出辨識符號**

-   使用 [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx)抓取您想要查看其辨識符號的物件，然後透過 **限定詞** 屬性存取限定詞：

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。

您可以藉由先取得物件，然後檢查限定詞是否為集合，以 c # 取出 WMI 實例上的限定詞。

**若要使用 c # 取出辨識符號 (Microsoft.System。管理)**

1.  使用指定的類別名稱和命名空間來建立 CimInstance 物件，以抓取您想要查看其限定詞的類別。

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。

2.  您可以從 [CimInstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85))、 [CimInstance. CimClass.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))CimClassProperties 的屬性限定詞，以及 [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)). CimClass 的方法限定詞取得類別限定詞。

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。

您可以先取得物件，然後檢查限定詞是否為集合，以在 c # 中抓取 WMI 物件上的限定詞。

> [!Note]  
> **系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。

 

**若要使用 c # (System. 管理來取得限定詞)**

1.  使用 [system.management.managementobject](/dotnet/api/system.management.managementobject)抓取您想要查看其限定詞的物件。

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。

2.  將限定詞放入 [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)，並列舉 [QualifierData](/dotnet/api/system.management.qualifierdata) 值。

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。

下列程式描述如何使用 VBScript 取出辨識符號。

**使用 VBScript 取出辨識符號**

1.  取得您想要查看其限定詞的物件，如下列範例所示：

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    取得物件最常見的方式是使用 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 方法。 如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。

2.  透過 [**SWbemObject \_**](swbemobject-qualifiers-.md)的限定詞屬性存取物件的限定詞，如下列範例所示：

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

下列程式碼範例說明如何存取 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 程式物件上的所有限定詞。


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



下列程式說明如何使用 c + + 來取得限定詞。

**使用 c + + 取出辨識符號**

1.  取得您想要查看其限定詞的物件。

    取得物件最常見的方式是使用 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)的呼叫。 如需詳細資訊，請參閱抓取 [WMI 類別或實例資料](retrieving-class-or-instance-data.md)。

2.  藉由呼叫 [**IWbemClassObject：： GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) 或 [**IWbemClassObject：： GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) 方法，取得指定屬性的限定詞集合。

3.  透過傳回的 [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) 介面存取物件的限定詞。

## <a name="examples"></a>範例

如需有關如何抓取限定詞的詳細資訊，請參閱 TechNet 資源庫上的 [WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell 程式碼範例。

 

 
