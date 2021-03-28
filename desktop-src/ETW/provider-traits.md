---
description: 提供者特性是將更多資料附加至個別提供者註冊的方法。
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: 提供者特性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973569"
---
# <a name="provider-traits"></a><span data-ttu-id="49c06-103">提供者特性</span><span class="sxs-lookup"><span data-stu-id="49c06-103">Provider Traits</span></span>

<span data-ttu-id="49c06-104">提供者特性是將更多資料附加至個別提供者註冊的方法。</span><span class="sxs-lookup"><span data-stu-id="49c06-104">Provider Traits are a method of attaching more data to an individual provider registration.</span></span> <span data-ttu-id="49c06-105">它們可用於以資訊清單為基礎或 TraceLogging 的提供者。</span><span class="sxs-lookup"><span data-stu-id="49c06-105">They can be used for manifest-based or TraceLogging providers.</span></span> <span data-ttu-id="49c06-106">目前支援將提供者名稱和/或提供者群組新增至個別提供者註冊。</span><span class="sxs-lookup"><span data-stu-id="49c06-106">This currently includes support for adding a Provider Name and/or Provider Group to an individual provider registration.</span></span> <span data-ttu-id="49c06-107">未來可能會加入更多特性類型。</span><span class="sxs-lookup"><span data-stu-id="49c06-107">More trait types are likely to be added in the future.</span></span> <span data-ttu-id="49c06-108">這項資訊會以集合格式的二進位 blob 形式儲存在核心中。</span><span class="sxs-lookup"><span data-stu-id="49c06-108">This information is stored in the kernel as a binary blob of a set format.</span></span>

<span data-ttu-id="49c06-109">您只能針對註冊設定一次特性。</span><span class="sxs-lookup"><span data-stu-id="49c06-109">Traits can only be set once for a registration.</span></span> <span data-ttu-id="49c06-110">任何進一步嘗試在該註冊上設定特性的嘗試都會失敗。</span><span class="sxs-lookup"><span data-stu-id="49c06-110">Any further attempts to set the traits on that registration will fail.</span></span>

<span data-ttu-id="49c06-111">若要在以資訊清單為基礎的提供者上設定提供者特性，請使用 EventProviderSetTraits 資訊類別呼叫 [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) 函數。</span><span class="sxs-lookup"><span data-stu-id="49c06-111">To set Provider Traits on a manifest-based provider, call the [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) function with the EventProviderSetTraits information class.</span></span> <span data-ttu-id="49c06-112">EventInformation 緩衝區應包含下列格式的二進位 blob：</span><span class="sxs-lookup"><span data-stu-id="49c06-112">The EventInformation buffer should contain a binary blob of the following format:</span></span>

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

<span data-ttu-id="49c06-113">個別的特性應該採用下列格式：</span><span class="sxs-lookup"><span data-stu-id="49c06-113">Individual traits should be in the following format:</span></span>

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

<span data-ttu-id="49c06-114">從個別的特性，ETW \_ 提供者特性 \_ \_ 類型定義如下：</span><span class="sxs-lookup"><span data-stu-id="49c06-114">From the individual trait, ETW\_PROVIDER\_TRAIT\_TYPE is defined as:</span></span>

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

<span data-ttu-id="49c06-115">呼叫 [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) 函數時，TraceLogging 提供者會自動設定提供者特徵。</span><span class="sxs-lookup"><span data-stu-id="49c06-115">TraceLogging providers automatically set the Provider Traits when the [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) function is called.</span></span> <span data-ttu-id="49c06-116">TraceLogging 提供者的名稱一律會包含在其特性中。</span><span class="sxs-lookup"><span data-stu-id="49c06-116">The TraceLogging provider's name will always be included in its traits.</span></span> <span data-ttu-id="49c06-117">您可以在提供者定義中使用 [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) 宏，在 TraceLogging 提供者上設定群組。</span><span class="sxs-lookup"><span data-stu-id="49c06-117">A group can be set on a TraceLogging provider using the [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) macro in the provider definition.</span></span>

## <a name="custom-traits"></a><span data-ttu-id="49c06-118">自訂特性</span><span class="sxs-lookup"><span data-stu-id="49c06-118">Custom Traits</span></span>

<span data-ttu-id="49c06-119">雖然可能尚未定義大部分的255可能特性類型，但特性類型1-127 是由 Microsoft 所保留供定義。</span><span class="sxs-lookup"><span data-stu-id="49c06-119">Although most of the 255 possible trait types are not yet defined, trait types 1-127 are reserved for definition by Microsoft.</span></span> <span data-ttu-id="49c06-120">其餘較高的索引類型值可供外部開發人員使用，如其所見。</span><span class="sxs-lookup"><span data-stu-id="49c06-120">The remaining higher indexed type values can be used by external developers as they see fit.</span></span> <span data-ttu-id="49c06-121">考慮將自己的自訂特性新增至提供者的任何人，都應該嘗試將其特徵大小總計保持在256個位元組以下，原因如下：</span><span class="sxs-lookup"><span data-stu-id="49c06-121">Anyone considering adding their own custom traits to their provider should try to keep their total trait size under 256 bytes for the following reasons:</span></span>

