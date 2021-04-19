---
description: Merge 物件的 OpenModule 方法會以唯讀模式開啟 Windows Installer 合併模組。 必須先開啟模組，才能與安裝資料庫合併。
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: 'OpenModule 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991362"
---
# <a name="mergeopenmodule-method"></a><span data-ttu-id="9db32-104">Merge. OpenModule 方法</span><span class="sxs-lookup"><span data-stu-id="9db32-104">Merge.OpenModule method</span></span>

<span data-ttu-id="9db32-105">[**Merge**](merge-object.md)物件的 **OpenModule** 方法會以唯讀模式開啟 Windows Installer 合併模組。</span><span class="sxs-lookup"><span data-stu-id="9db32-105">The **OpenModule** method of the [**Merge**](merge-object.md) object opens a Windows Installer merge module in read-only mode.</span></span> <span data-ttu-id="9db32-106">必須先開啟模組，才能與安裝資料庫合併。</span><span class="sxs-lookup"><span data-stu-id="9db32-106">A module must be opened before it can be merged with an installation database.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db32-107">語法</span><span class="sxs-lookup"><span data-stu-id="9db32-107">Syntax</span></span>


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="9db32-108">參數</span><span class="sxs-lookup"><span data-stu-id="9db32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db32-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="9db32-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="9db32-110">指向合併模組的完整檔案名。</span><span class="sxs-lookup"><span data-stu-id="9db32-110">Fully qualified file name pointing to a merge module.</span></span>

</dd> <dt>

<span data-ttu-id="9db32-111">*Language*</span><span class="sxs-lookup"><span data-stu-id="9db32-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="9db32-112"> (LANGID) 的有效語言識別項。</span><span class="sxs-lookup"><span data-stu-id="9db32-112">A valid language identifier (LANGID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db32-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9db32-113">Return value</span></span>

<span data-ttu-id="9db32-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9db32-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db32-115">備註</span><span class="sxs-lookup"><span data-stu-id="9db32-115">Remarks</span></span>

<span data-ttu-id="9db32-116">此函式會在唯讀模式中開啟合併模組，並且在呼叫 [**CloseModule**](merge-closemodule.md) 方法之前，不會將其他程式寫入至合併模組。</span><span class="sxs-lookup"><span data-stu-id="9db32-116">This function opens the merge module in read-only mode and excludes other programs from writing to the merge module until the [**CloseModule**](merge-closemodule.md) method is called.</span></span>

<span data-ttu-id="9db32-117">安裝程式會嘗試以 *語言* 指定的語言或更通用的語言來開啟模組。</span><span class="sxs-lookup"><span data-stu-id="9db32-117">The installer attempts to open the module in the language specified by *Language*, or a more general language.</span></span> <span data-ttu-id="9db32-118">例如，如果 *Language* 指定為1033，則可以使用預設語言來開啟具有1033、9或0之預設語言的模組。</span><span class="sxs-lookup"><span data-stu-id="9db32-118">For example, if *Language* is specified as 1033, a module with a default language of 1033, 9, or 0 can be opened in its default language.</span></span> <span data-ttu-id="9db32-119">*語言* 值9會開啟預設語言為9或0的模組。</span><span class="sxs-lookup"><span data-stu-id="9db32-119">A *Language* value of 9 opens modules with a default language of 9 or 0.</span></span> <span data-ttu-id="9db32-120">如果模組的預設語言不符合指定的需求，則會嘗試將模組轉換成所要求的語言。</span><span class="sxs-lookup"><span data-stu-id="9db32-120">If the default language of the module does not meet the specified requirements, an attempt is made to transform the module to the requested language.</span></span> <span data-ttu-id="9db32-121">如果發生這種情況，則會將模組轉換成逐漸普及的語言，而不是語言中立的。</span><span class="sxs-lookup"><span data-stu-id="9db32-121">If that fails, the module is transformed to increasingly general languages, all the way to language neutral.</span></span> <span data-ttu-id="9db32-122">如果沒有任何轉換成功，則模組無法開啟。</span><span class="sxs-lookup"><span data-stu-id="9db32-122">If none of the transforms succeed, the module fails to open.</span></span> <span data-ttu-id="9db32-123">在此情況下，會將錯誤加入至 msmErrorLanguageUnsupported 類型的錯誤清單。</span><span class="sxs-lookup"><span data-stu-id="9db32-123">In this case, an error is added to the error list of type msmErrorLanguageUnsupported.</span></span> <span data-ttu-id="9db32-124">如果將模組轉換成所需的語言時發生錯誤，則會將錯誤加入至 msmErrorLanguageFailed 類型的錯誤清單。</span><span class="sxs-lookup"><span data-stu-id="9db32-124">If there is an error transforming the module to the desired language, an error is added to the error list of type msmErrorLanguageFailed.</span></span> <span data-ttu-id="9db32-125">如需詳細資訊，請參閱 [**Error**](error-object.md)物件的 [**Type**](error-type.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="9db32-125">For details, see the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span> <span data-ttu-id="9db32-126">開啟合併模組會清除尚未抓取的任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="9db32-126">Opening a merge module clears any errors that have not already been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="9db32-127">C++</span><span class="sxs-lookup"><span data-stu-id="9db32-127">C++</span></span>

<span data-ttu-id="9db32-128">請參閱 [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) 函式。</span><span class="sxs-lookup"><span data-stu-id="9db32-128">See [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db32-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9db32-129">Requirements</span></span>



| <span data-ttu-id="9db32-130">需求</span><span class="sxs-lookup"><span data-stu-id="9db32-130">Requirement</span></span> | <span data-ttu-id="9db32-131">值</span><span class="sxs-lookup"><span data-stu-id="9db32-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9db32-132">版本</span><span class="sxs-lookup"><span data-stu-id="9db32-132">Version</span></span><br/> | <span data-ttu-id="9db32-133">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9db32-133">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="9db32-134">標頭</span><span class="sxs-lookup"><span data-stu-id="9db32-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9db32-135"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="9db32-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="9db32-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9db32-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="9db32-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db32-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
