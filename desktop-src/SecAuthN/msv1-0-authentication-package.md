---
description: Microsoft \_ 針對不需要自訂驗證的本機電腦登入提供 MSV1 0 驗證套件。
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 Authentication 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 662ae65f60bec61c30b12271a34dc9d3c2883d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194067"
---
# <a name="msv1_0-authentication-package"></a><span data-ttu-id="01a87-103">MSV1 \_ 0 驗證套件</span><span class="sxs-lookup"><span data-stu-id="01a87-103">MSV1\_0 Authentication Package</span></span>

<span data-ttu-id="01a87-104">Microsoft \_ 針對不需要自訂驗證的本機電腦登入提供 MSV1 0 [*驗證套件*](../secgloss/a-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="01a87-104">Microsoft provides the MSV1\_0 [*authentication package*](../secgloss/a-gly.md) for local machine logons that do not require custom authentication.</span></span> <span data-ttu-id="01a87-105">「 [*本地安全機構*](../secgloss/l-gly.md) 」 (LSA) 會呼叫 MSV1 \_ 0 authentication 封裝，以處理 [*GINA*](../secgloss/g-gly.md) 針對 [*Winlogon*](../secgloss/w-gly.md) 登入程式所收集的登入資料。</span><span class="sxs-lookup"><span data-stu-id="01a87-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) calls the MSV1\_0 authentication package to process logon data collected by the [*GINA*](../secgloss/g-gly.md) for the [*Winlogon*](../secgloss/w-gly.md) logon process.</span></span> <span data-ttu-id="01a87-106">MSV1 \_ 0 封裝會檢查本機安全性帳戶管理員 (SAM) 資料庫，以判斷登入資料是否屬於有效的 [*安全性主體*](../secgloss/s-gly.md) ，然後將登入嘗試的結果傳回至 LSA。</span><span class="sxs-lookup"><span data-stu-id="01a87-106">The MSV1\_0 package checks the local security accounts manager (SAM) database to determine whether the logon data belongs to a valid [*security principal*](../secgloss/s-gly.md) and then returns the result of the logon attempt to the LSA.</span></span>

<span data-ttu-id="01a87-107">MSV1 \_ 0 也支援網域登入。</span><span class="sxs-lookup"><span data-stu-id="01a87-107">MSV1\_0 also supports domain logons.</span></span> <span data-ttu-id="01a87-108">MSV1 \_ 0 會使用傳遞驗證來處理網域登入，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="01a87-108">MSV1\_0 processes domain logons using pass-through authentication, as illustrated in the following diagram.</span></span>

![msv1 \- 0 驗證套件](images/lsaint4.png)

<span data-ttu-id="01a87-110">在傳遞驗證中，MSV1 0 的本機實例會 \_ 使用 Netlogon 服務來呼叫網域控制站上執行的 MSV1 \_ 0 實例。</span><span class="sxs-lookup"><span data-stu-id="01a87-110">In pass-through authentication, the local instance of MSV1\_0 uses the Netlogon service to call the instance of MSV1\_0 running on the domain controller.</span></span> <span data-ttu-id="01a87-111">網域控制站的 MSV1 0 實例會 \_ 接著檢查網域控制站的 SAM 資料庫，並將登入結果傳回至 \_ 本機電腦上的 MSV1 0 實例。</span><span class="sxs-lookup"><span data-stu-id="01a87-111">The domain controller's instance of MSV1\_0 then checks the SAM database of the domain controller and returns the logon result to the instance of MSV1\_0 on the local machine.</span></span> <span data-ttu-id="01a87-112">本機版本的 MSV1 0 會將 \_ 登入結果轉送到本機電腦上的 LSA 實例。</span><span class="sxs-lookup"><span data-stu-id="01a87-112">The local version of MSV1\_0 forwards the logon result to the instance of the LSA on the local machine.</span></span>

<span data-ttu-id="01a87-113">如果網域控制站無法使用，而且 LSA 包含使用者的快取 [*認證*](../secgloss/c-gly.md) ，則 MSV1 0 的本機實例 \_ 可以使用快取的登入資料來驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="01a87-113">If the domain controller is not available, and the LSA contains cached [*credentials*](../secgloss/c-gly.md) for the user, the local instance of MSV1\_0 can authenticate the user using the cached logon data.</span></span>

<span data-ttu-id="01a87-114">MSV1 \_ 0 驗證套件也支援 [子驗證套件](subauthentication-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="01a87-114">The MSV1\_0 authentication package also supports [subauthentication packages](subauthentication-packages.md).</span></span> <span data-ttu-id="01a87-115">子驗證套件是一個 DLL，可取代 MSV1 0 驗證套件所使用的驗證和驗證準則的一部分 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01a87-115">A subauthentication package is a DLL that can replace part of the authentication and validation criteria used by the MSV1\_0 authentication package.</span></span>

<span data-ttu-id="01a87-116">MSV1 \_ 0 authentication 套件會定義 [*主要認證*](../secgloss/p-gly.md) 的索引鍵/字串值組。</span><span class="sxs-lookup"><span data-stu-id="01a87-116">The MSV1\_0 authentication package defines a [*primary credentials*](../secgloss/p-gly.md) key/string value pair.</span></span> <span data-ttu-id="01a87-117">主要認證字串會保存從登入期間所提供之資料衍生的認證。</span><span class="sxs-lookup"><span data-stu-id="01a87-117">The primary credentials string holds the credentials derived from the data provided at logon time.</span></span> <span data-ttu-id="01a87-118">它包含使用者名稱，以及區分大小寫且區分大小寫的使用者密碼格式。</span><span class="sxs-lookup"><span data-stu-id="01a87-118">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

 

 
