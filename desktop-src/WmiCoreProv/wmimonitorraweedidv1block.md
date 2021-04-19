---
description: 表示來自視頻電子郵件標準關聯的原始資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 結構。
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: WmiMonitorRawEEdidV1Block 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982488"
---
# <a name="wmimonitorraweedidv1block-class"></a><span data-ttu-id="b824b-103">WmiMonitorRawEEdidV1Block 類別</span><span class="sxs-lookup"><span data-stu-id="b824b-103">WmiMonitorRawEEdidV1Block class</span></span>

<span data-ttu-id="b824b-104">**WmiMonitorRawEEdidV1Block** WMI 類別代表來自視頻電子郵件標準關聯的原始資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 結構。</span><span class="sxs-lookup"><span data-stu-id="b824b-104">The **WmiMonitorRawEEdidV1Block** WMI class represents the raw data from a Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span> <span data-ttu-id="b824b-105">這個128位元組資料結構包含的資訊會描述顯示的最佳設定。</span><span class="sxs-lookup"><span data-stu-id="b824b-105">This 128-byte data structure contains information that describes the optimal configuration for a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="b824b-106">語法</span><span class="sxs-lookup"><span data-stu-id="b824b-106">Syntax</span></span>

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a><span data-ttu-id="b824b-107">成員</span><span class="sxs-lookup"><span data-stu-id="b824b-107">Members</span></span>

<span data-ttu-id="b824b-108">**WmiMonitorRawEEdidV1Block** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b824b-108">The **WmiMonitorRawEEdidV1Block** class has these types of members:</span></span>

-   [<span data-ttu-id="b824b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b824b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b824b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b824b-110">Properties</span></span>

<span data-ttu-id="b824b-111">**WmiMonitorRawEEdidV1Block** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b824b-111">The **WmiMonitorRawEEdidV1Block** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b824b-112">**使用中**</span><span class="sxs-lookup"><span data-stu-id="b824b-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b824b-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b824b-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b824b-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b824b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b824b-115">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="b824b-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b824b-116">**內容**</span><span class="sxs-lookup"><span data-stu-id="b824b-116">**Content**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b824b-117">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="b824b-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b824b-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b824b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b824b-119">128位元組陣列，其中包含原始區塊內容。</span><span class="sxs-lookup"><span data-stu-id="b824b-119">128 byte array that contains the raw block content.</span></span>

</dd> <dt>

<span data-ttu-id="b824b-120">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="b824b-120">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b824b-121">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="b824b-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b824b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b824b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b824b-123">資料區塊的識別。</span><span class="sxs-lookup"><span data-stu-id="b824b-123">Identity of the data block.</span></span>

</dd> <dt>

<span data-ttu-id="b824b-124">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b824b-124">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b824b-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b824b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b824b-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b824b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b824b-127">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="b824b-127">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b824b-128">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b824b-128">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="b824b-129">**型別**</span><span class="sxs-lookup"><span data-stu-id="b824b-129">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b824b-130">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="b824b-130">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b824b-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b824b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b824b-132">資料區塊的類型。</span><span class="sxs-lookup"><span data-stu-id="b824b-132">Type of data block.</span></span> <span data-ttu-id="b824b-133">下表列出可以傳回的可能值。</span><span class="sxs-lookup"><span data-stu-id="b824b-133">The following table lists possible values that can be returned.</span></span>



| <span data-ttu-id="b824b-134">值</span><span class="sxs-lookup"><span data-stu-id="b824b-134">Value</span></span>                                                                                 | <span data-ttu-id="b824b-135">意義</span><span class="sxs-lookup"><span data-stu-id="b824b-135">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="b824b-136"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="b824b-136"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="b824b-137">未初始化：</span><span class="sxs-lookup"><span data-stu-id="b824b-137">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="b824b-138"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="b824b-138"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="b824b-139">EDID 基底區塊</span><span class="sxs-lookup"><span data-stu-id="b824b-139">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="b824b-140"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="b824b-140"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="b824b-141">EDID 區塊對應</span><span class="sxs-lookup"><span data-stu-id="b824b-141">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="b824b-142"><dt>255 (0xFF) </dt></span><span class="sxs-lookup"><span data-stu-id="b824b-142"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="b824b-143">其他</span><span class="sxs-lookup"><span data-stu-id="b824b-143">Other</span></span><br/>           |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b824b-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="b824b-144">Requirements</span></span>



| <span data-ttu-id="b824b-145">需求</span><span class="sxs-lookup"><span data-stu-id="b824b-145">Requirement</span></span> | <span data-ttu-id="b824b-146">值</span><span class="sxs-lookup"><span data-stu-id="b824b-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b824b-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b824b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b824b-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b824b-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b824b-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b824b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b824b-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b824b-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b824b-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="b824b-151">Namespace</span></span><br/>                | <span data-ttu-id="b824b-152">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="b824b-152">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b824b-153">MOF</span><span class="sxs-lookup"><span data-stu-id="b824b-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b824b-154"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="b824b-154"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b824b-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b824b-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b824b-156"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b824b-156"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b824b-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b824b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b824b-158">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="b824b-158">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="b824b-159">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="b824b-159">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




