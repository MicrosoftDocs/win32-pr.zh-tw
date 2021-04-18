---
description: 離線登錄庫是用來修改作用中系統登錄外部的登錄 hive。
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: 關於離線登錄庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e08b401a4a77f55a54c48ad147bf38c8796472
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468013"
---
# <a name="about-the-offline-registry-library"></a><span data-ttu-id="f2c62-103">關於離線登錄庫</span><span class="sxs-lookup"><span data-stu-id="f2c62-103">About the Offline Registry Library</span></span>

<span data-ttu-id="f2c62-104">離線登錄庫是用來修改作用中系統登錄外部的登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="f2c62-104">The offline registry library is used to modify a registry hive outside of the active system registry.</span></span>

<span data-ttu-id="f2c62-105">離線登錄庫適用于登錄更新案例，例如服務作業系統映射。</span><span class="sxs-lookup"><span data-stu-id="f2c62-105">The offline registry library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="f2c62-106">離線登錄函式提供標準登錄功能無法使用的下列功能：</span><span class="sxs-lookup"><span data-stu-id="f2c62-106">The offline registry functions provide the following capabilities that are not available with the standard registry functions:</span></span>

-   <span data-ttu-id="f2c62-107">離線登錄功能可以用來修改任何支援的登錄格式的登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="f2c62-107">The offline registry functions can be used to modify a registry hive in any supported registry format.</span></span> <span data-ttu-id="f2c62-108">標準登錄函式只能變更作用中的登錄區，而變更必須與系統上執行的 Windows 版本相容。</span><span class="sxs-lookup"><span data-stu-id="f2c62-108">The standard registry functions can make changes only to an active registry hive and the changes must be compatible with the version of Windows running on the system.</span></span>
-   <span data-ttu-id="f2c62-109">離線登錄庫只需要讀取權限，即可開啟登錄 hive 檔案和寫入存取權來儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="f2c62-109">The offline registry library requires only read access to open a registry hive file and write access to save the file.</span></span> <span data-ttu-id="f2c62-110">系統不會對 hive 中的物件執行其他存取檢查，因此可以使用標準使用者權限來修改 hive。</span><span class="sxs-lookup"><span data-stu-id="f2c62-110">No other access checks are performed on objects in the hive, making it possible to modify the hive with standard user privileges.</span></span> <span data-ttu-id="f2c62-111">使用標準登錄功能時，將 hive 載入 active registry 是需要系統管理存取權的特殊許可權作業。</span><span class="sxs-lookup"><span data-stu-id="f2c62-111">With the standard registry functions, loading a hive into the active registry is a privileged operation that requires administrative access.</span></span>

<span data-ttu-id="f2c62-112">離線登錄功能不應該用來代替系統登錄功能，原因如下：</span><span class="sxs-lookup"><span data-stu-id="f2c62-112">The offline registry functions should not be used as a substitute for the system registry functions for the following reasons:</span></span>

-   <span data-ttu-id="f2c62-113">使用離線登錄功能時，無法在進程之間共用登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="f2c62-113">It is impossible to share registry hives between processes using the offline registry functions.</span></span>
-   <span data-ttu-id="f2c62-114">離線登錄函式使用簡單的鎖定，可能會對多執行緒應用程式造成嚴重的效能降低。</span><span class="sxs-lookup"><span data-stu-id="f2c62-114">The offline registry functions use simple locking that can lead to serious performance degradation for multithreaded applications.</span></span>
-   <span data-ttu-id="f2c62-115">在呼叫 [**ORSaveHive**](orsavehive.md) 函式之前，不會儲存離線登錄功能所做的變更。</span><span class="sxs-lookup"><span data-stu-id="f2c62-115">Changes made with the offline registry functions are not saved until the [**ORSaveHive**](orsavehive.md) function is called.</span></span>

<span data-ttu-id="f2c62-116">應用程式不應該使用離線登錄功能來略過系統登錄的安全性需求。</span><span class="sxs-lookup"><span data-stu-id="f2c62-116">Applications should not use the offline registry functions to bypass the security requirements of the system registry.</span></span> <span data-ttu-id="f2c62-117">若要載入 hive，在沒有 [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) 函式所需特殊許可權的情況下執行的應用程式可以使用 [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) 函數。</span><span class="sxs-lookup"><span data-stu-id="f2c62-117">To load a hive, an application running without the special privileges required by the [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) function can use the [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) function.</span></span>

<span data-ttu-id="f2c62-118">**Windows Server 2003 和 WINDOWS XP：** 不支援 [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) 函數。</span><span class="sxs-lookup"><span data-stu-id="f2c62-118">**Windows Server 2003 and Windows XP:** The [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) function is not supported.</span></span>

