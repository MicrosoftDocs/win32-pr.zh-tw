---
title: 使用 NPS 擴充功能
description: 網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- 網際網路驗證服務 IAS，工作
- 網際網路驗證服務 IAS，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104507844"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="c9c83-105">使用 NPS 擴充功能</span><span class="sxs-lookup"><span data-stu-id="c9c83-105">Using NPS Extensions</span></span>

<span data-ttu-id="c9c83-106">網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="c9c83-106">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="c9c83-107">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="c9c83-107">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="c9c83-108">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="c9c83-108">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="c9c83-109">\* \* Windows Server 2008 R2 和 Windows Server 2008： \* \*</span><span class="sxs-lookup"><span data-stu-id="c9c83-109">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="c9c83-110">撥入和 MapName 範例會擴充 NPS 功能。</span><span class="sxs-lookup"><span data-stu-id="c9c83-110">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="c9c83-111">範例</span><span class="sxs-lookup"><span data-stu-id="c9c83-111">Sample</span></span>             | <span data-ttu-id="c9c83-112">描述</span><span class="sxs-lookup"><span data-stu-id="c9c83-112">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c83-113">撥</span><span class="sxs-lookup"><span data-stu-id="c9c83-113">DialIn</span></span><br/>  | <span data-ttu-id="c9c83-114">此範例會執行 RADIUS 延伸模組 DLL，以檢查使用者的撥入位。</span><span class="sxs-lookup"><span data-stu-id="c9c83-114">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="c9c83-115">MapName</span><span class="sxs-lookup"><span data-stu-id="c9c83-115">MapName</span></span><br/> | <span data-ttu-id="c9c83-116">此範例延伸模組 DLL 會搜尋指定帳戶的所有受信任網域。</span><span class="sxs-lookup"><span data-stu-id="c9c83-116">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="c9c83-117">這可讓來自多個網域的使用者進行驗證，而不需要使用者提供其功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="c9c83-117">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="c9c83-118">您可以在下列清單中找到 MapName 和撥入範例應用程式的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="c9c83-118">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="c9c83-119">*位置*，% 安裝路徑%，指定 x64 電腦的基底安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="c9c83-119">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="c9c83-120">另請參閱 [Windows 軟體開發套件 (sdk) 以取得 Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)、Microsoft WINDOWS 軟體開發套件 (sdk) ，以及 [適用于 Windows Store 應用程式開發的下載](https://msdn.microsoft.com/windows/apps/br229516)。</span><span class="sxs-lookup"><span data-stu-id="c9c83-120">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="c9c83-121">Windows 8 的 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c9c83-121">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="c9c83-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9c83-122">Windows Server 2012</span></span>

<span data-ttu-id="c9c83-123">下載連結： N/A</span><span class="sxs-lookup"><span data-stu-id="c9c83-123">Download link: N/A</span></span>

<span data-ttu-id="c9c83-124">MapName：否</span><span class="sxs-lookup"><span data-stu-id="c9c83-124">MapName: No</span></span>

<span data-ttu-id="c9c83-125">撥入：否</span><span class="sxs-lookup"><span data-stu-id="c9c83-125">DialIn: No</span></span>

<span data-ttu-id="c9c83-126">位置： N/A</span><span class="sxs-lookup"><span data-stu-id="c9c83-126">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="c9c83-127">適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK) </span><span class="sxs-lookup"><span data-stu-id="c9c83-127">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="c9c83-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9c83-128">Windows Server 2008 R2</span></span>

<span data-ttu-id="c9c83-129">下載連結： <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="c9c83-129">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="c9c83-130">MapName：是</span><span class="sxs-lookup"><span data-stu-id="c9c83-130">MapName: Yes</span></span>

<span data-ttu-id="c9c83-131">撥入：否</span><span class="sxs-lookup"><span data-stu-id="c9c83-131">DialIn: No</span></span>

<span data-ttu-id="c9c83-132">位置：% 安裝路徑% \\ Microsoft sdk \\ Windows \\ 7.1 \\ 範例 \\ netds \\ ias</span><span class="sxs-lookup"><span data-stu-id="c9c83-132">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="c9c83-133">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c9c83-133">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="c9c83-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9c83-134">Windows Server 2008</span></span>

<span data-ttu-id="c9c83-135">下載連結： <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="c9c83-135">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="c9c83-136">MapName：是</span><span class="sxs-lookup"><span data-stu-id="c9c83-136">MapName: Yes</span></span>

<span data-ttu-id="c9c83-137">撥入：否</span><span class="sxs-lookup"><span data-stu-id="c9c83-137">DialIn: No</span></span>

<span data-ttu-id="c9c83-138">位置：% 安裝路徑% \\ Microsoft sdk \\ Windows \\ 6.1 \\ 範例 \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="c9c83-138">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c9c83-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9c83-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9c83-140">適用于開發人員的下載</span><span class="sxs-lookup"><span data-stu-id="c9c83-140">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="c9c83-141">Windows 8 的 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c9c83-141">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





