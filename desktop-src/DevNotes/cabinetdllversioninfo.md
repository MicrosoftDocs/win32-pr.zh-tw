---
description: CABINETDLLVERSIONINFO 包含 Cabinet.dll 的版本資訊。
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: CABINETDLLVERSIONINFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847236"
---
# <a name="cabinetdllversioninfo-structure"></a><span data-ttu-id="5cef2-103">CABINETDLLVERSIONINFO 結構</span><span class="sxs-lookup"><span data-stu-id="5cef2-103">CABINETDLLVERSIONINFO structure</span></span>

<span data-ttu-id="5cef2-104">\[只有在使用不支援的 **DllGetVersion** 函數時，此結構才會包含所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="5cef2-104">\[This structure contains information required only when using the **DllGetVersion** function, which is not supported.</span></span> <span data-ttu-id="5cef2-105">本檔僅供參考之用。\]</span><span class="sxs-lookup"><span data-stu-id="5cef2-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="5cef2-106">**CABINETDLLVERSIONINFO** 包含 Cabinet.dll 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="5cef2-106">The **CABINETDLLVERSIONINFO** contains the version information for Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cef2-107">語法</span><span class="sxs-lookup"><span data-stu-id="5cef2-107">Syntax</span></span>


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="5cef2-108">成員</span><span class="sxs-lookup"><span data-stu-id="5cef2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5cef2-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="5cef2-109">**cbStruct**</span></span>
</dt> <dd>

<span data-ttu-id="5cef2-110">此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5cef2-110">The size of this structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5cef2-111">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="5cef2-111">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="5cef2-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="5cef2-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5cef2-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="5cef2-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="5cef2-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="5cef2-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5cef2-115">**dwFileVersionMS**</span><span class="sxs-lookup"><span data-stu-id="5cef2-115">**dwFileVersionMS**</span></span>
</dt> <dd>

<span data-ttu-id="5cef2-116">包含版本資訊的最高有效位。</span><span class="sxs-lookup"><span data-stu-id="5cef2-116">Contains the most significant bits of the version information.</span></span> <span data-ttu-id="5cef2-117">Bits 0-15 包含次要版本，而 bits 16-31 包含主要版本。</span><span class="sxs-lookup"><span data-stu-id="5cef2-117">Bits 0-15 contain the minor version, and bits 16-31 contain the major version.</span></span>

</dd> <dt>

<span data-ttu-id="5cef2-118">**dwFileVersionLS**</span><span class="sxs-lookup"><span data-stu-id="5cef2-118">**dwFileVersionLS**</span></span>
</dt> <dd>

<span data-ttu-id="5cef2-119">包含版本資訊的最小有效位。</span><span class="sxs-lookup"><span data-stu-id="5cef2-119">Contains the least significant bits of the version information.</span></span> <span data-ttu-id="5cef2-120">Bits 0-15 包含修訂編號，而 bits 16-31 包含組建編號。</span><span class="sxs-lookup"><span data-stu-id="5cef2-120">Bits 0-15 contain the revision number, and bits 16-31 contain the build number.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="5cef2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cef2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cef2-122">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="5cef2-122">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 



