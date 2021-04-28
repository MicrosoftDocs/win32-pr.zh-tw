---
description: Image_V1_Load 類別-這個類別是影像載入事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e8a8c31cee7e45311887c16a1d10545e6a38e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106496"
---
# <a name="image_v1_load-class"></a><span data-ttu-id="d0054-104">映射 \_ V1 \_ 載入類別</span><span class="sxs-lookup"><span data-stu-id="d0054-104">Image\_V1\_Load class</span></span>

<span data-ttu-id="d0054-105">這個類別是影像載入事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="d0054-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="d0054-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d0054-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0054-107">語法</span><span class="sxs-lookup"><span data-stu-id="d0054-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="d0054-108">成員</span><span class="sxs-lookup"><span data-stu-id="d0054-108">Members</span></span>

<span data-ttu-id="d0054-109">**映射 \_ V1 \_ 載入** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d0054-109">The **Image\_V1\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="d0054-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d0054-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0054-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d0054-111">Properties</span></span>

<span data-ttu-id="d0054-112">**映射 \_ V1 \_ 載入** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d0054-112">The **Image\_V1\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0054-113">FileName</span><span class="sxs-lookup"><span data-stu-id="d0054-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0054-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d0054-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0054-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0054-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0054-116">限定詞： WmiDataId (4) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="d0054-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="d0054-117">要載入之 DLL 或可執行映射的檔案名和副檔名。</span><span class="sxs-lookup"><span data-stu-id="d0054-117">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="d0054-118">Imagebase 設定</span><span class="sxs-lookup"><span data-stu-id="d0054-118">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0054-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d0054-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0054-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0054-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0054-121">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="d0054-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d0054-122">載入映射之應用程式的基底位址。</span><span class="sxs-lookup"><span data-stu-id="d0054-122">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d0054-123">ImageSize</span><span class="sxs-lookup"><span data-stu-id="d0054-123">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0054-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d0054-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0054-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0054-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0054-126">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="d0054-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d0054-127">所載入映射的大小。</span><span class="sxs-lookup"><span data-stu-id="d0054-127">Size of the image being loaded.</span></span>

<span data-ttu-id="d0054-128">使用這個屬性時，這個屬性的資料類型實際上是大小 \_ t。</span><span class="sxs-lookup"><span data-stu-id="d0054-128">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="d0054-129">指標辨識符號用來判斷大小 \_ t 是4個位元組或8個位元組。</span><span class="sxs-lookup"><span data-stu-id="d0054-129">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d0054-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="d0054-130">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0054-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d0054-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0054-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d0054-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0054-133">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="d0054-133">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="d0054-134">識別載入影像的進程。</span><span class="sxs-lookup"><span data-stu-id="d0054-134">Identifies the process into which the image is loaded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0054-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0054-135">Requirements</span></span>



| <span data-ttu-id="d0054-136">需求</span><span class="sxs-lookup"><span data-stu-id="d0054-136">Requirement</span></span> | <span data-ttu-id="d0054-137">值</span><span class="sxs-lookup"><span data-stu-id="d0054-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0054-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0054-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d0054-139">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0054-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d0054-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0054-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d0054-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0054-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0054-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0054-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0054-143">**映射 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="d0054-143">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




