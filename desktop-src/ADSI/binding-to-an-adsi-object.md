---
title: 系結至 ADSI 物件
description: 連接到目錄服務中的物件稱為「系結」（binding）。
ms.assetid: f3963019-9b3a-42d5-a978-484f294110e5
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、using、binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0fefcdb62d374d98e3007864168e2626ecc5d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671183"
---
# <a name="binding-to-an-adsi-object"></a><span data-ttu-id="6b828-104">系結至 ADSI 物件</span><span class="sxs-lookup"><span data-stu-id="6b828-104">Binding to an ADSI Object</span></span>

<span data-ttu-id="6b828-105">連接到目錄服務中的物件稱為「系結」（binding）。</span><span class="sxs-lookup"><span data-stu-id="6b828-105">Connecting to an object in a directory service is known as binding.</span></span> <span data-ttu-id="6b828-106">系結至 ADSI 物件是與基礎目錄系統進行通訊的第一個步驟。</span><span class="sxs-lookup"><span data-stu-id="6b828-106">Binding to an ADSI object is the first step to communicating with the underlying directory system.</span></span> <span data-ttu-id="6b828-107">物件必須系結至，才能流覽其命名空間、搜尋資料、修改資料，或模擬使用者。</span><span class="sxs-lookup"><span data-stu-id="6b828-107">An object must be bound to in order to navigate its namespace, search for data, modify data, or impersonate a user.</span></span> <span data-ttu-id="6b828-108">您也可以提供其他系結特性，例如使用者名稱、密碼、伺服器名稱、加密方法和安全驗證。</span><span class="sxs-lookup"><span data-stu-id="6b828-108">It is also possible to supply additional binding characteristics, such as user name, password, server name, encryption methods, and secured authentication.</span></span> <span data-ttu-id="6b828-109">您可以使用的實際額外系結特性將視提供者而定。</span><span class="sxs-lookup"><span data-stu-id="6b828-109">The actual additional binding characteristics that can be used will depend on the provider.</span></span>

<span data-ttu-id="6b828-110">如需 ADSI 系結的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="6b828-110">For more information about ADSI binding, see:</span></span>

-   [<span data-ttu-id="6b828-111">系結字串</span><span class="sxs-lookup"><span data-stu-id="6b828-111">Binding String</span></span>](binding-string.md)
-   [<span data-ttu-id="6b828-112">Active Directory 特定的系結類型</span><span class="sxs-lookup"><span data-stu-id="6b828-112">Binding Types Specific to Active Directory</span></span>](binding-types-specific-to-active-directory.md)
-   [<span data-ttu-id="6b828-113">混合式環境的系結問題</span><span class="sxs-lookup"><span data-stu-id="6b828-113">Binding Issues for Mixed Environments</span></span>](binding-issues-for-mixed-environments.md)
-   [<span data-ttu-id="6b828-114">使用 ADSI 介面以程式設計方式系結</span><span class="sxs-lookup"><span data-stu-id="6b828-114">Binding Programmatically Using an ADSI Interface</span></span>](binding-programmatically-using-an-adsi-interface.md)
-   [<span data-ttu-id="6b828-115">連接快取</span><span class="sxs-lookup"><span data-stu-id="6b828-115">Connection Caching</span></span>](connection-caching.md)
-   [<span data-ttu-id="6b828-116">系結至子物件</span><span class="sxs-lookup"><span data-stu-id="6b828-116">Binding to Child Objects</span></span>](binding-to-child-objects.md)
-   [<span data-ttu-id="6b828-117">系結至物件的父系</span><span class="sxs-lookup"><span data-stu-id="6b828-117">Binding to an Object's Parent</span></span>](binding-to-an-objectampaposs-parent.md)
-   [<span data-ttu-id="6b828-118">批次寫入/修改作業的快速系結選項</span><span class="sxs-lookup"><span data-stu-id="6b828-118">Fast Binding Option for Batch Write/Modify Operations</span></span>](fast-binding-option-for-batch-writemodify-operations.md)
-   [<span data-ttu-id="6b828-119">選擇系結的介面</span><span class="sxs-lookup"><span data-stu-id="6b828-119">Choosing an Interface for Binding</span></span>](choosing-an-interface.md)

 

 




