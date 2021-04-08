---
title: '架構 (AD DS) '
description: Active Directory 架構會實作為一組儲存在目錄中的物件類別實例。
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory 架構 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "103679456"
---
# <a name="schema-ad-ds"></a><span data-ttu-id="761e4-104">架構 (AD DS) </span><span class="sxs-lookup"><span data-stu-id="761e4-104">Schema (AD DS)</span></span>

<span data-ttu-id="761e4-105">Active Directory 架構會實作為一組儲存在目錄中的物件類別實例。</span><span class="sxs-lookup"><span data-stu-id="761e4-105">Active Directory schema is implemented as a set of object class instances stored in the directory.</span></span> <span data-ttu-id="761e4-106">這與多個具有架構的目錄不同，但會將它儲存為在啟動時讀取的文字檔。</span><span class="sxs-lookup"><span data-stu-id="761e4-106">This is very different than many directories that have a schema but store it as a text file read at startup.</span></span> <span data-ttu-id="761e4-107">在目錄中儲存架構有許多優點。</span><span class="sxs-lookup"><span data-stu-id="761e4-107">Storing the schema in the directory has many advantages.</span></span> <span data-ttu-id="761e4-108">例如，使用者應用程式可以讀取它以探索可用的物件和屬性。</span><span class="sxs-lookup"><span data-stu-id="761e4-108">For example, user applications can read it to discover what objects and properties are available.</span></span>

<span data-ttu-id="761e4-109">Active Directory 架構可以動態更新。</span><span class="sxs-lookup"><span data-stu-id="761e4-109">Active Directory schema can be updated dynamically.</span></span> <span data-ttu-id="761e4-110">也就是說，應用程式可以使用新的屬性和類別來延伸架構，並立即使用延伸模組。</span><span class="sxs-lookup"><span data-stu-id="761e4-110">That is, an application can extend the schema with new attributes and classes and use the extensions immediately.</span></span> <span data-ttu-id="761e4-111">架構更新是藉由建立或修改儲存在目錄中的架構物件來完成。</span><span class="sxs-lookup"><span data-stu-id="761e4-111">Schema updates are accomplished by creating or modifying the schema objects stored in the directory.</span></span> <span data-ttu-id="761e4-112">如同 Active Directory 中的每個物件，存取控制清單 (Acl) 保護架構物件，因此授權的使用者只會改變架構。</span><span class="sxs-lookup"><span data-stu-id="761e4-112">Like every object in Active Directory, access-control lists (ACLs) protect schema objects, so authorized users only may alter the schema.</span></span>

<span data-ttu-id="761e4-113">如需詳細資訊，請參閱 [Active Directory 架構](active-directory-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="761e4-113">For more information, see [Active Directory Schema](active-directory-schema.md).</span></span>

 

 




