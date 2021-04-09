---
description: DVDDirectory 屬性會設定或抓取目前 DVD 磁片區的目前的目錄。
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: DVDDirectory 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846344"
---
# <a name="dvddirectory-property"></a><span data-ttu-id="0cf18-103">DVDDirectory 屬性</span><span class="sxs-lookup"><span data-stu-id="0cf18-103">DVDDirectory Property</span></span>

> [!Note]  
> <span data-ttu-id="0cf18-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="0cf18-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0cf18-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0cf18-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0cf18-106">`DVDDirectory`屬性會設定或抓取目前 DVD 磁片區的目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="0cf18-106">The `DVDDirectory` property sets or retrieves the current directory of the current DVD volume.</span></span>

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a><span data-ttu-id="0cf18-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cf18-107">Return Value</span></span>

<span data-ttu-id="0cf18-108">傳回表示 DVD 根目錄路徑的字串值。</span><span class="sxs-lookup"><span data-stu-id="0cf18-108">Returns a string value indicating the path to the DVD root directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cf18-109">備註</span><span class="sxs-lookup"><span data-stu-id="0cf18-109">Remarks</span></span>

<span data-ttu-id="0cf18-110">此屬性是讀取/寫入，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="0cf18-110">This property is read/write with no default value.</span></span> <span data-ttu-id="0cf18-111">當系統上有一個以上的 DVD 光碟機時，請使用這個方法來設定根路徑。</span><span class="sxs-lookup"><span data-stu-id="0cf18-111">Use this method to set the root path when there is more than one DVD drive on a system.</span></span> <span data-ttu-id="0cf18-112">當系統上只有一個磁片磁碟機，而且其磁碟機號高於 "C" 時，MSWebDVD 物件會自動尋找它。</span><span class="sxs-lookup"><span data-stu-id="0cf18-112">When there is only one drive on the system and its drive letter is higher than "C", the MSWebDVD object finds it automatically.</span></span> <span data-ttu-id="0cf18-113">若為標準 DVD-Video 光碟，根路徑應該包含 ts \_ video 目錄：</span><span class="sxs-lookup"><span data-stu-id="0cf18-113">For a standard DVD-Video disc, the root path should include the ts\_video directory:</span></span>


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



<span data-ttu-id="0cf18-114">某些 DVD 磁片區的影片可能會在名為「影片 ts」以外的目錄中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0cf18-114">Some DVD volumes may have their video in a directory named something other than "video\_ts."</span></span> <span data-ttu-id="0cf18-115">一般的概念是，有一個額外的「DVD 磁片區」 (的組合。Ifo。</span><span class="sxs-lookup"><span data-stu-id="0cf18-115">The general idea is that an additional "DVD volume" (the set of .IFO.</span></span> <span data-ttu-id="0cf18-116">VOB、和。通常儲存在 VIDEO TS 目錄) 的 BUP 檔案 \_ 可以放在光碟片上的子目錄中。藉由將根變更為指向此目錄，MSWebDVD 會在此不同的 DVD 磁片區上運作。</span><span class="sxs-lookup"><span data-stu-id="0cf18-116">VOB, and .BUP files that would normally be stored in the VIDEO\_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume.</span></span> <span data-ttu-id="0cf18-117">您可以使用一組新的功能表、標題等等，與影片 TS 根目錄中的標題無關， \_ 這將無法再存取。</span><span class="sxs-lookup"><span data-stu-id="0cf18-117">A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO\_TS root, which will no longer be accessible.</span></span> <span data-ttu-id="0cf18-118">這類目錄稱為「隱藏目錄」。</span><span class="sxs-lookup"><span data-stu-id="0cf18-118">Such directories are called "hidden directories."</span></span> <span data-ttu-id="0cf18-119">下列範例示範如何將隱藏的目錄設定為根目錄，其中「隱藏」是光碟作者提供給目錄之任何名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="0cf18-119">The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.</span></span>


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



