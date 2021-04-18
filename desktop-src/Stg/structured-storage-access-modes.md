---
title: 結構化儲存體存取模式
description: 控制多個進程和使用者同時存取物件的機制是不可或缺的。
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- 結構化儲存體 Strctd Stg.、基本概念、API 函式、用於存取的旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968624"
---
# <a name="structured-storage-access-modes"></a><span data-ttu-id="04144-104">結構化儲存體存取模式</span><span class="sxs-lookup"><span data-stu-id="04144-104">Structured Storage Access Modes</span></span>

<span data-ttu-id="04144-105">控制多個進程和使用者同時存取物件的機制是不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="04144-105">Mechanisms for controlling simultaneous access to an object, by multiple processes and users, are essential.</span></span> <span data-ttu-id="04144-106">COM 藉由定義儲存體和資料流程物件的存取模式，提供這些機制。</span><span class="sxs-lookup"><span data-stu-id="04144-106">COM provides these mechanisms by defining access modes for both storage and stream objects.</span></span> <span data-ttu-id="04144-107">針對父儲存物件所指定的存取模式是由其子系所繼承，不過您可以對子系儲存體或串流進行額外的限制。</span><span class="sxs-lookup"><span data-stu-id="04144-107">The access mode specified for a parent storage object is inherited by its children, though you can place additional restrictions on the child storage or stream.</span></span> <span data-ttu-id="04144-108">嵌套的儲存或資料流程物件可以在相同的模式下開啟，或以比其父系更受限制的模式開啟，但無法在不受限制的模式下開啟。</span><span class="sxs-lookup"><span data-stu-id="04144-108">A nested storage or stream object can be opened in the same mode or in a more restricted mode than that of its parent, but it cannot be opened in a less restricted mode than that of its parent.</span></span>

<span data-ttu-id="04144-109">您可以使用 [**STGM 常數**](stgm-constants.md)中所列的值來指定存取模式。</span><span class="sxs-lookup"><span data-stu-id="04144-109">You specify access modes by using the values listed in [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="04144-110">這些值可作為要當做引數傳遞給 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面和相關 API 函式中之方法的旗標。</span><span class="sxs-lookup"><span data-stu-id="04144-110">These values serve as flags to be passed as arguments to methods in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and associated API functions.</span></span> <span data-ttu-id="04144-111">通常會使用布林值 **或** 運算，在參數 *grfMode* 中結合數個旗標。</span><span class="sxs-lookup"><span data-stu-id="04144-111">Typically, several flags are combined in the parameter *grfMode*, using a Boolean **OR** operation.</span></span>

<span data-ttu-id="04144-112">旗標分為六個群組。</span><span class="sxs-lookup"><span data-stu-id="04144-112">The flags fall into six groups.</span></span> <span data-ttu-id="04144-113">一次只能指定每個群組中的一個旗標：</span><span class="sxs-lookup"><span data-stu-id="04144-113">Only one flag from each group can be specified at a time:</span></span>

-   [<span data-ttu-id="04144-114">交易旗標</span><span class="sxs-lookup"><span data-stu-id="04144-114">Transaction Flags</span></span>](transaction-flags.md)
-   [<span data-ttu-id="04144-115">儲存體建立旗標</span><span class="sxs-lookup"><span data-stu-id="04144-115">Storage Creation Flags</span></span>](storage-creation-flags.md)
-   [<span data-ttu-id="04144-116">暫時建立旗標</span><span class="sxs-lookup"><span data-stu-id="04144-116">Temporary Creation Flags</span></span>](temporary-creation-flags.md)
-   [<span data-ttu-id="04144-117">優先權旗標</span><span class="sxs-lookup"><span data-stu-id="04144-117">Priority Flags</span></span>](priority-flags.md)
-   [<span data-ttu-id="04144-118">存取權限旗標</span><span class="sxs-lookup"><span data-stu-id="04144-118">Access Permission Flags</span></span>](access-permission-flags.md)
-   [<span data-ttu-id="04144-119">共用存取旗標</span><span class="sxs-lookup"><span data-stu-id="04144-119">Shared Access Flags</span></span>](shared-access-flags.md)

 

 




