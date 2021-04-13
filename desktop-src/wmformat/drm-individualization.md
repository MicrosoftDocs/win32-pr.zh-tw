---
title: DRM 的個人化
description: DRM 的個人化
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media Format SDK，DRM 的個人化
- 數位版權管理 (DRM) 、個人化
- DRM (數位版權管理) 、個人化
- DRM 的個人化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300452"
---
# <a name="drm-individualization"></a><span data-ttu-id="30333-107">DRM 的個人化</span><span class="sxs-lookup"><span data-stu-id="30333-107">DRM Individualization</span></span>

<span data-ttu-id="30333-108">受保護內容的擁有者可能會要求使用者在存取其內容之前，先升級 Windows Media Format SDK 中包含的一些數位版權管理 (DRM) 元件。</span><span class="sxs-lookup"><span data-stu-id="30333-108">Owners of protected content may require users to upgrade some of the digital rights management (DRM) components included in the Windows Media Format SDK before accessing their content.</span></span> <span data-ttu-id="30333-109">如果使用者接受升級，則會從 Microsoft 網站下載安全性檔案的個人化版本 (唯一的電腦) 。</span><span class="sxs-lookup"><span data-stu-id="30333-109">If a user accepts the upgrade, an individualized version of a security file (one unique to their computer) will be downloaded from a Microsoft Web site.</span></span> <span data-ttu-id="30333-110">如果使用者拒絕升級，則不能存取內容;不過，他們仍然可以存取未受保護的內容，以及不需要升級的受保護內容。</span><span class="sxs-lookup"><span data-stu-id="30333-110">If the user declines the upgrade, they will not be able to access the content; however, they will still be able to access unprotected content and protected content that does not require the upgrade.</span></span> <span data-ttu-id="30333-111">執行安全性升級有助於提高 DRM 所提供的保護層級。</span><span class="sxs-lookup"><span data-stu-id="30333-111">Performing a security upgrade helps increase the level of protection offered by DRM.</span></span>

<span data-ttu-id="30333-112">在安裝期間，或是當應用程式第一次遇到需要的 protected ASF 檔案時，就可以進行個人化。</span><span class="sxs-lookup"><span data-stu-id="30333-112">Individualization can be done either at setup time or when an application first encounters a protected ASF file that requires it.</span></span> <span data-ttu-id="30333-113">因為此程式會修改使用者的系統元件，所以在執行升級之前，應用程式必須通知使用者並取得其告知同意。</span><span class="sxs-lookup"><span data-stu-id="30333-113">Because this process modifies a user's system components, the application must notify the user and obtain their informed consent before performing the upgrade.</span></span> <span data-ttu-id="30333-114">例如，Microsoft Windows Media Player 會顯示具有下列文字的對話方塊：</span><span class="sxs-lookup"><span data-stu-id="30333-114">Microsoft Windows Media Player, for example, shows a dialog box with the following text:</span></span>

<span data-ttu-id="30333-115">**需要安全性升級**</span><span class="sxs-lookup"><span data-stu-id="30333-115">**Security Upgrade Required**</span></span>

<span data-ttu-id="30333-116">**您嘗試存取的受保護內容的擁有者，必須先在電腦上升級部分 Microsoft 數位版權管理 (DRM) 元件。**</span><span class="sxs-lookup"><span data-stu-id="30333-116">**The owner of the protected content you are trying to access requires you to first upgrade some of the Microsoft digital rights management (DRM) components on your computer.**</span></span>

<span data-ttu-id="30333-117">**按一下 [確定] 升級 DRM 元件。**</span><span class="sxs-lookup"><span data-stu-id="30333-117">**Click OK to upgrade your DRM components.**</span></span>

<span data-ttu-id="30333-118">**細節：**</span><span class="sxs-lookup"><span data-stu-id="30333-118">**Details:**</span></span>

<span data-ttu-id="30333-119">**當您按一下 [確定] 時，會將唯一識別碼和 DRM 安全性檔案傳送至網際網路上的 Microsoft 服務。檔案會取代為包含唯一識別碼的自訂版本。這會增加 DRM 所提供的保護層級。**</span><span class="sxs-lookup"><span data-stu-id="30333-119">**When you click OK, a unique identifier and a DRM security file are sent to a Microsoft service on the Internet. The file is replaced with a customized version that contains your unique identifier. This increases the level of protection provided by DRM.**</span></span>

<span data-ttu-id="30333-120">任何支援個人化的應用程式都應該使用相同或類似的用語。</span><span class="sxs-lookup"><span data-stu-id="30333-120">Any application that supports individualization should use the same or similar wording.</span></span> <span data-ttu-id="30333-121">如需 Microsoft 隱私權原則的詳細資訊，請參閱本檔的 [隱私權聲明](privacy-statement.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="30333-121">For more information on Microsoft's Privacy Policy, see the [Privacy Statement](privacy-statement.md) section of this documentation.</span></span>

> [!Note]  
> <span data-ttu-id="30333-122">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="30333-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="30333-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="30333-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30333-124">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="30333-124">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="30333-125">**Individualizing DRM 應用程式**</span><span class="sxs-lookup"><span data-stu-id="30333-125">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> </dl>

 

 




