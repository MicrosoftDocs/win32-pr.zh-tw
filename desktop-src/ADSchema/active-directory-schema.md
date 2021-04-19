---
title: 'Active Directory 架構 (AD 架構) '
description: Microsoft Active Directory 架構包含可在 Active Directory 樹系中建立的每個物件類別的正式定義。
ms.assetid: b3da4519-d0c6-47eb-9455-ada653ad5c9e
ms.tgt_platform: multiple
keywords:
- Active Directory 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3393a6da1b8d1bd2c2418084c8f7fc657732
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968693"
---
# <a name="active-directory-schema-ad-schema"></a><span data-ttu-id="cfff2-104">Active Directory 架構 (AD 架構) </span><span class="sxs-lookup"><span data-stu-id="cfff2-104">Active Directory Schema (AD Schema)</span></span>

<span data-ttu-id="cfff2-105">Microsoft Active Directory 架構包含可在 Active Directory 樹系中建立的每個物件類別的正式定義。</span><span class="sxs-lookup"><span data-stu-id="cfff2-105">The Microsoft Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="cfff2-106">架構也包含可存在於 Active Directory 物件中之每個屬性的正式定義。</span><span class="sxs-lookup"><span data-stu-id="cfff2-106">The schema also contains formal definitions of every attribute that can exist in an Active Directory object.</span></span> <span data-ttu-id="cfff2-107">本節提供每個架構物件的參考，並提供組成 Active Directory 架構之屬性、類別和其他物件的簡短說明。</span><span class="sxs-lookup"><span data-stu-id="cfff2-107">This section provides the reference for each schema object and provides a brief explanation of the attributes, classes, and other objects that make up the Active Directory schema.</span></span>

> [!Note]  
> <span data-ttu-id="cfff2-108">下列檔包含 Active Directory 架構的程式設計參考。</span><span class="sxs-lookup"><span data-stu-id="cfff2-108">The following documentation contains the programming reference for Active Directory schema.</span></span> <span data-ttu-id="cfff2-109">如果您是嘗試偵測印表機錯誤的終端使用者，請嘗試在 [Microsoft 社區網站](https://answers.microsoft.com)上搜尋。</span><span class="sxs-lookup"><span data-stu-id="cfff2-109">If you are an end-user attempting to debug a printer error, try searching on the [Microsoft community site](https://answers.microsoft.com).</span></span> <span data-ttu-id="cfff2-110">如果您是開發人員尋找 Active Directory 架構的一般總覽，請參閱 [Active Directory 架構](/windows/desktop/AD/active-directory-schema) 總覽主題。</span><span class="sxs-lookup"><span data-stu-id="cfff2-110">If you are a developer looking for a general overview of Active Directory schema, see the [Active Directory Schema](/windows/desktop/AD/active-directory-schema) overview topics.</span></span> <span data-ttu-id="cfff2-111">如果您要尋找更新或修改架構的程式設計指導方針，如需擴充和自訂架構的詳細資訊，請參閱 [延伸架構](/windows/desktop/AD/extending-the-schema)，以及 [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) 和 [Active Directory 輕量型目錄服務](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) 程式設計指南中的許多主題。</span><span class="sxs-lookup"><span data-stu-id="cfff2-111">If you are looking for programming guidelines for updating or modifying the schema, For more information about extending and customizing the schema, see [Extending the Schema](/windows/desktop/AD/extending-the-schema), as well as many of the topics in the [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) and [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) programming guides.</span></span>

 

<span data-ttu-id="cfff2-112">在每個參考主題中，主題適用的每個作業系統都有一個區段。</span><span class="sxs-lookup"><span data-stu-id="cfff2-112">In each of the reference topics, there is a section for each operating system that the topic applies to.</span></span> <span data-ttu-id="cfff2-113">目前支援下列作業系統。</span><span class="sxs-lookup"><span data-stu-id="cfff2-113">The following operating systems are currently supported.</span></span> 

| <span data-ttu-id="cfff2-114">平台</span><span class="sxs-lookup"><span data-stu-id="cfff2-114">Platform</span></span>                                                      | <span data-ttu-id="cfff2-115">主題中的名稱</span><span class="sxs-lookup"><span data-stu-id="cfff2-115">Name in topic</span></span>                               |
|---------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="cfff2-116">Microsoft Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfff2-116">Microsoft Windows Server 2003</span></span><br/>                      | <span data-ttu-id="cfff2-117">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfff2-117">Windows Server 2003</span></span><br/>              |
| <span data-ttu-id="cfff2-118">Microsoft Active Directory 應用程式模式 (ADAM) </span><span class="sxs-lookup"><span data-stu-id="cfff2-118">Microsoft Active Directory Application Mode (ADAM)</span></span><br/> | <span data-ttu-id="cfff2-119">亞當</span><span class="sxs-lookup"><span data-stu-id="cfff2-119">ADAM</span></span><br/>                             |
| <span data-ttu-id="cfff2-120">Microsoft Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cfff2-120">Microsoft Windows Server 2003 R2</span></span><br/>                   | <span data-ttu-id="cfff2-121">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cfff2-121">Windows Server 2003 R2</span></span><br/>           |
| <span data-ttu-id="cfff2-122">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfff2-122">Microsoft Windows Server 2008</span></span><br/>                      | <span data-ttu-id="cfff2-123">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfff2-123">Microsoft Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="cfff2-124">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfff2-124">Microsoft Windows Server 2008 R2</span></span><br/>                   | <span data-ttu-id="cfff2-125">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfff2-125">Microsoft Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="cfff2-126">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfff2-126">Microsoft Windows Server 2012</span></span><br/>                      | <span data-ttu-id="cfff2-127">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cfff2-127">Microsoft Windows Server 2012</span></span><br/>    |



 

<span data-ttu-id="cfff2-128">如果主題中未列出作業系統，則該作業系統不支援該主題。</span><span class="sxs-lookup"><span data-stu-id="cfff2-128">If an operating system is not listed in the topic, the topic is not supported on that operating system.</span></span> <span data-ttu-id="cfff2-129">例如，如果主題只列出 Windows Server 2003 和 ADAM，則本主題不適用於 Windows Server 2003 R2。</span><span class="sxs-lookup"><span data-stu-id="cfff2-129">For example, if a topic only lists Windows Server 2003 and ADAM, then the topic does not apply to Windows Server 2003 R2.</span></span>

<span data-ttu-id="cfff2-130">下列各節包含 Active Directory 架構元素的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cfff2-130">The following sections contain detailed information about the Active Directory schema elements.</span></span>

-   [<span data-ttu-id="cfff2-131">Active Directory 架構術語</span><span class="sxs-lookup"><span data-stu-id="cfff2-131">Active Directory Schema Terminology</span></span>](active-directory-schema-site.md)
-   [<span data-ttu-id="cfff2-132">類別</span><span class="sxs-lookup"><span data-stu-id="cfff2-132">Classes</span></span>](classes.md)
-   [<span data-ttu-id="cfff2-133">屬性</span><span class="sxs-lookup"><span data-stu-id="cfff2-133">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="cfff2-134">語法</span><span class="sxs-lookup"><span data-stu-id="cfff2-134">Syntaxes</span></span>](syntaxes.md)
-   [<span data-ttu-id="cfff2-135">控制存取權限</span><span class="sxs-lookup"><span data-stu-id="cfff2-135">Control Access Rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="cfff2-136">RootDSE</span><span class="sxs-lookup"><span data-stu-id="cfff2-136">RootDSE</span></span>](rootdse.md)

 

