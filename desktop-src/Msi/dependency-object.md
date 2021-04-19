---
description: 相依性物件會傳回目前模組相依的模組，而該模組尚未合併到目前的安裝資料庫中。
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: 'Dependency 物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992941"
---
# <a name="dependency-object"></a><span data-ttu-id="16bd5-103">Dependency 物件</span><span class="sxs-lookup"><span data-stu-id="16bd5-103">Dependency object</span></span>

<span data-ttu-id="16bd5-104">相依 **性物件會** 傳回目前模組相依的模組，而該模組尚未合併到目前的安裝資料庫中。</span><span class="sxs-lookup"><span data-stu-id="16bd5-104">The **Dependency** object returns a module that the current module is dependent upon and which has not yet been merged into the current installation database.</span></span>

## <a name="members"></a><span data-ttu-id="16bd5-105">成員</span><span class="sxs-lookup"><span data-stu-id="16bd5-105">Members</span></span>

<span data-ttu-id="16bd5-106">相依 **性物件具有** 下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16bd5-106">The **Dependency** object has these types of members:</span></span>

-   [<span data-ttu-id="16bd5-107">屬性</span><span class="sxs-lookup"><span data-stu-id="16bd5-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16bd5-108">屬性</span><span class="sxs-lookup"><span data-stu-id="16bd5-108">Properties</span></span>

<span data-ttu-id="16bd5-109">相依 **性物件具有** 這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16bd5-109">The **Dependency** object has these properties.</span></span>



| <span data-ttu-id="16bd5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="16bd5-110">Property</span></span>                                           | <span data-ttu-id="16bd5-111">描述</span><span class="sxs-lookup"><span data-stu-id="16bd5-111">Description</span></span>                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="16bd5-112">**語言**</span><span class="sxs-lookup"><span data-stu-id="16bd5-112">**Language**</span></span>](dependency-language.md)<br/> | <span data-ttu-id="16bd5-113">傳回模組的語言。</span><span class="sxs-lookup"><span data-stu-id="16bd5-113">Return the language of the module.</span></span><br/>           |
| [<span data-ttu-id="16bd5-114">**模組**</span><span class="sxs-lookup"><span data-stu-id="16bd5-114">**Module**</span></span>](dependency-module.md)<br/>     | <span data-ttu-id="16bd5-115">傳回所需模組的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="16bd5-115">Return the module ID of the required module.</span></span><br/> |
| [<span data-ttu-id="16bd5-116">**版本**</span><span class="sxs-lookup"><span data-stu-id="16bd5-116">**Version**</span></span>](dependency-version.md)<br/>   | <span data-ttu-id="16bd5-117">傳回所需模組的版本。</span><span class="sxs-lookup"><span data-stu-id="16bd5-117">Return the version of the required module.</span></span><br/>   |



 

## <a name="c"></a><span data-ttu-id="16bd5-118">C++</span><span class="sxs-lookup"><span data-stu-id="16bd5-118">C++</span></span>

<span data-ttu-id="16bd5-119">介面 **IMsmDependency： IDispatch**</span><span class="sxs-lookup"><span data-stu-id="16bd5-119">interface **IMsmDependency : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="16bd5-120">介面識別碼</span><span class="sxs-lookup"><span data-stu-id="16bd5-120">Interface ID</span></span>



| <span data-ttu-id="16bd5-121">常數</span><span class="sxs-lookup"><span data-stu-id="16bd5-121">Constant</span></span>                | <span data-ttu-id="16bd5-122">值</span><span class="sxs-lookup"><span data-stu-id="16bd5-122">Value</span></span>                                  |
|-------------------------|----------------------------------------|
| <span data-ttu-id="16bd5-123">**IID \_ IMsmDependency**</span><span class="sxs-lookup"><span data-stu-id="16bd5-123">**IID\_IMsmDependency**</span></span> | <span data-ttu-id="16bd5-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="16bd5-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="16bd5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="16bd5-125">Requirements</span></span>



| <span data-ttu-id="16bd5-126">需求</span><span class="sxs-lookup"><span data-stu-id="16bd5-126">Requirement</span></span> | <span data-ttu-id="16bd5-127">值</span><span class="sxs-lookup"><span data-stu-id="16bd5-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16bd5-128">版本</span><span class="sxs-lookup"><span data-stu-id="16bd5-128">Version</span></span><br/> | <span data-ttu-id="16bd5-129">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="16bd5-129">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="16bd5-130">標頭</span><span class="sxs-lookup"><span data-stu-id="16bd5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="16bd5-131"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="16bd5-131"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="16bd5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="16bd5-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="16bd5-133"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16bd5-133"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




