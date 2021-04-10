---
title: 在 Active Directory Domain Services 中控制物件存取
description: 每個 Active Directory 目錄服務物件都會受到 Windows 2000 安全性的保護。
ms.assetid: 0821069d-76bd-49cb-a617-8446d26e61d9
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services，使用安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cac744ef63fa95c45d5af535f5155378d479fdb
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/04/2019
ms.locfileid: "104022894"
---
# <a name="controlling-object-access-in-active-directory-domain-services"></a><span data-ttu-id="38a81-104">在 Active Directory Domain Services 中控制物件存取</span><span class="sxs-lookup"><span data-stu-id="38a81-104">Controlling object access in Active Directory Domain Services</span></span>

<span data-ttu-id="38a81-105">每個 Active Directory 目錄服務物件都會受到 Windows 2000 安全性的保護。</span><span class="sxs-lookup"><span data-stu-id="38a81-105">Each Active Directory directory service object is protected by Windows 2000 security.</span></span> <span data-ttu-id="38a81-106">此安全性保護可控制每個安全性主體可在目錄中執行的作業。</span><span class="sxs-lookup"><span data-stu-id="38a81-106">This security protection controls the operations that each security principal can perform in the directory.</span></span> <span data-ttu-id="38a81-107">下列各節說明啟用目錄的應用程式如何使用 Active Directory 中的存取控制功能。</span><span class="sxs-lookup"><span data-stu-id="38a81-107">The following sections describe how a directory-enabled application can use the access control features in Active Directory.</span></span>

-   [<span data-ttu-id="38a81-108">存取控制在 Active Directory Domain Services 中的運作方式</span><span class="sxs-lookup"><span data-stu-id="38a81-108">How Access Control Works in Active Directory Domain Services</span></span>](how-access-control-works-in-active-directory-domain-services.md)
-   [<span data-ttu-id="38a81-109">存取控制會如何影響讀取作業、寫入作業、物件的建立和刪除。</span><span class="sxs-lookup"><span data-stu-id="38a81-109">How access control affects read operations, write operation, object creation and deletion.</span></span>](how-security-affects-operations-in-active-directory-domain-services.md)
-   [<span data-ttu-id="38a81-110">使用 IADs 和 IDirectoryObject 介面處理物件的安全描述項</span><span class="sxs-lookup"><span data-stu-id="38a81-110">Using the IADs and IDirectoryObject interfaces to work with an object's security descriptor</span></span>](apis-for-working-with-security-descriptors.md)
-   [<span data-ttu-id="38a81-111">修改物件的存取權限</span><span class="sxs-lookup"><span data-stu-id="38a81-111">Modifying the access permissions on an object</span></span>](setting-access-rights-on-an-object.md)
-   [<span data-ttu-id="38a81-112">如何在新的目錄物件上設定安全描述項</span><span class="sxs-lookup"><span data-stu-id="38a81-112">How security descriptors are set on new directory objects</span></span>](how-security-descriptors-are-set-on-new-directory-objects.md)
-   [<span data-ttu-id="38a81-113">建立新目錄物件的安全描述項</span><span class="sxs-lookup"><span data-stu-id="38a81-113">Creating a Security Descriptor for a New Directory Object</span></span>](creating-a-security-descriptor-for-a-new-directory-object.md)
-   [<span data-ttu-id="38a81-114">使用存取權限的繼承來啟用目錄的整個子樹的系統管理存取權</span><span class="sxs-lookup"><span data-stu-id="38a81-114">Using inheritance of access permissions to enable administrative access to an entire subtree of the directory</span></span>](inheritance-and-delegation-of-administration.md)
-   [<span data-ttu-id="38a81-115">建立、修改和讀取物件類別的預設安全描述項</span><span class="sxs-lookup"><span data-stu-id="38a81-115">Creating, modifying, and reading the default security descriptor for an object class</span></span>](default-security-descriptor.md)
-   [<span data-ttu-id="38a81-116">針對超越預先定義許可權所涵蓋之作業的作業建立、設定和檢查控制權存取權限</span><span class="sxs-lookup"><span data-stu-id="38a81-116">Creating, setting, and checking control access rights for operations that go beyond those covered by the predefined rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="38a81-117">使用 DsAddSidHistory</span><span class="sxs-lookup"><span data-stu-id="38a81-117">Using DsAddSidHistory</span></span>](using-dsaddsidhistory.md)
-   [<span data-ttu-id="38a81-118">控制物件可見度</span><span class="sxs-lookup"><span data-stu-id="38a81-118">Controlling Object Visibility</span></span>](controlling-object-visibility.md)
-   [<span data-ttu-id="38a81-119">Null Dacl 和空白的 Dacl</span><span class="sxs-lookup"><span data-stu-id="38a81-119">Null DACLs and Empty DACLs</span></span>](null-dacls-and-empty-dacls.md)

 

 




