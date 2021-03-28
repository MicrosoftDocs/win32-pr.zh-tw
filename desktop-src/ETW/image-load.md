---
description: 這個類別是影像事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Image_Load 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513096"
---
# <a name="image_load-class"></a><span data-ttu-id="83842-104">映射 \_ 載入類別</span><span class="sxs-lookup"><span data-stu-id="83842-104">Image\_Load class</span></span>

<span data-ttu-id="83842-105">這個類別是影像事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="83842-105">This class is the event type class for image events.</span></span>

<span data-ttu-id="83842-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="83842-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="83842-107">語法</span><span class="sxs-lookup"><span data-stu-id="83842-107">Syntax</span></span>

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="83842-108">成員</span><span class="sxs-lookup"><span data-stu-id="83842-108">Members</span></span>

<span data-ttu-id="83842-109">**映射 \_ 載入** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="83842-109">The **Image\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="83842-110">屬性</span><span class="sxs-lookup"><span data-stu-id="83842-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83842-111">屬性</span><span class="sxs-lookup"><span data-stu-id="83842-111">Properties</span></span>

<span data-ttu-id="83842-112">**映射 \_ 載入** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="83842-112">The **Image\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83842-113">DefaultBase</span><span class="sxs-lookup"><span data-stu-id="83842-113">DefaultBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-116">限定詞： WmiDataId (7) ，指標</span><span class="sxs-lookup"><span data-stu-id="83842-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="83842-117">預設基底位址。</span><span class="sxs-lookup"><span data-stu-id="83842-117">Default base address.</span></span>

</dd> <dt>

<span data-ttu-id="83842-118">FileName</span><span class="sxs-lookup"><span data-stu-id="83842-118">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="83842-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83842-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-121">限定詞： WmiDataId (12) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="83842-121">Qualifiers: WmiDataId(12), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="83842-122">DLL 或可執行檔映射的檔案名和副檔名。</span><span class="sxs-lookup"><span data-stu-id="83842-122">File name and extension of the DLL or executable image.</span></span>

</dd> <dt>

<span data-ttu-id="83842-123">Imagebase 設定</span><span class="sxs-lookup"><span data-stu-id="83842-123">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-126">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="83842-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="83842-127">載入映射之應用程式的基底位址。</span><span class="sxs-lookup"><span data-stu-id="83842-127">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="83842-128">ImageCheckSum</span><span class="sxs-lookup"><span data-stu-id="83842-128">ImageCheckSum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-131">限定詞： WmiDataId (4) </span><span class="sxs-lookup"><span data-stu-id="83842-131">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="83842-132">影像檢查總和。</span><span class="sxs-lookup"><span data-stu-id="83842-132">Image check sum.</span></span>

</dd> <dt>

<span data-ttu-id="83842-133">ImageSize</span><span class="sxs-lookup"><span data-stu-id="83842-133">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-136">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="83842-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="83842-137">所載入映射的大小。</span><span class="sxs-lookup"><span data-stu-id="83842-137">Size of the image being loaded.</span></span>

<span data-ttu-id="83842-138">使用這個屬性時，這個屬性的資料類型實際上是大小 \_ t。</span><span class="sxs-lookup"><span data-stu-id="83842-138">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="83842-139">指標辨識符號用來判斷大小 \_ t 是4個位元組或8個位元組。</span><span class="sxs-lookup"><span data-stu-id="83842-139">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="83842-140">ProcessId</span><span class="sxs-lookup"><span data-stu-id="83842-140">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-143">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="83842-143">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="83842-144">識別載入影像的進程。</span><span class="sxs-lookup"><span data-stu-id="83842-144">Identifies the process into which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="83842-145">Reserved0</span><span class="sxs-lookup"><span data-stu-id="83842-145">Reserved0</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-148">限定詞： WmiDataId (6) </span><span class="sxs-lookup"><span data-stu-id="83842-148">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="83842-149">保留的。</span><span class="sxs-lookup"><span data-stu-id="83842-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="83842-150">Reserved1</span><span class="sxs-lookup"><span data-stu-id="83842-150">Reserved1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-153">限定詞： WmiDataId (8) </span><span class="sxs-lookup"><span data-stu-id="83842-153">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="83842-154">保留的。</span><span class="sxs-lookup"><span data-stu-id="83842-154">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="83842-155">Reserved2</span><span class="sxs-lookup"><span data-stu-id="83842-155">Reserved2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-156">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-158">限定詞： WmiDataId (9) </span><span class="sxs-lookup"><span data-stu-id="83842-158">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="83842-159">保留的。</span><span class="sxs-lookup"><span data-stu-id="83842-159">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="83842-160">Reserved3</span><span class="sxs-lookup"><span data-stu-id="83842-160">Reserved3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-163">限定詞： WmiDataId (10) </span><span class="sxs-lookup"><span data-stu-id="83842-163">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="83842-164">保留的。</span><span class="sxs-lookup"><span data-stu-id="83842-164">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="83842-165">Reserved4</span><span class="sxs-lookup"><span data-stu-id="83842-165">Reserved4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-166">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-168">限定詞： WmiDataId (11) </span><span class="sxs-lookup"><span data-stu-id="83842-168">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="83842-169">保留的。</span><span class="sxs-lookup"><span data-stu-id="83842-169">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="83842-170">TimeDateStamp</span><span class="sxs-lookup"><span data-stu-id="83842-170">TimeDateStamp</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83842-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="83842-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83842-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="83842-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83842-173">限定詞： WmiDataId (5) </span><span class="sxs-lookup"><span data-stu-id="83842-173">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="83842-174">載入或卸載映射的時間和日期。</span><span class="sxs-lookup"><span data-stu-id="83842-174">Time and date that the image was loaded or unloaded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83842-175">備註</span><span class="sxs-lookup"><span data-stu-id="83842-175">Remarks</span></span>

<span data-ttu-id="83842-176">DCStart 和 DCEnd 事件會分別列舉追蹤開頭和結尾的所有載入的影像。</span><span class="sxs-lookup"><span data-stu-id="83842-176">The DCStart and DCEnd events enumerate all loaded images at the beginning and end of the trace, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="83842-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="83842-177">Requirements</span></span>



| <span data-ttu-id="83842-178">需求</span><span class="sxs-lookup"><span data-stu-id="83842-178">Requirement</span></span> | <span data-ttu-id="83842-179">值</span><span class="sxs-lookup"><span data-stu-id="83842-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83842-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83842-180">Minimum supported client</span></span><br/> | <span data-ttu-id="83842-181">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83842-181">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="83842-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83842-182">Minimum supported server</span></span><br/> | <span data-ttu-id="83842-183">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83842-183">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83842-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83842-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83842-185">**Image**</span><span class="sxs-lookup"><span data-stu-id="83842-185">**Image**</span></span>](image.md)
</dt> <dt>

[<span data-ttu-id="83842-186">**影像 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="83842-186">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="83842-187">**映射 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="83842-187">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




