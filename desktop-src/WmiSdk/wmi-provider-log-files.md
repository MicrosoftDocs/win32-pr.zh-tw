---
description: WMI 提供者也可以維護記錄。 哪些記錄檔會出現在系統上，視安裝的提供者而定。
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: WMI 提供者記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b485c16c44ad5ac26c51db7551baa423ad1a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848609"
---
# <a name="wmi-provider-log-files"></a><span data-ttu-id="e78c0-104">WMI 提供者記錄檔</span><span class="sxs-lookup"><span data-stu-id="e78c0-104">WMI Provider Log Files</span></span>

<span data-ttu-id="e78c0-105">WMI 提供者也可以維護記錄。</span><span class="sxs-lookup"><span data-stu-id="e78c0-105">WMI providers also may maintain logs.</span></span> <span data-ttu-id="e78c0-106">哪些記錄檔會出現在系統上，視安裝的提供者而定。</span><span class="sxs-lookup"><span data-stu-id="e78c0-106">Which log files appear on a system depends on which providers are installed.</span></span>

<span data-ttu-id="e78c0-107">這些記錄檔可能位於% systemroot% \\ system32 \\ wbem 記錄檔 \\ 目錄中。</span><span class="sxs-lookup"><span data-stu-id="e78c0-107">These logs may be located in the %systemroot%\\system32\\wbem\\logs directory.</span></span>

