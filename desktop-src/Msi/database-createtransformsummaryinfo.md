---
description: Database 物件的 CreateTransformSummaryInfo 方法會建立並填入現有轉換檔案的摘要資訊資料流程。 這個方法會在屬性中填入基底，並參考 [ProductCode] 和 [ProductVersion]。
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: CreateTransformSummaryInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990163"
---
# <a name="databasecreatetransformsummaryinfo-method"></a><span data-ttu-id="6de53-104">CreateTransformSummaryInfo 方法</span><span class="sxs-lookup"><span data-stu-id="6de53-104">Database.CreateTransformSummaryInfo method</span></span>

<span data-ttu-id="6de53-105">[**Database**](database-object.md)物件的 **CreateTransformSummaryInfo** 方法會建立並填入現有轉換檔案的摘要資訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="6de53-105">The **CreateTransformSummaryInfo** method of the [**Database**](database-object.md) object creates and populates the summary information stream of an existing transform file.</span></span> <span data-ttu-id="6de53-106">這個方法會在屬性中填入基底，並參考 [ [**ProductCode**](productcode.md) ] 和 [ [**ProductVersion**](productversion.md)]。</span><span class="sxs-lookup"><span data-stu-id="6de53-106">This method fills in the properties with the base and reference [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6de53-107">語法</span><span class="sxs-lookup"><span data-stu-id="6de53-107">Syntax</span></span>


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a><span data-ttu-id="6de53-108">參數</span><span class="sxs-lookup"><span data-stu-id="6de53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de53-109">*reference*</span><span class="sxs-lookup"><span data-stu-id="6de53-109">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="6de53-110">不包含變更的必要資料庫。</span><span class="sxs-lookup"><span data-stu-id="6de53-110">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="6de53-111">*儲存體*</span><span class="sxs-lookup"><span data-stu-id="6de53-111">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="6de53-112">產生之轉換檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6de53-112">The name of the generated transform file.</span></span> <span data-ttu-id="6de53-113">這是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6de53-113">This is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6de53-114">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="6de53-114">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="6de53-115">套用轉換時應隱藏的必要錯誤條件。</span><span class="sxs-lookup"><span data-stu-id="6de53-115">Required error conditions that should be suppressed when the transform is applied.</span></span> <span data-ttu-id="6de53-116">合併一或多個下列錯誤條件值。</span><span class="sxs-lookup"><span data-stu-id="6de53-116">Combine one or more of the following error condition values.</span></span>



| <span data-ttu-id="6de53-117">錯誤條件名稱</span><span class="sxs-lookup"><span data-stu-id="6de53-117">Error condition name</span></span>                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="6de53-118">意義</span><span class="sxs-lookup"><span data-stu-id="6de53-118">Meaning</span></span>                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <span data-ttu-id="6de53-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span></span> </dl>                                                                         | <span data-ttu-id="6de53-120">下列情況都沒有。</span><span class="sxs-lookup"><span data-stu-id="6de53-120">None of the following conditions.</span></span><br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="6de53-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span></span> </dl>                                 | <span data-ttu-id="6de53-122">加入已經存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="6de53-122">Adds a row that already exists.</span></span><br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="6de53-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="6de53-124">刪除不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="6de53-124">Deletes a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="6de53-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="6de53-126">加入已經存在的資料表。</span><span class="sxs-lookup"><span data-stu-id="6de53-126">Adds a table that already exists.</span></span><br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="6de53-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="6de53-128">刪除不存在的資料表。</span><span class="sxs-lookup"><span data-stu-id="6de53-128">Deletes a table that does not exist.</span></span><br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="6de53-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span></span> </dl>        | <span data-ttu-id="6de53-130">更新不存在的資料列。</span><span class="sxs-lookup"><span data-stu-id="6de53-130">Updates a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="6de53-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span></span> </dl>                                | <span data-ttu-id="6de53-132">轉換和資料庫字碼頁不相符，且字碼頁不是中立的。</span><span class="sxs-lookup"><span data-stu-id="6de53-132">Transform and database code pages do not match and neither code page is neutral.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6de53-133">*validation*</span><span class="sxs-lookup"><span data-stu-id="6de53-133">*validation*</span></span> 
</dt> <dd>

<span data-ttu-id="6de53-134">當轉換套用至資料庫時為必要項;顯示應該驗證哪些屬性，以確認此轉換可以套用到資料庫。</span><span class="sxs-lookup"><span data-stu-id="6de53-134">Required when the transform is applied to a database; shows which properties should be validated to verify that this transform can be applied to the database.</span></span> <span data-ttu-id="6de53-135">所有屬性都包含在 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md)內。</span><span class="sxs-lookup"><span data-stu-id="6de53-135">The properties are all contained in the [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="6de53-136">結合下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="6de53-136">Combine one or more of the following values.</span></span>



| <span data-ttu-id="6de53-137">驗證旗標</span><span class="sxs-lookup"><span data-stu-id="6de53-137">Validation flag</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="6de53-138">意義</span><span class="sxs-lookup"><span data-stu-id="6de53-138">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <span data-ttu-id="6de53-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="6de53-140">未完成任何驗證。</span><span class="sxs-lookup"><span data-stu-id="6de53-140">No validation done.</span></span><br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <span data-ttu-id="6de53-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="6de53-142">預設語言必須符合基底資料庫。</span><span class="sxs-lookup"><span data-stu-id="6de53-142">Default language must match base database.</span></span><br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <span data-ttu-id="6de53-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="6de53-144">產品必須符合基底資料庫。</span><span class="sxs-lookup"><span data-stu-id="6de53-144">Product must match base database.</span></span><br/>          |



 

<span data-ttu-id="6de53-145">若要驗證產品版本，請先選擇這三個旗標中的一或多個旗標，以指出要驗證的版本數量。</span><span class="sxs-lookup"><span data-stu-id="6de53-145">To validate product version, first choose one or more of these three flags to indicate how much of the version is to be verified.</span></span>



| <span data-ttu-id="6de53-146">驗證旗標</span><span class="sxs-lookup"><span data-stu-id="6de53-146">Validation flag</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="6de53-147">意義</span><span class="sxs-lookup"><span data-stu-id="6de53-147">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <span data-ttu-id="6de53-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span></span> </dl>      | <span data-ttu-id="6de53-149">僅檢查主要版本。</span><span class="sxs-lookup"><span data-stu-id="6de53-149">Checks major version only.</span></span><br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <span data-ttu-id="6de53-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span></span> </dl>     | <span data-ttu-id="6de53-151">只檢查主要和次要版本。</span><span class="sxs-lookup"><span data-stu-id="6de53-151">Checks major and minor version only.</span></span><br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <span data-ttu-id="6de53-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span></span> </dl> | <span data-ttu-id="6de53-153">檢查主要、次要和更新版本。</span><span class="sxs-lookup"><span data-stu-id="6de53-153">Checks major, minor, and update versions.</span></span><br/> |



 

<span data-ttu-id="6de53-154">然後選擇下列其中一項，以指出要套用轉換之資料庫的產品版本與基底資料庫之間的必要關聯性。</span><span class="sxs-lookup"><span data-stu-id="6de53-154">Then choose one of the following to indicate the required relationship between the product version of the database the transform is being applied to and that of the base database.</span></span>



| <span data-ttu-id="6de53-155">驗證旗標</span><span class="sxs-lookup"><span data-stu-id="6de53-155">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="6de53-156">意義</span><span class="sxs-lookup"><span data-stu-id="6de53-156">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <span data-ttu-id="6de53-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span></span> </dl>                                          | <span data-ttu-id="6de53-158">< 基底版本套用的版本</span><span class="sxs-lookup"><span data-stu-id="6de53-158">Applied version < base version</span></span><br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <span data-ttu-id="6de53-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span></span> </dl>             | <span data-ttu-id="6de53-160">套用的版本 <= 基底版本</span><span class="sxs-lookup"><span data-stu-id="6de53-160">Applied version <= base version</span></span><br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <span data-ttu-id="6de53-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span></span> </dl>                                     | <span data-ttu-id="6de53-162">套用的版本 = 基底版本</span><span class="sxs-lookup"><span data-stu-id="6de53-162">Applied version = base version</span></span><br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <span data-ttu-id="6de53-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span></span> </dl> | <span data-ttu-id="6de53-164">套用的版本 >= 基底版本</span><span class="sxs-lookup"><span data-stu-id="6de53-164">Applied version >= base version</span></span><br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <span data-ttu-id="6de53-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span></span> </dl>                            | <span data-ttu-id="6de53-166">> 基底版本套用的版本</span><span class="sxs-lookup"><span data-stu-id="6de53-166">Applied version > base version</span></span><br/>  |



 

<span data-ttu-id="6de53-167">若要驗證是否已將轉換套用至具有適當 [**UpgradeCode**](upgradecode.md)的封裝，請設定下列旗標。</span><span class="sxs-lookup"><span data-stu-id="6de53-167">To validate that the transform is being applied to a package having the appropriate [**UpgradeCode**](upgradecode.md), set the following flag.</span></span>



| <span data-ttu-id="6de53-168">驗證旗標</span><span class="sxs-lookup"><span data-stu-id="6de53-168">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="6de53-169">意義</span><span class="sxs-lookup"><span data-stu-id="6de53-169">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <span data-ttu-id="6de53-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span></span> </dl> | <span data-ttu-id="6de53-171">驗證轉換是否為適當的 [**UpgradeCode**](upgradecode.md)。</span><span class="sxs-lookup"><span data-stu-id="6de53-171">Validates that the transform is the appropriate [**UpgradeCode**](upgradecode.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de53-172">傳回值</span><span class="sxs-lookup"><span data-stu-id="6de53-172">Return value</span></span>

<span data-ttu-id="6de53-173">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6de53-173">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6de53-174">備註</span><span class="sxs-lookup"><span data-stu-id="6de53-174">Remarks</span></span>

<span data-ttu-id="6de53-175">若要建立轉換的摘要資訊資料流程，必須在基底和參考資料庫的 [屬性](property-table.md)資料表中定義 [ [**ProductCode**](productcode.md) ] 和 [ [**ProductVersion**](productversion.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="6de53-175">To create a summary information stream for a transform, the [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md) properties must be defined in the [Property](property-table.md) tables of both the base and reference databases.</span></span> <span data-ttu-id="6de53-176">如果使用 msiTransformValidationUpgradeCode，則必須在這兩個資料庫中定義 [**UpgradeCode**](upgradecode.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6de53-176">If msiTransformValidationUpgradeCode is used, the [**UpgradeCode**](upgradecode.md) property must be defined in both databases.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de53-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="6de53-177">Requirements</span></span>



| <span data-ttu-id="6de53-178">需求</span><span class="sxs-lookup"><span data-stu-id="6de53-178">Requirement</span></span> | <span data-ttu-id="6de53-179">值</span><span class="sxs-lookup"><span data-stu-id="6de53-179">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de53-180">版本</span><span class="sxs-lookup"><span data-stu-id="6de53-180">Version</span></span><br/> | <span data-ttu-id="6de53-181">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="6de53-181">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6de53-182">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="6de53-182">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6de53-183">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6de53-183">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6de53-184">DLL</span><span class="sxs-lookup"><span data-stu-id="6de53-184">DLL</span></span><br/>     | <dl> <span data-ttu-id="6de53-185"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6de53-185"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6de53-186">IID</span><span class="sxs-lookup"><span data-stu-id="6de53-186">IID</span></span><br/>     | <span data-ttu-id="6de53-187">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6de53-187">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="6de53-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6de53-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de53-189">資料庫轉換</span><span class="sxs-lookup"><span data-stu-id="6de53-189">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




