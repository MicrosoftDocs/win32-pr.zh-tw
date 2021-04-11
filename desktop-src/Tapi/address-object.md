---
description: Address 物件代表可以進行或接收呼叫的實體。
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Address 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850499"
---
# <a name="address-object"></a><span data-ttu-id="8c2bb-103">Address 物件</span><span class="sxs-lookup"><span data-stu-id="8c2bb-103">Address Object</span></span>

<span data-ttu-id="8c2bb-104">Address 物件代表可以進行或接收呼叫的實體。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-104">The Address object represents an entity that can make or receive calls.</span></span> <span data-ttu-id="8c2bb-105">此物件會公開介面和方法，以允許應用程式執行一些作業，例如：</span><span class="sxs-lookup"><span data-stu-id="8c2bb-105">This object exposes interfaces and methods that allow an application to perform a number of operations, such as:</span></span>

-   <span data-ttu-id="8c2bb-106">探索指定的位址是否可支援一組特定的媒體類型需求。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-106">Discover whether a specified address can support a particular set of media type needs.</span></span>
-   <span data-ttu-id="8c2bb-107">列舉目前與位址相關聯的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-107">Enumerate calls currently associated with the address.</span></span>
-   <span data-ttu-id="8c2bb-108">建立或轉寄呼叫。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-108">Create or forward calls.</span></span>
-   <span data-ttu-id="8c2bb-109">取得相關聯服務提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-109">Get the name of the associated service provider.</span></span>
-   <span data-ttu-id="8c2bb-110">如果媒體服務提供者存在，請取得允許詳細終端機操作的介面指標。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-110">If a media service provider exists, get interface pointers that allow detailed terminal manipulation.</span></span>
-   <span data-ttu-id="8c2bb-111">取得和設定其他資訊，例如訊息是否正在等候。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-111">Get and set other information, such as whether a message is waiting.</span></span>

<span data-ttu-id="8c2bb-112">大部分的位址都與終端機相關聯，但這並不是一致的情況。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-112">Most addresses are associated with a terminal, but this is not uniformly the case.</span></span> <span data-ttu-id="8c2bb-113">例如，在伺服器上提供設備存取權的遠端 TSP，在本機電腦上會有位址，而不是終端機。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-113">For example, a remote TSP that provides access to equipment on a server will have an address on the local machine but not a terminal.</span></span> <span data-ttu-id="8c2bb-114">Speakerless 數據機也沒有與其位址相關聯的終端機。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-114">A speakerless modem also has no terminal associated with its address.</span></span>

<span data-ttu-id="8c2bb-115">如果位址沒有相關聯的終端機，就不會在物件上公開 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) 介面。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-115">If an address does not have an associated terminal, the [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is not exposed on the object.</span></span>

<span data-ttu-id="8c2bb-116">[ [選取位址程式](select-an-address.md) 代碼] 範例會顯示取得位址物件指標的基本流程。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-116">The [Select an Address](select-an-address.md) code example shows the basic process for acquiring an address object pointer.</span></span>

<span data-ttu-id="8c2bb-117">如需與 Address 物件相關聯的所有介面清單，請參閱 [Address 物件介面](address-object-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="8c2bb-117">See [Address Object Interfaces](address-object-interfaces.md) for a list of all interfaces associated with the Address object.</span></span>

 

 
