---
description: 當它安裝網路提供者時，您的應用程式應該建立登錄機碼，以及本主題中所述的值。
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: 驗證登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944464"
---
# <a name="authentication-registry-keys"></a><span data-ttu-id="3d0ce-103">驗證登錄機碼</span><span class="sxs-lookup"><span data-stu-id="3d0ce-103">Authentication Registry Keys</span></span>

<span data-ttu-id="3d0ce-104">當它安裝網路提供者時，您的應用程式應該建立登錄機碼，以及本主題中所述的值。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-104">When it installs a network provider, your application should create the registry keys and values described in this topic.</span></span> <span data-ttu-id="3d0ce-105">這些索引鍵和值提供有關系統上所安裝網路提供者的 MPR 資訊。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-105">These keys and values provide information to the MPR about the network providers installed on the system.</span></span> <span data-ttu-id="3d0ce-106">MPR 會在啟動時檢查這些金鑰，並載入其找到的網路提供者 Dll。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-106">The MPR checks these keys when it starts and loads the network provider DLLs that it finds.</span></span>

<span data-ttu-id="3d0ce-107">在您建立一組金鑰來保存網路提供者的相關資訊之前，您應該將網路提供者的名稱新增至 **訂單** 金鑰。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-107">Before you create a set of keys to hold information about your network provider, you should add the name of your network provider to the **order** key.</span></span> <span data-ttu-id="3d0ce-108">此金鑰是下列機碼的子機碼：</span><span class="sxs-lookup"><span data-stu-id="3d0ce-108">This key is a subkey of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

<span data-ttu-id="3d0ce-109">**Order** 索引鍵包含單一值 **ProviderOrder**，它會列出已安裝的提供者，並指定在作業期間，在提供者之間迴圈處理的順序，直到找到接受的提供者為止。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-109">The **order** key contains a single value, **ProviderOrder**, which lists the installed providers and specifies the order in which they should be tried during operations that cycle through providers until an accepting provider is found.</span></span>

<span data-ttu-id="3d0ce-110">**ProviderOrder** 值包含以逗號分隔的索引鍵名稱清單。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-110">The **ProviderOrder** value contains a comma-separated list of key names.</span></span> <span data-ttu-id="3d0ce-111">**ProviderOrder** 中的每個索引鍵名稱都會識別網路提供者。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-111">Each key name in **ProviderOrder** identifies a network provider.</span></span> <span data-ttu-id="3d0ce-112">當 MPR 迴圈處理提供者時，它會依其出現在這份清單中的順序來呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-112">When MPR cycles through the providers, it calls them in the order in which they appear in this list.</span></span>

<span data-ttu-id="3d0ce-113">您也應該在 **ProviderOrder** 中設定提供者名稱，作為包含該提供者相關資訊的登錄機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-113">The provider name set in **ProviderOrder** should also be used as the name of the registry key that contains information about that provider.</span></span> <span data-ttu-id="3d0ce-114">提供者特定的登錄機碼會建立為下列機碼的子機碼：</span><span class="sxs-lookup"><span data-stu-id="3d0ce-114">The provider-specific registry keys are created as subkeys of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="3d0ce-115">換句話說， **ProviderOrder** 中指定的提供者名稱是網路提供者特定金鑰登錄的路徑，相對於下列路徑：</span><span class="sxs-lookup"><span data-stu-id="3d0ce-115">In other words, the provider names specified in **ProviderOrder** are the path to the registry of the network provider-specific keys, relative to the following path:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="3d0ce-116">當您的網路提供者服務安裝完成時，安裝應用程式應新增金鑰，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3d0ce-116">When your network provider service is installed, the installation application should add a key as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

<span data-ttu-id="3d0ce-117">其中 *ProviderName* 是在 **order** 索引鍵的 **ProviderOrder** 值中所指定的網路提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-117">Where *ProviderName* is the name of the network provider as specified in the **ProviderOrder** value of the **order** key.</span></span> <span data-ttu-id="3d0ce-118">*ProviderName* 索引鍵下的 **群組** 值應該設定為 "NetworkProvider"。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-118">The **Group** value under the *ProviderName* key should be set to "NetworkProvider".</span></span> <span data-ttu-id="3d0ce-119">這會將服務識別為在網路提供者群組中。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-119">This identifies the service as being in the network provider group.</span></span>

<span data-ttu-id="3d0ce-120">您也必須建立 *ProviderName*、 **networkprovider** 的子機碼。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-120">You must also create a subkey of *ProviderName*, **networkprovider**.</span></span> <span data-ttu-id="3d0ce-121">此索引鍵包含描述網路提供者的下列值。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-121">This key contains the following values that describe the network provider.</span></span>



