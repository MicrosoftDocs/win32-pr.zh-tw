---
title: FACILITY_ITF 中的代碼
description: 設備 ITF 中的代碼 \_
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932049"
---
# <a name="codes-in-facility_itf"></a><span data-ttu-id="dc9b7-103">設備 ITF 中的代碼 \_</span><span class="sxs-lookup"><span data-stu-id="dc9b7-103">Codes in FACILITY\_ITF</span></span>

<span data-ttu-id="dc9b7-104">具有設備（例如設備 \_ Null 和設備 RPC）的 HRESULT \_ 具有通用意義，因為它們定義于單一來源： Microsoft。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-104">**HRESULT** s with facilities such as FACILITY\_NULL and FACILITY\_RPC have universal meaning because they are defined at a single source: Microsoft.</span></span> <span data-ttu-id="dc9b7-105">但是， 設備 \_ ITF 中的 HRESULT 會由傳回它們的函式或介面方法來決定。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-105">However, **HRESULT** s in FACILITY\_ITF are determined by the function or interface method from which they are returned.</span></span> <span data-ttu-id="dc9b7-106">這表示， \_ 從兩個不同介面方法傳回的設備 ITF 中相同的32位值可能會有不同的意義。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-106">This means that the same 32-bit value in FACILITY\_ITF returned from two different interface methods might have different meanings.</span></span>

<span data-ttu-id="dc9b7-107">設備 ITF 中的 **hresult** 的原因在 \_ 不同的介面中可能會有不同的意義，因為 **hresult** 會保持為有效率的資料類型大小32位。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-107">The reason **HRESULT** s in FACILITY\_ITF can have different meanings in different interfaces is that **HRESULT** s are kept to an efficient data type size of 32 bits.</span></span> <span data-ttu-id="dc9b7-108">可惜的是，32位不夠大，無法開發錯誤碼配置系統，以避免不同的程式設計人員在不同位置的不同時間所配置的衝突程式碼 (與) 介面識別碼和 Clsid 的處理方式不同。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-108">Unfortunately, 32 bits is not large enough for the development of an error code allocation system that avoids conflicting codes allocated by different programmers at different times in different places (unlike the handling of interface identifiers and CLSIDs).</span></span> <span data-ttu-id="dc9b7-109">因此，32位 **HRESULT** 是結構化的，因此 Microsoft 可以定義數個通用錯誤碼，而讓其他程式設計人員可以定義新的錯誤碼，而不會擔心衝突。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-109">As a result, the 32-bit **HRESULT** is structured such that Microsoft can define several universal error codes, while allowing other programmers to define new error codes without fear of conflict.</span></span> <span data-ttu-id="dc9b7-110">狀態碼慣例如下所示：</span><span class="sxs-lookup"><span data-stu-id="dc9b7-110">The status code convention is as follows:</span></span>

-   <span data-ttu-id="dc9b7-111">只有 Microsoft 才能定義設備 ITF 以外設施中的狀態碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-111">Status codes in facilities other than FACILITY\_ITF can be defined only by Microsoft.</span></span>
-   <span data-ttu-id="dc9b7-112">設備設施 ITF 中的狀態碼 \_ 是由傳回狀態碼之介面或函式的開發人員唯一定義。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-112">Status codes in facility FACILITY\_ITF are defined solely by the developer of the interface or function that returns the status code.</span></span> <span data-ttu-id="dc9b7-113">為了避免衝突的錯誤碼，定義介面的人員必須負責協調和發佈 \_ 與該介面相關聯的設施 ITF 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-113">To avoid conflicting error codes, whoever defines the interface is responsible for coordinating and publishing the FACILITY\_ITF status codes associated with that interface.</span></span>

<span data-ttu-id="dc9b7-114">所有的 COM 定義設備 \_ ITF 碼都有 0x0000-0x01FF 範圍內的代碼值。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-114">All the COM-defined FACILITY\_ITF codes have a code value in the range of 0x0000-0x01FF.</span></span> <span data-ttu-id="dc9b7-115">雖然在設備 ITF 中使用任何程式碼是合法的 \_ ，但建議您只使用 0x0200-0xffff 範圍內的程式碼值。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-115">While it is legal to use any codes in FACILITY\_ITF, it is recommended that only code values in the range of 0x0200-0xFFFF be used.</span></span> <span data-ttu-id="dc9b7-116">這項建議是為了減少與任何 COM 定義錯誤混淆的方式。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-116">This recommendation is made as a means of reducing confusion with any COM-defined errors.</span></span>

<span data-ttu-id="dc9b7-117">此外，也建議開發人員定義新的函式和介面，以傳回 COM 和設備 ITF 以外設備中的錯誤碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-117">It is also recommended that developers define new functions and interfaces to return error codes as defined by COM and in facilities other than FACILITY\_ITF.</span></span> <span data-ttu-id="dc9b7-118">尤其是，未來有機會使用 RPC 進行遠端處理的介面，應該將設備的 \_ RPC 代碼定義為合法。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-118">In particular, interfaces that have any chance of being remoted using RPC in the future should define the FACILITY\_RPC codes as legal.</span></span> <span data-ttu-id="dc9b7-119">電子 \_ 非預期的是，大部分的開發人員都想要進行普遍合法的特定錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc9b7-119">E\_UNEXPECTED is a specific error code that most developers will want to make universally legal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc9b7-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc9b7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc9b7-121">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="dc9b7-121">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




