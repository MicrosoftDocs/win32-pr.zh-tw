---
description: Image_V0_Load 類別-這個類別是影像載入事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Image_V0_Load 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106508"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="30cec-104">Image \_ V0 \_ Load 類別</span><span class="sxs-lookup"><span data-stu-id="30cec-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="30cec-105">這個類別是影像載入事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="30cec-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="30cec-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="30cec-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="30cec-107">語法</span><span class="sxs-lookup"><span data-stu-id="30cec-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="30cec-108">成員</span><span class="sxs-lookup"><span data-stu-id="30cec-108">Members</span></span>

<span data-ttu-id="30cec-109">**Image \_ V0 \_ Load** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="30cec-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="30cec-110">屬性</span><span class="sxs-lookup"><span data-stu-id="30cec-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30cec-111">屬性</span><span class="sxs-lookup"><span data-stu-id="30cec-111">Properties</span></span>

<span data-ttu-id="30cec-112">**Image \_ V0 \_ Load** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="30cec-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30cec-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="30cec-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30cec-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="30cec-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="30cec-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="30cec-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30cec-116">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="30cec-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="30cec-117">載入映射之應用程式的基底位址。</span><span class="sxs-lookup"><span data-stu-id="30cec-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="30cec-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="30cec-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30cec-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="30cec-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30cec-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="30cec-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30cec-121">限定詞： WmiDataId (3) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="30cec-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="30cec-122">要載入之 DLL 或可執行映射的檔案名和副檔名。</span><span class="sxs-lookup"><span data-stu-id="30cec-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="30cec-123">ModuleSize</span><span class="sxs-lookup"><span data-stu-id="30cec-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30cec-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="30cec-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="30cec-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="30cec-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30cec-126">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="30cec-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="30cec-127">影像的大小。</span><span class="sxs-lookup"><span data-stu-id="30cec-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30cec-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="30cec-128">Requirements</span></span>



| <span data-ttu-id="30cec-129">需求</span><span class="sxs-lookup"><span data-stu-id="30cec-129">Requirement</span></span> | <span data-ttu-id="30cec-130">值</span><span class="sxs-lookup"><span data-stu-id="30cec-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="30cec-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30cec-131">Minimum supported client</span></span><br/> | <span data-ttu-id="30cec-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30cec-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="30cec-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30cec-133">Minimum supported server</span></span><br/> | <span data-ttu-id="30cec-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30cec-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="30cec-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30cec-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30cec-136">**影像 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="30cec-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




