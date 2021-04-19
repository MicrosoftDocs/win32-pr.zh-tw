---
description: WFP 登錄值位於下列登錄機碼中： HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon。
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: WFP 登錄值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996940"
---
# <a name="wfp-registry-values"></a><span data-ttu-id="abdf2-103">WFP 登錄值</span><span class="sxs-lookup"><span data-stu-id="abdf2-103">WFP Registry Values</span></span>

<span data-ttu-id="abdf2-104">\[Windows Vista 不支援 WFP 登錄值。\]</span><span class="sxs-lookup"><span data-stu-id="abdf2-104">\[WFP registry values are not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="abdf2-105">WFP 使用數個登錄值進行自訂設定。</span><span class="sxs-lookup"><span data-stu-id="abdf2-105">WFP uses several registry values for customization settings.</span></span> <span data-ttu-id="abdf2-106">WFP 登錄值位於下列登錄機碼中：</span><span class="sxs-lookup"><span data-stu-id="abdf2-106">The WFP registry values are located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

<span data-ttu-id="abdf2-107">以下是 WFP 登錄值。</span><span class="sxs-lookup"><span data-stu-id="abdf2-107">The following are the WFP registry values.</span></span>

<dl> <dt>

<span data-ttu-id="abdf2-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span><span class="sxs-lookup"><span data-stu-id="abdf2-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span></span>
</dt> <dd>

<span data-ttu-id="abdf2-109">快取的位置。</span><span class="sxs-lookup"><span data-stu-id="abdf2-109">Location of the cache.</span></span> <span data-ttu-id="abdf2-110">這必須是本機路徑。</span><span class="sxs-lookup"><span data-stu-id="abdf2-110">This must be a local path.</span></span> <span data-ttu-id="abdf2-111">預設值為% systemroot% \\ system32 \\ dllcache。</span><span class="sxs-lookup"><span data-stu-id="abdf2-111">The default value is %systemroot%\\system32\\dllcache.</span></span>

</dd> <dt>

<span data-ttu-id="abdf2-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span><span class="sxs-lookup"><span data-stu-id="abdf2-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span></span>
</dt> <dd>

<span data-ttu-id="abdf2-113">配額選項。</span><span class="sxs-lookup"><span data-stu-id="abdf2-113">Quota options.</span></span> <span data-ttu-id="abdf2-114">此登錄值可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="abdf2-114">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="abdf2-115">值</span><span class="sxs-lookup"><span data-stu-id="abdf2-115">Value</span></span>                  | <span data-ttu-id="abdf2-116">意義</span><span class="sxs-lookup"><span data-stu-id="abdf2-116">Meaning</span></span>                                                  |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="abdf2-117">SFC \_ 配額 \_ 所有 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="abdf2-117">SFC\_QUOTA\_ALL\_FILES</span></span> | <span data-ttu-id="abdf2-118">DLL 快取的大小不受限制。</span><span class="sxs-lookup"><span data-stu-id="abdf2-118">Size of the DLL cache is unlimited.</span></span> <span data-ttu-id="abdf2-119">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="abdf2-119">This is the default.</span></span> |
| <span data-ttu-id="abdf2-120">其他值</span><span class="sxs-lookup"><span data-stu-id="abdf2-120">Other values</span></span>           | <span data-ttu-id="abdf2-121">DLL 快取的大小，以檔案為限。</span><span class="sxs-lookup"><span data-stu-id="abdf2-121">Size of the DLL cache, in files.</span></span>                         |



 

</dd> <dt>

<span data-ttu-id="abdf2-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span><span class="sxs-lookup"><span data-stu-id="abdf2-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span></span>
</dt> <dd>

<span data-ttu-id="abdf2-123">掃描選項。</span><span class="sxs-lookup"><span data-stu-id="abdf2-123">Scan options.</span></span> <span data-ttu-id="abdf2-124">此登錄值可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="abdf2-124">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="abdf2-125">值</span><span class="sxs-lookup"><span data-stu-id="abdf2-125">Value</span></span>             | <span data-ttu-id="abdf2-126">意義</span><span class="sxs-lookup"><span data-stu-id="abdf2-126">Meaning</span></span>                                                   |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="abdf2-127">SFC \_ 掃描 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="abdf2-127">SFC\_SCAN\_NORMAL</span></span> | <span data-ttu-id="abdf2-128">請勿在開機時掃描受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="abdf2-128">Do not scan protected files at boot.</span></span> <span data-ttu-id="abdf2-129">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="abdf2-129">This is the default.</span></span> |
| <span data-ttu-id="abdf2-130">\_一律掃描 \_ SFC</span><span class="sxs-lookup"><span data-stu-id="abdf2-130">SFC\_SCAN\_ALWAYS</span></span> | <span data-ttu-id="abdf2-131">在每次開機時掃描受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="abdf2-131">Scan protected files at every boot.</span></span>                       |
| <span data-ttu-id="abdf2-132">SFC \_ 掃描 \_ 一次</span><span class="sxs-lookup"><span data-stu-id="abdf2-132">SFC\_SCAN\_ONCE</span></span>   | <span data-ttu-id="abdf2-133">在下一次開機時掃描受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="abdf2-133">Scan protected files at the next boot.</span></span>                    |



 

</dd> </dl>

 

 



