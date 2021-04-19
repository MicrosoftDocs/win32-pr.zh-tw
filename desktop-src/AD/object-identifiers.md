---
title: '物件識別碼 (AD DS) '
description: " (Oid 的物件識別碼) 是由各種發行授權單位所發出的唯一數值，可唯一識別資料元素、語法，以及分散式應用程式的其他部分。"
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- 物件識別碼廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "106966434"
---
# <a name="object-identifiers-ad-ds"></a><span data-ttu-id="3751e-104">物件識別碼 (AD DS) </span><span class="sxs-lookup"><span data-stu-id="3751e-104">Object Identifiers (AD DS)</span></span>

<span data-ttu-id="3751e-105"> (Oid 的物件識別碼) 是由各種發行授權單位所發出的唯一數值，可唯一識別資料元素、語法，以及分散式應用程式的其他部分。</span><span class="sxs-lookup"><span data-stu-id="3751e-105">Object Identifiers (OIDs) are unique numeric values issued by various issuing authorities to uniquely identify data elements, syntaxes, and other parts of distributed applications.</span></span> <span data-ttu-id="3751e-106">在 OSI 應用程式、x.500 目錄、SNMP 和其他重要的應用程式中，都可以找到 Oid。</span><span class="sxs-lookup"><span data-stu-id="3751e-106">OIDs are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="3751e-107">Oid 是以樹狀結構為基礎，在此結構中，較高的發行授權單位（例如 ISO）會將樹狀結構的分支配置給 subauthority，進而可以配置 subbranches。</span><span class="sxs-lookup"><span data-stu-id="3751e-107">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a subauthority, who in turn can allocate subbranches.</span></span>

<span data-ttu-id="3751e-108">LDAP 通訊協定 (RFC 2251) 需要目錄服務來識別具有 Oid 的物件類別、屬性和語法。</span><span class="sxs-lookup"><span data-stu-id="3751e-108">The LDAP protocol (RFC 2251) requires a directory service to identify object classes, attributes, and syntaxes with OIDs.</span></span> <span data-ttu-id="3751e-109">這是 LDAP X. 500 舊版的一部分。</span><span class="sxs-lookup"><span data-stu-id="3751e-109">This is part of the LDAP X.500 legacy.</span></span>

<span data-ttu-id="3751e-110">Active Directory Domain Services 中的 Oid 包括由 ISO 針對 X. 500 類別和屬性簽發的部分，以及由 Microsoft 和其他發行授權單位所發行的部分。</span><span class="sxs-lookup"><span data-stu-id="3751e-110">OIDs in Active Directory Domain Services include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft and other issuing authorities.</span></span> <span data-ttu-id="3751e-111">OID 標記法是數位的點字串，例如 "1.2.840.113556.1.5.9"，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="3751e-111">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.9", which is described in the following table.</span></span>



| <span data-ttu-id="3751e-112">值</span><span class="sxs-lookup"><span data-stu-id="3751e-112">Value</span></span>  | <span data-ttu-id="3751e-113">意義</span><span class="sxs-lookup"><span data-stu-id="3751e-113">Meaning</span></span>          | <span data-ttu-id="3751e-114">描述</span><span class="sxs-lookup"><span data-stu-id="3751e-114">Description</span></span>                                              |
|--------|------------------|----------------------------------------------------------|
| <span data-ttu-id="3751e-115">1</span><span class="sxs-lookup"><span data-stu-id="3751e-115">1</span></span>      | <span data-ttu-id="3751e-116">ISO</span><span class="sxs-lookup"><span data-stu-id="3751e-116">ISO</span></span>              | <span data-ttu-id="3751e-117">識別根授權單位。</span><span class="sxs-lookup"><span data-stu-id="3751e-117">Identifies the root authority.</span></span>                           |
| <span data-ttu-id="3751e-118">2</span><span class="sxs-lookup"><span data-stu-id="3751e-118">2</span></span>      | <span data-ttu-id="3751e-119">ANSI</span><span class="sxs-lookup"><span data-stu-id="3751e-119">ANSI</span></span>             | <span data-ttu-id="3751e-120">由 ISO 指派的群組指定。</span><span class="sxs-lookup"><span data-stu-id="3751e-120">Group designation assigned by ISO.</span></span>                       |
| <span data-ttu-id="3751e-121">840</span><span class="sxs-lookup"><span data-stu-id="3751e-121">840</span></span>    | <span data-ttu-id="3751e-122">USA</span><span class="sxs-lookup"><span data-stu-id="3751e-122">USA</span></span>              | <span data-ttu-id="3751e-123">群組指派的國家/地區指定。</span><span class="sxs-lookup"><span data-stu-id="3751e-123">Country/region designation assigned by the group.</span></span>        |
| <span data-ttu-id="3751e-124">113556</span><span class="sxs-lookup"><span data-stu-id="3751e-124">113556</span></span> | <span data-ttu-id="3751e-125">Microsoft</span><span class="sxs-lookup"><span data-stu-id="3751e-125">Microsoft</span></span>        | <span data-ttu-id="3751e-126">國家/地區指派的組織指定。</span><span class="sxs-lookup"><span data-stu-id="3751e-126">Organization designation assigned by the country/region.</span></span> |
| <span data-ttu-id="3751e-127">1</span><span class="sxs-lookup"><span data-stu-id="3751e-127">1</span></span>      | <span data-ttu-id="3751e-128">Active Directory</span><span class="sxs-lookup"><span data-stu-id="3751e-128">Active Directory</span></span> | <span data-ttu-id="3751e-129">由組織指派。</span><span class="sxs-lookup"><span data-stu-id="3751e-129">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="3751e-130">5</span><span class="sxs-lookup"><span data-stu-id="3751e-130">5</span></span>      | <span data-ttu-id="3751e-131">類別</span><span class="sxs-lookup"><span data-stu-id="3751e-131">Classes</span></span>          | <span data-ttu-id="3751e-132">由組織指派。</span><span class="sxs-lookup"><span data-stu-id="3751e-132">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="3751e-133">9</span><span class="sxs-lookup"><span data-stu-id="3751e-133">9</span></span>      | <span data-ttu-id="3751e-134">**使用者** 類別</span><span class="sxs-lookup"><span data-stu-id="3751e-134">**user** class</span></span>   | <span data-ttu-id="3751e-135">由組織指派。</span><span class="sxs-lookup"><span data-stu-id="3751e-135">Assigned by the organization.</span></span>                            |



 

<span data-ttu-id="3751e-136">如需詳細資訊，以及用來取得有效 Oid 以用於擴充 Active Directory 架構的兩個程式的討論，請參閱 [取得物件識別碼](obtaining-an-object-identifier.md)。</span><span class="sxs-lookup"><span data-stu-id="3751e-136">For more information, and a discussion of two procedures used to obtain valid OIDs for use in extending the Active Directory schema, see [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>

 

 




