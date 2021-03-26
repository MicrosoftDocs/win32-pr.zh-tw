---
description: 這個類別是分頁檔案事件中映射載入的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: PageFault_ImageLoadBacked 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973416"
---
# <a name="pagefault_imageloadbacked-class"></a><span data-ttu-id="84fe4-104">PageFault \_ ImageLoadBacked 類別</span><span class="sxs-lookup"><span data-stu-id="84fe4-104">PageFault\_ImageLoadBacked class</span></span>

<span data-ttu-id="84fe4-105">這個類別是分頁檔案事件中映射載入的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="84fe4-105">This class is the event type class for image load in page file events.</span></span>

<span data-ttu-id="84fe4-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="84fe4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="84fe4-107">語法</span><span class="sxs-lookup"><span data-stu-id="84fe4-107">Syntax</span></span>

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a><span data-ttu-id="84fe4-108">成員</span><span class="sxs-lookup"><span data-stu-id="84fe4-108">Members</span></span>

<span data-ttu-id="84fe4-109">**PageFault \_ ImageLoadBacked** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="84fe4-109">The **PageFault\_ImageLoadBacked** class has these types of members:</span></span>

-   [<span data-ttu-id="84fe4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="84fe4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84fe4-111">屬性</span><span class="sxs-lookup"><span data-stu-id="84fe4-111">Properties</span></span>

<span data-ttu-id="84fe4-112">**PageFault \_ ImageLoadBacked** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="84fe4-112">The **PageFault\_ImageLoadBacked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84fe4-113">**DeviceChar**</span><span class="sxs-lookup"><span data-stu-id="84fe4-113">**DeviceChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84fe4-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84fe4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84fe4-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84fe4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84fe4-116">限定詞： WmiDataId (2) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="84fe4-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="84fe4-117">保留的。</span><span class="sxs-lookup"><span data-stu-id="84fe4-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="84fe4-118">**FileChar**</span><span class="sxs-lookup"><span data-stu-id="84fe4-118">**FileChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84fe4-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84fe4-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84fe4-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84fe4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84fe4-121">限定詞： WmiDataId (3) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="84fe4-121">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="84fe4-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="84fe4-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="84fe4-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="84fe4-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84fe4-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84fe4-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84fe4-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84fe4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84fe4-126">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="84fe4-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="84fe4-127">將 this 指標的值與 [**FileIo \_ Name**](fileio-name.md)事件中的 **FileObject** 指標值比對，以判斷檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="84fe4-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="84fe4-128">**LoadFlags**</span><span class="sxs-lookup"><span data-stu-id="84fe4-128">**LoadFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84fe4-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84fe4-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84fe4-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84fe4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84fe4-131">限定詞： WmiDataId (4) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="84fe4-131">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="84fe4-132">保留的。</span><span class="sxs-lookup"><span data-stu-id="84fe4-132">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84fe4-133">備註</span><span class="sxs-lookup"><span data-stu-id="84fe4-133">Remarks</span></span>

<span data-ttu-id="84fe4-134">此事件會在建立映射區段期間記錄 (例如，當記憶體管理員判斷映射需要複製到分頁檔案中並從中執行時，DLL 載入) 。</span><span class="sxs-lookup"><span data-stu-id="84fe4-134">The event is logged during an image section creation (for example, a DLL load) when the memory manager determines that the image needs to be copied into and run from the page file.</span></span> <span data-ttu-id="84fe4-135">一般而言，映射是從原始程式檔執行，但是當記憶體管理員判斷來源檔案可由現有的寫入器以非同步方式修改，或是當來源檔案位於卸載式媒體或遠端裝置上時，就可能會發生分頁檔案支援。</span><span class="sxs-lookup"><span data-stu-id="84fe4-135">Typically, images are run from the source file but pagefile-backing can occur when the memory manager determines that the source file may be modified asynchronously by existing writers or when the source file is on a removable media or a remote device.</span></span>

## <a name="requirements"></a><span data-ttu-id="84fe4-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="84fe4-136">Requirements</span></span>



| <span data-ttu-id="84fe4-137">需求</span><span class="sxs-lookup"><span data-stu-id="84fe4-137">Requirement</span></span> | <span data-ttu-id="84fe4-138">值</span><span class="sxs-lookup"><span data-stu-id="84fe4-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84fe4-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84fe4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="84fe4-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84fe4-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="84fe4-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84fe4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="84fe4-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84fe4-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84fe4-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84fe4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84fe4-144">**PageFault \_ V2**</span><span class="sxs-lookup"><span data-stu-id="84fe4-144">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




