---
title: DownloadCollection.id
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Id 屬性會抓取下載集合的識別碼。
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984758"
---
# <a name="downloadcollectionid"></a><span data-ttu-id="2db5f-106">DownloadCollection.id</span><span class="sxs-lookup"><span data-stu-id="2db5f-106">DownloadCollection.id</span></span>

> [!Note]  
> <span data-ttu-id="2db5f-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="2db5f-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2db5f-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="2db5f-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2db5f-109">**Id** 屬性會抓取下載集合的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2db5f-109">The **id** property retrieves the ID of the download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db5f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2db5f-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a><span data-ttu-id="2db5f-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="2db5f-111">Possible Values</span></span>

<span data-ttu-id="2db5f-112">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="2db5f-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2db5f-113">備註</span><span class="sxs-lookup"><span data-stu-id="2db5f-113">Remarks</span></span>

<span data-ttu-id="2db5f-114">當下載管理員建立新的下載集合時，它會為集合指派識別碼。</span><span class="sxs-lookup"><span data-stu-id="2db5f-114">When the Download Manager creates a new download collection, it assigns the collection an ID number.</span></span> <span data-ttu-id="2db5f-115">識別碼會在 Windows Media Player 會話與作業系統會話之間保存。</span><span class="sxs-lookup"><span data-stu-id="2db5f-115">ID numbers persist between Windows Media Player sessions and operating system sessions.</span></span>

<span data-ttu-id="2db5f-116">ID 號碼不是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2db5f-116">ID numbers are not unique.</span></span> <span data-ttu-id="2db5f-117">不過，32位值中有足夠的識別碼可用，但現有的識別碼不太可能會被新的識別碼覆寫。</span><span class="sxs-lookup"><span data-stu-id="2db5f-117">However, there are enough ID numbers available in the 32-bit value that it is extremely unlikely that an existing ID number will ever be overwritten by a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="2db5f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2db5f-118">Requirements</span></span>



| <span data-ttu-id="2db5f-119">需求</span><span class="sxs-lookup"><span data-stu-id="2db5f-119">Requirement</span></span> | <span data-ttu-id="2db5f-120">值</span><span class="sxs-lookup"><span data-stu-id="2db5f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2db5f-121">版本</span><span class="sxs-lookup"><span data-stu-id="2db5f-121">Version</span></span><br/> | <span data-ttu-id="2db5f-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2db5f-122">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="2db5f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2db5f-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="2db5f-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2db5f-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2db5f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2db5f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db5f-126">**DownloadCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="2db5f-126">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





