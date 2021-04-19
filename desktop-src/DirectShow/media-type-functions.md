---
description: DirectShow 基類會提供 helper 函式來處理 AM \_ 媒體 \_ 類型結構。
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: '媒體類型函數 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001490"
---
# <a name="media-type-functions"></a><span data-ttu-id="dcb2f-103">媒體類型函式</span><span class="sxs-lookup"><span data-stu-id="dcb2f-103">Media Type Functions</span></span>

<span data-ttu-id="dcb2f-104">DirectShow 基類會提供 helper 函式來處理 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-104">The DirectShow base classes provides helper functions for handling the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="dcb2f-105">**AM \_ 媒體 \_ 類型** 結構包含指標 (**pbFormat** 成員) 至另一個記憶體區塊，也就是所謂的 *格式區塊*。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-105">The **AM\_MEDIA\_TYPE** structure contains a pointer (the **pbFormat** member) to another block of memory, which is called the *format block*.</span></span> <span data-ttu-id="dcb2f-106">因此，當您使用此結構時，您必須小心處理記憶體配置，以避免記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-106">When you work with this structure, therefore, you must be careful about memory allocation in order to avoid memory leaks.</span></span>

<span data-ttu-id="dcb2f-107">下列函式會配置記憶體：</span><span class="sxs-lookup"><span data-stu-id="dcb2f-107">The following functions allocate memory:</span></span>

-   <span data-ttu-id="dcb2f-108">**CreateMediaType** 會配置新的 **AM \_ 媒體 \_ 類型** 結構和格式區塊。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-108">**CreateMediaType** allocates a new **AM\_MEDIA\_TYPE** structure and the format block.</span></span>
-   <span data-ttu-id="dcb2f-109">**CopyMediaType** 會複製到現有的 **AM \_ 媒體 \_ 類型** 結構，但會配置格式區塊。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-109">**CopyMediaType** copies to an existing **AM\_MEDIA\_TYPE** structure, but allocates the format block.</span></span>
-   <span data-ttu-id="dcb2f-110">**CreateAudioMediaType** 會初始化現有的 **AM \_ 媒體 \_ 類型** 結構，並選擇性地配置格式區塊。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-110">**CreateAudioMediaType** initializes an existing **AM\_MEDIA\_TYPE** structure, and optionally allocates the format block.</span></span>

<span data-ttu-id="dcb2f-111">下列功能可用的記憶體：</span><span class="sxs-lookup"><span data-stu-id="dcb2f-111">The following functions free memory:</span></span>

-   <span data-ttu-id="dcb2f-112">**FreeMediaType** 會釋放格式區塊。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-112">**FreeMediaType** releases the format block.</span></span>
-   <span data-ttu-id="dcb2f-113">**DeleteMediaType** 會釋出 **AM \_ 媒體 \_ 類型** 結構，包括格式區塊。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-113">**DeleteMediaType** frees an **AM\_MEDIA\_TYPE** structure, including the format block.</span></span>



| <span data-ttu-id="dcb2f-114">函式</span><span class="sxs-lookup"><span data-stu-id="dcb2f-114">Function</span></span>                                             | <span data-ttu-id="dcb2f-115">描述</span><span class="sxs-lookup"><span data-stu-id="dcb2f-115">Description</span></span>                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcb2f-116">**CopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="dcb2f-116">**CopyMediaType**</span></span>](copymediatype.md)               | <span data-ttu-id="dcb2f-117">複製工作分配的 **AM \_ 媒體 \_ 類型** 結構。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-117">Copies a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                      |
| [<span data-ttu-id="dcb2f-118">**CreateAudioMediaType**</span><span class="sxs-lookup"><span data-stu-id="dcb2f-118">**CreateAudioMediaType**</span></span>](createaudiomediatype.md) | <span data-ttu-id="dcb2f-119">使用指定的 wave 格式結構，初始化媒體類型結構。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-119">Initializes a media type structure given a wave format structure.</span></span>                                           |
| [<span data-ttu-id="dcb2f-120">**CreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="dcb2f-120">**CreateMediaType**</span></span>](createmediatype.md)           | <span data-ttu-id="dcb2f-121">從現有的 **am \_ 媒體 \_ 類型** 結構配置並初始化 **am \_ 媒體 \_ 類型** 結構。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-121">Allocates and initializes an **AM\_MEDIA\_TYPE** structure, from an existing **AM\_MEDIA\_TYPE** structure.</span></span> |
| [<span data-ttu-id="dcb2f-122">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="dcb2f-122">**DeleteMediaType**</span></span>](deletemediatype.md)           | <span data-ttu-id="dcb2f-123">刪除工作配置的 **AM \_ 媒體 \_ 類型** 結構。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-123">Deletes a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                     |
| [<span data-ttu-id="dcb2f-124">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="dcb2f-124">**FreeMediaType**</span></span>](freemediatype.md)               | <span data-ttu-id="dcb2f-125">從記憶體釋出工作分配的 **AM \_ 媒體 \_ 類型** 結構。</span><span class="sxs-lookup"><span data-stu-id="dcb2f-125">Frees a task-allocated **AM\_MEDIA\_TYPE** structure from memory.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="dcb2f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcb2f-126">Requirements</span></span>



| <span data-ttu-id="dcb2f-127">需求</span><span class="sxs-lookup"><span data-stu-id="dcb2f-127">Requirement</span></span> | <span data-ttu-id="dcb2f-128">值</span><span class="sxs-lookup"><span data-stu-id="dcb2f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb2f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="dcb2f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dcb2f-130"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dcb2f-130"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="dcb2f-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcb2f-131">Library</span></span><br/> | <dl> <span data-ttu-id="dcb2f-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dcb2f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




