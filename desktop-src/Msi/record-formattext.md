---
description: 記錄物件的 FormatText 方法會根據欄位0中的範本來格式化欄位。
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: FormatText 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999644"
---
# <a name="recordformattext-method"></a><span data-ttu-id="ea8fd-103">FormatText 方法</span><span class="sxs-lookup"><span data-stu-id="ea8fd-103">Record.FormatText method</span></span>

<span data-ttu-id="ea8fd-104">[**記錄**](record-object.md)物件的 **FormatText** 方法會根據欄位0中的範本來格式化欄位。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-104">The **FormatText** method of the [**Record**](record-object.md) object formats fields according to the template in field 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="ea8fd-105">Syntax</span></span>


```JScript
Record.FormatText()
```



## <a name="parameters"></a><span data-ttu-id="ea8fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="ea8fd-106">Parameters</span></span>

<span data-ttu-id="ea8fd-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea8fd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea8fd-108">Return value</span></span>

<span data-ttu-id="ea8fd-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8fd-110">備註</span><span class="sxs-lookup"><span data-stu-id="ea8fd-110">Remarks</span></span>

<span data-ttu-id="ea8fd-111">如果 **MsiFormatRecord** 傳遞了 null 安裝程式控制碼做為第一個參數，則 **FormatText** 方法會遵循 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式的功能。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-111">The **FormatText** method follows the functionality of the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function if **MsiFormatRecord** was passed a null installer handle as its first parameter.</span></span> <span data-ttu-id="ea8fd-112">如此一來，就只會處理記錄欄位參數，而且無法使用屬性來進行替代。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-112">As a result, only the record field parameters are processed and properties are not available for substitution.</span></span>

<span data-ttu-id="ea8fd-113">例如，"format this field： \[ 1 \] ，format this property： \[ property" 的字串 \] 會解析為 "format this field： value from field 1，format this property： \[ property \] 。"</span><span class="sxs-lookup"><span data-stu-id="ea8fd-113">For example, a string such as "format this field: \[1\], format this property: \[property\]" is resolved to "format this field: value from field 1, format this property: \[property\]."</span></span>

<span data-ttu-id="ea8fd-114">要[格式化](formatted.md)的參數會以方括弧括 \[ 住 ... \]</span><span class="sxs-lookup"><span data-stu-id="ea8fd-114">Parameters that are to be [formatted](formatted.md) are enclosed in square brackets \[...\].</span></span> <span data-ttu-id="ea8fd-115">可以反復執行方括弧，因為會從內部輸出中解析替代。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-115">The square brackets can be iterated because the substitutions are resolved from the inside out.</span></span>

<span data-ttu-id="ea8fd-116">如果字串的一部分是以大括弧 {} 括住，且未包含方括弧，則會保持不變，包括大括弧。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, it is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="ea8fd-117">請注意，在 [延後執行自訂動作](deferred-execution-custom-actions.md)的情況下， **FormatText** 只支援一組有限的屬性： CustomActionData 和 ProductCode 屬性。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-117">Note in the case of [deferred execution custom actions](deferred-execution-custom-actions.md), **FormatText** only supports a limited set of properties: the CustomActionData and ProductCode properties.</span></span> <span data-ttu-id="ea8fd-118">如需詳細資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-118">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8fd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea8fd-119">Requirements</span></span>



| <span data-ttu-id="ea8fd-120">需求</span><span class="sxs-lookup"><span data-stu-id="ea8fd-120">Requirement</span></span> | <span data-ttu-id="ea8fd-121">值</span><span class="sxs-lookup"><span data-stu-id="ea8fd-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8fd-122">版本</span><span class="sxs-lookup"><span data-stu-id="ea8fd-122">Version</span></span><br/> | <span data-ttu-id="ea8fd-123">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ea8fd-124">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ea8fd-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ea8fd-125">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ea8fd-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ea8fd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8fd-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea8fd-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8fd-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ea8fd-128">IID</span><span class="sxs-lookup"><span data-stu-id="ea8fd-128">IID</span></span><br/>     | <span data-ttu-id="ea8fd-129">IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ea8fd-129">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="ea8fd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea8fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8fd-131">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="ea8fd-131">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[<span data-ttu-id="ea8fd-132">格式 化</span><span class="sxs-lookup"><span data-stu-id="ea8fd-132">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="ea8fd-133">資料行資料類型</span><span class="sxs-lookup"><span data-stu-id="ea8fd-133">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




