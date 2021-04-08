---
description: 聯結視圖類別包含以通用屬性值（例如 Class1. Prop1 = Class2. This.prop2）連接之來源類別實例的屬性。 聯結視圖類別中的每個實例都是由不同類別實例的部分所組成。
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: 從舊的屬性建立新的實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945111"
---
# <a name="creating-a-new-instance-from-old-properties"></a>從舊的屬性建立新的實例

聯結視圖類別包含以通用屬性值（例如 **Class1. Prop1**  =  **Class2. this.prop2**）連接之來源類別實例的屬性。 聯結視圖類別中的每個實例都是由不同類別實例的部分所組成。

您可以根據屬性值的不等比較來建立聯結視圖類別，例如 **Prop1**  <>  **Class2. this.prop2** ，其中 **Prop1** 和 **this.prop2** 不會對應至 view 類別中的相同屬性。

當您要尋找的資訊包含在個別但相關的類別中時，聯結視圖類別會很有用。 例如，如果您想要有關印表機和印表機設定的資訊，您可以建立包含 [**win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer) 類別的部分屬性和 [**win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) 類別的部分屬性的聯結視圖類別。 如果沒有 View Provider，您必須抓取併合並不同實例的屬性，才能取得所需的資訊。

下列程式描述如何建立聯結視圖類別。

**建立聯結視圖類別**

1.  使用 [**JoinOn**](qualifiers-specific-to-the-view-provider.md) 字串辨識符號來開始類別定義。

    [**JoinOn**](qualifiers-specific-to-the-view-provider.md)、 **Association** 和 **Union** 限定詞都是互斥的。

2.  如有必要，請套用 [**PostJoinFilter**](postjoinfilter-qualifier.md) 限定詞，以篩選您想要在聯結類別中的實例。

    [**PostJoinFilter**](postjoinfilter-qualifier.md)提供者可讓您將 view 類別的實例限制為符合特定條件的實例。

3.  建立查詢，以使用 [**ViewSources**](viewsources-qualifier.md) 限定詞來定義 view 類別的來源實例。
4.  使用 [**ViewSpaces**](viewspaces-qualifier.md) 限定詞來定義來源實例所在之命名空間的名稱和位置。
5.  使用 [**PropertySources**](propertysources-qualifier.md) 限定詞，在聯結視圖類別中定義您想要的屬性。

    將屬性加入至根據相等的聯結視圖時，必須在一個 [**PropertySources**](propertysources-qualifier.md) 限定詞中對應兩個來源屬性。

    下列程式碼範例顯示在一個 **PropertySources** 辨識符號中對應的兩個屬性。

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    您可以使用 [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) 限定詞標記屬於來源類別的屬性。

下列程式碼範例示範從效能監視器提供者類別 [**Win32 \_ PerfRawData \_ Perfproc.dll \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 和 [**win32 \_ PerfRawData \_ perfproc.dll \_ 執行緒**](/previous-versions//aa394325(v=vs.85)) 建立的聯結視圖類別，其中包含由 **ProcessID** 屬性聯結的兩個類別的屬性。

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