<span data-ttu-id="f2c62-119">*離線登錄 hive* 是已使用離線登錄功能載入至記憶體的登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="f2c62-119">An *offline registry hive* is a registry hive that has been loaded into memory using the offline registry functions.</span></span> <span data-ttu-id="f2c62-120">若要建立空白的離線登錄 hive，請使用 [**ORCreateHive**](orcreatehive.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="f2c62-120">To create an empty offline registry hive, use the [**ORCreateHive**](orcreatehive.md) function.</span></span> <span data-ttu-id="f2c62-121">若要修改現有的登錄區，請使用 [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) 或 [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) 函式，將 hive 從 active system 登錄儲存至檔案，然後使用 [**OROpenHive**](oropenhive.md) 函數來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="f2c62-121">To modify an existing registry hive, use the [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) or [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) function to save a hive from the active system registry to a file, and then use the [**OROpenHive**](oropenhive.md) function to open the file.</span></span>

<span data-ttu-id="f2c62-122">[**ORCreateHive**](orcreatehive.md)和 [**OROpenHive**](oropenhive.md)函式會將控制碼傳回給離線登錄區的根機碼。</span><span class="sxs-lookup"><span data-stu-id="f2c62-122">The [**ORCreateHive**](orcreatehive.md) and [**OROpenHive**](oropenhive.md) functions return a handle to the root key of the offline registry hive.</span></span> <span data-ttu-id="f2c62-123">這個控制碼可作為離線登錄區中任何其他金鑰的控制碼，但有下列例外狀況： [**ORCreateKey**](orcreatekey.md) 和 [**OROpenKey**](oropenkey.md) 函式不能用來傳回根金鑰的控制碼; [**ORCloseKey**](orclosekey.md) 函式不能用來關閉根金鑰;而且 [**ORDeleteKey**](ordeletekey.md) 函式無法用來刪除根金鑰。</span><span class="sxs-lookup"><span data-stu-id="f2c62-123">This handle can be used like a handle to any other key in the offline registry hive with the following exceptions: the [**ORCreateKey**](orcreatekey.md) and [**OROpenKey**](oropenkey.md) functions cannot be used to return a handle to the root key; the [**ORCloseKey**](orclosekey.md) function cannot be used to close the root key; and the [**ORDeleteKey**](ordeletekey.md) function cannot be used to delete the root key.</span></span> <span data-ttu-id="f2c62-124">在上述所有情況下，此函式會失敗，並出現 **錯誤 \_ \_ 參數無效**。</span><span class="sxs-lookup"><span data-stu-id="f2c62-124">In all of these cases, the function fails with **ERROR\_INVALID\_PARAMETER**.</span></span>

<span data-ttu-id="f2c62-125">您可以使用 [**ORCreateKey**](orcreatekey.md) 函式，將金鑰新增至開啟的離線登錄 hive，並使用 [**ORSetValue**](orsetvalue.md) 函式來設定索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="f2c62-125">Use the [**ORCreateKey**](orcreatekey.md) function to add keys to an open offline registry hive and the [**ORSetValue**](orsetvalue.md) function to set the keys' values.</span></span> <span data-ttu-id="f2c62-126">離線登錄庫支援其他基本登錄作業，例如列舉、取出和刪除機碼和值，以及設定索引鍵屬性，例如安全性和虛擬化行為。</span><span class="sxs-lookup"><span data-stu-id="f2c62-126">The offline registry library supports other basic registry operations such as enumerating, retrieving, and deleting keys and values, and setting key attributes such as security and virtualization behavior.</span></span> <span data-ttu-id="f2c62-127">如需函式的清單，請參閱離線登錄連結 [庫函數](offline-registry-library-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="f2c62-127">For a list of functions, see [Offline Registry Library Functions](offline-registry-library-functions.md).</span></span>

<span data-ttu-id="f2c62-128">若要儲存對開啟離線登錄區的變更，請使用 [**ORSaveHive**](orsavehive.md) 函式將 hive 儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="f2c62-128">To save changes made to an open offline registry hive, use the [**ORSaveHive**](orsavehive.md) function to save the hive to a file.</span></span> <span data-ttu-id="f2c62-129"> (除非呼叫 **ORSaveHive** ，否則不會保存變更。 ) 儲存 hive 之後，請使用 [**ORCloseHive**](orclosehive.md) 函式來關閉 hive 和與其相關聯的可用資源。</span><span class="sxs-lookup"><span data-stu-id="f2c62-129">(The changes do not persist unless **ORSaveHive** is called.) After saving the hive, use the [**ORCloseHive**](orclosehive.md) function to close the hive and free resources associated with it.</span></span>

<span data-ttu-id="f2c62-130">只有在使用 [**OROpenHive**](oropenhive.md) 函式開啟離線登錄 hive 時，才會進行驗證。</span><span class="sxs-lookup"><span data-stu-id="f2c62-130">An offline registry hive is validated only when it is opened using the [**OROpenHive**](oropenhive.md) function.</span></span> <span data-ttu-id="f2c62-131">如果 hive 損毀，作業就會失敗;不嘗試修復 hive。</span><span class="sxs-lookup"><span data-stu-id="f2c62-131">If the hive is corrupt, the operation simply fails; no attempt is made to repair the hive.</span></span> <span data-ttu-id="f2c62-132">在使用 [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) 函式將 hive 載入至作用中登錄之前，不會執行 hive 中物件的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="f2c62-132">Access checks on objects in the hive are not performed until the hive is loaded into an active registry with the [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) function.</span></span>

<span data-ttu-id="f2c62-133">離線登錄功能不支援 [預先定義的金鑰](../sysinfo/predefined-keys.md)。</span><span class="sxs-lookup"><span data-stu-id="f2c62-133">The offline registry functions do not support the [predefined keys](../sysinfo/predefined-keys.md).</span></span>

<span data-ttu-id="f2c62-134">傳遞至離線登錄函式的所有索引鍵和值名稱字串都必須是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="f2c62-134">All key and value name strings passed to offline registry functions must be Unicode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2c62-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2c62-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2c62-136">離線登錄庫 \_ 函數</span><span class="sxs-lookup"><span data-stu-id="f2c62-136">Offline Registry Library\_Functions</span></span>](offline-registry-library-functions.md)
</dt> </dl>

 

 
