---
description: SourceListAddSource 方法會新增網路或 URL 來源。 接受 SourcePath、Type 和 Index 作為參數。 這個方法會呼叫 MsiSourceListAddSourceEx。
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: SourceListAddSource 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e0cfda9b8eab0e7dd00afd15eb701a6e7decf2ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990162"
---
# <a name="productsourcelistaddsource-method"></a><span data-ttu-id="32656-105">SourceListAddSource 方法</span><span class="sxs-lookup"><span data-stu-id="32656-105">Product.SourceListAddSource method</span></span>

<span data-ttu-id="32656-106">**SourceListAddSource** 方法會新增網路或 URL 來源。</span><span class="sxs-lookup"><span data-stu-id="32656-106">The **SourceListAddSource** method adds a network or URL source.</span></span> <span data-ttu-id="32656-107">接受 *SourcePath*、*Type* 和 *Index* 作為參數。</span><span class="sxs-lookup"><span data-stu-id="32656-107">Accepts *SourcePath*,*Type*, and *Index* as parameters.</span></span> <span data-ttu-id="32656-108">這個方法會呼叫 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)。</span><span class="sxs-lookup"><span data-stu-id="32656-108">This method calls [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="32656-109">語法</span><span class="sxs-lookup"><span data-stu-id="32656-109">Syntax</span></span>


```JScript
Product.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a><span data-ttu-id="32656-110">參數</span><span class="sxs-lookup"><span data-stu-id="32656-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32656-111">*型別*</span><span class="sxs-lookup"><span data-stu-id="32656-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="32656-112">要新增的來源類型： MSISOURCETYPE \_ NETWORK 或 MSISOURCETYPE \_ URL。</span><span class="sxs-lookup"><span data-stu-id="32656-112">Type of source to be added: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="32656-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="32656-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="32656-114">要加入之來源的路徑。</span><span class="sxs-lookup"><span data-stu-id="32656-114">Path to the source to be added.</span></span>

</dd> <dt>

<span data-ttu-id="32656-115">*Index*</span><span class="sxs-lookup"><span data-stu-id="32656-115">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="32656-116">如果使用新的來源呼叫 **SourceListAddSource** ，而且 *索引* 設定為0，則安裝程式會將來源新增至來源清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="32656-116">If **SourceListAddSource** is called with a new source and *Index* is set to 0, the installer adds the source to the end of the source list.</span></span>

<span data-ttu-id="32656-117">如果使用來源清單中已存在的來源來呼叫此函數，而且 *索引* 設定為0，則安裝程式會保留來源的現有索引。</span><span class="sxs-lookup"><span data-stu-id="32656-117">If this function is called with a source already existing in the source list and *Index* is set to 0, the installer retains the source's existing index.</span></span>

<span data-ttu-id="32656-118">如果函式是使用來源清單中的現有來源來呼叫，且 *索引* 設定為非零值，則會從清單中的目前位置移除來源，並將其插入 *索引* 所指定的位置，然後再插入至該位置已存在的任何來源。</span><span class="sxs-lookup"><span data-stu-id="32656-118">If the function is called with an existing source in the source list and *Index* is set to a non-zero value, the source is removed from its current location in the list and inserted at the position specified by *Index*, before any source that already exists at that position.</span></span>

<span data-ttu-id="32656-119">如果函式是以新的來源呼叫，且 *索引* 設定為非零值，則會在該位置已存在的任何來源之前，將來源插入 *索引* 所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="32656-119">If the function is called with a new source and *Index* is set to a non-zero value, the source is inserted at the position specified by *Index*, before any source that already exists at that position.</span></span> <span data-ttu-id="32656-120">在 *索引* 所指定的索引之後，清單中所有來源的索引值都會更新，以確保唯一的索引值，而且保證會維持不變的預先存在順序。</span><span class="sxs-lookup"><span data-stu-id="32656-120">The index value for all sources in the list after the index specified by *Index* are updated to ensure unique index values and the pre-existing order is guaranteed to remain unchanged.</span></span>

<span data-ttu-id="32656-121">如果 *索引* 大於清單中的來源數目，則會將來源放在清單結尾，且索引值大於任何現有來源。</span><span class="sxs-lookup"><span data-stu-id="32656-121">If *Index* is greater than the number of sources in the list, the source is placed at the end of the list with an index value one larger than any existing source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32656-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="32656-122">Return value</span></span>

<span data-ttu-id="32656-123">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="32656-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="32656-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="32656-124">Requirements</span></span>



| <span data-ttu-id="32656-125">需求</span><span class="sxs-lookup"><span data-stu-id="32656-125">Requirement</span></span> | <span data-ttu-id="32656-126">值</span><span class="sxs-lookup"><span data-stu-id="32656-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32656-127">版本</span><span class="sxs-lookup"><span data-stu-id="32656-127">Version</span></span><br/> | <span data-ttu-id="32656-128">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="32656-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="32656-129">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="32656-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="32656-130">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="32656-130">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="32656-131">DLL</span><span class="sxs-lookup"><span data-stu-id="32656-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="32656-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32656-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="32656-133">IID</span><span class="sxs-lookup"><span data-stu-id="32656-133">IID</span></span><br/>     | <span data-ttu-id="32656-134">IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="32656-134">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="32656-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32656-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32656-136">**產品**</span><span class="sxs-lookup"><span data-stu-id="32656-136">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="32656-137">**MsiSourceListAddSourceEx**</span><span class="sxs-lookup"><span data-stu-id="32656-137">**MsiSourceListAddSourceEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[<span data-ttu-id="32656-138">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="32656-138">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




