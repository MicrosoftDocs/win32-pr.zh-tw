---
description: 程式設計人員會使用授權技術來建立存取控制軟體、網際網路存取控制、安全性存取控制和檔案安全性。
ms.assetid: 1b8306da-7577-40b8-b77c-5762c1962f00
title: 授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c939a4dd8747b7219fe99650ab7a078239b5f643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195585"
---
# <a name="authorization"></a><span data-ttu-id="e8b98-103">授權</span><span class="sxs-lookup"><span data-stu-id="e8b98-103">Authorization</span></span>

## <a name="purpose"></a><span data-ttu-id="e8b98-104">目的</span><span class="sxs-lookup"><span data-stu-id="e8b98-104">Purpose</span></span>

<span data-ttu-id="e8b98-105">授權是授與個人使用系統及其儲存資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="e8b98-105">Authorization is the right granted an individual to use the system and the data stored on it.</span></span> <span data-ttu-id="e8b98-106">授權通常是由系統管理員設定，並由電腦根據某種形式的使用者識別碼（例如代碼號碼或密碼）進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e8b98-106">Authorization is typically set up by a system administrator and verified by the computer based on some form of user identification, such as a code number or password.</span></span>

<span data-ttu-id="e8b98-107">Microsoft 授權技術包括授權管理員和 Authz API。</span><span class="sxs-lookup"><span data-stu-id="e8b98-107">Microsoft authorization technologies include Authorization Manager and the Authz API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e8b98-108">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e8b98-108">Developer audience</span></span>

<span data-ttu-id="e8b98-109">Microsoft 授權技術適用于以控制資源存取權的 Windows Server 和 Windows 作業系統為基礎的應用程式開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="e8b98-109">Microsoft authorization technologies are intended for use by developers of applications based on the Windows Server and Windows operating systems that control access to resources.</span></span> <span data-ttu-id="e8b98-110">開發人員應該熟悉以 Windows 為基礎的程式設計。</span><span class="sxs-lookup"><span data-stu-id="e8b98-110">Developers should be familiar with Windows-based programming.</span></span> <span data-ttu-id="e8b98-111">雖然並非必要，但建議您瞭解授權或安全性相關的主題。</span><span class="sxs-lookup"><span data-stu-id="e8b98-111">Although not required, an understanding of authorization or security-related subjects is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e8b98-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="e8b98-112">Run-time requirements</span></span>

<span data-ttu-id="e8b98-113">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="e8b98-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e8b98-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="e8b98-114">In this section</span></span>



| <span data-ttu-id="e8b98-115">主題</span><span class="sxs-lookup"><span data-stu-id="e8b98-115">Topic</span></span>                                                             | <span data-ttu-id="e8b98-116">描述</span><span class="sxs-lookup"><span data-stu-id="e8b98-116">Description</span></span>                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8b98-117">關於授權</span><span class="sxs-lookup"><span data-stu-id="e8b98-117">About Authorization</span></span>](about-authorization.md)<br/>         | <span data-ttu-id="e8b98-118">重要的授權概念，以及 Microsoft 授權技術的高階觀點。</span><span class="sxs-lookup"><span data-stu-id="e8b98-118">Key authorization concepts and a high-level view of Microsoft authorization technologies.</span></span><br/>                                                                                                                                                                                  |
| <span data-ttu-id="e8b98-119">使用授權</span><span class="sxs-lookup"><span data-stu-id="e8b98-119">Using Authorization</span></span><br/>                                    | <span data-ttu-id="e8b98-120">使用 Microsoft 授權技術的授權進程、程式和程式範例。</span><span class="sxs-lookup"><span data-stu-id="e8b98-120">Authorization processes, procedures, and examples of programs using Microsoft authorization technologies.</span></span> <span data-ttu-id="e8b98-121">這項資訊會在 [c + +](using-authorization-in-c--.md) 和 [腳本](using-authorization-in-script.md) 程式設計語言的區段中顯示。</span><span class="sxs-lookup"><span data-stu-id="e8b98-121">This information is presented in using sections for [C++](using-authorization-in-c--.md) and [Script](using-authorization-in-script.md) programming languages.</span></span><br/> |
| [<span data-ttu-id="e8b98-122">授權參考</span><span class="sxs-lookup"><span data-stu-id="e8b98-122">Authorization Reference</span></span>](authorization-reference.md)<br/> | <span data-ttu-id="e8b98-123">授權函數、介面、結構和其他程式設計專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e8b98-123">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                                                                                                                                                                |



 

 

 




