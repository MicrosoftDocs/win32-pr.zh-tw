---
description: 資料庫物件的 ApplyTransform 方法會將轉換套用至這個資料庫。
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: ApplyTransform 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996017"
---
# <a name="databaseapplytransform-method"></a><span data-ttu-id="5731b-103">ApplyTransform 方法</span><span class="sxs-lookup"><span data-stu-id="5731b-103">Database.ApplyTransform method</span></span>

<span data-ttu-id="5731b-104">[**資料庫**](database-object.md)物件的 **ApplyTransform** 方法會將轉換套用至這個資料庫。</span><span class="sxs-lookup"><span data-stu-id="5731b-104">The **ApplyTransform** method of the [**Database**](database-object.md) object applies the transform to this database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5731b-105">語法</span><span class="sxs-lookup"><span data-stu-id="5731b-105">Syntax</span></span>


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a><span data-ttu-id="5731b-106">參數</span><span class="sxs-lookup"><span data-stu-id="5731b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5731b-107">*儲存體*</span><span class="sxs-lookup"><span data-stu-id="5731b-107">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="5731b-108">要套用之轉換檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="5731b-108">Path to the transform file being applied.</span></span> <span data-ttu-id="5731b-109">此為必要參數。</span><span class="sxs-lookup"><span data-stu-id="5731b-109">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="5731b-110">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="5731b-110">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="5731b-111">指定要隱藏的錯誤條件。</span><span class="sxs-lookup"><span data-stu-id="5731b-111">Specifies the error conditions that are to be suppressed.</span></span> <span data-ttu-id="5731b-112">指定為下列整數值的組合。</span><span class="sxs-lookup"><span data-stu-id="5731b-112">Specify as a combination of the following integer values.</span></span>



| <span data-ttu-id="5731b-113">錯誤狀況</span><span class="sxs-lookup"><span data-stu-id="5731b-113">Error condition</span></span>                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="5731b-114">意義</span><span class="sxs-lookup"><span data-stu-id="5731b-114">Meaning</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="5731b-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="5731b-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span></span> </dl>                                 | <span data-ttu-id="5731b-116">加入已經存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="5731b-116">Adds a row that already exists.</span></span><br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="5731b-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="5731b-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="5731b-118">刪除不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="5731b-118">Deletes a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="5731b-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="5731b-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span></span> </dl>                         | <span data-ttu-id="5731b-120">加入已經存在的資料表。</span><span class="sxs-lookup"><span data-stu-id="5731b-120">Adds a table that already exists.</span></span><br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="5731b-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="5731b-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="5731b-122">刪除不存在的資料表。</span><span class="sxs-lookup"><span data-stu-id="5731b-122">Deletes a table that does not exist.</span></span><br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="5731b-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="5731b-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span></span> </dl>         | <span data-ttu-id="5731b-124">更新不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="5731b-124">Updates a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="5731b-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="5731b-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span></span> </dl>                                 | <span data-ttu-id="5731b-126">轉換和資料庫字碼頁不相符，且沒有中性的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="5731b-126">Transform and database code pages do not match and neither has a neutral code page.</span></span><br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <span data-ttu-id="5731b-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="5731b-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span></span> </dl>                                     | <span data-ttu-id="5731b-128">建立暫存的[ \_ TransformView 資料表](-transformview-table.md)。</span><span class="sxs-lookup"><span data-stu-id="5731b-128">Creates the temporary [\_TransformView table](-transformview-table.md).</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5731b-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="5731b-129">Return value</span></span>

<span data-ttu-id="5731b-130">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5731b-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5731b-131">備註</span><span class="sxs-lookup"><span data-stu-id="5731b-131">Remarks</span></span>

<span data-ttu-id="5731b-132">**ApplyTransform** 方法會延遲轉換資料表，直到最後一個可能的時間為止。</span><span class="sxs-lookup"><span data-stu-id="5731b-132">The **ApplyTransform** method delays transforming tables until the last possible moment.</span></span> <span data-ttu-id="5731b-133">**ApplyTransform** 中所採取的步驟，是立即轉換資料庫的資料表和資料行目錄。</span><span class="sxs-lookup"><span data-stu-id="5731b-133">The steps taken in **ApplyTransform** are to immediately transform the table and column catalogs for the database.</span></span> <span data-ttu-id="5731b-134">資料表和資料行目錄會根據新增或刪除的資料表，以及要加入的資料行來更新 () 不允許刪除資料行。</span><span class="sxs-lookup"><span data-stu-id="5731b-134">The table and column catalogs are updated according to which table is added or deleted and which column is added (no deletion of columns is allowed).</span></span> <span data-ttu-id="5731b-135">如果資料表目前已載入記憶體，且需要轉換，則會轉換。</span><span class="sxs-lookup"><span data-stu-id="5731b-135">If a table is currently loaded in memory and needs to be transformed, it is transformed.</span></span> <span data-ttu-id="5731b-136">否則，資料表狀態會設定為，需要進行轉換，以便在載入資料表時或認可資料庫時，套用轉換。</span><span class="sxs-lookup"><span data-stu-id="5731b-136">Otherwise, the table state is set to that requiring a transform so that when the table is loaded, or when the database is committed, the transform is applied.</span></span> <span data-ttu-id="5731b-137">此實例中的轉換表示會新增、刪除或更新資料表的實際 (資料列) 資料。</span><span class="sxs-lookup"><span data-stu-id="5731b-137">Transform in this instance means that the actual (row) data of the table is added, deleted, or updated.</span></span>

<span data-ttu-id="5731b-138">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="5731b-138">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5731b-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="5731b-139">Requirements</span></span>



| <span data-ttu-id="5731b-140">需求</span><span class="sxs-lookup"><span data-stu-id="5731b-140">Requirement</span></span> | <span data-ttu-id="5731b-141">值</span><span class="sxs-lookup"><span data-stu-id="5731b-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5731b-142">版本</span><span class="sxs-lookup"><span data-stu-id="5731b-142">Version</span></span><br/> | <span data-ttu-id="5731b-143">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5731b-143">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5731b-144">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5731b-144">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5731b-145">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5731b-145">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5731b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5731b-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="5731b-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5731b-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5731b-148">IID</span><span class="sxs-lookup"><span data-stu-id="5731b-148">IID</span></span><br/>     | <span data-ttu-id="5731b-149">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5731b-149">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="5731b-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5731b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5731b-151">**資料庫**</span><span class="sxs-lookup"><span data-stu-id="5731b-151">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="5731b-152">資料庫轉換</span><span class="sxs-lookup"><span data-stu-id="5731b-152">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




