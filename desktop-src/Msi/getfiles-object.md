---
description: GetFiles 物件會抓取模組特定語言所需的檔案。 需要透過 Merge 物件執行某些動作，此介面的所有部分才會傳回有效的結果。
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: 'GetFiles 物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984862"
---
# <a name="getfiles-object"></a><span data-ttu-id="34668-104">GetFiles 物件</span><span class="sxs-lookup"><span data-stu-id="34668-104">GetFiles object</span></span>

<span data-ttu-id="34668-105">**GetFiles** 物件會抓取模組特定語言所需的檔案。</span><span class="sxs-lookup"><span data-stu-id="34668-105">The **GetFiles** object retrieves the files needed in a particular language of the module.</span></span> <span data-ttu-id="34668-106">需要透過 [Merge 物件](merge-object.md) 執行某些動作，此介面的所有部分才會傳回有效的結果。</span><span class="sxs-lookup"><span data-stu-id="34668-106">Requires certain actions be performed through the [Merge object](merge-object.md) before all parts of this interface returns valid results.</span></span>

## <a name="members"></a><span data-ttu-id="34668-107">成員</span><span class="sxs-lookup"><span data-stu-id="34668-107">Members</span></span>

<span data-ttu-id="34668-108">**GetFiles** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="34668-108">The **GetFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="34668-109">屬性</span><span class="sxs-lookup"><span data-stu-id="34668-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34668-110">屬性</span><span class="sxs-lookup"><span data-stu-id="34668-110">Properties</span></span>

<span data-ttu-id="34668-111">**GetFiles** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="34668-111">The **GetFiles** object has these properties.</span></span>



| <span data-ttu-id="34668-112">屬性</span><span class="sxs-lookup"><span data-stu-id="34668-112">Property</span></span>                                               | <span data-ttu-id="34668-113">描述</span><span class="sxs-lookup"><span data-stu-id="34668-113">Description</span></span>                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34668-114">**ModuleFiles**</span><span class="sxs-lookup"><span data-stu-id="34668-114">**ModuleFiles**</span></span>](getfiles-modulefiles.md)<br/> | <span data-ttu-id="34668-115">[**ModuleFiles**](getfiles-modulefiles.md) 屬性會傳回目前開啟之模組的檔案 [資料表](file-table.md) 的所有主鍵。</span><span class="sxs-lookup"><span data-stu-id="34668-115">[**ModuleFiles**](getfiles-modulefiles.md) property returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span><br/> |



 

## <a name="c"></a><span data-ttu-id="34668-116">C++</span><span class="sxs-lookup"><span data-stu-id="34668-116">C++</span></span>

<span data-ttu-id="34668-117">介面 **IMsmGetFiles： IDispatch**</span><span class="sxs-lookup"><span data-stu-id="34668-117">interface **IMsmGetFiles : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="34668-118">介面識別碼</span><span class="sxs-lookup"><span data-stu-id="34668-118">Interface ID</span></span>



| <span data-ttu-id="34668-119">常數</span><span class="sxs-lookup"><span data-stu-id="34668-119">Constant</span></span>              | <span data-ttu-id="34668-120">值</span><span class="sxs-lookup"><span data-stu-id="34668-120">Value</span></span>                                  |
|-----------------------|----------------------------------------|
| <span data-ttu-id="34668-121">**IID \_ IMsmGetFiles**</span><span class="sxs-lookup"><span data-stu-id="34668-121">**IID\_IMsmGetFiles**</span></span> | <span data-ttu-id="34668-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="34668-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="34668-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="34668-123">Requirements</span></span>



| <span data-ttu-id="34668-124">需求</span><span class="sxs-lookup"><span data-stu-id="34668-124">Requirement</span></span> | <span data-ttu-id="34668-125">值</span><span class="sxs-lookup"><span data-stu-id="34668-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34668-126">版本</span><span class="sxs-lookup"><span data-stu-id="34668-126">Version</span></span><br/> | <span data-ttu-id="34668-127">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="34668-127">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="34668-128">標頭</span><span class="sxs-lookup"><span data-stu-id="34668-128">Header</span></span><br/>  | <dl> <span data-ttu-id="34668-129"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="34668-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="34668-130">DLL</span><span class="sxs-lookup"><span data-stu-id="34668-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="34668-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34668-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




