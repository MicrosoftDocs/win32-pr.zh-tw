---
description: 針對32位作業系統撰寫的腳本和應用程式應該會繼續正常執行。
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: 在64位平臺上提供 WMI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512492"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="8e895-103">在64位平臺上提供 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="8e895-103">Providing WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="8e895-104">針對32位作業系統撰寫的腳本和應用程式應該會繼續正常執行。</span><span class="sxs-lookup"><span data-stu-id="8e895-104">Scripts and applications written for 32-bit operating systems should continue to run properly.</span></span> <span data-ttu-id="8e895-105">如果您有現有的32位提供者，您可以評估是否需要撰寫適用于並存作業的64位版本。</span><span class="sxs-lookup"><span data-stu-id="8e895-105">If you have an existing 32-bit provider, you can evaluate whether you need to write a 64-bit version for side-by-side operation.</span></span> <span data-ttu-id="8e895-106">一般而言，這兩個版本都不是必要的，而且64位版本可以同時為32位和64位本機或遠端用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="8e895-106">Generally, both versions are not necessary and the 64-bit version can service both 32-bit and 64-bit local or remote clients.</span></span> <span data-ttu-id="8e895-107">不過，若為32位應用程式相容性模式，請在以32位 WOW64 模式執行的64位系統上，使用現有的32位 WMI 提供者。</span><span class="sxs-lookup"><span data-stu-id="8e895-107">However, for 32-bit application compatibility mode, use your existing 32-bit WMI provider on a 64-bit system that runs in the 32-bit WOW64 mode.</span></span>

<span data-ttu-id="8e895-108">在罕見的情況下，32位和64位提供者必須並行在64位系統上執行。</span><span class="sxs-lookup"><span data-stu-id="8e895-108">In rare situations, both the 32-bit and 64-bit providers must run side-by-side on 64-bit systems.</span></span> <span data-ttu-id="8e895-109">在此情況下，所載入的適當提供者版本取決於呼叫端為32位或64位，以及本機或遠端。</span><span class="sxs-lookup"><span data-stu-id="8e895-109">In this case, the appropriate version of provider that is loaded depends on whether the caller is 32-bit or 64-bit and local or remote.</span></span> <span data-ttu-id="8e895-110">使用連線物件內容旗標（ **\_ \_ microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 和 **\_ \_ RequiredArchitecture**）的呼叫端可以要求 WMI 載入非預設的提供者。</span><span class="sxs-lookup"><span data-stu-id="8e895-110">A caller using the connection object context flags, **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture**, can request that WMI load a nondefault provider.</span></span> <span data-ttu-id="8e895-111">如需詳細資訊，請參閱 [在64位電腦上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="8e895-111">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="8e895-112">在不尋常的情況下，您必須並存執行32位和64位提供者，您必須確定已謹慎處理安裝和卸載案例。</span><span class="sxs-lookup"><span data-stu-id="8e895-112">In the unusual case that you must run both the 32-bit and 64-bit providers side-by-side, then you must ensure that install and uninstall scenarios are handled carefully.</span></span> <span data-ttu-id="8e895-113">這是因為 WMI 只有一個存放 [*庫*](gloss-w.md) ，而且32位和64位版本的 [**mofcomp.exe**](mofcomp.md) 將資料放在相同的存放庫中;32位或64位的 mof 檔案沒有任何差別。</span><span class="sxs-lookup"><span data-stu-id="8e895-113">This is because WMI has only one [*repository*](gloss-w.md) and both the 32-bit and 64-bit versions of [**mofcomp.exe**](mofcomp.md) put the data in the same repository; there is no distinction between a 32-bit or a 64-bit .mof file.</span></span> <span data-ttu-id="8e895-114">重新安裝一個版本的提供者將不會造成損害：將會編譯 mof 檔案，並將類別儲存在存放庫中。</span><span class="sxs-lookup"><span data-stu-id="8e895-114">Reinstalling one version of the provider will not hurt: the .mof files will be compiled and the classes stored in the repository.</span></span> <span data-ttu-id="8e895-115">不過，刪除命名空間的第二個卸載可能會干擾其他提供者的作業。</span><span class="sxs-lookup"><span data-stu-id="8e895-115">However, a second uninstall that deletes a namespace can interfere with the operation of the other provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e895-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e895-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e895-117">在64位電腦上取得和提供資料</span><span class="sxs-lookup"><span data-stu-id="8e895-117">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[<span data-ttu-id="8e895-118">在64位平臺上要求 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="8e895-118">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="8e895-119">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="8e895-119">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> </dl>

 

 



