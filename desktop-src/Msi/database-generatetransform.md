---
description: 資料庫物件的轉換方法會建立一個轉換，在套用至物件資料庫時，會產生參考資料庫。 轉換會儲存在儲存物件中。
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: 資料庫. 此方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995265"
---
# <a name="databasegeneratetransform-method"></a><span data-ttu-id="8d028-104">資料庫. 此方法</span><span class="sxs-lookup"><span data-stu-id="8d028-104">Database.GenerateTransform method</span></span>

<span data-ttu-id="8d028-105">[**資料庫**](database-object.md)物件的轉換 **方法會** 建立一個 [*轉換*](t-gly.md)，在套用至物件資料庫時，會產生參考資料庫。</span><span class="sxs-lookup"><span data-stu-id="8d028-105">The **GenerateTransform** method of the [**Database**](database-object.md) object creates a [*transform*](t-gly.md) that, when applied to the object database, results in the reference database.</span></span> <span data-ttu-id="8d028-106">轉換會儲存在儲存物件中。</span><span class="sxs-lookup"><span data-stu-id="8d028-106">The transform is stored in the storage object.</span></span>

<span data-ttu-id="8d028-107">如果要在安裝期間套用轉換，您必須使用 [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) 方法來填入摘要資訊串流。</span><span class="sxs-lookup"><span data-stu-id="8d028-107">If the transform is to be applied during an installation you must use the [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) method to populate the summary information stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d028-108">語法</span><span class="sxs-lookup"><span data-stu-id="8d028-108">Syntax</span></span>


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a><span data-ttu-id="8d028-109">參數</span><span class="sxs-lookup"><span data-stu-id="8d028-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d028-110">*reference*</span><span class="sxs-lookup"><span data-stu-id="8d028-110">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="8d028-111">不包含變更的必要資料庫。</span><span class="sxs-lookup"><span data-stu-id="8d028-111">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="8d028-112">*儲存體*</span><span class="sxs-lookup"><span data-stu-id="8d028-112">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="8d028-113">產生之轉換檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d028-113">The name of the generated transform file.</span></span> <span data-ttu-id="8d028-114">這是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8d028-114">This is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d028-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d028-115">Return value</span></span>

<span data-ttu-id="8d028-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8d028-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d028-117">備註</span><span class="sxs-lookup"><span data-stu-id="8d028-117">Remarks</span></span>

<span data-ttu-id="8d028-118">轉換可以將非主鍵資料行加入至資料表的結尾。</span><span class="sxs-lookup"><span data-stu-id="8d028-118">A transform can add non-primary key columns to the end of a table.</span></span> <span data-ttu-id="8d028-119">無法建立轉換，將主鍵資料行加入至資料表。</span><span class="sxs-lookup"><span data-stu-id="8d028-119">A transform cannot be created that adds primary key columns to a table.</span></span> <span data-ttu-id="8d028-120">無法建立變更資料行順序、名稱或定義的轉換。</span><span class="sxs-lookup"><span data-stu-id="8d028-120">A transform cannot be created that changes the order, names, or definitions of columns.</span></span>

<span data-ttu-id="8d028-121">這個方法會傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="8d028-121">This method returns a Boolean value.</span></span> <span data-ttu-id="8d028-122">如果產生轉換，則會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="8d028-122">It returns TRUE if a transform is generated.</span></span> <span data-ttu-id="8d028-123">如果未產生轉換，則會傳回 FALSE，因為兩個資料庫之間沒有任何差異。</span><span class="sxs-lookup"><span data-stu-id="8d028-123">It returns FALSE if a transform is not generated because there are no differences between the two databases.</span></span> <span data-ttu-id="8d028-124">如果方法失敗，則會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="8d028-124">If the method fails, it generates an error.</span></span>

<span data-ttu-id="8d028-125">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="8d028-125">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d028-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d028-126">Requirements</span></span>



| <span data-ttu-id="8d028-127">需求</span><span class="sxs-lookup"><span data-stu-id="8d028-127">Requirement</span></span> | <span data-ttu-id="8d028-128">值</span><span class="sxs-lookup"><span data-stu-id="8d028-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d028-129">版本</span><span class="sxs-lookup"><span data-stu-id="8d028-129">Version</span></span><br/> | <span data-ttu-id="8d028-130">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="8d028-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8d028-131">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="8d028-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8d028-132">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="8d028-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8d028-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8d028-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="8d028-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d028-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8d028-135">IID</span><span class="sxs-lookup"><span data-stu-id="8d028-135">IID</span></span><br/>     | <span data-ttu-id="8d028-136">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8d028-136">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="8d028-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d028-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d028-138">**資料庫**</span><span class="sxs-lookup"><span data-stu-id="8d028-138">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="8d028-139">資料庫轉換</span><span class="sxs-lookup"><span data-stu-id="8d028-139">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




