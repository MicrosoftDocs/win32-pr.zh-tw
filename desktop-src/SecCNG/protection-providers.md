---
description: 從 Windows 8 開始，Microsoft 開始散發可讓您安全地在電腦之間共用加密秘密和訊息的提供者。
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: 保護提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943930"
---
# <a name="protection-providers"></a><span data-ttu-id="fa162-103">保護提供者</span><span class="sxs-lookup"><span data-stu-id="fa162-103">Protection Providers</span></span>

<span data-ttu-id="fa162-104">從 Windows 8 開始，Microsoft 開始散發可讓您安全地在電腦之間共用加密秘密和訊息的提供者。</span><span class="sxs-lookup"><span data-stu-id="fa162-104">Beginning with Windows 8, Microsoft began distributing the providers that enable you to securely share encrypted secrets and messages across computers.</span></span> <span data-ttu-id="fa162-105">目前有兩個金鑰保護提供者。</span><span class="sxs-lookup"><span data-stu-id="fa162-105">There are currently two key protection providers.</span></span> <span data-ttu-id="fa162-106">Microsoft 金鑰保護提供者可讓您保護 Active Directory 樹系中群組的內容。</span><span class="sxs-lookup"><span data-stu-id="fa162-106">The Microsoft Key Protection provider allows you to protect content to a group in an Active Directory forest.</span></span> <span data-ttu-id="fa162-107">Microsoft 用戶端金鑰保護提供者可讓您將內容保護為一組 web 認證。</span><span class="sxs-lookup"><span data-stu-id="fa162-107">The Microsoft Client Key Protection provider allows you to protect content to a set of web credentials.</span></span>

<span data-ttu-id="fa162-108">當 [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) 函式剖析您提供做為輸入的保護描述項規則字串時，會自動為您選擇所要使用的正確保護裝置。</span><span class="sxs-lookup"><span data-stu-id="fa162-108">The correct protector to use is automatically chosen for you when the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function parses the protection descriptor rule string your provide as input.</span></span> <span data-ttu-id="fa162-109">針對以 SID、SDDL 和本機開頭的規則字串選擇 Microsoft 金鑰保護提供者。</span><span class="sxs-lookup"><span data-stu-id="fa162-109">The Microsoft Key Protection provider is chosen for rule strings that begin with SID, SDDL, and LOCAL.</span></span> <span data-ttu-id="fa162-110">Microsoft 用戶端金鑰保護提供者會剖析以 WEBCREDENTIALS 開頭的規則字串。</span><span class="sxs-lookup"><span data-stu-id="fa162-110">The Microsoft Client Key Protection provider parses rule strings that begin with WEBCREDENTIALS.</span></span> <span data-ttu-id="fa162-111">如需規則字串的詳細資訊，請參閱 [保護描述](protection-descriptors.md)項。</span><span class="sxs-lookup"><span data-stu-id="fa162-111">For more information about rule strings, see [Protection Descriptors](protection-descriptors.md).</span></span>

> [!Note]  
> <span data-ttu-id="fa162-112">目前不允許自訂提供者。[CNG DPAPI](cng-dpapi.md)</span><span class="sxs-lookup"><span data-stu-id="fa162-112">Custom providers are not currently allowed.[CNG DPAPI](cng-dpapi.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fa162-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa162-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa162-114">CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="fa162-114">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="fa162-115">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fa162-115">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[<span data-ttu-id="fa162-116">保護描述項</span><span class="sxs-lookup"><span data-stu-id="fa162-116">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> </dl>

 

 



