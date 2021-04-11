---
description: 每一電腦的系統原則可用來指定 Windows Installer 在使用較高許可權的受控安裝期間，將所有公用屬性傳遞至伺服器端。
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114569"
---
# <a name="enableusercontrol"></a><span data-ttu-id="7d9f4-103">EnableUserControl</span><span class="sxs-lookup"><span data-stu-id="7d9f4-103">EnableUserControl</span></span>

<span data-ttu-id="7d9f4-104">在受控安裝的情況下，封裝作者可能需要限制哪些公用屬性會傳遞至伺服器端，並且可由非系統管理員的使用者進行變更。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-104">In the case of a managed installation, the package author may need to limit which public properties are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="7d9f4-105">當安裝要求安裝程式需要使用較高的許可權時，通常需要一些限制才能維護安全的環境。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span>

<span data-ttu-id="7d9f4-106">如果每一電腦的 [系統原則](system-policy.md) 設定為 "1"，則安裝程式可以在使用較高許可權的受控安裝期間，將所有 [公用屬性](public-properties.md) 傳遞至伺服器端。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-106">If this per-machine [system policy](system-policy.md) is set to "1", then the installer can pass all [public properties](public-properties.md) to the server side during a managed installation using elevated privileges.</span></span> <span data-ttu-id="7d9f4-107">設定此原則的效果與設定 **EnableUserControl** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-107">Setting this policy has the same effect as setting the **EnableUserControl** property.</span></span> <span data-ttu-id="7d9f4-108">設定此原則可讓所有公用屬性都傳遞至服務，並由非管理員使用者進行變更。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-108">Setting this policy allows all public properties to be passed to the service and to be changeable by nonadministrative users.</span></span> <span data-ttu-id="7d9f4-109">依預設，不會啟用此原則;只有受限制的公用屬性會傳遞至伺服器端，並由非系統管理員的使用者進行變更。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-109">By default, this policy is not enabled; only restricted public properties are passed to the server side and changeable by a nonadministrative user.</span></span> <span data-ttu-id="7d9f4-110">所有其他公用屬性都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-110">All other public properties are ignored.</span></span>

<span data-ttu-id="7d9f4-111">如果作業系統是 Windows 2000、使用者不是系統管理員，而且應用程式或產品是以較高的許可權安裝，則不是系統管理員的使用者只能覆寫受限制公用屬性的核准清單。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-111">If the operating system is Windows 2000, the user is not a system administrator, and the application or product is being installed with elevated privileges, then a user that is not a system administrator can only override an approved list of restricted public properties.</span></span> <span data-ttu-id="7d9f4-112">如需詳細資訊，請參閱 [限制的公用屬性](restricted-public-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="7d9f4-112">For more information see [Restricted Public Properties](restricted-public-properties.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="7d9f4-113">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="7d9f4-113">Registry Key</span></span>

<span data-ttu-id="7d9f4-114">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="7d9f4-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="7d9f4-115">資料類型</span><span class="sxs-lookup"><span data-stu-id="7d9f4-115">Data Type</span></span>

<span data-ttu-id="7d9f4-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7d9f4-116">**REG\_DWORD**</span></span>

 

 



