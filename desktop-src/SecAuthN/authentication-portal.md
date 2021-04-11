---
description: 程式設計人員會使用驗證技術來建立密碼管理軟體、單一登入驗證、強式驗證、使用者驗證和身分識別驗證。
ms.assetid: 7863dbee-aa48-4024-886c-1056d7141e60
title: '驗證 (驗證) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3989944068ade080b6b819dc34b77c914ed2e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943762"
---
# <a name="authentication-authentication"></a><span data-ttu-id="4ca92-103">驗證 (驗證) </span><span class="sxs-lookup"><span data-stu-id="4ca92-103">Authentication (Authentication)</span></span>

## <a name="purpose"></a><span data-ttu-id="4ca92-104">目的</span><span class="sxs-lookup"><span data-stu-id="4ca92-104">Purpose</span></span>

<span data-ttu-id="4ca92-105">驗證是系統用來驗證使用者登入資訊的程式。</span><span class="sxs-lookup"><span data-stu-id="4ca92-105">Authentication is the process by which the system validates a user's logon information.</span></span> <span data-ttu-id="4ca92-106">使用者的名稱和密碼會與授權清單相比較，如果系統偵測到相符項，則會將存取權授與給該使用者的許可權清單中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="4ca92-106">A user's name and password are compared to an authorized list, and if the system detects a match, access is granted to the extent specified in the permission list for that user.</span></span>

<span data-ttu-id="4ca92-107">Microsoft 驗證技術包括 LSA 驗證、認證管理、智慧卡驗證、網路提供者、安全性支援提供者介面 (SSPI) 、Winlogon 和 GINA。</span><span class="sxs-lookup"><span data-stu-id="4ca92-107">Microsoft authentication technologies include LSA Authentication, Credentials Management, Smart Card Authentication, Network Provider, Security Support Provider Interface (SSPI), Winlogon, and GINA.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4ca92-108">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="4ca92-108">Developer audience</span></span>

<span data-ttu-id="4ca92-109">Microsoft 驗證技術適用于應用程式開發人員，這些應用程式是以驗證用戶端的 Windows Server、Windows Vista 和 Windows 作業系統為基礎的應用程式開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="4ca92-109">Microsoft authentication technologies are intended for use by developers of applications that are based on the Windows Server, Windows Vista, and Windows operating systems that authenticate clients.</span></span> <span data-ttu-id="4ca92-110">開發人員應該熟悉以 Windows 為基礎的程式設計。</span><span class="sxs-lookup"><span data-stu-id="4ca92-110">Developers should be familiar with Windows-based programming.</span></span> <span data-ttu-id="4ca92-111">雖然並非必要，但建議您瞭解驗證或安全性相關的主題。</span><span class="sxs-lookup"><span data-stu-id="4ca92-111">Although not required, an understanding of authentication or security-related subjects is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4ca92-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="4ca92-112">Run-time requirements</span></span>

<span data-ttu-id="4ca92-113">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="4ca92-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4ca92-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="4ca92-114">In this section</span></span>



| <span data-ttu-id="4ca92-115">主題</span><span class="sxs-lookup"><span data-stu-id="4ca92-115">Topic</span></span>                                                               | <span data-ttu-id="4ca92-116">描述</span><span class="sxs-lookup"><span data-stu-id="4ca92-116">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ca92-117">關於驗證</span><span class="sxs-lookup"><span data-stu-id="4ca92-117">About Authentication</span></span>](about-authentication.md)<br/>         | <span data-ttu-id="4ca92-118">重要驗證概念和 Microsoft 驗證技術的高階觀點。</span><span class="sxs-lookup"><span data-stu-id="4ca92-118">Key authentication concepts and a high-level view of Microsoft authentication technologies.</span></span><br/>                           |
| [<span data-ttu-id="4ca92-119">使用驗證</span><span class="sxs-lookup"><span data-stu-id="4ca92-119">Using Authentication</span></span>](using-authentication.md)<br/>         | <span data-ttu-id="4ca92-120">使用 Microsoft 驗證技術之程式的驗證程式、程式和範例。</span><span class="sxs-lookup"><span data-stu-id="4ca92-120">Authentication processes, procedures, and examples of programs that use Microsoft authentication technologies.</span></span><br/>        |
| [<span data-ttu-id="4ca92-121">驗證參考</span><span class="sxs-lookup"><span data-stu-id="4ca92-121">Authentication Reference</span></span>](authentication-reference.md)<br/> | <span data-ttu-id="4ca92-122">驗證函式、介面、物件、結構和其他程式設計項目的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4ca92-122">Detailed information about authentication functions, interfaces, objects, structures, and other programming elements.</span></span><br/> |



 

 

 




