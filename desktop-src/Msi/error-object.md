---
description: Error 物件會傳回單一合併錯誤的資訊。
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: '錯誤物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000727"
---
# <a name="error-object"></a><span data-ttu-id="0fad4-103">Error 物件</span><span class="sxs-lookup"><span data-stu-id="0fad4-103">Error object</span></span>

<span data-ttu-id="0fad4-104">**Error** 物件會傳回單一合併錯誤的資訊。</span><span class="sxs-lookup"><span data-stu-id="0fad4-104">The **Error** object returns the information of a single merge error.</span></span>

## <a name="members"></a><span data-ttu-id="0fad4-105">成員</span><span class="sxs-lookup"><span data-stu-id="0fad4-105">Members</span></span>

<span data-ttu-id="0fad4-106">**Error** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0fad4-106">The **Error** object has these types of members:</span></span>

-   [<span data-ttu-id="0fad4-107">屬性</span><span class="sxs-lookup"><span data-stu-id="0fad4-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fad4-108">屬性</span><span class="sxs-lookup"><span data-stu-id="0fad4-108">Properties</span></span>

<span data-ttu-id="0fad4-109">**Error** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0fad4-109">The **Error** object has these properties.</span></span>



| <span data-ttu-id="0fad4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0fad4-110">Property</span></span>                                                | <span data-ttu-id="0fad4-111">描述</span><span class="sxs-lookup"><span data-stu-id="0fad4-111">Description</span></span>                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fad4-112">**DatabaseKeys**</span><span class="sxs-lookup"><span data-stu-id="0fad4-112">**DatabaseKeys**</span></span>](error-databasekeys.md)<br/>   | <span data-ttu-id="0fad4-113">傳回資料庫資料表中造成錯誤之資料列的主鍵。</span><span class="sxs-lookup"><span data-stu-id="0fad4-113">Returns the primary keys of the row in the database table that caused the error.</span></span><br/> |
| [<span data-ttu-id="0fad4-114">**DatabaseTable**</span><span class="sxs-lookup"><span data-stu-id="0fad4-114">**DatabaseTable**</span></span>](error-databasetable.md)<br/> | <span data-ttu-id="0fad4-115">傳回資料庫中造成錯誤之資料表的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="0fad4-115">Returns the table name of the table in the database causing the error.</span></span><br/>           |
| [<span data-ttu-id="0fad4-116">**語言**</span><span class="sxs-lookup"><span data-stu-id="0fad4-116">**Language**</span></span>](error-language.md)<br/>           | <span data-ttu-id="0fad4-117">傳回錯誤的語言。</span><span class="sxs-lookup"><span data-stu-id="0fad4-117">Return the language of the error.</span></span><br/>                                                |
| [<span data-ttu-id="0fad4-118">**ModuleKeys**</span><span class="sxs-lookup"><span data-stu-id="0fad4-118">**ModuleKeys**</span></span>](error-modulekeys.md)<br/>       | <span data-ttu-id="0fad4-119">傳回模組資料表中造成錯誤之資料列的主鍵。</span><span class="sxs-lookup"><span data-stu-id="0fad4-119">Returns the primary keys of the row in the module table that caused the error.</span></span><br/>   |
| [<span data-ttu-id="0fad4-120">**ModuleTable**</span><span class="sxs-lookup"><span data-stu-id="0fad4-120">**ModuleTable**</span></span>](error-moduletable.md)<br/>     | <span data-ttu-id="0fad4-121">傳回模組中造成錯誤之資料表的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="0fad4-121">Returns the table name of the table in the module causing the error.</span></span><br/>             |
| [<span data-ttu-id="0fad4-122">**路徑**</span><span class="sxs-lookup"><span data-stu-id="0fad4-122">**Path**</span></span>](error-path.md)<br/>                   | <span data-ttu-id="0fad4-123">傳回造成錯誤之檔案或目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="0fad4-123">Return the path to the file or directory causing the error.</span></span> <span data-ttu-id="0fad4-124">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="0fad4-124">Currently unused.</span></span><br/>    |
| [<span data-ttu-id="0fad4-125">**類型**</span><span class="sxs-lookup"><span data-stu-id="0fad4-125">**Type**</span></span>](error-type.md)<br/>                   | <span data-ttu-id="0fad4-126">傳回錯誤的類型。</span><span class="sxs-lookup"><span data-stu-id="0fad4-126">Return the type of error.</span></span><br/>                                                        |



 

## <a name="c"></a><span data-ttu-id="0fad4-127">C++</span><span class="sxs-lookup"><span data-stu-id="0fad4-127">C++</span></span>

<span data-ttu-id="0fad4-128">介面 **IMsmError： IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0fad4-128">interface **IMsmError : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="0fad4-129">介面識別碼</span><span class="sxs-lookup"><span data-stu-id="0fad4-129">Interface ID</span></span>



| <span data-ttu-id="0fad4-130">常數</span><span class="sxs-lookup"><span data-stu-id="0fad4-130">Constant</span></span>           | <span data-ttu-id="0fad4-131">值</span><span class="sxs-lookup"><span data-stu-id="0fad4-131">Value</span></span>                                  |
|--------------------|----------------------------------------|
| <span data-ttu-id="0fad4-132">**IID \_ IMsmError**</span><span class="sxs-lookup"><span data-stu-id="0fad4-132">**IID\_IMsmError**</span></span> | <span data-ttu-id="0fad4-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="0fad4-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0fad4-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fad4-134">Requirements</span></span>



| <span data-ttu-id="0fad4-135">需求</span><span class="sxs-lookup"><span data-stu-id="0fad4-135">Requirement</span></span> | <span data-ttu-id="0fad4-136">值</span><span class="sxs-lookup"><span data-stu-id="0fad4-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fad4-137">版本</span><span class="sxs-lookup"><span data-stu-id="0fad4-137">Version</span></span><br/> | <span data-ttu-id="0fad4-138">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0fad4-138">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="0fad4-139">標頭</span><span class="sxs-lookup"><span data-stu-id="0fad4-139">Header</span></span><br/>  | <dl> <span data-ttu-id="0fad4-140"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fad4-140"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="0fad4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0fad4-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="0fad4-142"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fad4-142"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




