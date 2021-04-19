---
description: SummaryInfo 物件是用來讀取、建立和更新儲存物件之摘要資訊資料流程中的檔案屬性。
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: SummaryInfo 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985773"
---
# <a name="summaryinfo-object"></a><span data-ttu-id="88af1-103">SummaryInfo 物件</span><span class="sxs-lookup"><span data-stu-id="88af1-103">SummaryInfo object</span></span>

<span data-ttu-id="88af1-104">**SummaryInfo** 物件是用來讀取、建立和更新儲存物件之 [摘要資訊資料流程](summary-information-stream.md)中的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="88af1-104">The **SummaryInfo** object is used to read, create, and update document properties from the [summary information stream](summary-information-stream.md) of a storage object.</span></span>

## <a name="members"></a><span data-ttu-id="88af1-105">成員</span><span class="sxs-lookup"><span data-stu-id="88af1-105">Members</span></span>

<span data-ttu-id="88af1-106">**SummaryInfo** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="88af1-106">The **SummaryInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="88af1-107">方法</span><span class="sxs-lookup"><span data-stu-id="88af1-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="88af1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="88af1-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88af1-109">方法</span><span class="sxs-lookup"><span data-stu-id="88af1-109">Methods</span></span>

<span data-ttu-id="88af1-110">**SummaryInfo** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="88af1-110">The **SummaryInfo** object has these methods.</span></span>



| <span data-ttu-id="88af1-111">方法</span><span class="sxs-lookup"><span data-stu-id="88af1-111">Method</span></span>                                 | <span data-ttu-id="88af1-112">描述</span><span class="sxs-lookup"><span data-stu-id="88af1-112">Description</span></span>                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88af1-113">**堅持**</span><span class="sxs-lookup"><span data-stu-id="88af1-113">**Persist**</span></span>](summaryinfo-persist.md) | <span data-ttu-id="88af1-114">將先前儲存的屬性格式化並寫入標準 [摘要資訊資料流程](summary-information-stream.md)中。</span><span class="sxs-lookup"><span data-stu-id="88af1-114">Formats and writes the previously stored properties into the standard [summary information stream](summary-information-stream.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="88af1-115">屬性</span><span class="sxs-lookup"><span data-stu-id="88af1-115">Properties</span></span>

<span data-ttu-id="88af1-116">**SummaryInfo** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="88af1-116">The **SummaryInfo** object has these properties.</span></span>



| <span data-ttu-id="88af1-117">屬性</span><span class="sxs-lookup"><span data-stu-id="88af1-117">Property</span></span>                                                                             | <span data-ttu-id="88af1-118">描述</span><span class="sxs-lookup"><span data-stu-id="88af1-118">Description</span></span>                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88af1-119">**屬性屬性 (SummaryInfo 物件)**</span><span class="sxs-lookup"><span data-stu-id="88af1-119">**Property Property (SummaryInfo Object)**</span></span>](summaryinfo-summaryinfo.md)<br/> | <span data-ttu-id="88af1-120">取得或設定摘要資訊資料流程中指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="88af1-120">Gets or sets the value for the specified property in the summary information stream.</span></span><br/> |
| [<span data-ttu-id="88af1-121">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="88af1-121">**PropertyCount**</span></span>](summaryinfo-propertycount.md)<br/>                        | <span data-ttu-id="88af1-122">表示摘要資訊物件中目前的屬性值數目。</span><span class="sxs-lookup"><span data-stu-id="88af1-122">Indicates the current number of property values in the summary information object.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="88af1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="88af1-123">Requirements</span></span>



| <span data-ttu-id="88af1-124">需求</span><span class="sxs-lookup"><span data-stu-id="88af1-124">Requirement</span></span> | <span data-ttu-id="88af1-125">值</span><span class="sxs-lookup"><span data-stu-id="88af1-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88af1-126">版本</span><span class="sxs-lookup"><span data-stu-id="88af1-126">Version</span></span><br/> | <span data-ttu-id="88af1-127">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="88af1-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="88af1-128">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="88af1-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="88af1-129">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="88af1-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="88af1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="88af1-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="88af1-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88af1-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="88af1-132">IID</span><span class="sxs-lookup"><span data-stu-id="88af1-132">IID</span></span><br/>     | <span data-ttu-id="88af1-133">IID \_ ISummaryInfo 定義為 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="88af1-133">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="88af1-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88af1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88af1-135">**SummaryInformation 屬性 (資料庫物件)**</span><span class="sxs-lookup"><span data-stu-id="88af1-135">**SummaryInformation Property (Database Object)**</span></span>](database-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="88af1-136">**SummaryInformation 屬性 (安裝程式物件)**</span><span class="sxs-lookup"><span data-stu-id="88af1-136">**SummaryInformation Property (Installer Object)**</span></span>](installer-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="88af1-137">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="88af1-137">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




