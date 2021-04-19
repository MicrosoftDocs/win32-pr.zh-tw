---
description: 請注意，這個 API 已被取代。 新的應用程式不應使用它。 MSPID 資料類型可識別媒體資料流程的用途。
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: 'MSPID (Mmstream) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984364"
---
# <a name="mspid"></a><span data-ttu-id="0a018-105">MSPID</span><span class="sxs-lookup"><span data-stu-id="0a018-105">MSPID</span></span>

> [!Note]  
> <span data-ttu-id="0a018-106">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="0a018-106">This API is deprecated.</span></span> <span data-ttu-id="0a018-107">新的應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="0a018-107">New applications should not use it.</span></span>

 

<span data-ttu-id="0a018-108">**MSPID** 資料類型可識別媒體資料流程的用途。</span><span class="sxs-lookup"><span data-stu-id="0a018-108">The **MSPID** data type identifies the purpose of a media steam.</span></span>


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a><span data-ttu-id="0a018-109">備註</span><span class="sxs-lookup"><span data-stu-id="0a018-109">Remarks</span></span>

<span data-ttu-id="0a018-110">**MSPID** 只是 GUID 的 typedef。</span><span class="sxs-lookup"><span data-stu-id="0a018-110">**MSPID** is simply a typedef for GUID.</span></span> <span data-ttu-id="0a018-111">已定義下列 MSPIDs。</span><span class="sxs-lookup"><span data-stu-id="0a018-111">The following MSPIDs are defined.</span></span>



| <span data-ttu-id="0a018-112">值</span><span class="sxs-lookup"><span data-stu-id="0a018-112">Value</span></span>               | <span data-ttu-id="0a018-113">描述</span><span class="sxs-lookup"><span data-stu-id="0a018-113">Description</span></span>           |
|---------------------|-----------------------|
| <span data-ttu-id="0a018-114">MSPID \_ PrimaryVideo</span><span class="sxs-lookup"><span data-stu-id="0a018-114">MSPID\_PrimaryVideo</span></span> | <span data-ttu-id="0a018-115">主要影片串流。</span><span class="sxs-lookup"><span data-stu-id="0a018-115">Primary video stream.</span></span> |
| <span data-ttu-id="0a018-116">MSPID \_ PrimaryAudio</span><span class="sxs-lookup"><span data-stu-id="0a018-116">MSPID\_PrimaryAudio</span></span> | <span data-ttu-id="0a018-117">主要音訊串流。</span><span class="sxs-lookup"><span data-stu-id="0a018-117">Primary audio stream.</span></span> |



 

<span data-ttu-id="0a018-118">**REFMSPID** 型別會定義 **MSPID** 的參考。</span><span class="sxs-lookup"><span data-stu-id="0a018-118">The **REFMSPID** type defines a reference to an **MSPID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a018-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a018-119">Requirements</span></span>



| <span data-ttu-id="0a018-120">需求</span><span class="sxs-lookup"><span data-stu-id="0a018-120">Requirement</span></span> | <span data-ttu-id="0a018-121">值</span><span class="sxs-lookup"><span data-stu-id="0a018-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a018-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0a018-122">Header</span></span><br/> | <dl> <span data-ttu-id="0a018-123"><dt>Mmstream。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a018-123"><dt>Mmstream.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a018-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a018-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a018-125">多媒體串流資料類型</span><span class="sxs-lookup"><span data-stu-id="0a018-125">Multimedia Streaming Data Types</span></span>](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




