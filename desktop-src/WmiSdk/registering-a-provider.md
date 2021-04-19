---
description: 在執行提供者之前，您應該先向 WMI 註冊您的提供者。 註冊提供者會定義提供者的類型和提供者支援的類別。 WMI 只能存取已註冊的提供者。
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: 註冊提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974524"
---
# <a name="registering-a-provider"></a><span data-ttu-id="2d4db-105">註冊提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-105">Registering a Provider</span></span>

<span data-ttu-id="2d4db-106">在執行提供者之前，您應該先向 WMI 註冊您的提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-106">Before implementing your provider, you should first register your provider with WMI.</span></span> <span data-ttu-id="2d4db-107">註冊提供者會定義提供者的類型和提供者支援的類別。</span><span class="sxs-lookup"><span data-stu-id="2d4db-107">Registering the provider defines the type of the provider and the classes that the provider supports.</span></span> <span data-ttu-id="2d4db-108">WMI 只能存取已註冊的提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-108">WMI can only access registered providers.</span></span>

> [!Note]  
> <span data-ttu-id="2d4db-109">如需註冊 MI 提供者的詳細資訊，請參閱 [如何：註冊 Mi 提供者](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-109">For more information on registering an MI provider, see [How to: Register an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span></span>

 

<span data-ttu-id="2d4db-110">註冊提供者之前，您可以撰寫提供者程式碼。</span><span class="sxs-lookup"><span data-stu-id="2d4db-110">You can write your provider code before you register the provider.</span></span> <span data-ttu-id="2d4db-111">不過，您很難對未向 WMI 註冊的提供者進行 debug 錯。</span><span class="sxs-lookup"><span data-stu-id="2d4db-111">However, it is very difficult to debug a provider that is not registered with WMI.</span></span> <span data-ttu-id="2d4db-112">判斷您提供者的介面也有助於概述提供者的用途和結構。</span><span class="sxs-lookup"><span data-stu-id="2d4db-112">Determining the interfaces for your provider also helps to outline the purpose and structure of a provider.</span></span> <span data-ttu-id="2d4db-113">因此，註冊您的提供者可協助您設計您的提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-113">Therefore, registering your provider helps you design your provider.</span></span>

<span data-ttu-id="2d4db-114">只有系統管理員可以註冊或刪除提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-114">Only administrators can register or delete a provider.</span></span>

<span data-ttu-id="2d4db-115">提供者必須針對其執行的所有不同類型的提供者函式註冊。</span><span class="sxs-lookup"><span data-stu-id="2d4db-115">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="2d4db-116">幾乎所有提供者都提供其定義的類別實例，但它們也可以提供屬性資料、方法、事件或類別。</span><span class="sxs-lookup"><span data-stu-id="2d4db-116">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="2d4db-117">提供者也可以註冊為事件取用者提供者或效能計數器提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-117">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span> <span data-ttu-id="2d4db-118">建議您將所有提供者功能合併成一個提供者，而不是針對每個類型各有許多不同的提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-118">It is recommended that you combine all provider functionality in one provider rather than having many separate providers for each type.</span></span> <span data-ttu-id="2d4db-119">例如，提供方法和實例的 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)，以及提供實例、方法和事件的 [磁片配額提供者](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-119">An example is the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which provides methods and instances, and the [Disk Quota provider](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), which supplies instances, methods, and events.</span></span>

<span data-ttu-id="2d4db-120">提供者必須針對其執行的所有不同類型的提供者函式註冊。</span><span class="sxs-lookup"><span data-stu-id="2d4db-120">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="2d4db-121">幾乎所有提供者都提供其定義的類別實例，但它們也可以提供屬性資料、方法、事件或類別。</span><span class="sxs-lookup"><span data-stu-id="2d4db-121">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="2d4db-122">提供者也可以註冊為事件取用者提供者或效能計數器提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-122">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span>

<span data-ttu-id="2d4db-123">每種類型的註冊都使用相同的 [**\_ \_ Win32Provider**](--win32provider.md)實例：</span><span class="sxs-lookup"><span data-stu-id="2d4db-123">The same instance of [**\_\_Win32Provider**](--win32provider.md) is used for each type of registration:</span></span>

-   [<span data-ttu-id="2d4db-124">註冊執行個體提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-124">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
-   [<span data-ttu-id="2d4db-125">註冊類別提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-125">Registering a Class Provider</span></span>](registering-a-class-provider.md)
-   [<span data-ttu-id="2d4db-126">註冊方法提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-126">Registering a Method Provider</span></span>](registering-a-method-provider.md)
-   [<span data-ttu-id="2d4db-127">註冊事件提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-127">Registering an Event Provider</span></span>](registering-an-event-provider.md)
-   [<span data-ttu-id="2d4db-128">註冊事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-128">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
-   [<span data-ttu-id="2d4db-129">讓執行個體提供者成為 High-Performance 提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-129">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a><span data-ttu-id="2d4db-130">範例：建立及註冊提供者的實例</span><span class="sxs-lookup"><span data-stu-id="2d4db-130">Example: Creating and Registering an Instance of a Provider</span></span>

<span data-ttu-id="2d4db-131">下列範例顯示一個 MOF 檔案，該檔案會在根 cimv2 命名空間中建立並註冊 [System Registry 提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 的實例 \\ 。</span><span class="sxs-lookup"><span data-stu-id="2d4db-131">The following example shows a MOF file that creates and registers an instance of the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="2d4db-132">它會將別名 $Reg 指派給提供者，以避免在實例和方法註冊中所需的完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="2d4db-132">It assigns the alias $Reg to the provider to avoid the long pathname required in the instance and method registrations.</span></span> <span data-ttu-id="2d4db-133">如需詳細資訊，請參閱 [建立別名](creating-an-alias.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-133">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a><span data-ttu-id="2d4db-134">範例：註冊提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-134">Example: Registering a Provider</span></span>

<span data-ttu-id="2d4db-135">下列程式說明如何註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-135">The following procedure describes how to register a provider.</span></span>

<span data-ttu-id="2d4db-136">**註冊提供者**</span><span class="sxs-lookup"><span data-stu-id="2d4db-136">**To register a provider**</span></span>

1.  <span data-ttu-id="2d4db-137">將提供者註冊為 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2d4db-137">Register the provider as a COM server.</span></span>

    <span data-ttu-id="2d4db-138">如有必要，您可能需要建立登錄專案。</span><span class="sxs-lookup"><span data-stu-id="2d4db-138">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="2d4db-139">此程式適用于所有的 COM 伺服器，而且與 WMI 無關。</span><span class="sxs-lookup"><span data-stu-id="2d4db-139">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="2d4db-140">如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 檔中的 COM 一節。</span><span class="sxs-lookup"><span data-stu-id="2d4db-140">For more information, see the COM section in the Microsoft Windows Software Development Kit (SDK) documentation.</span></span>

2.  <span data-ttu-id="2d4db-141">建立 MOF 檔案，其中包含 [**\_ \_ Win32Provider**](--win32provider.md)的實例，以及直接或間接從 [**\_ \_ ProviderRegistration**](--providerregistration.md)（例如 [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md)）衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2d4db-141">Create a MOF file that contains instances of [**\_\_Win32Provider**](--win32provider.md) and an instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), such as [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="2d4db-142">只有系統管理員可以藉由建立衍生自 **\_ \_ Win32Provider** 或 [**\_ \_ ProviderRegistration**](--providerregistration.md)的類別實例來註冊或刪除提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-142">Only administrators can register or delete a provider by creating instances of classes derived from **\_\_Win32Provider** or [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>
3.  <span data-ttu-id="2d4db-143">根據 [裝載模型](provider-hosting-and-security.md)中的值，在 **\_ \_ Win32Provider** 的實例中設定 [**HostingModel**](--win32provider.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d4db-143">Set the [**HostingModel**](--win32provider.md) in the instance of **\_\_Win32Provider** according to the values in [Hosting models](provider-hosting-and-security.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="2d4db-144">除非提供者需要 LocalSystem 帳戶的高許可權，否則 [**\_ \_ Win32Provider. HostingModel**](--win32provider.md)屬性應設定為 "NetworkServiceHost"。</span><span class="sxs-lookup"><span data-stu-id="2d4db-144">Unless the provider requires the high privileges of the LocalSystem account, the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property should be set to "NetworkServiceHost".</span></span> <span data-ttu-id="2d4db-145">如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-145">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

     

    <span data-ttu-id="2d4db-146">下列來自完整範例的 MOF 範例顯示建立 [**\_ \_ Win32Provider**](--win32provider.md)實例的程式碼。</span><span class="sxs-lookup"><span data-stu-id="2d4db-146">The following MOF example from the full example shows the code that creates an instance of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  <span data-ttu-id="2d4db-147">直接或間接衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)的類別實例，用來描述提供者的邏輯實作為。</span><span class="sxs-lookup"><span data-stu-id="2d4db-147">An instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), to describe the logical implementation of the provider.</span></span> <span data-ttu-id="2d4db-148">您可以針對數種不同類型的功能來註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-148">A provider can be registered for several different types of functionality.</span></span> <span data-ttu-id="2d4db-149">上述範例會將 RegProv 註冊為實例和方法提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-149">The example above registers RegProv as an instance and method provider.</span></span> <span data-ttu-id="2d4db-150">但是，如果 RegProv 支援此功能，也可以將它註冊為屬性或事件提供者。</span><span class="sxs-lookup"><span data-stu-id="2d4db-150">But if RegProv supports the functionality, it could also be registered as a property or event provider.</span></span> <span data-ttu-id="2d4db-151">下表列出註冊提供者功能的類別。</span><span class="sxs-lookup"><span data-stu-id="2d4db-151">The following table lists the classes that register provider functionality.</span></span>

    

    | <span data-ttu-id="2d4db-152">提供者註冊類別</span><span class="sxs-lookup"><span data-stu-id="2d4db-152">Provider registration classes</span></span>                                                        | <span data-ttu-id="2d4db-153">Description</span><span class="sxs-lookup"><span data-stu-id="2d4db-153">Description</span></span>                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [<span data-ttu-id="2d4db-154">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="2d4db-154">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)           | <span data-ttu-id="2d4db-155">註冊 [執行個體提供者](registering-an-instance-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-155">Registers an [instance provider](registering-an-instance-provider.md).</span></span>             |
    | [<span data-ttu-id="2d4db-156">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="2d4db-156">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)                 | <span data-ttu-id="2d4db-157">註冊 [事件提供者](registering-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-157">Registers an [event provider](registering-an-event-provider.md).</span></span>                   |
    | [<span data-ttu-id="2d4db-158">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="2d4db-158">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md) | <span data-ttu-id="2d4db-159">註冊 [事件取用者提供者](registering-an-event-consumer-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-159">Registers an [event consumer provider](registering-an-event-consumer-provider.md).</span></span> |
    | [<span data-ttu-id="2d4db-160">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="2d4db-160">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)               | <span data-ttu-id="2d4db-161">註冊 [方法提供者](registering-an-event-consumer-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-161">Registers a [method provider](registering-an-event-consumer-provider.md).</span></span>          |
    | [<span data-ttu-id="2d4db-162">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="2d4db-162">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)           | <span data-ttu-id="2d4db-163">註冊 [屬性提供者](registering-a-property-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4db-163">Registers a [property provider](registering-a-property-provider.md).</span></span>               |

    

     

5.  <span data-ttu-id="2d4db-164">將 MOF 檔案放入永久目錄。</span><span class="sxs-lookup"><span data-stu-id="2d4db-164">Place the MOF file into a permanent directory.</span></span>

    <span data-ttu-id="2d4db-165">一般而言，您應該將檔案放在提供者的安裝目錄中。</span><span class="sxs-lookup"><span data-stu-id="2d4db-165">Typically, you should place the file in the installation directory of the provider.</span></span>

6.  <span data-ttu-id="2d4db-166">使用 [mofcomp.exe](mofcomp.md) 或 [**IMOFCOMPILER**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 介面編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="2d4db-166">Compile the MOF file using [mofcomp](mofcomp.md) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="2d4db-167">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="2d4db-167">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

    <span data-ttu-id="2d4db-168">**Windows 8 和 Windows Server 2012：** 當安裝提供者時， [**mofcomp.exe**](mofcomp.md) 和 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 介面都會將 \[ 金鑰 \] 和 \[ 靜態 \] 限定詞視為 true （如果存在的話），而不論其實際值為何。</span><span class="sxs-lookup"><span data-stu-id="2d4db-168">**Windows 8 and Windows Server 2012:** When installing providers, both [**mofcomp**](mofcomp.md) and the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface treat the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="2d4db-169">如果有其他限定詞存在但未明確設定為 true，則會將它們視為 false。</span><span class="sxs-lookup"><span data-stu-id="2d4db-169">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d4db-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d4db-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d4db-171">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-171">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="2d4db-172">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="2d4db-172">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="2d4db-173">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="2d4db-173">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
