---
description: 本節說明如何使用 XPS 數位簽章 API 來執行基本的程式設計工作。
ms.assetid: a25a8d33-000a-4774-8beb-56d3bb39d5ae
title: 一般數位簽章程式設計工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346b29c7768f4c4e972284afa697f97bb1da5f69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469488"
---
# <a name="common-digital-signature-programming-tasks"></a><span data-ttu-id="c8503-103">一般數位簽章程式設計工作</span><span class="sxs-lookup"><span data-stu-id="c8503-103">Common Digital Signature Programming Tasks</span></span>

<span data-ttu-id="c8503-104">本節說明如何使用 XPS 數位簽章 API 來執行基本的程式設計工作。</span><span class="sxs-lookup"><span data-stu-id="c8503-104">This section describes how to perform basic programming tasks with the XPS Digital Signature API.</span></span>

<span data-ttu-id="c8503-105">工作</span><span class="sxs-lookup"><span data-stu-id="c8503-105">Tasks</span></span>

-   [<span data-ttu-id="c8503-106">初始化簽章管理員</span><span class="sxs-lookup"><span data-stu-id="c8503-106">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)
-   [<span data-ttu-id="c8503-107">簽署檔</span><span class="sxs-lookup"><span data-stu-id="c8503-107">Sign a Document</span></span>](sign-a-document.md)
-   [<span data-ttu-id="c8503-108">將簽名要求新增至 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="c8503-108">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
-   [<span data-ttu-id="c8503-109">驗證檔簽章</span><span class="sxs-lookup"><span data-stu-id="c8503-109">Verify Document Signatures</span></span>](verify-document-signatures.md)

## <a name="disclaimer"></a><span data-ttu-id="c8503-110">免責聲明</span><span class="sxs-lookup"><span data-stu-id="c8503-110">Disclaimer</span></span>

<span data-ttu-id="c8503-111">程式碼範例的目的不是完整且正常運作的程式。</span><span class="sxs-lookup"><span data-stu-id="c8503-111">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="c8503-112">例如，此頁面所參考的程式碼範例不會執行參數檢查、錯誤檢查、完成記憶體或資源管理或錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="c8503-112">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, complete memory or resource management, or error handling.</span></span> <span data-ttu-id="c8503-113">使用這些範例作為起點，然後新增必要的程式碼以建立健全的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c8503-113">Use these examples as a starting point, then add the necessary code to create a robust application.</span></span> <span data-ttu-id="c8503-114">如需 **HRESULT** 傳回值和錯誤處理策略的詳細資訊，請參閱 [COM 中的錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="c8503-114">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="c8503-115">為了清楚起見，這些程式碼範例使用非常簡單的 XPS 檔和簽章案例，這些案例可能不夠複雜，無法滿足您的需求。</span><span class="sxs-lookup"><span data-stu-id="c8503-115">For clarity, these code examples use very simple XPS document and signature scenarios, which might not be sufficiently complex to meet your needs.</span></span>

 

 
