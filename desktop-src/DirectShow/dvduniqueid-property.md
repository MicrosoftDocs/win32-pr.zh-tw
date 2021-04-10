---
description: DVDUniqueID 屬性會抓取可唯一識別目前光碟的系統產生數位。
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: DVDUniqueID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846340"
---
# <a name="dvduniqueid-property"></a><span data-ttu-id="a51f8-103">DVDUniqueID 屬性</span><span class="sxs-lookup"><span data-stu-id="a51f8-103">DVDUniqueID Property</span></span>

> [!Note]  
> <span data-ttu-id="a51f8-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="a51f8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a51f8-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a51f8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a51f8-106">`DVDUniqueID`屬性會抓取可唯一識別目前光碟的系統產生數位。</span><span class="sxs-lookup"><span data-stu-id="a51f8-106">The `DVDUniqueID` property retrieves a system-generated number that uniquely identifies the current disc.</span></span>

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a><span data-ttu-id="a51f8-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="a51f8-107">Return Value</span></span>

<span data-ttu-id="a51f8-108">傳回可唯一識別目前光碟的整數值。</span><span class="sxs-lookup"><span data-stu-id="a51f8-108">Returns an integer value that uniquely identifies the current disc.</span></span>

## <a name="remarks"></a><span data-ttu-id="a51f8-109">備註</span><span class="sxs-lookup"><span data-stu-id="a51f8-109">Remarks</span></span>

<span data-ttu-id="a51f8-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="a51f8-110">This property is read-only with no default value.</span></span> <span data-ttu-id="a51f8-111">識別碼 (識別碼) 號碼不是絕對唯一的，但在所有實際用途中都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a51f8-111">The identifier (ID) number is not absolutely unique, but it is unique for all practical purposes.</span></span> <span data-ttu-id="a51f8-112">此識別碼會套用至所有已複寫的光碟複本。換句話說，特定電影的所有複本都有相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a51f8-112">The ID applies to all replicated copies of a disc. In other words, all copies of a specific movie have the same ID.</span></span> <span data-ttu-id="a51f8-113">此識別碼是根據檔案大小、日期和其他資訊，而不是 BCA 值。</span><span class="sxs-lookup"><span data-stu-id="a51f8-113">The ID is based on file sizes, dates, and other information, and not the BCA value.</span></span>

 

 



