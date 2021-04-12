---
description: 憑證是根據定義要求者必須符合以接收憑證之準則的原則來授與。
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: 原則獨立性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319591"
---
# <a name="policy-independence"></a><span data-ttu-id="8f972-103">原則獨立性</span><span class="sxs-lookup"><span data-stu-id="8f972-103">Policy Independence</span></span>

<span data-ttu-id="8f972-104">憑證是根據定義要求者必須符合以接收憑證之準則的原則來授與。</span><span class="sxs-lookup"><span data-stu-id="8f972-104">Certificates are granted according to policies that define criteria that requesters must meet to receive a certificate.</span></span> <span data-ttu-id="8f972-105">例如，一個原則可能是只有在申請人出示其身分識別時，才授與商業憑證。</span><span class="sxs-lookup"><span data-stu-id="8f972-105">For example, one policy may be to grant commercial certificates only if applicants present their identification in person.</span></span> <span data-ttu-id="8f972-106">另一個原則可能會根據電子郵件要求授與 [*認證*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="8f972-106">Another policy may grant [*credentials*](../secgloss/c-gly.md) based on email requests.</span></span> <span data-ttu-id="8f972-107">發出信用卡的機構可以選擇查閱資料庫，並在發出卡片之前進行電話查詢。</span><span class="sxs-lookup"><span data-stu-id="8f972-107">An agency that issues credit cards may choose to consult a database and make phone inquiries before issuing a card.</span></span>

<span data-ttu-id="8f972-108">原則會在以 c + +、C 或 Visual Basic 撰寫的原則模組中執行。</span><span class="sxs-lookup"><span data-stu-id="8f972-108">Policies are implemented in policy modules written in C++, C, or Visual Basic.</span></span> <span data-ttu-id="8f972-109">憑證服務函式與機構可能會實行的原則中的任何變更隔離。</span><span class="sxs-lookup"><span data-stu-id="8f972-109">Certificate Services functions are isolated from any changes in policy that an agency might implement.</span></span> <span data-ttu-id="8f972-110">原則中的變更可以完整地在伺服器原則模組程式碼中執行。</span><span class="sxs-lookup"><span data-stu-id="8f972-110">Changes in policy can be fully implemented in the server policy module code.</span></span> <span data-ttu-id="8f972-111"> (CA) 的企業 [*憑證授權單位*](../secgloss/c-gly.md) 單位只能使用 Microsoft 提供的企業原則模組。</span><span class="sxs-lookup"><span data-stu-id="8f972-111">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

 

 
