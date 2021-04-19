---
description: 建立憑證要求的程式牽涉到收集要求者的特定資訊。
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: 建立憑證要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972834"
---
# <a name="creating-the-certificate-request"></a><span data-ttu-id="11bf2-103">建立憑證要求</span><span class="sxs-lookup"><span data-stu-id="11bf2-103">Creating the Certificate Request</span></span>

<span data-ttu-id="11bf2-104">建立憑證要求的程式牽涉到收集要求者的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="11bf2-104">The process of creating a certificate request involves collecting certain information from the requester.</span></span> <span data-ttu-id="11bf2-105">通常，這是透過某種使用者介面 (UI) 來完成，不過，您可以直接從資料庫取得資訊，而不需要 UI。</span><span class="sxs-lookup"><span data-stu-id="11bf2-105">Usually, this is done through some sort of user interface (UI), although the information could be taken directly from a database without the need for a UI.</span></span> <span data-ttu-id="11bf2-106">所需的資訊層級是由 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 的原則所設定。</span><span class="sxs-lookup"><span data-stu-id="11bf2-106">The level of information required is set by the policy of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="11bf2-107">必要資訊的範例如下所示：</span><span class="sxs-lookup"><span data-stu-id="11bf2-107">An example of the required information might be as follows:</span></span>

-   <span data-ttu-id="11bf2-108">一般名稱</span><span class="sxs-lookup"><span data-stu-id="11bf2-108">Common Name</span></span>
-   <span data-ttu-id="11bf2-109">單位名稱</span><span class="sxs-lookup"><span data-stu-id="11bf2-109">Unit Name</span></span>
-   <span data-ttu-id="11bf2-110">公司名稱</span><span class="sxs-lookup"><span data-stu-id="11bf2-110">Company Name</span></span>
-   <span data-ttu-id="11bf2-111">City</span><span class="sxs-lookup"><span data-stu-id="11bf2-111">City</span></span>
-   <span data-ttu-id="11bf2-112">狀態</span><span class="sxs-lookup"><span data-stu-id="11bf2-112">State</span></span>
-   <span data-ttu-id="11bf2-113">國家/地區</span><span class="sxs-lookup"><span data-stu-id="11bf2-113">Country/Region</span></span>

> [!Note]  
> <span data-ttu-id="11bf2-114">介面是設計來針對每個 xenroll.dll 實例提出單一要求。</span><span class="sxs-lookup"><span data-stu-id="11bf2-114">The interface is designed to make a single request for each xenroll instance.</span></span> <span data-ttu-id="11bf2-115">您必須建立個別的 xenroll.dll 實例，才能建立每個 [*憑證要求*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="11bf2-115">A separate xenroll instance must be created to create each [*certificate request*](../secgloss/c-gly.md).</span></span>

 

<span data-ttu-id="11bf2-116">如需如何使用憑證註冊控制項以特定程式設計語言要求憑證的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="11bf2-116">For information about how to use the Certificate Enrollment Control to request a certificate in specific programming languages, see the following topics:</span></span>

-   [<span data-ttu-id="11bf2-117">C + + 中的要求範例</span><span class="sxs-lookup"><span data-stu-id="11bf2-117">Request Sample in C++</span></span>](request-sample-in-c-.md)
-   [<span data-ttu-id="11bf2-118">VBScript 中的要求範例</span><span class="sxs-lookup"><span data-stu-id="11bf2-118">Request Sample in VBScript</span></span>](request-sample-in-vbscript.md)

 

 
