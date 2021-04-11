---
description: WDM (Windows Driver Model) 提供者會授與符合 WDM 模型的硬體驅動程式之類別、實例、方法和事件的存取權。
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: WDM 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691532"
---
# <a name="wdm-provider"></a><span data-ttu-id="ec02b-103">WDM 提供者</span><span class="sxs-lookup"><span data-stu-id="ec02b-103">WDM Provider</span></span>

<span data-ttu-id="ec02b-104">WDM (Windows Driver Model) 提供者會授與符合 WDM 模型的硬體驅動程式之類別、實例、方法和事件的存取權。</span><span class="sxs-lookup"><span data-stu-id="ec02b-104">The WDM (Windows Driver Model) provider grants access to the classes, instances, methods, and events of hardware drivers that conform to the WDM model.</span></span> <span data-ttu-id="ec02b-105">硬體驅動程式的類別位於「根 \\ wmi 命名空間」中。</span><span class="sxs-lookup"><span data-stu-id="ec02b-105">The classes for hardware drivers reside in the "root\\wmi namespace".</span></span>

<span data-ttu-id="ec02b-106">WDM 類別主要是在 Wmi 中定義。</span><span class="sxs-lookup"><span data-stu-id="ec02b-106">WDM classes are defined primarily in Wmi.mof.</span></span>

<span data-ttu-id="ec02b-107">WDM 是一種作業系統介面，可用來提供資訊和事件通知。</span><span class="sxs-lookup"><span data-stu-id="ec02b-107">WDM is an operating system interface through which hardware components provide information and event notification.</span></span> <span data-ttu-id="ec02b-108">WDM 提供者是一種類別、實例、事件和方法提供者，可讓管理應用程式從啟用 WMI 的裝置驅動程式存取資料和事件。</span><span class="sxs-lookup"><span data-stu-id="ec02b-108">The WDM provider is a class, instance, event, and method provider that allows management applications access to data and events from WMI-for-WDM enabled device drivers.</span></span> <span data-ttu-id="ec02b-109">WDM 提供者所建立用來代表設備磁碟機資料的類別，只位於「根 \\ WMI」命名空間中。</span><span class="sxs-lookup"><span data-stu-id="ec02b-109">The classes created by the WDM provider to represent device driver data reside only in the "Root\\WMI" namespace.</span></span> <span data-ttu-id="ec02b-110">在 WDM 提供者將處理已安裝的 WDM 驅動程式之前，這個命名空間必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="ec02b-110">This namespace must already exist before the WDM provider will process the installed WDM drivers.</span></span>

<span data-ttu-id="ec02b-111">WDM 提供者會在 WmiProv 檔案中記錄 WDM 作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ec02b-111">The WDM provider records information about WDM operations in the WmiProv.log file.</span></span> <span data-ttu-id="ec02b-112">如需詳細資訊，請參閱 [WMI 記錄](/windows/desktop/WmiSdk/wmi-log-files)檔。</span><span class="sxs-lookup"><span data-stu-id="ec02b-112">For more information, see [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span>

<span data-ttu-id="ec02b-113">針對類別、實例、方法和事件提供者，WDM 提供者會實作為標準 [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及下列 [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) 方法：</span><span class="sxs-lookup"><span data-stu-id="ec02b-113">As a class, instance, method, and event provider, the WDM provider implements the standard [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface, as well as the following [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="ec02b-114">**CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="ec02b-114">**CreateClassEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="ec02b-115">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="ec02b-115">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="ec02b-116">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="ec02b-116">**GetObjectAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="ec02b-117">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="ec02b-117">**ExecMethodAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="ec02b-118">**ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="ec02b-118">**ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="ec02b-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="ec02b-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="ec02b-120">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="ec02b-120">**PutInstanceAsync**</span></span>](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="ec02b-121">WDM 提供者支援 [**>register-wmievent**](/windows/desktop/WmiCoreProv/wmievent) 外建事件，此事件會通知 WMI 有關來自以 WDM 為基礎之驅動程式的事件。</span><span class="sxs-lookup"><span data-stu-id="ec02b-121">The WDM provider supports the [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) extrinsic event, which notifies WMI regarding events from WDM-based drivers.</span></span> <span data-ttu-id="ec02b-122">您可以註冊事件取用者來 **>register-wmievent** 事件，就像任何其他事件一樣。</span><span class="sxs-lookup"><span data-stu-id="ec02b-122">You can register your event consumers for **WMIEvent** events as you would any other event.</span></span> <span data-ttu-id="ec02b-123">如需詳細資訊，請參閱 [接收 WMI 事件](/windows/desktop/WmiSdk/receiving-a-wmi-event)。</span><span class="sxs-lookup"><span data-stu-id="ec02b-123">For more information, see [Receiving a WMI Event](/windows/desktop/WmiSdk/receiving-a-wmi-event).</span></span> <span data-ttu-id="ec02b-124">啟動驅動程式時，不會引發任何類別建立事件。</span><span class="sxs-lookup"><span data-stu-id="ec02b-124">No class creation events are raised when starting a driver.</span></span>

<span data-ttu-id="ec02b-125">WDM 提供者支援下列類別：</span><span class="sxs-lookup"><span data-stu-id="ec02b-125">The WDM provider supports the following class:</span></span>

-   [<span data-ttu-id="ec02b-126">**WMIBinaryMofResource**</span><span class="sxs-lookup"><span data-stu-id="ec02b-126">**WMIBinaryMofResource**</span></span>](wmibinarymofresource.md)

## <a name="related-topics"></a><span data-ttu-id="ec02b-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec02b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec02b-128">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="ec02b-128">WMI Providers</span></span>](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[<span data-ttu-id="ec02b-129">從設備磁碟機存取資料</span><span class="sxs-lookup"><span data-stu-id="ec02b-129">Accessing Data from Device Drivers</span></span>](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