-   <span data-ttu-id="49c06-122">這些特性會包含在針對提供者所撰寫的每個事件中。</span><span class="sxs-lookup"><span data-stu-id="49c06-122">The traits are included in every event written for the provider.</span></span> <span data-ttu-id="49c06-123">大型特性可能會導致大量記錄檔。</span><span class="sxs-lookup"><span data-stu-id="49c06-123">Large traits could lead to very large log files.</span></span>
-   <span data-ttu-id="49c06-124">在提供者的存留期內，特性會儲存在非分頁核心集區中。</span><span class="sxs-lookup"><span data-stu-id="49c06-124">The traits are stored in nonpaged kernel pool for the lifetime of the provider.</span></span>

## <a name="provider-groups"></a><span data-ttu-id="49c06-125">提供者群組</span><span class="sxs-lookup"><span data-stu-id="49c06-125">Provider Groups</span></span>

<span data-ttu-id="49c06-126">提供者群組是 GUID 定義的可控制實體，與提供者本身很類似。</span><span class="sxs-lookup"><span data-stu-id="49c06-126">A provider group is a GUID-defined controllable entity much like a provider itself.</span></span> <span data-ttu-id="49c06-127">主要差異在於，雖然提供者 GUID 只會用來控制其提供者的註冊，但群組將會控制其所有成員註冊。</span><span class="sxs-lookup"><span data-stu-id="49c06-127">The key difference is that while a provider GUID is used to control registrations of just its provider, a group will control all of its member registrations.</span></span> <span data-ttu-id="49c06-128">例如，啟用具有指定關鍵字和層級的提供者群組，將會啟用所有群組成員註冊與該關鍵字和層級。</span><span class="sxs-lookup"><span data-stu-id="49c06-128">For example, enabling a provider group with a given keyword and level will enable all of the groups member registrations with that keyword and level.</span></span>

<span data-ttu-id="49c06-129">群組成員資格可能會受到許可權限制。</span><span class="sxs-lookup"><span data-stu-id="49c06-129">Group membership may be restricted by permissions.</span></span> <span data-ttu-id="49c06-130">如果 [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) 的呼叫端沒有加入指定群組的許可權，則會拒絕成員資格。</span><span class="sxs-lookup"><span data-stu-id="49c06-130">If the caller of [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) doesn't have permissions to join the specified group, then membership will be denied.</span></span>

<span data-ttu-id="49c06-131">在某些情況下，追蹤會話控制器可能會想要從其啟用群組中排除幾個提供者。</span><span class="sxs-lookup"><span data-stu-id="49c06-131">In some cases the trace session controller may want to exclude a few providers from its enable of a group.</span></span> <span data-ttu-id="49c06-132">這可以藉由設定不允許的清單來完成。</span><span class="sxs-lookup"><span data-stu-id="49c06-132">This can be done by setting a disallow list.</span></span> <span data-ttu-id="49c06-133">不允許的清單是提供者 Guid 清單，將不會根據單一記錄會話的群組設定來啟用。</span><span class="sxs-lookup"><span data-stu-id="49c06-133">A disallow list is a list of provider GUIDs that will not be enabled based on the group settings for a single logging session.</span></span> <span data-ttu-id="49c06-134">您可以使用 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 和 TraceSetDisallowList 資訊類別，動態變更不允許的清單。</span><span class="sxs-lookup"><span data-stu-id="49c06-134">Disallow lists can be changed dynamically with [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) and the TraceSetDisallowList information class.</span></span>

<span data-ttu-id="49c06-135">雖然可以針對個別提供者以類似的方式針對提供者群組進行大部分的啟用動作，但還是有一些例外狀況。</span><span class="sxs-lookup"><span data-stu-id="49c06-135">While most enable actions can be done for Provider Groups in a similar manner to individual providers, there are some exceptions.</span></span> <span data-ttu-id="49c06-136">例外狀況包括：</span><span class="sxs-lookup"><span data-stu-id="49c06-136">Exceptions include:</span></span>

-   <span data-ttu-id="49c06-137">私用追蹤會話無法控制提供者群組。</span><span class="sxs-lookup"><span data-stu-id="49c06-137">Provider Groups cannot be controlled by private trace sessions.</span></span>
-   <span data-ttu-id="49c06-138">當提供者群組採用個別提供者的特定資訊時，事件名稱、事件識別碼和裝載篩選器並不適用。</span><span class="sxs-lookup"><span data-stu-id="49c06-138">Event Name, Event ID, and Payload filters are not applicable to Provider Groups as they assume specific information of an individual provider.</span></span>

 

 
