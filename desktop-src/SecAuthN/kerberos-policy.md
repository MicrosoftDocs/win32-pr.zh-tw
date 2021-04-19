---
description: Kerberos 票證原則是在網域層級定義，並由網域的金鑰發佈中心 (KDC) 所執行。
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Kerberos 原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983683"
---
# <a name="kerberos-policy"></a><span data-ttu-id="68bbe-103">Kerberos 原則</span><span class="sxs-lookup"><span data-stu-id="68bbe-103">Kerberos Policy</span></span>

<span data-ttu-id="68bbe-104">Kerberos 票證原則是在網域層級定義，並由網域的 [*金鑰發佈中心*](../secgloss/k-gly.md) (KDC) 所執行。</span><span class="sxs-lookup"><span data-stu-id="68bbe-104">Kerberos ticket policy is defined at the domain level and implemented by the domain's [*Key Distribution Center*](../secgloss/k-gly.md) (KDC).</span></span> <span data-ttu-id="68bbe-105">Kerberos 原則會以網域安全性原則的屬性子集的形式儲存在 Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="68bbe-105">Kerberos policy is stored in the Active Directory as a subset of the attributes of domain security policy.</span></span> <span data-ttu-id="68bbe-106">根據預設，原則選項只能由 Domain Administrators 群組的成員設定。</span><span class="sxs-lookup"><span data-stu-id="68bbe-106">By default, policy options can be set only by members of the Domain Administrators group.</span></span> <span data-ttu-id="68bbe-107">網域原則包含下列選項：</span><span class="sxs-lookup"><span data-stu-id="68bbe-107">Domain policy includes options that:</span></span>

-   <span data-ttu-id="68bbe-108">支援遠期票證</span><span class="sxs-lookup"><span data-stu-id="68bbe-108">Support postdated tickets</span></span>
-   <span data-ttu-id="68bbe-109">支援限制委派 (僅限 Windows Server 2003) </span><span class="sxs-lookup"><span data-stu-id="68bbe-109">Support constrained delegation (Windows Server 2003 only)</span></span>
-   <span data-ttu-id="68bbe-110">可以轉寄的支援票證</span><span class="sxs-lookup"><span data-stu-id="68bbe-110">Support tickets that can be forwarded</span></span>
-   <span data-ttu-id="68bbe-111">支援可再生票證</span><span class="sxs-lookup"><span data-stu-id="68bbe-111">Support renewable tickets</span></span>
-   <span data-ttu-id="68bbe-112">設定票證最長使用期限</span><span class="sxs-lookup"><span data-stu-id="68bbe-112">Set maximum ticket age</span></span>
-   <span data-ttu-id="68bbe-113">設定最大續約期限</span><span class="sxs-lookup"><span data-stu-id="68bbe-113">Set maximum renewal age</span></span>
-   <span data-ttu-id="68bbe-114">設定最大 proxy 票證存留期</span><span class="sxs-lookup"><span data-stu-id="68bbe-114">Set maximum proxy ticket age</span></span>
-   <span data-ttu-id="68bbe-115">當票證到期時強制登出使用者</span><span class="sxs-lookup"><span data-stu-id="68bbe-115">Forcibly log off users when tickets expire</span></span>

<span data-ttu-id="68bbe-116">使用 [*限制委派*](../secgloss/c-gly.md)時，可以將電腦設定為只允許將認證轉送到特定的服務清單。</span><span class="sxs-lookup"><span data-stu-id="68bbe-116">With [*constrained delegation*](../secgloss/c-gly.md), a computer can be set to allow forwarding of credentials only to a specific list of services.</span></span> <span data-ttu-id="68bbe-117">這些服務必須位於與轉送認證的電腦相同的網域中。</span><span class="sxs-lookup"><span data-stu-id="68bbe-117">Those services must reside in the same domain as the computer forwarding the credentials.</span></span> <span data-ttu-id="68bbe-118">在 *限制委派* 下，票證不再從用戶端傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="68bbe-118">Under *constrained delegation*, tickets are no longer sent from the client to the server.</span></span> <span data-ttu-id="68bbe-119">伺服器電腦會根據所需的資訊，從用來驗證用戶端的資訊建立服務票證。</span><span class="sxs-lookup"><span data-stu-id="68bbe-119">The server computer creates service tickets to forward as necessary from information used to authenticate the client.</span></span>

<span data-ttu-id="68bbe-120">雖然網域的 Kerberos 原則可能會允許轉送票證來允許委派的驗證，但該原則的部分不需要套用至所有使用者或所有電腦。</span><span class="sxs-lookup"><span data-stu-id="68bbe-120">Although Kerberos policy for a domain may permit delegated authentication by allowing tickets to be forwarded, that aspect of policy need not apply to all users or all computers.</span></span> <span data-ttu-id="68bbe-121">您可以將個別使用者帳戶的屬性設定為停用任何伺服器轉送該使用者的 [*認證*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="68bbe-121">An attribute of an individual user account can be set to disable forwarding of that user's [*credentials*](../secgloss/c-gly.md) by any server.</span></span> <span data-ttu-id="68bbe-122">個別電腦帳戶的屬性可以設定為停用從任何使用者轉送認證。</span><span class="sxs-lookup"><span data-stu-id="68bbe-122">An attribute of an individual computer's account can be set to disable forwarding of credentials from any user.</span></span> <span data-ttu-id="68bbe-123">在這兩種情況下，都可以藉由建立群組原則來停用委派，以套用至 Active Directory 組織單位中的所有使用者或所有電腦。</span><span class="sxs-lookup"><span data-stu-id="68bbe-123">In both cases, delegation can be disabled by creating a group policy to apply to all users or all computers in an organizational unit of the Active Directory.</span></span>

<span data-ttu-id="68bbe-124">**WINDOWS XP/2000：** 不支援限制委派。</span><span class="sxs-lookup"><span data-stu-id="68bbe-124">**Windows XP/2000:** Constrained delegation is not supported.</span></span>

 

 
