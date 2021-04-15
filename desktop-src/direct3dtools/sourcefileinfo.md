---
description: 表示原始程式碼檔的相關資訊。
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SourceFileInfo 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467759"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span data-ttu-id="e0516-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo 結構</span><span class="sxs-lookup"><span data-stu-id="e0516-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo structure</span></span>

<span data-ttu-id="e0516-104">表示原始程式碼檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e0516-104">Represents information about a source code file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0516-105">語法</span><span class="sxs-lookup"><span data-stu-id="e0516-105">Syntax</span></span>


```C++
} SourceFileInfo;
```

## <a name="members"></a><span data-ttu-id="e0516-106">成員</span><span class="sxs-lookup"><span data-stu-id="e0516-106">Members</span></span>

<span data-ttu-id="e0516-107">**檔案名**</span><span class="sxs-lookup"><span data-stu-id="e0516-107">**fileName**</span></span>  
<span data-ttu-id="e0516-108">COM 字串 comtaining 相關原始程式檔的 filepath。</span><span class="sxs-lookup"><span data-stu-id="e0516-108">A COM string comtaining the filepath of the associated source file.</span></span>

<span data-ttu-id="e0516-109">**checksumByteCount**</span><span class="sxs-lookup"><span data-stu-id="e0516-109">**checksumByteCount**</span></span>  
<span data-ttu-id="e0516-110">總和檢查碼中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e0516-110">The number of bytes in the checksum.</span></span> <span data-ttu-id="e0516-111">當 checkSumAlgorithm 等於 CHECKSUMALGORITHM：： md5 時，checkSumByteCount 是16。</span><span class="sxs-lookup"><span data-stu-id="e0516-111">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::md5, checkSumByteCount is 16.</span></span> <span data-ttu-id="e0516-112">當 checkSumAlgorithm 等於 CHECKSUMALGORITHM：： sha1 時，checkSumByteCount 為20。</span><span class="sxs-lookup"><span data-stu-id="e0516-112">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::sha1, checkSumByteCount is 20.</span></span>

<span data-ttu-id="e0516-113">**checkSumAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="e0516-113">**checkSumAlgorithm**</span></span>  
<span data-ttu-id="e0516-114">指定用來產生檔案總和檢查碼的演算法。</span><span class="sxs-lookup"><span data-stu-id="e0516-114">Specifies the algorithm used to generate the checksum of the file.</span></span> <span data-ttu-id="e0516-115">支援的演算法為 MD5 和 SHA1。</span><span class="sxs-lookup"><span data-stu-id="e0516-115">Supported algorithms are MD5 and SHA1.</span></span> <span data-ttu-id="e0516-116">如需詳細資訊，請參閱 CHECKSUMALGORITHM 列舉。</span><span class="sxs-lookup"><span data-stu-id="e0516-116">For more information, see the CHECKSUMALGORITHM enum.</span></span>

<span data-ttu-id="e0516-117">**checkSumFirstPart**</span><span class="sxs-lookup"><span data-stu-id="e0516-117">**checkSumFirstPart**</span></span>  
<span data-ttu-id="e0516-118">總和檢查碼的前8個位元組部分。</span><span class="sxs-lookup"><span data-stu-id="e0516-118">The first 8 byte portion of the checksum.</span></span>

<span data-ttu-id="e0516-119">**checkSumSecondPart**</span><span class="sxs-lookup"><span data-stu-id="e0516-119">**checkSumSecondPart**</span></span>  
<span data-ttu-id="e0516-120">總和檢查碼的第二個8位元組部分。</span><span class="sxs-lookup"><span data-stu-id="e0516-120">The second 8 byte portion of the checksum.</span></span>

<span data-ttu-id="e0516-121">**checkSumThirdPart**</span><span class="sxs-lookup"><span data-stu-id="e0516-121">**checkSumThirdPart**</span></span>  
<span data-ttu-id="e0516-122">總和檢查碼的第三個8位元組部分。</span><span class="sxs-lookup"><span data-stu-id="e0516-122">The third 8 byte portion of the checksum.</span></span>

<span data-ttu-id="e0516-123">**checkSumFourthPart**</span><span class="sxs-lookup"><span data-stu-id="e0516-123">**checkSumFourthPart**</span></span>  
<span data-ttu-id="e0516-124">總和檢查碼的第四個8位元組部分。</span><span class="sxs-lookup"><span data-stu-id="e0516-124">The fourth 8 byte portion of the checksum.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0516-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0516-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e0516-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e0516-126">Header</span></span></p></td><td><span data-ttu-id="e0516-127">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="e0516-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



