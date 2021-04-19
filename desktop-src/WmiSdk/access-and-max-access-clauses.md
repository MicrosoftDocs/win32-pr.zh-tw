---
description: 每個 MIB 物件定義都包含存取 (SNMPv1) 或 MAX 存取 (SNMPv2C) 子句，可定義物件的存取權限。
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: 存取和最大存取權子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978256"
---
# <a name="access-and-max-access-clauses"></a><span data-ttu-id="7cfb7-103">存取和最大存取權子句</span><span class="sxs-lookup"><span data-stu-id="7cfb7-103">ACCESS and MAX-ACCESS Clauses</span></span>

<span data-ttu-id="7cfb7-104">每個 MIB 物件定義都包含存取 (SNMPv1) 或 MAX 存取 (SNMPv2C) 子句，可定義物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="7cfb7-104">Each MIB object definition contains either an ACCESS (SNMPv1) or MAX-ACCESS (SNMPv2C) clause that defines the access rights to the object.</span></span>

> [!Note]  
> <span data-ttu-id="7cfb7-105">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="7cfb7-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="7cfb7-106">下表列出 SNMPv1 存取子句的對應。</span><span class="sxs-lookup"><span data-stu-id="7cfb7-106">The following table lists the mapping of the SNMPv1 ACCESS clause.</span></span>



| <span data-ttu-id="7cfb7-107">MIB 存取子句</span><span class="sxs-lookup"><span data-stu-id="7cfb7-107">MIB ACCESS clause</span></span> | <span data-ttu-id="7cfb7-108">CIM 辨識符號</span><span class="sxs-lookup"><span data-stu-id="7cfb7-108">CIM qualifier</span></span>       |
|-------------------|---------------------|
| <span data-ttu-id="7cfb7-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="7cfb7-109">read-only</span></span>         | <span data-ttu-id="7cfb7-110">**讀取**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-110">**Read**</span></span>            |
| <span data-ttu-id="7cfb7-111">讀寫</span><span class="sxs-lookup"><span data-stu-id="7cfb7-111">read-write</span></span>        | <span data-ttu-id="7cfb7-112">**讀取**、 **寫入**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-112">**Read**, **Write**</span></span> |
| <span data-ttu-id="7cfb7-113">唯寫</span><span class="sxs-lookup"><span data-stu-id="7cfb7-113">write-only</span></span>        | <span data-ttu-id="7cfb7-114">**寫入**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-114">**Write**</span></span>           |
| <span data-ttu-id="7cfb7-115">無法存取</span><span class="sxs-lookup"><span data-stu-id="7cfb7-115">not-accessible</span></span>    | <span data-ttu-id="7cfb7-116">**無法 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-116">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="7cfb7-117">下表列出 SNMPv2C MAX ACCESS 子句的對應。</span><span class="sxs-lookup"><span data-stu-id="7cfb7-117">The following table lists the mapping of the SNMPv2C MAX-ACCESS clause.</span></span>



| <span data-ttu-id="7cfb7-118">MIB-存取子句</span><span class="sxs-lookup"><span data-stu-id="7cfb7-118">MIB-ACCESS clause</span></span>     | <span data-ttu-id="7cfb7-119">CIM 辨識符號</span><span class="sxs-lookup"><span data-stu-id="7cfb7-119">CIM qualifier</span></span>       |
|-----------------------|---------------------|
| <span data-ttu-id="7cfb7-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="7cfb7-120">read-only</span></span>             | <span data-ttu-id="7cfb7-121">**讀取**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-121">**Read**</span></span>            |
| <span data-ttu-id="7cfb7-122">讀寫</span><span class="sxs-lookup"><span data-stu-id="7cfb7-122">read-write</span></span>            | <span data-ttu-id="7cfb7-123">**讀取**、 **寫入**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-123">**Read**, **Write**</span></span> |
| <span data-ttu-id="7cfb7-124">讀取-建立</span><span class="sxs-lookup"><span data-stu-id="7cfb7-124">read-create</span></span>           | <span data-ttu-id="7cfb7-125">**讀取**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-125">**Read**</span></span>            |
| <span data-ttu-id="7cfb7-126">可存取-通知</span><span class="sxs-lookup"><span data-stu-id="7cfb7-126">accessible-for-notify</span></span> | <span data-ttu-id="7cfb7-127">**無法 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-127">**Not\_Accessible**</span></span> |
| <span data-ttu-id="7cfb7-128">無法存取</span><span class="sxs-lookup"><span data-stu-id="7cfb7-128">not-accessible</span></span>        | <span data-ttu-id="7cfb7-129">**無法 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="7cfb7-129">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="7cfb7-130">當 MIB 物件對應到無法存取的，而且不是類別的索引鍵屬性時，就不會有 MIB 物件本身的對應。</span><span class="sxs-lookup"><span data-stu-id="7cfb7-130">When a MIB object maps to not-accessible and is not a keyed property of the class, there is no mapping of the MIB object itself.</span></span>

 

 



