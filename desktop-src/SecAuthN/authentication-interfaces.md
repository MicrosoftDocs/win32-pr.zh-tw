---
description: 列出驗證 Api 中的介面。
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: 驗證介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193288"
---
# <a name="authentication-interfaces"></a><span data-ttu-id="8481b-103">驗證介面</span><span class="sxs-lookup"><span data-stu-id="8481b-103">Authentication Interfaces</span></span>

<span data-ttu-id="8481b-104">驗證介面會根據使用方式進行分類，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8481b-104">Authentication interfaces are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="8481b-105">智慧卡介面</span><span class="sxs-lookup"><span data-stu-id="8481b-105">Smart Card Interfaces</span></span>](#smart-card-interfaces)
-   [<span data-ttu-id="8481b-106">身分識別共用介面</span><span class="sxs-lookup"><span data-stu-id="8481b-106">Identity Sharing Interfaces</span></span>](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a><span data-ttu-id="8481b-107">智慧卡介面</span><span class="sxs-lookup"><span data-stu-id="8481b-107">Smart Card Interfaces</span></span>

<span data-ttu-id="8481b-108">智慧卡 SDK 提供下列 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="8481b-108">The Smart Card SDK provides the following COM interfaces.</span></span> <span data-ttu-id="8481b-109">特定介面的方法會列在 [目錄] 和該介面的 [參考] 頁面上。</span><span class="sxs-lookup"><span data-stu-id="8481b-109">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="8481b-110">介面</span><span class="sxs-lookup"><span data-stu-id="8481b-110">Interface</span></span>                                    | <span data-ttu-id="8481b-111">描述</span><span class="sxs-lookup"><span data-stu-id="8481b-111">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8481b-112">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="8481b-112">**IByteBuffer**</span></span>](ibytebuffer.md)           | <span data-ttu-id="8481b-113">管理資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="8481b-113">Manages a stream object.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="8481b-114">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="8481b-114">**ISCard**</span></span>](iscard.md)                     | <span data-ttu-id="8481b-115">開啟並管理與 [*智慧卡*](/windows/desktop/SecGloss/s-gly)的連接。</span><span class="sxs-lookup"><span data-stu-id="8481b-115">Opens and manages a connection to a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span>                                                                    |
| [<span data-ttu-id="8481b-116">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="8481b-116">**ISCardAuth**</span></span>](iscardauth.md)             | <span data-ttu-id="8481b-117">驗證應用程式、智慧卡或使用者。</span><span class="sxs-lookup"><span data-stu-id="8481b-117">Authenticates an application, smart card, or user.</span></span>                                                                                                                                       |
| [<span data-ttu-id="8481b-118">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="8481b-118">**ISCardCmd**</span></span>](iscardcmd.md)               | <span data-ttu-id="8481b-119"> (APDU) 來建立和管理智慧卡 [*應用程式協定資料單位*](/windows/desktop/SecGloss/a-gly) 。</span><span class="sxs-lookup"><span data-stu-id="8481b-119">Constructs and manages a smart card [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) (APDU).</span></span> |
| [<span data-ttu-id="8481b-120">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="8481b-120">**ISCardDatabase**</span></span>](iscarddatabase.md)     | <span data-ttu-id="8481b-121">執行智慧卡 [*資源管理員*](/windows/desktop/SecGloss/r-gly) 資料庫作業。</span><span class="sxs-lookup"><span data-stu-id="8481b-121">Performs smart card [*resource manager*](/windows/desktop/SecGloss/r-gly) database operations.</span></span>                                              |
| [<span data-ttu-id="8481b-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="8481b-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md) | <span data-ttu-id="8481b-123">執行常見的檔案服務，例如尋找、選取、讀取、寫入、建立和刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="8481b-123">Performs common file services such as locating, selecting, reading, writing, creating, and deleting files.</span></span>                                                                               |
| [<span data-ttu-id="8481b-124">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="8481b-124">**ISCardISO7816**</span></span>](iscardiso7816.md)       | <span data-ttu-id="8481b-125">構造 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="8481b-125">Constructs an APDU command.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="8481b-126">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="8481b-126">**ISCardLocate**</span></span>](iscardlocate.md)         | <span data-ttu-id="8481b-127">尋找智慧卡。</span><span class="sxs-lookup"><span data-stu-id="8481b-127">Locates a smart card.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="8481b-128">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="8481b-128">**ISCardManage**</span></span>](iscardmanage.md)         | <span data-ttu-id="8481b-129">管理智慧卡系統。</span><span class="sxs-lookup"><span data-stu-id="8481b-129">Manages the smart card system.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="8481b-130">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="8481b-130">**ISCardTypeConv**</span></span>](iscardtypeconv.md)     | <span data-ttu-id="8481b-131">提供用來支援其他智慧卡 COM 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="8481b-131">Provides methods used to support other smart card COM interfaces.</span></span> <span data-ttu-id="8481b-132">這個介面僅提供回溯相容性，不應再使用。</span><span class="sxs-lookup"><span data-stu-id="8481b-132">This interface is provided for backward compatibility only and should no longer be used.</span></span>                               |
| [<span data-ttu-id="8481b-133">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="8481b-133">**ISCardVerify**</span></span>](iscardverify.md)         | <span data-ttu-id="8481b-134">驗證或變更信用卡持有者驗證 (CHV) 原則。</span><span class="sxs-lookup"><span data-stu-id="8481b-134">Verifies or changes card holder verification (CHV) policy.</span></span>                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a><span data-ttu-id="8481b-135">身分識別共用介面</span><span class="sxs-lookup"><span data-stu-id="8481b-135">Identity Sharing Interfaces</span></span>

<span data-ttu-id="8481b-136">身分識別共用 SDK 提供下列 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="8481b-136">The Identity Sharing SDK provides the following COM interfaces.</span></span> <span data-ttu-id="8481b-137">特定介面的方法會列在 [目錄] 和該介面的 [參考] 頁面上。</span><span class="sxs-lookup"><span data-stu-id="8481b-137">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="8481b-138">介面</span><span class="sxs-lookup"><span data-stu-id="8481b-138">Interface</span></span>                                                          | <span data-ttu-id="8481b-139">描述</span><span class="sxs-lookup"><span data-stu-id="8481b-139">Description</span></span>                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8481b-140">**IAssociatedIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="8481b-140">**IAssociatedIdentityProvider**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | <span data-ttu-id="8481b-141">允許身分識別提供者將身分識別與本機使用者帳戶建立關聯。</span><span class="sxs-lookup"><span data-stu-id="8481b-141">Allows an identity provider to associate identities with local user accounts.</span></span>            |
| [<span data-ttu-id="8481b-142">**IIdentityAdvise**</span><span class="sxs-lookup"><span data-stu-id="8481b-142">**IIdentityAdvise**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | <span data-ttu-id="8481b-143">允許身分識別提供者在更新身分識別時通知呼叫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8481b-143">Allows an identity provider to notify a calling application when an identity is updated.</span></span> |
| [<span data-ttu-id="8481b-144">**IIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="8481b-144">**IIdentityProvider**</span></span>](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | <span data-ttu-id="8481b-145">代表身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="8481b-145">Represents an identity provider.</span></span>                                                         |
| [<span data-ttu-id="8481b-146">**IIdentityStore**</span><span class="sxs-lookup"><span data-stu-id="8481b-146">**IIdentityStore**</span></span>](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | <span data-ttu-id="8481b-147">提供列舉和管理身分識別和身分識別提供者的方法。</span><span class="sxs-lookup"><span data-stu-id="8481b-147">Provides methods to enumerate and manage identities and identity providers.</span></span>              |



 

 

 
