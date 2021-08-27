---
description: 更新 WMI 類別實例最常見的方法，就是一次更新整個實例。
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: 更新整個實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41cac29805eeff1f8c659c0bee6832eb65e9e6b5bdee8cd15bd0a052247a70e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995537"
---
# <a name="updating-an-entire-instance"></a>更新整個實例

更新 WMI 類別實例最常見的方法，就是一次更新整個實例。 藉由更新整個實例，WMI 不需要將實例剖析為個別的屬性，並將其傳送至您的應用程式。 相反地，WMI 可以直接傳送整個實例給您。 當您完成時，WMI 可以將整個變更的實例複製到原始實例上。

下列程式描述如何使用 PowerShell 修改或更新實例。

**使用 PowerShell 修改或更新實例**

1.  使用 >get-wmiobject 的呼叫取出物件的本機複本。

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  如有必要，請使用屬性集合的呼叫來查看物件的屬性。

    雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  對本機物件屬性進行任何變更。

    這麼做只會變更本機複本。 若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  使用 Put 方法的呼叫，將物件放回 WMI 存放庫。

    ```PowerShell
    $mySettings.Put()
    ```

    

下列程式說明如何使用 c # 來修改或更新實例。

**若要使用 c # (的) 修改或更新實例，請使用基礎結構**

1.  使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85))的呼叫來取出物件的本機複本，如抓取 [WMI 實例](retrieving-an-instance.md)中所述。

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  如有必要，請使用屬性集合的呼叫來查看物件的屬性。

    雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  對本機物件屬性進行任何變更。

    這麼做只會變更本機複本。 若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  使用 [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85))的呼叫，將物件放回 WMI 存放庫。

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

下列程式描述如何使用 PowerShell 修改或更新實例。

> [!Note]  
> **系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。

 

**若要使用 c # (Microsoft. 管理) 來修改或更新實例**

1.  使用 [system.management.managementobject](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get)的呼叫取出物件的本機複本。

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  如有必要，請使用屬性集合的呼叫來查看物件的屬性。

    雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  對本機物件屬性進行任何變更。

    這麼做只會變更本機複本。 若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  使用 [system.management.managementobject](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) 或方法的呼叫，將物件放回 WMI 存放庫。

    ```CSharp
    myDisk.Put();
    ```

    

下列程式描述如何使用 VBScript 修改或更新實例。

**使用 VBScript 修改或更新實例**

1.  使用 **GetObject** 的呼叫來取出物件的本機複本。
2.  如有必要，請使用 [**屬性 \_**](swbemobject-properties-.md)方法的呼叫來查看物件的屬性。

    雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。

3.  使用 [**swbempropertyset**](swbemproperty-value.md) 方法的呼叫對物件屬性進行任何變更。

    **Value** 方法只會變更本機複本。 若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。

4.  使用呼叫 [**\_ SWbemObject**](swbemobject-put-.md)或 [**SWbemObject PutAsync \_**](swbemobject-putasync-.md)方法，將物件放回 WMI 存放庫。

顧名思義， [**PutAsync \_**](swbemobject-putasync-.md)更新時，會以同步方式 [**放置 \_**](swbemobject-put-.md)更新。 這兩種方法都會使用已修改的實例複製原始實例。 不過，若要利用非同步處理，您必須建立 [**SWbemSink**](swbemsink.md) 物件。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

下列程式描述如何使用 c + + 修改或更新實例。

**使用 c + + 修改或更新實例**

1.  藉由呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)，取出實例的本機複本。
2.  如有必要，請使用 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)的呼叫來查看物件的屬性。

    雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。

3.  使用 IWbemClassObject 的呼叫對複製進行任何必要的變更 [**：:P 的內容**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)。

    **Put** 方法只會變更本機複本。 若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。

4.  將您的複本放回 WMI 儲存機制中，並呼叫 [**iwbemservices：:P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) 或 [**IWbemServices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) 方法。

    顧名思義，在以非同步方式 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)更新時， **PutInstance** 會同步更新。 這兩種方法都會使用已修改的實例複製原始實例。 不過，若要利用非同步處理，您必須執行 [**IWbemObjectSink**](iwbemobjectsink.md) 介面。

    請注意，屬於類別階層的實例上的更新作業可能會因為與階層中另一個類別有關的錯誤而無法成功。 WMI 會呼叫每個提供者的 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) 方法，這些提供者負責衍生原始實例之類別的類別。 如果有任何這些提供者失敗，原始的更新要求就會失敗。 如需詳細資訊，請參閱 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)的「備註」一節。

如需詳細資訊，請參閱 [呼叫提供者方法](calling-a-provider-method.md)。

> [!Note]  
> 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

 

 
