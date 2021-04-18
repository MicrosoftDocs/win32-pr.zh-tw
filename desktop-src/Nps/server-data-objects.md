---
title: 伺服器資料物件
description: 伺服器資料物件 (SDO) API 可讓您以程式設計方式設定及管理執行 NPS 的系統。
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106976339"
---
# <a name="server-data-objects"></a><span data-ttu-id="65404-103">伺服器資料物件</span><span class="sxs-lookup"><span data-stu-id="65404-103">Server Data Objects</span></span>

> [!Note]  
> <span data-ttu-id="65404-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="65404-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="65404-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="65404-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="65404-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="65404-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="65404-107">伺服器資料物件 (SDO) API 可讓您以程式設計方式設定及管理執行 NPS 的系統。</span><span class="sxs-lookup"><span data-stu-id="65404-107">The Server Data Objects (SDO) API makes it possible to programmatically configure and administer a system running NPS.</span></span> <span data-ttu-id="65404-108">開發人員也可以使用 SDO 來撰寫管理遠端存取原則和設定檔的應用程式。</span><span class="sxs-lookup"><span data-stu-id="65404-108">Using SDO, a developer can also write applications that administer remote access policies and profiles.</span></span> <span data-ttu-id="65404-109">「路由及遠端存取」服務 (RRAS) 和 NPS 使用遠端存取原則和設定檔，以判斷是否允許遠端用戶端連接到網路存取伺服器 (NAS) 。</span><span class="sxs-lookup"><span data-stu-id="65404-109">The remote access policies and profiles are used by the Routing and Remote Access Service (RRAS) as well as NPS to determine whether a remote client is allowed to connect to a network access server (NAS).</span></span>

<span data-ttu-id="65404-110">SDO API 適用于使用 NPS 或遠端存取原則的任何環境。</span><span class="sxs-lookup"><span data-stu-id="65404-110">The SDO API is applicable in any environment that uses NPS or Remote Access Policies.</span></span>

<span data-ttu-id="65404-111">使用 SDO API，開發人員可以管理可透過 NPS 使用者介面存取之 NPS 設定的任何元素。</span><span class="sxs-lookup"><span data-stu-id="65404-111">With the SDO API, a developer can manipulate any element of the NPS configuration that is accessible through the NPS user interface.</span></span>

<span data-ttu-id="65404-112">SDO API 也可讓您設定或抓取任何可透過 [使用者撥入設定] 屬性頁存取的值。</span><span class="sxs-lookup"><span data-stu-id="65404-112">The SDO API also makes it possible to set or retrieve any of the values accessible through the user dial-in settings property page.</span></span>

<span data-ttu-id="65404-113">SDO API 是由 COM 介面所組成。</span><span class="sxs-lookup"><span data-stu-id="65404-113">The SDO API is composed of COM interfaces.</span></span> <span data-ttu-id="65404-114">SDO API 中的每個介面都繼承自 COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面。</span><span class="sxs-lookup"><span data-stu-id="65404-114">Each of the interfaces in the SDO API inherits from the COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="65404-115">**IDispatch** 介面可讓開發人員從 Visual Basic 或任何 Automation 用戶端，以及從 C/c + + 呼叫 SDO 介面方法。</span><span class="sxs-lookup"><span data-stu-id="65404-115">The **IDispatch** interface enables developers to call the SDO interface methods from Visual Basic or any Automation client, as well as from C/C++.</span></span>

<span data-ttu-id="65404-116">開發人員也可以從指令碼語言（例如 VBScript）呼叫 SDO API。</span><span class="sxs-lookup"><span data-stu-id="65404-116">Developers can also call the SDO API from scripting languages such as VBScript.</span></span> <span data-ttu-id="65404-117">不過，因為 VBScript 僅限於使用 VARIANT 類型參數，所以不能使用 SDO 的所有功能。</span><span class="sxs-lookup"><span data-stu-id="65404-117">However, because VBScript is limited to using VARIANT-type parameters only, not all the functionality of SDO is available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65404-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="65404-118">In This Section</span></span>

[<span data-ttu-id="65404-119">概觀</span><span class="sxs-lookup"><span data-stu-id="65404-119">Overview</span></span>](/windows/desktop/Nps/sdo-about-server-data-objects)

<span data-ttu-id="65404-120">有關伺服器資料物件 API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="65404-120">General information about the Server Data Objects API.</span></span>

[<span data-ttu-id="65404-121">使用</span><span class="sxs-lookup"><span data-stu-id="65404-121">Using</span></span>](/windows/desktop/Nps/sdo-using-server-data-objects)

<span data-ttu-id="65404-122">示範如何使用伺服器資料物件 API 的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="65404-122">Sample code that demonstrates how to use the Server Data Objects API.</span></span>

[<span data-ttu-id="65404-123">參考</span><span class="sxs-lookup"><span data-stu-id="65404-123">Reference</span></span>](/windows/desktop/Nps/sdo-server-data-objects-reference)

<span data-ttu-id="65404-124">組成伺服器資料物件 API 之列舉型別和介面的檔。</span><span class="sxs-lookup"><span data-stu-id="65404-124">Documentation of the enumerated types and interfaces that compose the Server Data Objects API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65404-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="65404-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65404-126">網路原則伺服器 (網際網路驗證服務) </span><span class="sxs-lookup"><span data-stu-id="65404-126">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="65404-127">遠端存取服務</span><span class="sxs-lookup"><span data-stu-id="65404-127">Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 