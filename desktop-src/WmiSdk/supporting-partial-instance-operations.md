---
description: 提供者不需要支援任何部分實例作業。 但是，提供者必須支援部分實例作業的所有語義、處理完整的實例，或傳回 WBEM \_ E \_ 不支援的 \_ 參數。
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: 支援 Partial-Instance 作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf656688ffbcc6981c6a3e55dc480570ad0f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977237"
---
# <a name="supporting-partial-instance-operations"></a><span data-ttu-id="d57c5-104">支援 Partial-Instance 作業</span><span class="sxs-lookup"><span data-stu-id="d57c5-104">Supporting Partial-Instance Operations</span></span>

<span data-ttu-id="d57c5-105">提供者不需要支援任何部分實例作業。</span><span class="sxs-lookup"><span data-stu-id="d57c5-105">A provider is not required to support any partial-instance operations.</span></span> <span data-ttu-id="d57c5-106">但是，提供者必須支援部分實例作業的所有語義、處理完整的實例，或傳回 **WBEM \_ E \_ 不支援的 \_ 參數**。</span><span class="sxs-lookup"><span data-stu-id="d57c5-106">However, a provider must either support all the semantics of a partial-instance operation, process a complete instance, or return **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="d57c5-107">建立支援部分實例作業的提供者時，您必須遵守下列規則：</span><span class="sxs-lookup"><span data-stu-id="d57c5-107">When creating a provider that supports partial-instance operations, you must observe the following rules:</span></span>

-   <span data-ttu-id="d57c5-108">重複使用 WMI 傳送給提供者的相同內容物件。</span><span class="sxs-lookup"><span data-stu-id="d57c5-108">Reuse the same context object that WMI sends to the provider.</span></span> <span data-ttu-id="d57c5-109">WMI 會使用 \_ \_ \_ 名為 value 的 "GET EXT \_ CLIENT \_ REQUEST" 來防止鎖死，並移除此用戶端，然後再將內容物件轉送到提供者。</span><span class="sxs-lookup"><span data-stu-id="d57c5-109">WMI uses the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value to prevent deadlocks and removes this client before forwarding the context object to a provider.</span></span>
-   <span data-ttu-id="d57c5-110">針對不需要部分實例作業的重新進入 WMI，請務必傳回相同的內容物件，而不進行任何修改。</span><span class="sxs-lookup"><span data-stu-id="d57c5-110">For reentrant calls back into WMI that do not require a partial-instance operation, ensure to pass back the same context object without any modifications.</span></span> <span data-ttu-id="d57c5-111">WMI 會接收未 \_ \_ 設定 "GET \_ EXT \_ CLIENT REQUEST" 的內容物件 \_ ，並從內容物件中刪除所有與部分實例作業相關聯的已命名值，再將它傳遞給其他提供者。</span><span class="sxs-lookup"><span data-stu-id="d57c5-111">WMI receives the context object without the "\_\_GET\_EXT\_CLIENT\_REQUEST" named value set and deletes all named values associated with partial-instance operations from the context object before passing it to other providers.</span></span> <span data-ttu-id="d57c5-112">不變更內容物件會封鎖其他提供者接收針對不同、不相關的物件所使用的部分實例抓取作業。</span><span class="sxs-lookup"><span data-stu-id="d57c5-112">Not changing the context object blocks other providers from receiving partial-instance retrieval operations intended for a different, unrelated object.</span></span>
-   <span data-ttu-id="d57c5-113">若要在執行要求時執行可重新進入的部分實例作業，請將遺漏的「 \_ \_ 取得 \_ EXT \_ 用戶端 \_ 要求」命名為 value 和 property clear。</span><span class="sxs-lookup"><span data-stu-id="d57c5-113">To perform a reentrant partial-instance operation while carrying out a request, set the missing "\_\_GET\_EXT\_CLIENT\_REQUEST" named value and property clear.</span></span> <span data-ttu-id="d57c5-114">（選擇性）您可以在 \_ \_ \_ \_ 使用可重新進入的呼叫將內容物件傳送回 WMI 之前，修改 "GET EXT properties" 中的屬性（稱為值）。</span><span class="sxs-lookup"><span data-stu-id="d57c5-114">Optionally, you can modify the properties in the "\_\_GET\_EXT\_PROPERTIES" named value before sending the context object back into WMI with the reentrant call.</span></span>
-   <span data-ttu-id="d57c5-115">當您在重新進入呼叫期間將內容物件傳回 WMI 時，請勿存取該內容物件;其他提供者可能會在重新進入期間修改屬性清單或其他值。</span><span class="sxs-lookup"><span data-stu-id="d57c5-115">Do not access the context object after you return it to WMI during a reentrant call; other providers may modify the property lists or other values during reentrancy.</span></span> <span data-ttu-id="d57c5-116">您只可以在執行的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 呼叫期間檢查或修改內容物件。</span><span class="sxs-lookup"><span data-stu-id="d57c5-116">You can examine or modify the context object only for the duration of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call that you implement.</span></span>

 

 



