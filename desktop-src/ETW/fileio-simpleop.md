---
description: 這個類別是簡單檔案作業事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: FileIo_SimpleOp 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973553"
---
# <a name="fileio_simpleop-class"></a><span data-ttu-id="3f9ee-104">FileIo \_ SimpleOp 類別</span><span class="sxs-lookup"><span data-stu-id="3f9ee-104">FileIo\_SimpleOp class</span></span>

<span data-ttu-id="3f9ee-105">這個類別是簡單檔案作業事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-105">This class is the event type class for simple file operation events.</span></span>

<span data-ttu-id="3f9ee-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f9ee-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f9ee-107">Syntax</span></span>

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a><span data-ttu-id="3f9ee-108">成員</span><span class="sxs-lookup"><span data-stu-id="3f9ee-108">Members</span></span>

<span data-ttu-id="3f9ee-109">**FileIo \_ SimpleOp** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3f9ee-109">The **FileIo\_SimpleOp** class has these types of members:</span></span>

-   [<span data-ttu-id="3f9ee-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3f9ee-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f9ee-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3f9ee-111">Properties</span></span>

<span data-ttu-id="3f9ee-112">**FileIo \_ SimpleOp** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-112">The **FileIo\_SimpleOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f9ee-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f9ee-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f9ee-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f9ee-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f9ee-116">限定詞： WmiDataId (4) ，指標</span><span class="sxs-lookup"><span data-stu-id="3f9ee-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3f9ee-117">若要判斷檔案名，請將這個屬性的值與 [**FileIo \_ name**](fileio-name.md)事件的 **FileObject** 屬性比對。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="3f9ee-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f9ee-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f9ee-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f9ee-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f9ee-121">限定詞： WmiDataId (3) ，指標</span><span class="sxs-lookup"><span data-stu-id="3f9ee-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3f9ee-122">可在檔案建立和關閉事件之間，用來將作業相互關聯至相同開啟檔案物件實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="3f9ee-123">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-123">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f9ee-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f9ee-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f9ee-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f9ee-126">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="3f9ee-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3f9ee-127">IO 要求封包。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-127">IO request packet.</span></span> <span data-ttu-id="3f9ee-128">這個屬性會識別 IO 活動。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-128">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="3f9ee-129">**TTID**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-129">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f9ee-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f9ee-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f9ee-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f9ee-132">限定詞： WmiDataId (2) ，指標</span><span class="sxs-lookup"><span data-stu-id="3f9ee-132">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3f9ee-133">執行作業之執行緒的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-133">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f9ee-134">備註</span><span class="sxs-lookup"><span data-stu-id="3f9ee-134">Remarks</span></span>

<span data-ttu-id="3f9ee-135">當檔案的最後控制碼關閉時，就會記錄清除事件。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-135">The Cleanup event is logged when the last handle to the file is closed.</span></span> <span data-ttu-id="3f9ee-136">Close 事件指定正在釋放檔案物件。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-136">The Close event specifies that a file object is being freed.</span></span> <span data-ttu-id="3f9ee-137">Flush 事件會指定將檔案緩衝區完整排清至磁片的時間。</span><span class="sxs-lookup"><span data-stu-id="3f9ee-137">The Flush event specifies when the file buffers are fully flushed to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f9ee-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f9ee-138">Requirements</span></span>



| <span data-ttu-id="3f9ee-139">需求</span><span class="sxs-lookup"><span data-stu-id="3f9ee-139">Requirement</span></span> | <span data-ttu-id="3f9ee-140">值</span><span class="sxs-lookup"><span data-stu-id="3f9ee-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f9ee-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f9ee-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3f9ee-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f9ee-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f9ee-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f9ee-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3f9ee-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f9ee-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f9ee-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f9ee-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f9ee-146">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="3f9ee-146">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




