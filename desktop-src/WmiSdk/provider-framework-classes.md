---
description: 瞭解屬於 WMI 提供者架構的 WMI c + + 類別，現在會被視為最終狀態。
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: 提供者架構類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf4ef94b25e51b7f012987552babd30a93e7792
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120443"
---
# <a name="provider-framework-classes"></a><span data-ttu-id="3443e-103">提供者架構類別</span><span class="sxs-lookup"><span data-stu-id="3443e-103">Provider Framework Classes</span></span>

<span data-ttu-id="3443e-104">\[屬於 WMI 提供者架構一部分的 WMI c + + 類別現在會被視為最終狀態，而且不會有任何進一步的開發、增強功能或更新可用於影響這些程式庫的非安全性相關問題。</span><span class="sxs-lookup"><span data-stu-id="3443e-104">\[WMI C++ classes that are part of the WMI Provider Framework are are now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="3443e-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="3443e-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="3443e-106">提供者架構會實作為下列類別。</span><span class="sxs-lookup"><span data-stu-id="3443e-106">The provider framework implements the following classes.</span></span>



| <span data-ttu-id="3443e-107">Framework 類別</span><span class="sxs-lookup"><span data-stu-id="3443e-107">Framework class</span></span>                                | <span data-ttu-id="3443e-108">描述</span><span class="sxs-lookup"><span data-stu-id="3443e-108">Description</span></span>                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3443e-109">**CFrameworkQuery**</span><span class="sxs-lookup"><span data-stu-id="3443e-109">**CFrameworkQuery**</span></span>](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | <span data-ttu-id="3443e-110">包含查詢處理的方法。</span><span class="sxs-lookup"><span data-stu-id="3443e-110">Contains methods for query processing.</span></span>                                                                                                                                                                              |
| [<span data-ttu-id="3443e-111">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="3443e-111">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)                 | <span data-ttu-id="3443e-112">包含用來設定和取出屬性的方法，而且是 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 介面的封裝。</span><span class="sxs-lookup"><span data-stu-id="3443e-112">Contains methods to set and retrieve properties and is an encapsulation of the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span> <span data-ttu-id="3443e-113">實施者應該不需要直接存取 **IWbemClassObject** 方法。</span><span class="sxs-lookup"><span data-stu-id="3443e-113">Implementer should not have to access **IWbemClassObject** methods directly.</span></span> |
| [<span data-ttu-id="3443e-114">**CThreadBase**</span><span class="sxs-lookup"><span data-stu-id="3443e-114">**CThreadBase**</span></span>](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | <span data-ttu-id="3443e-115">提供 WMI 提供者架構內部執行緒安全機制的基類。</span><span class="sxs-lookup"><span data-stu-id="3443e-115">A base class that supplies the internal thread safety mechanisms for the WMI Provider Framework.</span></span>                                                                                                                    |
| [<span data-ttu-id="3443e-116">**CWbemGlueFactory**</span><span class="sxs-lookup"><span data-stu-id="3443e-116">**CWbemGlueFactory**</span></span>](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | <span data-ttu-id="3443e-117">WMI 提供者架構的一部分。</span><span class="sxs-lookup"><span data-stu-id="3443e-117">Part of the WMI Provider Framework.</span></span> <span data-ttu-id="3443e-118">提供者架構會在內部實作為此介面的方法，為提供者建立新的類別實例。</span><span class="sxs-lookup"><span data-stu-id="3443e-118">The Provider Framework implements methods of this interface internally to create new instances of classes for the provider.</span></span>                                                     |
| [<span data-ttu-id="3443e-119">**CWbemProviderGlue**</span><span class="sxs-lookup"><span data-stu-id="3443e-119">**CWbemProviderGlue**</span></span>](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | <span data-ttu-id="3443e-120">會實 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和方法，以控制架構提供者的載入和卸載。</span><span class="sxs-lookup"><span data-stu-id="3443e-120">Implements [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and methods that control the loading and unloading of the framework provider.</span></span>                                                                             |
| [<span data-ttu-id="3443e-121">**提供者**</span><span class="sxs-lookup"><span data-stu-id="3443e-121">**Provider**</span></span>](/windows/desktop/api/Provider/nl-provider-provider)                   | <span data-ttu-id="3443e-122">包含 helper 函式，並提供 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)方法的預設實作為。</span><span class="sxs-lookup"><span data-stu-id="3443e-122">Contains helper functions and provides default implementations of the methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>                                                                                            |



 

<span data-ttu-id="3443e-123">請注意，許多 framework 方法都使用 [**CHString**](chstring.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="3443e-123">Note that many of the framework methods use [**CHString**](chstring.md) parameters.</span></span> <span data-ttu-id="3443e-124">**CHString** 支援許多與 Microsoft Foundation 類別 (mfc) 相同的方法和屬性，但是不會有 mfc 的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="3443e-124">**CHString** supports many of the same methods and properties as the Microsoft Foundation Classes (MFC), but without the overhead of MFC.</span></span> <span data-ttu-id="3443e-125">如需 **CHString** 的詳細資訊，請參閱 **CHString 類別參考**。</span><span class="sxs-lookup"><span data-stu-id="3443e-125">For more information about **CHString**, see **CHString Class Reference**.</span></span>

 

 
