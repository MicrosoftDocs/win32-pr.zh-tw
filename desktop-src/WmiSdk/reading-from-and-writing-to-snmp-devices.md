---
description: 您可以在 WMI SMIR (SNMP 模組資訊存放庫) 中，讀取或寫入其對應的類別實例，以存取 SNMP 裝置。
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: 讀取和寫入 SNMP 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513064"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a><span data-ttu-id="71044-103">讀取和寫入 SNMP 裝置</span><span class="sxs-lookup"><span data-stu-id="71044-103">Reading from and Writing to SNMP Devices</span></span>

<span data-ttu-id="71044-104">您可以在 WMI SMIR (SNMP 模組資訊存放庫) 中，讀取或寫入其對應的類別實例，以存取 SNMP 裝置。</span><span class="sxs-lookup"><span data-stu-id="71044-104">SNMP devices can be accessed by reading from or writing to their corresponding class instance in the WMI SMIR (SNMP Module Information Repository).</span></span> <span data-ttu-id="71044-105">當您使用相同類型的多個裝置時，為了提高效率，請將一個 SNMP 裝置類型的 Mib 載入 SMIR 中。</span><span class="sxs-lookup"><span data-stu-id="71044-105">When you are working with multiple devices of the same type, for efficiency, load the MIBs for one SNMP device type into the SMIR.</span></span>

> [!Note]  
> <span data-ttu-id="71044-106">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="71044-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="71044-107">選取下列其中一個選項，以在與每個 SNMP 裝置通訊之前，先更新實例的內容資訊，以讀取或寫入每一種 SNMP 裝置類型。</span><span class="sxs-lookup"><span data-stu-id="71044-107">Select one of the following options to read to or write from each SNMP device type by updating the context information of the instance before communicating with each one.</span></span>

-   <span data-ttu-id="71044-108">參考特定裝置時，請使用 DNS 名稱，而非 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="71044-108">Use a DNS name instead of the IP address when referencing a specific device.</span></span>

    <span data-ttu-id="71044-109">下列範例顯示如何使用特定裝置的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="71044-109">The following example shows how to use the DNS name for a specific device.</span></span>

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   <span data-ttu-id="71044-110">建立不同的命名空間，並使用 AgentAddress 實例辨識符號將裝置位址與命名空間物件建立關聯，以便將命名空間永久系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="71044-110">Create a separate namespace and associate a device address to the namespace object using the AgentAddress instance qualifier so that the namespace is permanently bound to the device.</span></span> <span data-ttu-id="71044-111">在此情況下，您不需要指定內容物件資訊。</span><span class="sxs-lookup"><span data-stu-id="71044-111">In this case, you need not specify the context object information.</span></span>
-   <span data-ttu-id="71044-112">從 SNMP 裝置讀取。</span><span class="sxs-lookup"><span data-stu-id="71044-112">Read from an SNMP device.</span></span>

    <span data-ttu-id="71044-113">下列範例會在裝置類別上執行 Get 作業。</span><span class="sxs-lookup"><span data-stu-id="71044-113">The following example performs a Get operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   <span data-ttu-id="71044-114">寫入 SNMP 裝置。</span><span class="sxs-lookup"><span data-stu-id="71044-114">Write to an SNMP device.</span></span>

    <span data-ttu-id="71044-115">下列範例會在裝置類別上執行設定作業。</span><span class="sxs-lookup"><span data-stu-id="71044-115">The following example performs a Set operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

<span data-ttu-id="71044-116">相互關聯的類別是指當發生列舉時，指定的 SNMP 裝置可支援的類別。</span><span class="sxs-lookup"><span data-stu-id="71044-116">Correlated classes are those that a given SNMP device is known to support when enumeration occurs.</span></span> <span data-ttu-id="71044-117">相互關聯會影響從 SMIR 傳回的一組類別。</span><span class="sxs-lookup"><span data-stu-id="71044-117">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="71044-118">Noncorrelated 列舉會傳回 SMIR 中所有出現的類別，不論裝置是否支援它們。</span><span class="sxs-lookup"><span data-stu-id="71044-118">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="71044-119">如需有關使用 WMI 相互關聯技術的詳細資訊，請參閱 [WMI SNMP 類別相互關聯](wmi-snmp-class-correlation.md)。</span><span class="sxs-lookup"><span data-stu-id="71044-119">For more information about using WMI correlation techniques, see [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).</span></span>

 

 



