---
title: 使用 NPS 擴充功能
description: 瞭解如何使用 NPS 擴充功能。 網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- 網際網路驗證服務 IAS，工作
- 網際網路驗證服務 IAS，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989066"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="a4304-106">使用 NPS 擴充功能</span><span class="sxs-lookup"><span data-stu-id="a4304-106">Using NPS Extensions</span></span>

<span data-ttu-id="a4304-107">網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="a4304-107">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="a4304-108">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="a4304-108">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="a4304-109">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="a4304-109">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="a4304-110">\* \* Windows Server 2008 R2 和 Windows Server 2008： \* \*</span><span class="sxs-lookup"><span data-stu-id="a4304-110">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="a4304-111">撥入和 MapName 範例會擴充 NPS 功能。</span><span class="sxs-lookup"><span data-stu-id="a4304-111">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="a4304-112">範例</span><span class="sxs-lookup"><span data-stu-id="a4304-112">Sample</span></span>             | <span data-ttu-id="a4304-113">描述</span><span class="sxs-lookup"><span data-stu-id="a4304-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4304-114">撥</span><span class="sxs-lookup"><span data-stu-id="a4304-114">DialIn</span></span><br/>  | <span data-ttu-id="a4304-115">此範例會執行 RADIUS 延伸模組 DLL，以檢查使用者的撥入位。</span><span class="sxs-lookup"><span data-stu-id="a4304-115">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="a4304-116">MapName</span><span class="sxs-lookup"><span data-stu-id="a4304-116">MapName</span></span><br/> | <span data-ttu-id="a4304-117">此範例延伸模組 DLL 會搜尋指定帳戶的所有受信任網域。</span><span class="sxs-lookup"><span data-stu-id="a4304-117">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="a4304-118">這可讓來自多個網域的使用者進行驗證，而不需要使用者提供其功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a4304-118">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="a4304-119">您可以在下列清單中找到 MapName 和撥入範例應用程式的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="a4304-119">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="a4304-120">*位置*，% 安裝路徑%，指定 x64 電腦的基底安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="a4304-120">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="a4304-121">另請參閱 [Windows 軟體開發套件 (sdk) 以取得 Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)、Microsoft WINDOWS 軟體開發套件 (sdk) ，以及 [適用于 Windows Store 應用程式開發的下載](https://msdn.microsoft.com/windows/apps/br229516)。</span><span class="sxs-lookup"><span data-stu-id="a4304-121">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="a4304-122">Windows 8 的 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a4304-122">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="a4304-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4304-123">Windows Server 2012</span></span>

<span data-ttu-id="a4304-124">下載連結： N/A</span><span class="sxs-lookup"><span data-stu-id="a4304-124">Download link: N/A</span></span>

<span data-ttu-id="a4304-125">MapName：否</span><span class="sxs-lookup"><span data-stu-id="a4304-125">MapName: No</span></span>

<span data-ttu-id="a4304-126">撥入：否</span><span class="sxs-lookup"><span data-stu-id="a4304-126">DialIn: No</span></span>

<span data-ttu-id="a4304-127">位置： N/A</span><span class="sxs-lookup"><span data-stu-id="a4304-127">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="a4304-128">適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK) </span><span class="sxs-lookup"><span data-stu-id="a4304-128">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="a4304-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4304-129">Windows Server 2008 R2</span></span>

<span data-ttu-id="a4304-130">下載連結： <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="a4304-130">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="a4304-131">MapName：是</span><span class="sxs-lookup"><span data-stu-id="a4304-131">MapName: Yes</span></span>

<span data-ttu-id="a4304-132">撥入：否</span><span class="sxs-lookup"><span data-stu-id="a4304-132">DialIn: No</span></span>

<span data-ttu-id="a4304-133">位置：% 安裝路徑% \\ Microsoft sdk \\ Windows \\ 7.1 \\ 範例 \\ netds \\ ias</span><span class="sxs-lookup"><span data-stu-id="a4304-133">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="a4304-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a4304-134">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="a4304-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4304-135">Windows Server 2008</span></span>

<span data-ttu-id="a4304-136">下載連結： <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="a4304-136">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="a4304-137">MapName：是</span><span class="sxs-lookup"><span data-stu-id="a4304-137">MapName: Yes</span></span>

<span data-ttu-id="a4304-138">撥入：否</span><span class="sxs-lookup"><span data-stu-id="a4304-138">DialIn: No</span></span>

<span data-ttu-id="a4304-139">位置：% 安裝路徑% \\ Microsoft sdk \\ Windows \\ 6.1 \\ 範例 \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="a4304-139">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a4304-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4304-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4304-141">適用于開發人員的下載</span><span class="sxs-lookup"><span data-stu-id="a4304-141">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="a4304-142">Windows 8 的 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a4304-142">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