| <span data-ttu-id="3d0ce-122">值</span><span class="sxs-lookup"><span data-stu-id="3d0ce-122">Value</span></span>                       | <span data-ttu-id="3d0ce-123">描述</span><span class="sxs-lookup"><span data-stu-id="3d0ce-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d0ce-124">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-124">**Name**</span></span><br/>         | <span data-ttu-id="3d0ce-125">包含提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-125">Contains the name of the provider.</span></span> <span data-ttu-id="3d0ce-126">在 [流覽] 對話方塊中，使用者會看到此名稱做為網路的名稱，且應符合 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea)結構中傳回的 **lpProvider** 欄位。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-126">This name is displayed to the user as the name of the network in the browse dialog boxes and should match the **lpProvider** field returned in [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures.</span></span> <span data-ttu-id="3d0ce-127">這個名稱應該是產品名稱的一些變化，最好也要有公司的某些指示，讓它成為清楚且獨一無二的。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-127">This name should be some variation of the product name, preferably with some indication of the company as well, so that it is clear and unique.</span></span> <span data-ttu-id="3d0ce-128">例如，"MS-LanMan" 是不錯的名稱，而 "Net" 則是不佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-128">"MS-LanMan" for example is a good name, whereas "The Net" would be a poor choice.</span></span><br/> |
| <span data-ttu-id="3d0ce-129">**ProviderPath**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-129">**ProviderPath**</span></span><br/> | <span data-ttu-id="3d0ce-130">包含可執行網路提供者之 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-130">Contains the full path of the DLL that implements the network provider.</span></span> <span data-ttu-id="3d0ce-131">MPR 會在此路徑上呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-131">MPR calls [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) on this path.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="3d0ce-132">下列值僅供支援認證管理函式（ [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) 和 [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)）的網路提供者使用。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-132">The following values are used only by network providers that support the credential management functions, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span></span>



| <span data-ttu-id="3d0ce-133">值</span><span class="sxs-lookup"><span data-stu-id="3d0ce-133">Value</span></span>                              | <span data-ttu-id="3d0ce-134">描述</span><span class="sxs-lookup"><span data-stu-id="3d0ce-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d0ce-135">**類別**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-135">**Class**</span></span><br/>               | <span data-ttu-id="3d0ce-136">**DWORD** ，識別此提供者支援之提供者功能的類別或類型。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-136">A **DWORD** that identifies the class, or type, of provider functionality that this provider supports.</span></span> <span data-ttu-id="3d0ce-137">值可能會在適當時由 **OR** 運算子聯結。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-137">Values may be joined by the **OR** operator when appropriate.</span></span> <span data-ttu-id="3d0ce-138">此值的有效值為 WN \_ NETWORK \_ CLASS、WN \_ CREDENTIAL \_ class、WN \_ PRIMARY \_ AUTHENT \_ class 和 WN \_ SERVICE \_ 類別。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-138">Valid values for this are WN\_NETWORK\_CLASS, WN\_CREDENTIAL\_CLASS, WN\_PRIMARY\_AUTHENT\_CLASS, and WN\_SERVICE\_CLASS.</span></span><br/> <span data-ttu-id="3d0ce-139">雖然提供者可能支援主要驗證器功能，但另一種方法則是用來判斷哪個驗證器是主要的。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-139">Although a provider may support primary authenticator functionality, another means will be used to determine which authenticator is primary.</span></span><br/> <span data-ttu-id="3d0ce-140">**WINDOWS XP/2000：** 不支援切換主要驗證器，所以會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-140">**Windows XP/2000:** Switching primary authenticators is not supported, so this value is ignored.</span></span> <br/> |
| <span data-ttu-id="3d0ce-141">**AuthentProviderPath**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-141">**AuthentProviderPath**</span></span><br/> | <span data-ttu-id="3d0ce-142">這是匯出認證管理功能之 DLL 的完整檔案名。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-142">This is the fully qualified file name for the DLL that exports the Credential Management Functions.</span></span> <span data-ttu-id="3d0ce-143">此值很有用 (但只有在將提供者識別為認證 \_ 類別或主要 \_ AUTHENT \_ 類別提供者時，才需要) 。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-143">This value is useful (but not required) only when the provider is identified as being a CREDENTIAL\_CLASS or PRIMARY\_AUTHENT\_CLASS provider.</span></span> <span data-ttu-id="3d0ce-144">如果這個類別的提供者沒有這個值，則應該從 ProviderPath 值所識別的 DLL 匯出認證管理函式。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-144">If this value is not present for a provider of this class, the credential management functions are expected to be exported from the DLL identified by the ProviderPath value.</span></span> <span data-ttu-id="3d0ce-145">只有在需要將網路功能和認證管理員函式封裝在不同的 Dll 時，才會使用此值。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-145">This value is used only if it is desirable to package the network functions and the credential manager functions in separate DLLs.</span></span><br/>  |



 

