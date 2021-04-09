---
title: 一致性 Guid
description: 一致性 Guid 是一種偵測策略，可讓應用程式偵測部分更新。
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020742"
---
# <a name="consistency-guids"></a><span data-ttu-id="781e6-103">一致性 Guid</span><span class="sxs-lookup"><span data-stu-id="781e6-103">Consistency GUIDs</span></span>

<span data-ttu-id="781e6-104">一致性 Guid 是一種偵測策略，可讓應用程式偵測部分更新。</span><span class="sxs-lookup"><span data-stu-id="781e6-104">Consistency GUIDs are a detection strategy that allows an application to detect partial updates.</span></span> <span data-ttu-id="781e6-105">一致性 GUID (全域唯一識別碼) 會套用至相關集合中的每個物件。</span><span class="sxs-lookup"><span data-stu-id="781e6-105">A consistency GUID (Globally Unique IDentifier) is applied to each object in a related set.</span></span> <span data-ttu-id="781e6-106">在執行時，來源應用程式會產生新的 GUID，並將其套用至它在相關物件集中更新的每一個物件。</span><span class="sxs-lookup"><span data-stu-id="781e6-106">In implementation, a source application generates a new GUID and applies it to each object it updates in the set of related objects.</span></span> <span data-ttu-id="781e6-107">然後，它會將新的 GUID 套用至集合中其餘的物件，並將新的 GUID 套用至 "master" 物件來完成。</span><span class="sxs-lookup"><span data-stu-id="781e6-107">It then applies the new GUID to the rest of the objects in the set, and finishes by applying the new GUID to the "master" object.</span></span> <span data-ttu-id="781e6-108">一般而言，「主要」物件會是容器，也就是集合中其他物件的父系。</span><span class="sxs-lookup"><span data-stu-id="781e6-108">Typically, the "master" object will be a container that is the parent of the other objects in the set.</span></span>

<span data-ttu-id="781e6-109">一些重要考量︰</span><span class="sxs-lookup"><span data-stu-id="781e6-109">Some important considerations:</span></span>

-   <span data-ttu-id="781e6-110">與物件計數或總和檢查碼結合的一致性 Guid 比一致性 Guid 更有效率，因為讀取物件的應用程式可能不知道有多少物件有 GUID 存在。</span><span class="sxs-lookup"><span data-stu-id="781e6-110">Consistency GUIDs combined with object counts or checksums are more effective than consistency GUIDs alone, because the application reading the objects may not know how many objects with the GUID should be present.</span></span>
-   <span data-ttu-id="781e6-111">應用程式必須產生自己的 Guid (Microsoft WIN32 API （UuidCreate）提供此函式) ，而不使用在物件的 **objectGUID** 屬性中找到的系統產生的 guid。</span><span class="sxs-lookup"><span data-stu-id="781e6-111">Applications must generate their own GUIDs (a Microsoft Win32 API, UuidCreate, provides this function), and not use the system-generated GUIDs found in an object's **objectGUID** attribute.</span></span> <span data-ttu-id="781e6-112">這是因為每次更新物件集時，一致性 GUID 都需要變更。</span><span class="sxs-lookup"><span data-stu-id="781e6-112">This is because a consistency GUID needs to change each time the set of objects is updated.</span></span> <span data-ttu-id="781e6-113">在 **objectGUID** 中找到的物件識別 guid 永遠不會在建立物件之後變更。</span><span class="sxs-lookup"><span data-stu-id="781e6-113">Object identity GUIDs found in **objectGUID** never change after the object has been created.</span></span>
-   <span data-ttu-id="781e6-114">一致性 Guid 假設不會在集合之間共用任何物件，因此每個集合都可以有唯一的一致性 GUID。</span><span class="sxs-lookup"><span data-stu-id="781e6-114">Consistency GUIDs assume that no object is shared among sets, so each set can have a unique consistency GUID.</span></span>

 

 




