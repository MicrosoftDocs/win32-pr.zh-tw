---
description: 記錄物件是用來保存和傳送變數值數目的容器。
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Record 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984327"
---
# <a name="record-object"></a><span data-ttu-id="6a392-103">Record 物件</span><span class="sxs-lookup"><span data-stu-id="6a392-103">Record object</span></span>

<span data-ttu-id="6a392-104">**記錄** 物件是用來保存和傳送變數值數目的容器。</span><span class="sxs-lookup"><span data-stu-id="6a392-104">The **Record** object is a container for holding and transferring a variable number of values.</span></span> <span data-ttu-id="6a392-105">記錄中的欄位是以數位的索引，而且可以包含字串、整數、物件和 null 值。</span><span class="sxs-lookup"><span data-stu-id="6a392-105">Fields within the record are numerically indexed and can contain strings, integers, objects, and null values.</span></span> <span data-ttu-id="6a392-106">超過配置記錄大小的欄位會被視為具有永久 null 值。</span><span class="sxs-lookup"><span data-stu-id="6a392-106">Fields beyond the allocated record size are treated as having permanently null values.</span></span> <span data-ttu-id="6a392-107">欄位編號0是保留的。</span><span class="sxs-lookup"><span data-stu-id="6a392-107">Field number 0 is reserved.</span></span>

## <a name="members"></a><span data-ttu-id="6a392-108">成員</span><span class="sxs-lookup"><span data-stu-id="6a392-108">Members</span></span>

<span data-ttu-id="6a392-109">**記錄** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6a392-109">The **Record** object has these types of members:</span></span>