<span data-ttu-id="3d0ce-146">除了用來註冊網路提供者和認證管理員的值之外，您還可以將值新增至登錄，以註冊 DLL 以接收連接通知。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-146">In addition to the values used to register network providers and credential managers, you can add a value to the registry to register a DLL to receive connection notifications.</span></span> <span data-ttu-id="3d0ce-147">若要這樣做，請在下列機碼底下建立 REG \_ EXPAND \_ SZ 值：</span><span class="sxs-lookup"><span data-stu-id="3d0ce-147">To do so, create a REG\_EXPAND\_SZ value under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

<span data-ttu-id="3d0ce-148">此值應指定可執行 [連接通知 API](connection-notification-api.md)之 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-148">This value should specify the path to a DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span> <span data-ttu-id="3d0ce-149">此值的名稱可以是任何您想要的名稱，前提是它不會與預先存在的值名稱衝突。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-149">The name of this value can be anything you want, as long as it does not conflict with preexisting value names.</span></span>

## <a name="example"></a><span data-ttu-id="3d0ce-150">範例</span><span class="sxs-lookup"><span data-stu-id="3d0ce-150">Example</span></span>

<span data-ttu-id="3d0ce-151">下列範例顯示安裝了兩個網路提供者的系統登錄機碼： LanmanWorkStation 和 AnotherNetSvc。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-151">The following example shows the registry keys for a system that has two network providers installed: LanmanWorkStation and AnotherNetSvc.</span></span> <span data-ttu-id="3d0ce-152">AnotherNetSvc 也是認證管理員。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-152">AnotherNetSvc is also a credential manager.</span></span> <span data-ttu-id="3d0ce-153">在此範例中，索引鍵名稱為粗體，而值名稱為斜體。</span><span class="sxs-lookup"><span data-stu-id="3d0ce-153">In the example, key names are bold and value names are italic.</span></span>

<span data-ttu-id="3d0ce-154">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **NetworkProvider** \\ **順序**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-154">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**order**</span></span>

<span data-ttu-id="3d0ce-155">*ProviderOrder* = "LanmanWorkStation，AnotherNetSvc"</span><span class="sxs-lookup"><span data-stu-id="3d0ce-155">*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"</span></span>

<span data-ttu-id="3d0ce-156">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **NetworkProvider** \\ **Notifyees**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-156">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="3d0ce-157">*MyNotifyApp* = "c： \\ connect \\connect.dll"</span><span class="sxs-lookup"><span data-stu-id="3d0ce-157">*MyNotifyApp* = "c:\\connect\\connect.dll"</span></span>

<span data-ttu-id="3d0ce-158">**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-158">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**</span></span>\\

<span data-ttu-id="3d0ce-159">*Group* = "NetworkProvider"</span><span class="sxs-lookup"><span data-stu-id="3d0ce-159">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="3d0ce-160">**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-160">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**\\**NetworkProvider**</span></span>

<span data-ttu-id="3d0ce-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span><span class="sxs-lookup"><span data-stu-id="3d0ce-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span></span>

<span data-ttu-id="3d0ce-162">*Class* = 0X00000001 (WN \_ NETWORK \_ 類別) </span><span class="sxs-lookup"><span data-stu-id="3d0ce-162">*Class* = 0x00000001 (WN\_NETWORK\_CLASS)</span></span>

<span data-ttu-id="3d0ce-163">**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-163">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**</span></span>\\

<span data-ttu-id="3d0ce-164">*Group* = "NetworkProvider"</span><span class="sxs-lookup"><span data-stu-id="3d0ce-164">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="3d0ce-165">**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="3d0ce-165">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**\\**NetworkProvider**</span></span>

<span data-ttu-id="3d0ce-166">*Name* = "其他網路"*ProviderPath* = "c： \\ 其他 \\anet.dll"</span><span class="sxs-lookup"><span data-stu-id="3d0ce-166">*Name* = "Another Network"*ProviderPath* = "c:\\another\\anet.dll"</span></span>

<span data-ttu-id="3d0ce-167">*Class* = 0X00000003 (WN \_ NETWORK \_ Class \| WN \_ CREDENTIAL \_ class) </span><span class="sxs-lookup"><span data-stu-id="3d0ce-167">*Class* = 0x00000003 (WN\_NETWORK\_CLASS \| WN\_CREDENTIAL\_CLASS)</span></span>

<span data-ttu-id="3d0ce-168">*AuthentProviderPath* = "c： \\ 其他 \\anetCM.dll"</span><span class="sxs-lookup"><span data-stu-id="3d0ce-168">*AuthentProviderPath* = "c:\\another\\anetCM.dll"</span></span>

 

