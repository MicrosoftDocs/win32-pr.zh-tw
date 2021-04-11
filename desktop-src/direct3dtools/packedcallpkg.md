---
description: 代表四個呼叫的封裝。
MS-HAID: vspixengine.PackedCallPkg
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PackedCallPkg 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE345C1A-9F6E-4FE0-99C7-6B332A1ED079
api_name:
- PackedCallPkg
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 104e764725213f7030c90a0240641c7c9b063785
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935784"
---
# <a name="span-idvspixenginepackedcallpkgspanpackedcallpkg-structure"></a><span data-ttu-id="127a3-103"><span id="vspixengine.packedcallpkg"></span>PackedCallPkg 結構</span><span class="sxs-lookup"><span data-stu-id="127a3-103"><span id="vspixengine.packedcallpkg"></span>PackedCallPkg structure</span></span>

<span data-ttu-id="127a3-104">代表四個呼叫的封裝。</span><span class="sxs-lookup"><span data-stu-id="127a3-104">Represents a package of four calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="127a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="127a3-105">Syntax</span></span>


```C++
typedef struct PackedCallPkg {
  UINT pcp1;
  UINT pcp2;
  UINT pcp3;
  UINT pcp4;
} PackedCallPkg;
```

## <a name="members"></a><span data-ttu-id="127a3-106">成員</span><span class="sxs-lookup"><span data-stu-id="127a3-106">Members</span></span>

<span data-ttu-id="127a3-107">**pcp1**</span><span class="sxs-lookup"><span data-stu-id="127a3-107">**pcp1**</span></span>  
<span data-ttu-id="127a3-108">封裝中的第一個呼叫。</span><span class="sxs-lookup"><span data-stu-id="127a3-108">The first call in the package.</span></span>

<span data-ttu-id="127a3-109">**pcp2**</span><span class="sxs-lookup"><span data-stu-id="127a3-109">**pcp2**</span></span>  
<span data-ttu-id="127a3-110">封裝中的第二個呼叫。</span><span class="sxs-lookup"><span data-stu-id="127a3-110">The second call in the package.</span></span>

<span data-ttu-id="127a3-111">**pcp3**</span><span class="sxs-lookup"><span data-stu-id="127a3-111">**pcp3**</span></span>  
<span data-ttu-id="127a3-112">封裝中的第三個呼叫。</span><span class="sxs-lookup"><span data-stu-id="127a3-112">The third call in the package.</span></span>

<span data-ttu-id="127a3-113">**pcp4**</span><span class="sxs-lookup"><span data-stu-id="127a3-113">**pcp4**</span></span>  
<span data-ttu-id="127a3-114">封裝中的第四個呼叫。</span><span class="sxs-lookup"><span data-stu-id="127a3-114">The fourth call in the package.</span></span>

## <a name="requirements"></a><span data-ttu-id="127a3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="127a3-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="127a3-116">標頭</span><span class="sxs-lookup"><span data-stu-id="127a3-116">Header</span></span></p></td><td><span data-ttu-id="127a3-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="127a3-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



