---
description: 是針對登入會話執行互動式登入的 Windows 模組。 您可以藉由執行和註冊認證提供者來自訂 Winlogon 行為。
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon 和認證提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943365"
---
# <a name="winlogon-and-credential-providers"></a><span data-ttu-id="d44f3-104">Winlogon 和認證提供者</span><span class="sxs-lookup"><span data-stu-id="d44f3-104">Winlogon and Credential Providers</span></span>

<span data-ttu-id="d44f3-105">[*Winlogon*](../secgloss/w-gly.md) 是針對 [*登入會話*](../secgloss/l-gly.md)執行互動式登入的 Windows 模組。</span><span class="sxs-lookup"><span data-stu-id="d44f3-105">[*Winlogon*](../secgloss/w-gly.md) is the Windows module that performs interactive logon for a [*logon session*](../secgloss/l-gly.md).</span></span> <span data-ttu-id="d44f3-106">您可以藉由執行和註冊認證提供者來自訂 Winlogon 行為。</span><span class="sxs-lookup"><span data-stu-id="d44f3-106">Winlogon behavior can be customized by implementing and registering a Credential Provider.</span></span>

<span data-ttu-id="d44f3-107">如需有關如何執行認證提供者的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="d44f3-107">For information about implementing a Credential Provider, see the following topics.</span></span>



| <span data-ttu-id="d44f3-108">主題</span><span class="sxs-lookup"><span data-stu-id="d44f3-108">Topic</span></span>                                                                                                           | <span data-ttu-id="d44f3-109">描述</span><span class="sxs-lookup"><span data-stu-id="d44f3-109">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d44f3-110">認證提供者驅動的 Windows 登入體驗</span><span class="sxs-lookup"><span data-stu-id="d44f3-110">Credential Provider driven Windows Logon Experience</span></span>](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | <span data-ttu-id="d44f3-111">Winlogon 和認證提供者架構的總覽，以及範例認證提供者。</span><span class="sxs-lookup"><span data-stu-id="d44f3-111">Overview of Winlogon and Credential Provider architecture and a sample Credential Provider.</span></span><br/> |
| [<span data-ttu-id="d44f3-112">Shell 介面</span><span class="sxs-lookup"><span data-stu-id="d44f3-112">Shell Interfaces</span></span>](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | <span data-ttu-id="d44f3-113">認證提供者介面參考。</span><span class="sxs-lookup"><span data-stu-id="d44f3-113">Credential Provider interface reference.</span></span><br/>                                                    |
| [<span data-ttu-id="d44f3-114">Windows 10 中的認證提供者</span><span class="sxs-lookup"><span data-stu-id="d44f3-114">Credential Providers in Windows 10</span></span>](credential-providers-in-windows.md)<br/>                            | <span data-ttu-id="d44f3-115">Windows 10 中的協力廠商認證提供者和系統認證提供者。</span><span class="sxs-lookup"><span data-stu-id="d44f3-115">Third-party credential providers and system credential providers in Windows 10.</span></span><br/>             |



 

<span data-ttu-id="d44f3-116">如需範例認證提供者的範例，請參閱位於 Windows SDK 安裝目錄中的範例 \\ \\ 安全性 \\ credentialprovider.h。</span><span class="sxs-lookup"><span data-stu-id="d44f3-116">For a sample Credential Provider implementation, see the sample located in the Windows SDK installation directory under \\Samples\\Security\\CredentialProvider.</span></span>

<span data-ttu-id="d44f3-117">**Windows Server 2003 和 WINDOWS XP：** 不支援認證提供者。</span><span class="sxs-lookup"><span data-stu-id="d44f3-117">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span> <span data-ttu-id="d44f3-118">如需自訂 Winlogon 的詳細資訊，請參閱 [Winlogon 和 GINA](winlogon-and-gina.md)。</span><span class="sxs-lookup"><span data-stu-id="d44f3-118">For information about customizing Winlogon, see [Winlogon and GINA](winlogon-and-gina.md).</span></span>

 

 
