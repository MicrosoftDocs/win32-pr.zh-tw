---
description: 系統登錄包含作業系統、服務和應用程式所使用的設定資料。
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: 修改系統登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb274163999996267b5f1df62fb9352831763d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971986"
---
# <a name="modifying-the-system-registry"></a><span data-ttu-id="c191f-103">修改系統登錄</span><span class="sxs-lookup"><span data-stu-id="c191f-103">Modifying the System Registry</span></span>

<span data-ttu-id="c191f-104">系統登錄包含作業系統、服務和應用程式所使用的設定資料。</span><span class="sxs-lookup"><span data-stu-id="c191f-104">The system registry contains configuration data that the operating system, services, and applications use.</span></span> <span data-ttu-id="c191f-105">Windows Management Instrumentation (WMI) 具有 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 和 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 類別，其具有可用來監視或修改本機電腦或遠端電腦上登錄的方法。</span><span class="sxs-lookup"><span data-stu-id="c191f-105">Windows Management Instrumentation (WMI) has a [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) and the [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class with methods that use to monitor or modify the registry on the local computer or remote computers.</span></span> <span data-ttu-id="c191f-106">[Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)支援 [**win32 \_ 登錄類別**](/windows/desktop/CIMWin32Prov/win32-registry)，其中包含有關登錄大小的靜態資料。</span><span class="sxs-lookup"><span data-stu-id="c191f-106">The [Win32 Provider](/windows/desktop/CIMWin32Prov/win32-provider) supports the [**Win32\_Registry**](/windows/desktop/CIMWin32Prov/win32-registry) class that contains static data about the size of a registry.</span></span>

<span data-ttu-id="c191f-107">系統登錄提供者是與系統登錄介面互動的實例、屬性和事件提供者。</span><span class="sxs-lookup"><span data-stu-id="c191f-107">The System Registry Provider is an instance, property, and event provider that interfaces with the system registry.</span></span> <span data-ttu-id="c191f-108">System Registry Provider 是具有 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面的標準提供者。</span><span class="sxs-lookup"><span data-stu-id="c191f-108">The System Registry Provider is a standard provider with the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span> <span data-ttu-id="c191f-109">您可以使用系統登錄提供者來存取本機和遠端系統上的登錄機碼和資訊。</span><span class="sxs-lookup"><span data-stu-id="c191f-109">You can use the System Registry Provider to access registry keys and information on local and remote systems.</span></span> <span data-ttu-id="c191f-110">如需詳細資訊，請參閱 [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider)。</span><span class="sxs-lookup"><span data-stu-id="c191f-110">For more information, see [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).</span></span>

<span data-ttu-id="c191f-111">WMI 會將 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 放在根 \\ 預設命名空間中。</span><span class="sxs-lookup"><span data-stu-id="c191f-111">WMI places the [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) in the root\\default namespace.</span></span> <span data-ttu-id="c191f-112">不過，您可以將 Regevent 的 mof 檔案編譯成其他命名空間，以供其他應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="c191f-112">However, you can compile the Regevent.mof file into other namespaces for other applications to use.</span></span>

<span data-ttu-id="c191f-113">下表中所識別的主題可示範如何使用 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 類別和系統登錄提供者。</span><span class="sxs-lookup"><span data-stu-id="c191f-113">The topics identified in the following table can show you how to use the [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class and the System Registry Provider.</span></span>



| <span data-ttu-id="c191f-114">主題</span><span class="sxs-lookup"><span data-stu-id="c191f-114">Topic</span></span>                                                                                              | <span data-ttu-id="c191f-115">描述</span><span class="sxs-lookup"><span data-stu-id="c191f-115">Description</span></span>                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c191f-116">取得登錄資料</span><span class="sxs-lookup"><span data-stu-id="c191f-116">Obtaining Registry Data</span></span>](obtaining-registry-data.md)                                             | <span data-ttu-id="c191f-117">您可以透過 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 類別的方法取得或修改登錄資料，讓您可以在本機或遠端自動化登錄活動。</span><span class="sxs-lookup"><span data-stu-id="c191f-117">You can obtain or modify registry data through methods of the [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class, which allows you to automate registry activities locally or remotely.</span></span>                    |
| [<span data-ttu-id="c191f-118">變更登錄資料</span><span class="sxs-lookup"><span data-stu-id="c191f-118">Changing Registry Data</span></span>](changing-registry-data.md)                                               | <span data-ttu-id="c191f-119">您可以新增或刪除金鑰，以及新增或變更機碼下的登錄專案值。</span><span class="sxs-lookup"><span data-stu-id="c191f-119">You can add or delete keys, and add or change registry entry values under keys.</span></span>                                                                                                                    |
| [<span data-ttu-id="c191f-120">使用系統登錄提供者進行程式設計</span><span class="sxs-lookup"><span data-stu-id="c191f-120">Programming with the System Registry Provider</span></span>](programming-with-the-system-registry-provider.md) | <span data-ttu-id="c191f-121">您可以定義您自己的類別，讓系統登錄提供資料。</span><span class="sxs-lookup"><span data-stu-id="c191f-121">You can define your own classes that the System Registry supplies with data.</span></span>                                                                                                                       |
| [<span data-ttu-id="c191f-122">註冊系統登錄事件</span><span class="sxs-lookup"><span data-stu-id="c191f-122">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)               | <span data-ttu-id="c191f-123">System Registry provider 可將事件傳送給取用者。</span><span class="sxs-lookup"><span data-stu-id="c191f-123">The System Registry provider can send events to a consumer.</span></span> <span data-ttu-id="c191f-124">若要接收事件，您必須註冊您的取用者、建立查詢，然後確保提供者會正確地傳送事件給您。</span><span class="sxs-lookup"><span data-stu-id="c191f-124">To receive events, you must register your consumer, create a query, and then ensure that the provider is sending you events—correctly.</span></span> |
| [<span data-ttu-id="c191f-125">註冊系統登錄提供者</span><span class="sxs-lookup"><span data-stu-id="c191f-125">Registering the System Registry Provider</span></span>](registering-the-system-registry-provider.md)           | <span data-ttu-id="c191f-126">System Registry provider 會註冊為 WMI 安裝程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="c191f-126">The System Registry provider is registered as part of the WMI installation process.</span></span>                                                                                                                |



 

 

 