-   [<span data-ttu-id="e78c0-108">Wmiprov .log</span><span class="sxs-lookup"><span data-stu-id="e78c0-108">Wmiprov.log</span></span>](#wmiprovlog)
-   [<span data-ttu-id="e78c0-109">Ntevt .log</span><span class="sxs-lookup"><span data-stu-id="e78c0-109">Ntevt.log</span></span>](#ntevtlog)
-   [<span data-ttu-id="e78c0-110">Dsprovider .log</span><span class="sxs-lookup"><span data-stu-id="e78c0-110">Dsprovider.log</span></span>](#dsproviderlog)
-   [<span data-ttu-id="e78c0-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e78c0-111">Related topics</span></span>](#related-topics)

## <a name="wmiprovlog"></a><span data-ttu-id="e78c0-112">Wmiprov .log</span><span class="sxs-lookup"><span data-stu-id="e78c0-112">Wmiprov.log</span></span>

<span data-ttu-id="e78c0-113">Wmiprov 檔案包含已啟用 WMI 的 Windows Driver Model (WDM) 驅動程式和 [Wdm 提供者](/windows/desktop/WmiCoreProv/wdm-provider)的管理資料和事件。</span><span class="sxs-lookup"><span data-stu-id="e78c0-113">The Wmiprov.log file contains management data and events from WMI-enabled Windows Driver Model (WDM) drivers and the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider).</span></span> <span data-ttu-id="e78c0-114">它會提供警告和錯誤資訊，主要用於疑難排解和偵測使用它的提供者和用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="e78c0-114">It supplies warning and error information primarily for troubleshooting and debugging the provider and client applications that use it.</span></span>

<span data-ttu-id="e78c0-115">Wmiprov 包含：</span><span class="sxs-lookup"><span data-stu-id="e78c0-115">The Wmiprov.log contains:</span></span>

-   <span data-ttu-id="e78c0-116">來自 [WDM 提供者](/windows/desktop/WmiCoreProv/wdm-provider) 或設備磁碟機的錯誤，例如二元 MOF 編譯失敗或無法取出資料。</span><span class="sxs-lookup"><span data-stu-id="e78c0-116">Errors from the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) or the device driver such as the binary MOF compile failing or failure to retrieve data.</span></span>
-   <span data-ttu-id="e78c0-117">針對每個使用 MOF 格式的驅動程式，MOF 的狀態會進行編譯。</span><span class="sxs-lookup"><span data-stu-id="e78c0-117">The status of the MOF compile for each of the drivers which use MOF format.</span></span>
-   <span data-ttu-id="e78c0-118">提供者結構和解構事件。</span><span class="sxs-lookup"><span data-stu-id="e78c0-118">Provider construction and deconstruction events.</span></span>
-   <span data-ttu-id="e78c0-119">WNODE 的列印。</span><span class="sxs-lookup"><span data-stu-id="e78c0-119">Printout of WNODE.</span></span>

## <a name="ntevtlog"></a><span data-ttu-id="e78c0-120">Ntevt .log</span><span class="sxs-lookup"><span data-stu-id="e78c0-120">Ntevt.log</span></span>

<span data-ttu-id="e78c0-121">Ntevt 檔案包含 [事件記錄提供者](/previous-versions/windows/desktop/eventlogprov/event-log-provider)的追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="e78c0-121">The Ntevt.log file contains trace messages from the [Event Log Provider](/previous-versions/windows/desktop/eventlogprov/event-log-provider).</span></span>

## <a name="dsproviderlog"></a><span data-ttu-id="e78c0-122">Dsprovider .log</span><span class="sxs-lookup"><span data-stu-id="e78c0-122">Dsprovider.log</span></span>

<span data-ttu-id="e78c0-123">Dsprovider 記錄檔包含 [Active Directory 提供者](/previous-versions/windows/desktop/dsprov/active-directory-provider)的追蹤資訊和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e78c0-123">The Dsprovider.log file contains trace information and error messages for the [Active Directory Provider](/previous-versions/windows/desktop/dsprov/active-directory-provider).</span></span>

<span data-ttu-id="e78c0-124">下表列出一些可能會發生的常見問題，並提供可能的原因和解決方案。</span><span class="sxs-lookup"><span data-stu-id="e78c0-124">The following table lists some common problems that can occur and offers possible causes and solutions.</span></span>



| <span data-ttu-id="e78c0-125">訊息</span><span class="sxs-lookup"><span data-stu-id="e78c0-125">Message</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="e78c0-126">描述</span><span class="sxs-lookup"><span data-stu-id="e78c0-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78c0-127">RootDSE 上的 CLDAPClassProvider：： InitializeLDAPProvider ADsGetObject 失敗： <hresult></span><span class="sxs-lookup"><span data-stu-id="e78c0-127">CLDAPClassProvider::InitializeLDAPProvider ADsGetObject on RootDSE FAILED : <hresult></span></span>                                                                                                                                                                                                                    | <span data-ttu-id="e78c0-128">嘗試取得目錄服務的根目錄時，ADSI 呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="e78c0-128">The ADSI call failed while trying to get the root of your directory services.</span></span> <span data-ttu-id="e78c0-129">確認您的電腦是網域的成員。</span><span class="sxs-lookup"><span data-stu-id="e78c0-129">Verify that your computer is a member of a domain.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e78c0-130">CDSClassProvider：： GetObjectAsync () GetClassFromCacheOrADSI 失敗 <class name><hresult></span><span class="sxs-lookup"><span data-stu-id="e78c0-130">CDSClassProvider::GetObjectAsync() GetClassFromCacheOrADSI FAILED for <class name> with <hresult></span></span>                                                                                                                                                                                                  | <span data-ttu-id="e78c0-131">您嘗試取得的類別不是目錄中的有效類別。</span><span class="sxs-lookup"><span data-stu-id="e78c0-131">The class you are trying to get is not a valid class in the directory.</span></span> <span data-ttu-id="e78c0-132">確認類別名稱是正確的。</span><span class="sxs-lookup"><span data-stu-id="e78c0-132">Verify that the class name is correct.</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="e78c0-133">CLDAPInstanceProvider：:P utInstanceAsync () ModifyExistingInstance 失敗，LDAP：//CN = foo1，CN = Users，DC = dsprovider，DC = nttest，DC = Microsoft，DC = com with <hresult></span><span class="sxs-lookup"><span data-stu-id="e78c0-133">CLDAPInstanceProvider::PutInstanceAsync() ModifyExistingInstance FAILED for LDAP://CN=foo1, CN=Users, DC=dsprovider,DC=nttest, DC=Microsoft, DC=com with <hresult></span></span>                                                                                                                                       | <span data-ttu-id="e78c0-134">提供者無法將修改過的實例寫入目錄服務。</span><span class="sxs-lookup"><span data-stu-id="e78c0-134">The provider was unable to write a modified instance to directory services.</span></span> <span data-ttu-id="e78c0-135">確定您使用的是 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 介面，以指定您要修改的屬性集。</span><span class="sxs-lookup"><span data-stu-id="e78c0-135">Ensure that you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface to specify the set of properties that you are modifying.</span></span> <span data-ttu-id="e78c0-136">如需有關如何搭配使用 **IWbemCoNtext** 介面和 [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))的詳細資訊，請參閱 [更新整個實例](updating-an-entire-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="e78c0-136">For more information about how to use the **IWbemContext** interface with [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long)), see [Updating an Entire Instance](updating-an-entire-instance.md).</span></span> |
| <span data-ttu-id="e78c0-137">CLDAPHelper：： GetADSIInstance ADsOpenObject <class name> () 在上失敗 <hresult></span><span class="sxs-lookup"><span data-stu-id="e78c0-137">CLDAPHelper::GetADSIInstance ADsOpenObject() FAILED on <class name> with <hresult></span></span><br/> <span data-ttu-id="e78c0-138">CLDAPInstanceProvider：： GetObjectAsync： GetADSIInstance () 失敗 <hresult></span><span class="sxs-lookup"><span data-stu-id="e78c0-138">CLDAPInstanceProvider::GetObjectAsync : GetADSIInstance() FAILED with <hresult></span></span><br/> <span data-ttu-id="e78c0-139">Ds 使用者的 CLDAPInstanceProvider：： GetObjectAsync () 失敗 \_ 。ADSIPath = "<class name></span><span class="sxs-lookup"><span data-stu-id="e78c0-139">CLDAPInstanceProvider::GetObjectAsync() FAILED for ds\_user.ADSIPath="<class name></span></span><br/> | <span data-ttu-id="e78c0-140">這三個訊息表示您嘗試取得的實例不存在於目錄服務中。</span><span class="sxs-lookup"><span data-stu-id="e78c0-140">These three messages indicate that the instance you are trying to get does not exist in the directory service.</span></span> <span data-ttu-id="e78c0-141">確認 **ADSIPath** 值和類別名稱正確無誤。</span><span class="sxs-lookup"><span data-stu-id="e78c0-141">Verify that the **ADSIPath** value and class name are correct.</span></span>                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="e78c0-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="e78c0-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e78c0-143">WMI 記錄檔</span><span class="sxs-lookup"><span data-stu-id="e78c0-143">WMI Log Files</span></span>](wmi-log-files.md)
</dt> </dl>

 

