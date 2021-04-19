---
description: 可插入的終端會分類為終端超類。
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: " (電話語音 API) 的登錄專案"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976374"
---
# <a name="registry-entries-telephony-api"></a><span data-ttu-id="7426d-103"> (電話語音 API) 的登錄專案</span><span class="sxs-lookup"><span data-stu-id="7426d-103">Registry Entries (Telephony API)</span></span>

<span data-ttu-id="7426d-104">可插入的終端會分類為終端超類。</span><span class="sxs-lookup"><span data-stu-id="7426d-104">The pluggable terminals are classified into Terminal Superclasses.</span></span> <span data-ttu-id="7426d-105">在登錄中，每個終端超級類別都有下列機碼專案：</span><span class="sxs-lookup"><span data-stu-id="7426d-105">Each Terminal Superclass has an entry in the registry under the following key:</span></span>

<span data-ttu-id="7426d-106">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **電話語音** \\ **TerminalManager**</span><span class="sxs-lookup"><span data-stu-id="7426d-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Telephony**\\**TerminalManager**</span></span>

<span data-ttu-id="7426d-107">在終端超級類別下，終端超級類別機碼為終端超級類別內每個可插入終端機的專案。</span><span class="sxs-lookup"><span data-stu-id="7426d-107">Below the Terminal Superclass key are entries for each pluggable terminal within the Terminal Superclass.</span></span>

<span data-ttu-id="7426d-108">每個終端超級類別的專案都是由終端超級類別 CLSID 所識別。</span><span class="sxs-lookup"><span data-stu-id="7426d-108">The entry for each Terminal Superclass is identified by a Terminal Superclass CLSID.</span></span> <span data-ttu-id="7426d-109">這是終端機類別的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="7426d-109">This is a unique identifier for a terminal class.</span></span> <span data-ttu-id="7426d-110">終端機類別具有選擇性的屬性：名稱，這是終端機類別的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="7426d-110">The terminal class has an optional attribute: name, which is a friendly name for the terminal class.</span></span> <span data-ttu-id="7426d-111">每個可插入的終端機都是由 CLSID 終端機類別來識別;亦即 GUID。</span><span class="sxs-lookup"><span data-stu-id="7426d-111">Each pluggable terminal is identified by a CLSID Terminal class; that is, a GUID.</span></span> <span data-ttu-id="7426d-112">插即用終端機的屬性會儲存至可插入的終端機碼值。</span><span class="sxs-lookup"><span data-stu-id="7426d-112">The attributes for pluggable terminal are stored into pluggable terminal key values.</span></span> <span data-ttu-id="7426d-113">插入式終端機的屬性如下所示。</span><span class="sxs-lookup"><span data-stu-id="7426d-113">The attributes for a pluggable terminal are the following.</span></span>



| <span data-ttu-id="7426d-114">Terminal 類別</span><span class="sxs-lookup"><span data-stu-id="7426d-114">Terminal class</span></span> | <span data-ttu-id="7426d-115">索引鍵名稱</span><span class="sxs-lookup"><span data-stu-id="7426d-115">Key name</span></span> | <span data-ttu-id="7426d-116">公用識別碼</span><span class="sxs-lookup"><span data-stu-id="7426d-116">Public identifier</span></span>                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7426d-117">Name</span><span class="sxs-lookup"><span data-stu-id="7426d-117">Name</span></span>           | <span data-ttu-id="7426d-118">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7426d-118">REG\_SZ</span></span>  | <span data-ttu-id="7426d-119">終端機易記名稱</span><span class="sxs-lookup"><span data-stu-id="7426d-119">Terminal friendly name</span></span>                                                            |
| <span data-ttu-id="7426d-120">公司</span><span class="sxs-lookup"><span data-stu-id="7426d-120">Company</span></span>        | <span data-ttu-id="7426d-121">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7426d-121">REG\_SZ</span></span>  | <span data-ttu-id="7426d-122">公司名稱</span><span class="sxs-lookup"><span data-stu-id="7426d-122">Company name</span></span>                                                                      |
| <span data-ttu-id="7426d-123">版本</span><span class="sxs-lookup"><span data-stu-id="7426d-123">Version</span></span>        | <span data-ttu-id="7426d-124">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7426d-124">REG\_SZ</span></span>  | <span data-ttu-id="7426d-125">版本資訊</span><span class="sxs-lookup"><span data-stu-id="7426d-125">Version information</span></span>                                                               |
| <span data-ttu-id="7426d-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="7426d-126">CLSID</span></span>          | <span data-ttu-id="7426d-127">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7426d-127">REG\_SZ</span></span>  | <span data-ttu-id="7426d-128">COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 方法中使用的終端機 CLSID () </span><span class="sxs-lookup"><span data-stu-id="7426d-128">Terminal CLSID (used in COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method)</span></span> |
| <span data-ttu-id="7426d-129">方向</span><span class="sxs-lookup"><span data-stu-id="7426d-129">Directions</span></span>     | <span data-ttu-id="7426d-130">DWORD</span><span class="sxs-lookup"><span data-stu-id="7426d-130">DWORD</span></span>    | <span data-ttu-id="7426d-131">終端機方向</span><span class="sxs-lookup"><span data-stu-id="7426d-131">Terminal direction</span></span>                                                                |
| <span data-ttu-id="7426d-132">MediaTypes</span><span class="sxs-lookup"><span data-stu-id="7426d-132">MediaTypes</span></span>     | <span data-ttu-id="7426d-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="7426d-133">DWORD</span></span>    | <span data-ttu-id="7426d-134">支援的終端媒體類型</span><span class="sxs-lookup"><span data-stu-id="7426d-134">Terminal media types supported</span></span>                                                    |



 

<span data-ttu-id="7426d-135">終端機類別的屬性如下所示。</span><span class="sxs-lookup"><span data-stu-id="7426d-135">For a terminal class the attributes are the following.</span></span>



| <span data-ttu-id="7426d-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="7426d-136">CLSID</span></span> | <span data-ttu-id="7426d-137">索引鍵名稱</span><span class="sxs-lookup"><span data-stu-id="7426d-137">Key name</span></span> | <span data-ttu-id="7426d-138">公用識別碼</span><span class="sxs-lookup"><span data-stu-id="7426d-138">Public identifier</span></span>            |
|-------|----------|------------------------------|
| <span data-ttu-id="7426d-139">Name</span><span class="sxs-lookup"><span data-stu-id="7426d-139">Name</span></span>  | <span data-ttu-id="7426d-140">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="7426d-140">REG\_SZ</span></span>  | <span data-ttu-id="7426d-141">終端機類別易記名稱</span><span class="sxs-lookup"><span data-stu-id="7426d-141">Terminal class friendly name</span></span> |



 

 

 
