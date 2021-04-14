---
description: 如果每一電腦的系統原則設定為大於0的值，Windows Installer 將修補程式套用至應用程式時，會將舊版本的檔案儲存在快取中。
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469217"
---
# <a name="maxpatchcachesize"></a><span data-ttu-id="6e0ad-103">MaxPatchCacheSize</span><span class="sxs-lookup"><span data-stu-id="6e0ad-103">MaxPatchCacheSize</span></span>

<span data-ttu-id="6e0ad-104">如果每一電腦的 [系統原則](system-policy.md) 設定為大於0的值，Windows Installer 將修補程式套用至應用程式時，會將舊版本的檔案儲存在快取中。</span><span class="sxs-lookup"><span data-stu-id="6e0ad-104">If this per-machine [system policy](system-policy.md) is set to a value greater than 0, Windows Installer saves older versions of files in a cache when a patch is applied to an application.</span></span> <span data-ttu-id="6e0ad-105">快取可能會增加未來安裝的效能，否則需要從原始應用程式來源取得舊的檔案。</span><span class="sxs-lookup"><span data-stu-id="6e0ad-105">Caching can increase the performance of future installations that otherwise need to obtain the old files from a original application source.</span></span>

<span data-ttu-id="6e0ad-106">MaxPatchCacheSize 原則的值是安裝程式可用於快取舊檔案的磁碟空間的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="6e0ad-106">The value of the MaxPatchCacheSize policy is the maximum percentage of disk space that the installer can use for the cache of old files.</span></span> <span data-ttu-id="6e0ad-107">例如，值20表示不超過20% 的使用。</span><span class="sxs-lookup"><span data-stu-id="6e0ad-107">For example, a value of 20 specifies no more than 20% be used.</span></span> <span data-ttu-id="6e0ad-108">如果快取的總大小達到指定的磁碟空間百分比，則不會將其他檔案儲存至快取。</span><span class="sxs-lookup"><span data-stu-id="6e0ad-108">If the total size of the cache reaches the specified percentage of disk space, no additional files are saved to the cache.</span></span> <span data-ttu-id="6e0ad-109">原則不會影響已儲存的檔案。</span><span class="sxs-lookup"><span data-stu-id="6e0ad-109">The policy does not affect files that have already been saved.</span></span>

<span data-ttu-id="6e0ad-110">如果 MaxPatchCacheSize 原則的值設定為0，則不會儲存其他檔案。</span><span class="sxs-lookup"><span data-stu-id="6e0ad-110">If the value of the MaxPatchCacheSize policy is set to 0, no additional files are saved.</span></span>

<span data-ttu-id="6e0ad-111">如果未設定 MaxPatchCacheSize 原則，預設值為10，且最多可以使用10% 的磁碟空間來儲存舊檔案。</span><span class="sxs-lookup"><span data-stu-id="6e0ad-111">If the MaxPatchCacheSize policy is not set, the default value is 10 and a maximum of 10% of the disk space can be used to save old files.</span></span>

## <a name="registry-key"></a><span data-ttu-id="6e0ad-112">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="6e0ad-112">Registry Key</span></span>

<span data-ttu-id="6e0ad-113">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="6e0ad-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="6e0ad-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="6e0ad-114">Data Type</span></span>

<span data-ttu-id="6e0ad-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6e0ad-115">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e0ad-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e0ad-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e0ad-117">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="6e0ad-117">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



