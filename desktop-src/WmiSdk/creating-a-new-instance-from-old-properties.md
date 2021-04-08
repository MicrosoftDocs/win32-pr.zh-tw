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
# <a name="creating-a-new-instance-from-old-properties"></a><span data-ttu-id="cb3d4-104">從舊的屬性建立新的實例</span><span class="sxs-lookup"><span data-stu-id="cb3d4-104">Creating a New Instance from Old Properties</span></span>

<span data-ttu-id="cb3d4-105">聯結視圖類別包含以通用屬性值（例如 **Class1. Prop1**  =  **Class2. this.prop2**）連接之來源類別實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-105">A join view class contains properties from source class instances that are connected by a common property value, such as **Class1.Prop1** = **Class2.Prop2**.</span></span> <span data-ttu-id="cb3d4-106">聯結視圖類別中的每個實例都是由不同類別實例的部分所組成。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-106">Each instance in a join view class consists of parts of different class instances.</span></span>

<span data-ttu-id="cb3d4-107">您可以根據屬性值的不等比較來建立聯結視圖類別，例如 **Prop1**  <>  **Class2. this.prop2** ，其中 **Prop1** 和 **this.prop2** 不會對應至 view 類別中的相同屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-107">You can base a join view class on inequality of property values, such as **Class1.Prop1** <> **Class2.Prop2** where **Prop1** and **Prop2** are not mapped to the same property in the view class.</span></span>

<span data-ttu-id="cb3d4-108">當您要尋找的資訊包含在個別但相關的類別中時，聯結視圖類別會很有用。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-108">A join view class is helpful when the information you are looking for is contained in separate but related classes.</span></span> <span data-ttu-id="cb3d4-109">例如，如果您想要有關印表機和印表機設定的資訊，您可以建立包含 [**win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer) 類別的部分屬性和 [**win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) 類別的部分屬性的聯結視圖類別。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-109">For example, if you want information about a printer and about the printer configuration, you can create a join view class that contains some of the properties of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and some of the properties of the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) class.</span></span> <span data-ttu-id="cb3d4-110">如果沒有 View Provider，您必須抓取併合並不同實例的屬性，才能取得所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-110">Without the View Provider, you must retrieve and merge the properties of the separate instances to get the information you need.</span></span>

<span data-ttu-id="cb3d4-111">下列程式描述如何建立聯結視圖類別。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-111">The following procedure describes how to create a join view class.</span></span>

<span data-ttu-id="cb3d4-112">**建立聯結視圖類別**</span><span class="sxs-lookup"><span data-stu-id="cb3d4-112">**To create a join view class**</span></span>

1.  <span data-ttu-id="cb3d4-113">使用 [**JoinOn**](qualifiers-specific-to-the-view-provider.md) 字串辨識符號來開始類別定義。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-113">Begin a class definition with the [**JoinOn**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="cb3d4-114">[**JoinOn**](qualifiers-specific-to-the-view-provider.md)、 **Association** 和 **Union** 限定詞都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-114">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="cb3d4-115">如有必要，請套用 [**PostJoinFilter**](postjoinfilter-qualifier.md) 限定詞，以篩選您想要在聯結類別中的實例。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-115">If necessary, filter the instances that you want in the join class by applying the [**PostJoinFilter**](postjoinfilter-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="cb3d4-116">[**PostJoinFilter**](postjoinfilter-qualifier.md)提供者可讓您將 view 類別的實例限制為符合特定條件的實例。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-116">The [**PostJoinFilter**](postjoinfilter-qualifier.md) provider allows you to restrict the instances of a view class to instances that meet specific conditions.</span></span>

3.  <span data-ttu-id="cb3d4-117">建立查詢，以使用 [**ViewSources**](viewsources-qualifier.md) 限定詞來定義 view 類別的來源實例。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-117">Create the queries that define source instances of the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="cb3d4-118">使用 [**ViewSpaces**](viewspaces-qualifier.md) 限定詞來定義來源實例所在之命名空間的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-118">Define the names and locations of the namespaces where the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
5.  <span data-ttu-id="cb3d4-119">使用 [**PropertySources**](propertysources-qualifier.md) 限定詞，在聯結視圖類別中定義您想要的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-119">Define the properties that you want in a join view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="cb3d4-120">將屬性加入至根據相等的聯結視圖時，必須在一個 [**PropertySources**](propertysources-qualifier.md) 限定詞中對應兩個來源屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-120">When properties are added to the join view based on equality, the two source properties must be mapped in one [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="cb3d4-121">下列程式碼範例顯示在一個 **PropertySources** 辨識符號中對應的兩個屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-121">The following code example shows two properties that are mapped in one **PropertySources** qualifier.</span></span>

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    <span data-ttu-id="cb3d4-122">您可以使用 [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) 限定詞標記屬於來源類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-122">By using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier, you can tag the properties that belong to a source class.</span></span>

<span data-ttu-id="cb3d4-123">下列程式碼範例示範從效能監視器提供者類別 [**Win32 \_ PerfRawData \_ Perfproc.dll \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) 和 [**win32 \_ PerfRawData \_ perfproc.dll \_ 執行緒**](/previous-versions//aa394325(v=vs.85)) 建立的聯結視圖類別，其中包含由 **ProcessID** 屬性聯結的兩個類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3d4-123">The following code example shows a join view class created from the Performance Monitor provider classes [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) and [**Win32\_PerfRawData\_PerfProc\_Thread**](/previous-versions//aa394325(v=vs.85)) with properties of both classes joined by the **ProcessID** property.</span></span>

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

 

 
