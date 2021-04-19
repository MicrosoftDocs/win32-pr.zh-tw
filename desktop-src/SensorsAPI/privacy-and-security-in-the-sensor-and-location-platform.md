---
description: Windows 感應器和位置平台包含隱私權設定，以協助保護使用者的個人資訊。
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Windows 感應器和位置平台的隱私權與安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973822"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a><span data-ttu-id="67d55-103">Windows 感應器和位置平台的隱私權與安全性</span><span class="sxs-lookup"><span data-stu-id="67d55-103">Privacy and Security in the Windows Sensor and Location Platform</span></span>

<span data-ttu-id="67d55-104">Windows 感應器和位置平台包含隱私權設定，以協助保護使用者的個人資訊。</span><span class="sxs-lookup"><span data-stu-id="67d55-104">The Windows Sensor and Location platform includes privacy settings to help protect users' personal information.</span></span>

<span data-ttu-id="67d55-105">此平臺可協助確保感應器資料在需要隱私權時維持私密，方法如下：</span><span class="sxs-lookup"><span data-stu-id="67d55-105">The platform helps to ensure that sensor data remains private, when privacy is required, in the following ways:</span></span>

-   <span data-ttu-id="67d55-106">感應器預設為關閉。</span><span class="sxs-lookup"><span data-stu-id="67d55-106">By default, sensors are off.</span></span> <span data-ttu-id="67d55-107">由於平臺設計會假設任何感應器都可以提供個人資料，因此每個感應器都會停用，直到使用者明確同意存取感應器資料為止。</span><span class="sxs-lookup"><span data-stu-id="67d55-107">Because the platform design presumes that any sensor can provide personal data, each sensor is disabled until the user provides explicit consent to access the sensor data.</span></span>
-   <span data-ttu-id="67d55-108">Windows 會提供洩漏訊息和使用者的說明內容。</span><span class="sxs-lookup"><span data-stu-id="67d55-108">Windows provides disclosure messages and Help content for the user.</span></span> <span data-ttu-id="67d55-109">此內容可協助使用者瞭解感應器會如何影響其個人資料的隱私權，並協助使用者做出明智的決策。</span><span class="sxs-lookup"><span data-stu-id="67d55-109">This content helps users understand how sensors can affect the privacy of their personal data and helps users make informed decisions.</span></span>
-   <span data-ttu-id="67d55-110">提供感應器的許可權需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="67d55-110">Providing permission for a sensor requires administrator rights.</span></span>
-   <span data-ttu-id="67d55-111">啟用時，感應器裝置適用于在特定使用者帳戶下執行的所有程式 (或所有使用者帳戶) 。</span><span class="sxs-lookup"><span data-stu-id="67d55-111">When it is enabled, a sensor device works for all programs running under a particular user account (or for all user accounts).</span></span> <span data-ttu-id="67d55-112">這包括非互動式使用者和服務，例如 ASPNET 或 SYSTEM。</span><span class="sxs-lookup"><span data-stu-id="67d55-112">This includes noninteractive users and services, such as ASPNET or SYSTEM.</span></span> <span data-ttu-id="67d55-113">例如，如果您為使用者帳戶啟用 GPS 感應器，則只有在您的使用者帳戶下執行的程式才能存取 GPS。</span><span class="sxs-lookup"><span data-stu-id="67d55-113">For example, if you enable a GPS sensor for your user account, only programs running under your user account have access to the GPS.</span></span> <span data-ttu-id="67d55-114">如果您為所有使用者啟用 GPS，則在任何使用者帳戶下執行的任何程式都可以存取 GPS。</span><span class="sxs-lookup"><span data-stu-id="67d55-114">If you enable the GPS for all users, any program running under any user account has access to the GPS.</span></span>
-   <span data-ttu-id="67d55-115">使用感應器的程式可以呼叫方法來開啟系統對話方塊，該對話方塊會提示使用者啟用所需的感應器裝置。</span><span class="sxs-lookup"><span data-stu-id="67d55-115">Programs that use sensors can call a method to open a system dialog box that prompts users to enable needed sensor devices.</span></span> <span data-ttu-id="67d55-116">這項功能可讓開發人員和使用者在程式需要時輕鬆地確保感應器能正常運作，同時保有使用者對感應器資料洩漏的控制權。</span><span class="sxs-lookup"><span data-stu-id="67d55-116">This feature makes it easy for developers and users to make sure that sensors work when programs need them, while maintaining user control of disclosure of sensor data.</span></span>
-   <span data-ttu-id="67d55-117">感應器驅動程式會使用特殊物件來處理所有 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="67d55-117">Sensor drivers use a special object that processes all I/O requests.</span></span> <span data-ttu-id="67d55-118">此物件可確保只有具有使用者權限的程式可以存取感應器資料。</span><span class="sxs-lookup"><span data-stu-id="67d55-118">This object makes sure that only programs that have user permission can access sensor data.</span></span>

 

 



