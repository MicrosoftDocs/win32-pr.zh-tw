---
description: ConfigureModule 物件是由用戶端所執行的介面。
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: 'ConfigureModule 物件 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996063"
---
# <a name="configuremodule-object"></a><span data-ttu-id="b1028-103">ConfigureModule 物件</span><span class="sxs-lookup"><span data-stu-id="b1028-103">ConfigureModule object</span></span>

<span data-ttu-id="b1028-104">**ConfigureModule 物件** 是由用戶端所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="b1028-104">The **ConfigureModule object** is an interface implemented by the client.</span></span> <span data-ttu-id="b1028-105">Mergemod.dll在 **IMsmConfigureModule** 介面上呼叫方法，以要求用戶端工具提供設定資訊。</span><span class="sxs-lookup"><span data-stu-id="b1028-105">Mergemod.dllcalls methods on the **IMsmConfigureModule** interface to request that the client tool provide configuration information.</span></span> <span data-ttu-id="b1028-106">此模組會根據用戶端對此介面呼叫的回應進行設定。</span><span class="sxs-lookup"><span data-stu-id="b1028-106">The module is configured based on the client's responses to calls on this interface.</span></span>

## <a name="members"></a><span data-ttu-id="b1028-107">成員</span><span class="sxs-lookup"><span data-stu-id="b1028-107">Members</span></span>

<span data-ttu-id="b1028-108">**ConfigureModule** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b1028-108">The **ConfigureModule** object has these types of members:</span></span>

-   [<span data-ttu-id="b1028-109">方法</span><span class="sxs-lookup"><span data-stu-id="b1028-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b1028-110">方法</span><span class="sxs-lookup"><span data-stu-id="b1028-110">Methods</span></span>

<span data-ttu-id="b1028-111">**ConfigureModule** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b1028-111">The **ConfigureModule** object has these methods.</span></span>



| <span data-ttu-id="b1028-112">方法</span><span class="sxs-lookup"><span data-stu-id="b1028-112">Method</span></span>                                                           | <span data-ttu-id="b1028-113">描述</span><span class="sxs-lookup"><span data-stu-id="b1028-113">Description</span></span>                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b1028-114">**ProvideIntegerData**</span><span class="sxs-lookup"><span data-stu-id="b1028-114">**ProvideIntegerData**</span></span>](configuremodule-provideintegerdata.md) | <span data-ttu-id="b1028-115">由 Mergemod.dll 呼叫以取得用來設定模組的整數。</span><span class="sxs-lookup"><span data-stu-id="b1028-115">Called by Mergemod.dll to obtain integers used to configure the module.</span></span><br/> |
| [<span data-ttu-id="b1028-116">**ProvideTextData**</span><span class="sxs-lookup"><span data-stu-id="b1028-116">**ProvideTextData**</span></span>](configuremodule-providetextdata.md)       | <span data-ttu-id="b1028-117">由 Mergemod.dll 呼叫以取得用來設定模組的文字。</span><span class="sxs-lookup"><span data-stu-id="b1028-117">Called by Mergemod.dll to obtain text used to configure the module.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="b1028-118">備註</span><span class="sxs-lookup"><span data-stu-id="b1028-118">Remarks</span></span>

### <a name="c"></a><span data-ttu-id="b1028-119">C++</span><span class="sxs-lookup"><span data-stu-id="b1028-119">C++</span></span>

<span data-ttu-id="b1028-120">介面 **IMsmConfigureModule： IDispatch**</span><span class="sxs-lookup"><span data-stu-id="b1028-120">interface **IMsmConfigureModule : IDispatch**</span></span>

### <a name="interface-id"></a><span data-ttu-id="b1028-121">介面識別碼</span><span class="sxs-lookup"><span data-stu-id="b1028-121">Interface ID</span></span>



| <span data-ttu-id="b1028-122">常數</span><span class="sxs-lookup"><span data-stu-id="b1028-122">Constant</span></span>                     | <span data-ttu-id="b1028-123">值</span><span class="sxs-lookup"><span data-stu-id="b1028-123">Value</span></span>                                  |
|------------------------------|----------------------------------------|
| <span data-ttu-id="b1028-124">**IID \_ IMsmConfigureModule**</span><span class="sxs-lookup"><span data-stu-id="b1028-124">**IID\_IMsmConfigureModule**</span></span> | <span data-ttu-id="b1028-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span><span class="sxs-lookup"><span data-stu-id="b1028-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b1028-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1028-126">Requirements</span></span>



| <span data-ttu-id="b1028-127">需求</span><span class="sxs-lookup"><span data-stu-id="b1028-127">Requirement</span></span> | <span data-ttu-id="b1028-128">值</span><span class="sxs-lookup"><span data-stu-id="b1028-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1028-129">版本</span><span class="sxs-lookup"><span data-stu-id="b1028-129">Version</span></span><br/> | <span data-ttu-id="b1028-130">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b1028-130">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b1028-131">標頭</span><span class="sxs-lookup"><span data-stu-id="b1028-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b1028-132"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1028-132"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1028-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b1028-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1028-134"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1028-134"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




