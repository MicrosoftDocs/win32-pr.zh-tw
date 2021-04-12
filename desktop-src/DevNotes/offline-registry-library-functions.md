---
description: 以下是離線登錄庫功能。
ms.assetid: 378811d2-064c-4d81-979e-392097d55baa
title: 離線登錄庫函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c36afac0b8f5f0aed17b12a7e0562cce75ea69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385884"
---
# <a name="offline-registry-library-functions"></a><span data-ttu-id="95690-103">離線登錄庫函數</span><span class="sxs-lookup"><span data-stu-id="95690-103">Offline Registry Library Functions</span></span>

<span data-ttu-id="95690-104">以下是離線登錄庫功能。</span><span class="sxs-lookup"><span data-stu-id="95690-104">The following are the offline registry library functions.</span></span>



| <span data-ttu-id="95690-105">函式</span><span class="sxs-lookup"><span data-stu-id="95690-105">Function</span></span>                                       | <span data-ttu-id="95690-106">描述</span><span class="sxs-lookup"><span data-stu-id="95690-106">Description</span></span>                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95690-107">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="95690-107">**ORCloseHive**</span></span>](orclosehive.md)             | <span data-ttu-id="95690-108">關閉指定的離線登錄 hive，並釋出配置給 hive 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="95690-108">Closes the specified offline registry hive and frees memory allocated for the hive.</span></span>                                 |
| [<span data-ttu-id="95690-109">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="95690-109">**ORCloseKey**</span></span>](orclosekey.md)               | <span data-ttu-id="95690-110">關閉離線登錄 hive 中指定之登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="95690-110">Closes a handle to the specified registry key in an offline registry hive.</span></span>                                          |
| [<span data-ttu-id="95690-111">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="95690-111">**ORCreateHive**</span></span>](orcreatehive.md)           | <span data-ttu-id="95690-112">建立包含單一空根金鑰的離線登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="95690-112">Creates an offline registry hive that contains a single empty root key.</span></span>                                             |
| [<span data-ttu-id="95690-113">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="95690-113">**ORCreateKey**</span></span>](orcreatekey.md)             | <span data-ttu-id="95690-114">在離線登錄 hive 中建立指定的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="95690-114">Creates the specified registry key in an offline registry hive.</span></span> <span data-ttu-id="95690-115">如果索引鍵已經存在，則函式會將它開啟。</span><span class="sxs-lookup"><span data-stu-id="95690-115">If the key already exists, the function opens it.</span></span>   |
| [<span data-ttu-id="95690-116">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="95690-116">**ORDeleteKey**</span></span>](ordeletekey.md)             | <span data-ttu-id="95690-117">從離線登錄 hive 刪除子機碼及其值。</span><span class="sxs-lookup"><span data-stu-id="95690-117">Deletes a subkey and its values from an offline registry hive.</span></span>                                                      |
| [<span data-ttu-id="95690-118">**ORDeleteValue**</span><span class="sxs-lookup"><span data-stu-id="95690-118">**ORDeleteValue**</span></span>](ordeletevalue.md)         | <span data-ttu-id="95690-119">從離線登錄 hive 中的指定登錄機碼移除值。</span><span class="sxs-lookup"><span data-stu-id="95690-119">Removes a value from the specified registry key in an offline registry hive.</span></span>                                        |
| [<span data-ttu-id="95690-120">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="95690-120">**OREnumKey**</span></span>](orenumkey.md)                 | <span data-ttu-id="95690-121">列舉離線登錄 hive 中指定之開啟登錄機碼的子機碼。</span><span class="sxs-lookup"><span data-stu-id="95690-121">Enumerates the subkeys of the specified open registry key in an offline registry hive.</span></span>                              |
| [<span data-ttu-id="95690-122">**OREnumValue**</span><span class="sxs-lookup"><span data-stu-id="95690-122">**OREnumValue**</span></span>](orenumvalue.md)             | <span data-ttu-id="95690-123">列舉離線登錄區中指定之開啟登錄機碼的值。</span><span class="sxs-lookup"><span data-stu-id="95690-123">Enumerates the values for the specified open registry key in an offline registry hive.</span></span>                              |
| [<span data-ttu-id="95690-124">**ORGetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="95690-124">**ORGetKeySecurity**</span></span>](orgetkeysecurity.md)   | <span data-ttu-id="95690-125">抓取保護離線登錄區中指定之開啟登錄機碼的安全描述項複本。</span><span class="sxs-lookup"><span data-stu-id="95690-125">Retrieves a copy of the security descriptor protecting the specified open registry key in an offline registry hive.</span></span> |
| [<span data-ttu-id="95690-126">**ORGetValue**</span><span class="sxs-lookup"><span data-stu-id="95690-126">**ORGetValue**</span></span>](orgetvalue.md)               | <span data-ttu-id="95690-127">抓取離線登錄 hive 中指定之登錄值的類型和資料。</span><span class="sxs-lookup"><span data-stu-id="95690-127">Retrieves the type and data for the specified registry value in an offline registry hive.</span></span>                           |
| [<span data-ttu-id="95690-128">**ORGetVersion**</span><span class="sxs-lookup"><span data-stu-id="95690-128">**ORGetVersion**</span></span>](orgetversion.md)           | <span data-ttu-id="95690-129">捕獲離線登錄庫的版本。</span><span class="sxs-lookup"><span data-stu-id="95690-129">Retrieves the version of the offline registry library.</span></span>                                                              |
| [<span data-ttu-id="95690-130">**ORGetVirtualFlags**</span><span class="sxs-lookup"><span data-stu-id="95690-130">**ORGetVirtualFlags**</span></span>](orgetvirtualflags.md) | <span data-ttu-id="95690-131">抓取離線登錄區中指定的開啟登錄機碼上的虛擬旗標。</span><span class="sxs-lookup"><span data-stu-id="95690-131">Retrieves the virtual flags on the specified open registry key in an offline registry hive.</span></span>                         |
| [<span data-ttu-id="95690-132">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="95690-132">**OROpenHive**</span></span>](oropenhive.md)               | <span data-ttu-id="95690-133">將指定的 hive 檔案載入記憶體中，並驗證 hive。</span><span class="sxs-lookup"><span data-stu-id="95690-133">Loads the specified hive file into memory and validates the hive.</span></span>                                                   |
| [<span data-ttu-id="95690-134">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="95690-134">**OROpenKey**</span></span>](oropenkey.md)                 | <span data-ttu-id="95690-135">在離線登錄 hive 中開啟指定的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="95690-135">Opens the specified registry key in an offline registry hive.</span></span>                                                       |
| [<span data-ttu-id="95690-136">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="95690-136">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)       | <span data-ttu-id="95690-137">抓取離線登錄 hive 中指定之登錄機碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="95690-137">Retrieves information about the specified registry key in an offline registry hive.</span></span>                                 |
| [<span data-ttu-id="95690-138">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="95690-138">**ORSaveHive**</span></span>](orsavehive.md)               | <span data-ttu-id="95690-139">將指定的離線登錄 hive 寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="95690-139">Writes the specified offline registry hive to a file.</span></span>                                                               |
| [<span data-ttu-id="95690-140">**ORSetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="95690-140">**ORSetKeySecurity**</span></span>](orsetkeysecurity.md)   | <span data-ttu-id="95690-141">設定離線登錄區中已開啟登錄機碼的安全性。</span><span class="sxs-lookup"><span data-stu-id="95690-141">Sets the security of an open registry key in an offline registry hive.</span></span>                                              |
| [<span data-ttu-id="95690-142">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="95690-142">**ORSetValue**</span></span>](orsetvalue.md)               | <span data-ttu-id="95690-143">設定離線登錄區中所指定登錄機碼值的資料。</span><span class="sxs-lookup"><span data-stu-id="95690-143">Sets the data for the value of a specified registry key in an offline registry hive.</span></span>                                |
| [<span data-ttu-id="95690-144">**ORSetVirtualFlags**</span><span class="sxs-lookup"><span data-stu-id="95690-144">**ORSetVirtualFlags**</span></span>](orsetvirtualflags.md) | <span data-ttu-id="95690-145">在離線登錄區中，于指定的開啟登錄機碼上設定虛擬旗標。</span><span class="sxs-lookup"><span data-stu-id="95690-145">Sets virtualization flags on the specified open registry key in an offline registry hive.</span></span>                           |



 

 

 