-   [<span data-ttu-id="6a392-110">方法</span><span class="sxs-lookup"><span data-stu-id="6a392-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6a392-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6a392-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6a392-112">方法</span><span class="sxs-lookup"><span data-stu-id="6a392-112">Methods</span></span>

<span data-ttu-id="6a392-113">**記錄** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6a392-113">The **Record** object has these methods.</span></span>



| <span data-ttu-id="6a392-114">方法</span><span class="sxs-lookup"><span data-stu-id="6a392-114">Method</span></span>                                  | <span data-ttu-id="6a392-115">描述</span><span class="sxs-lookup"><span data-stu-id="6a392-115">Description</span></span>                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a392-116">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="6a392-116">**ClearData**</span></span>](record-cleardata.md)   | <span data-ttu-id="6a392-117">清除所有欄位中的資料，並將其設定為 null。</span><span class="sxs-lookup"><span data-stu-id="6a392-117">Clears the data in all fields, setting them to null.</span></span><br/>                                      |
| [<span data-ttu-id="6a392-118">**FormatText**</span><span class="sxs-lookup"><span data-stu-id="6a392-118">**FormatText**</span></span>](record-formattext.md) | <span data-ttu-id="6a392-119">根據欄位0中的範本來格式化欄位。</span><span class="sxs-lookup"><span data-stu-id="6a392-119">Formats fields according to the template in field 0.</span></span><br/>                                      |
| [<span data-ttu-id="6a392-120">**ReadStream**</span><span class="sxs-lookup"><span data-stu-id="6a392-120">**ReadStream**</span></span>](record-readstream.md) | <span data-ttu-id="6a392-121">從保存資料流程資料的記錄欄位讀取指定的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6a392-121">Reads a specified number of bytes from a record field holding stream data.</span></span><br/>                |
| [<span data-ttu-id="6a392-122">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="6a392-122">**SetStream**</span></span>](record-setstream.md)   | <span data-ttu-id="6a392-123">將指定之檔案的內容複寫到指定的記錄欄位中，做為資料流程資料。</span><span class="sxs-lookup"><span data-stu-id="6a392-123">Copies the content of the specified file into the designated record field as stream data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6a392-124">屬性</span><span class="sxs-lookup"><span data-stu-id="6a392-124">Properties</span></span>

<span data-ttu-id="6a392-125">**記錄** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6a392-125">The **Record** object has these properties.</span></span>



| <span data-ttu-id="6a392-126">屬性</span><span class="sxs-lookup"><span data-stu-id="6a392-126">Property</span></span>                                             | <span data-ttu-id="6a392-127">存取類型</span><span class="sxs-lookup"><span data-stu-id="6a392-127">Access type</span></span>           | <span data-ttu-id="6a392-128">Description</span><span class="sxs-lookup"><span data-stu-id="6a392-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a392-129">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="6a392-129">**DataSize**</span></span>](record-datasize.md)<br/>       |                       | <span data-ttu-id="6a392-130">傳回指定欄位的資料大小。</span><span class="sxs-lookup"><span data-stu-id="6a392-130">Returns the size of the data for the designated field.</span></span><br/>                             |
| [<span data-ttu-id="6a392-131">**FieldCount**</span><span class="sxs-lookup"><span data-stu-id="6a392-131">**FieldCount**</span></span>](record-fieldcount.md)<br/>   |                       | <span data-ttu-id="6a392-132">傳回記錄中的欄位數目。</span><span class="sxs-lookup"><span data-stu-id="6a392-132">Returns the number of fields in the record.</span></span><br/>                                        |
| [<span data-ttu-id="6a392-133">**IntegerData**</span><span class="sxs-lookup"><span data-stu-id="6a392-133">**IntegerData**</span></span>](record-integerdata.md)<br/> | <span data-ttu-id="6a392-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6a392-134">Read/write</span></span><br/> | <span data-ttu-id="6a392-135">將32位整數資料傳入或移出記錄內的指定欄位。</span><span class="sxs-lookup"><span data-stu-id="6a392-135">Transfers 32-bit integer data in to or out of a specified field within the record.</span></span><br/> |
| [<span data-ttu-id="6a392-136">**IsNull**</span><span class="sxs-lookup"><span data-stu-id="6a392-136">**IsNull**</span></span>](record-isnull.md)<br/>           |                       | <span data-ttu-id="6a392-137">如果指定的欄位為 null，則傳回 True，如果欄位包含資料，則傳回 False。</span><span class="sxs-lookup"><span data-stu-id="6a392-137">Returns True if the indicated field is null and False if the field contains data.</span></span><br/>  |
| [<span data-ttu-id="6a392-138">**至 convertfrom-stringdata**</span><span class="sxs-lookup"><span data-stu-id="6a392-138">**StringData**</span></span>](record-stringdata.md)<br/>   | <span data-ttu-id="6a392-139">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6a392-139">Read/write</span></span><br/> | <span data-ttu-id="6a392-140">將字串資料傳入或傳出記錄內的指定欄位。</span><span class="sxs-lookup"><span data-stu-id="6a392-140">Transfers string data in to or out of a specified field within the record.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="6a392-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a392-141">Requirements</span></span>



| <span data-ttu-id="6a392-142">需求</span><span class="sxs-lookup"><span data-stu-id="6a392-142">Requirement</span></span> | <span data-ttu-id="6a392-143">值</span><span class="sxs-lookup"><span data-stu-id="6a392-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a392-144">版本</span><span class="sxs-lookup"><span data-stu-id="6a392-144">Version</span></span><br/> | <span data-ttu-id="6a392-145">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="6a392-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6a392-146">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="6a392-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6a392-147">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6a392-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6a392-148">DLL</span><span class="sxs-lookup"><span data-stu-id="6a392-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="6a392-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a392-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6a392-150">IID</span><span class="sxs-lookup"><span data-stu-id="6a392-150">IID</span></span><br/>     | <span data-ttu-id="6a392-151">IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6a392-151">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="6a392-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a392-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a392-153">**CreateRecord 方法**</span><span class="sxs-lookup"><span data-stu-id="6a392-153">**CreateRecord Method**</span></span>](installer-createrecord.md)
</dt> <dt>

[<span data-ttu-id="6a392-154">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="6a392-154">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




