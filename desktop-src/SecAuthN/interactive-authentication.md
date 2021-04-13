---
description: 當系統提示使用者提供登入資訊時，驗證是互動式的。 當使用者透過 GINA 使用者介面登入時， (LSA) 的「本地安全機構」會執行互動式驗證。
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: 互動式驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320200"
---
# <a name="interactive-authentication"></a><span data-ttu-id="405d3-104">互動式驗證</span><span class="sxs-lookup"><span data-stu-id="405d3-104">Interactive Authentication</span></span>

<span data-ttu-id="405d3-105">當系統提示使用者提供登入資訊時，驗證是互動式的。</span><span class="sxs-lookup"><span data-stu-id="405d3-105">Authentication is interactive when a user is prompted to supply logon information.</span></span> <span data-ttu-id="405d3-106">當使用者透過 [*GINA*](../secgloss/g-gly.md)使用者介面登入時， (LSA) 的「[*本地安全機構*](../secgloss/l-gly.md)」會執行互動式驗證。</span><span class="sxs-lookup"><span data-stu-id="405d3-106">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) performs an interactive authentication when a user logs on through the [*GINA*](../secgloss/g-gly.md) user interface.</span></span> <span data-ttu-id="405d3-107">下圖顯示一般互動式驗證的部分。</span><span class="sxs-lookup"><span data-stu-id="405d3-107">The following illustration shows the parts of a typical interactive authentication.</span></span>

![互動式驗證](images/lsaint3.png)

<span data-ttu-id="405d3-109">使用者將 CTRL + ALT + DEL [*安全的注意順序*](../secgloss/s-gly.md) 輸入 (SAS) ，以通知系統開始登入順序。</span><span class="sxs-lookup"><span data-stu-id="405d3-109">A user signals the system to begin the logon sequence by typing the CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS).</span></span> <span data-ttu-id="405d3-110">[*Winlogon*](../secgloss/w-gly.md) 會接收 SAS 並呼叫 GINA，以顯示使用者介面並取得使用者的登入資料，例如使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="405d3-110">[*Winlogon*](../secgloss/w-gly.md) receives the SAS and calls the GINA to display a user interface and obtain the user's logon data, such as a user name and password.</span></span>

<span data-ttu-id="405d3-111">取得登入資料之後，GINA 會呼叫 [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) 函式來驗證使用者，指定必須使用哪個驗證套件來評估登入資料。</span><span class="sxs-lookup"><span data-stu-id="405d3-111">After obtaining the logon data, the GINA calls the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) function to authenticate the user, specifying which authentication package must be used to evaluate the logon data.</span></span>

<span data-ttu-id="405d3-112">LSA 會呼叫指定的驗證套件，並將登入資料傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="405d3-112">The LSA calls the specified authentication package and passes the logon data to it.</span></span> <span data-ttu-id="405d3-113">驗證套件會檢查資料，並判斷驗證是否成功。</span><span class="sxs-lookup"><span data-stu-id="405d3-113">The authentication package examines the data and determines whether the authentication is successful.</span></span> <span data-ttu-id="405d3-114">驗證結果會從 lsa 傳回至 GINA。</span><span class="sxs-lookup"><span data-stu-id="405d3-114">The authentication result is returned to the LSA and from the LSA, to the GINA.</span></span>

<span data-ttu-id="405d3-115">GINA 會顯示使用者驗證成功或失敗，並將驗證的結果傳回給 Winlogon。</span><span class="sxs-lookup"><span data-stu-id="405d3-115">The GINA displays the success or failure of the authentication to the user and returns the result of the authentication to Winlogon.</span></span> <span data-ttu-id="405d3-116">如果驗證成功，使用者的登入會話就會開始，並儲存一組登入 [*認證*](../secgloss/c-gly.md) 以供日後參考。</span><span class="sxs-lookup"><span data-stu-id="405d3-116">If the authentication succeeds, the user's logon session begins and a set of logon [*credentials*](../secgloss/c-gly.md) are saved for future reference.</span></span>

> [!Note]  
> <span data-ttu-id="405d3-117">一般而言，撰寫自訂 GINA 以接受特殊登入資料的開發人員（例如 [*智慧卡*](../secgloss/s-gly.md) 或視網膜掃描資料）也必須撰寫負責處理該資料及判斷其真實性的驗證套件。</span><span class="sxs-lookup"><span data-stu-id="405d3-117">In general, a developer who writes a custom GINA to accept specialized logon data, such as a [*smart card*](../secgloss/s-gly.md) or retinal-scan data, must also write an authentication package responsible for processing that data and determining its authenticity.</span></span>

 

<span data-ttu-id="405d3-118">如需 Winlogon 和 Gina 的詳細資訊，請參閱 [winlogon 和 GINA](winlogon-and-gina.md)。</span><span class="sxs-lookup"><span data-stu-id="405d3-118">For more information about Winlogon and GINAs, see [Winlogon and GINA](winlogon-and-gina.md).</span></span> <span data-ttu-id="405d3-119">如需有關驗證套件的詳細資訊，請參閱 [建立自訂安全性封裝](creating-custom-security-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="405d3-119">For more information about authentication packages, see [Creating Custom Security Packages](creating-custom-security-packages.md).</span></span>

 

 
