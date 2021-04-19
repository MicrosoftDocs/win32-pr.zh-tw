---
title: 'D2D1CreateFactory Factory (D2D1_FACTORY_TYPE、D2D1_FACTORY_OPTIONS、Factory ) 函數 (D2d1 .h) '
description: '建立可用於建立 Direct2D 資源的 factory 物件。 |D2D1CreateFactory Factory (D2D1_FACTORY_TYPE、D2D1_FACTORY_OPTIONS、Factory ) 函數 (D2d1 .h) '
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE、D2D1_FACTORY_OPTIONS、Factory ) 函數 Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982852"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a><span data-ttu-id="e565b-105">D2D1CreateFactory <Factory> (D2D1 \_ factory \_ 類型、D2D1 \_ Factory \_ 選項&、factory \* \*) 函式</span><span class="sxs-lookup"><span data-stu-id="e565b-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,D2D1\_FACTORY\_OPTIONS&,Factory\*\*) Function</span></span>

<span data-ttu-id="e565b-106">建立可用於建立 Direct2D 資源的 factory 物件。</span><span class="sxs-lookup"><span data-stu-id="e565b-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="e565b-107">範本參數</span><span class="sxs-lookup"><span data-stu-id="e565b-107">Template Parameters</span></span>



| <span data-ttu-id="e565b-108">參數</span><span class="sxs-lookup"><span data-stu-id="e565b-108">Parameter</span></span> | <span data-ttu-id="e565b-109">Description</span><span class="sxs-lookup"><span data-stu-id="e565b-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="e565b-110">*廠*</span><span class="sxs-lookup"><span data-stu-id="e565b-110">*Factory*</span></span> | <span data-ttu-id="e565b-111">要建立之 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 的類型。</span><span class="sxs-lookup"><span data-stu-id="e565b-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="e565b-112">參數</span><span class="sxs-lookup"><span data-stu-id="e565b-112">Parameters</span></span>



| <span data-ttu-id="e565b-113">參數</span><span class="sxs-lookup"><span data-stu-id="e565b-113">Parameter</span></span>        | <span data-ttu-id="e565b-114">Description</span><span class="sxs-lookup"><span data-stu-id="e565b-114">Description</span></span>                                                                     |
|------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e565b-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="e565b-115">*factoryType*</span></span>    | <span data-ttu-id="e565b-116">Factory 的執行緒模型和它所建立的資源。</span><span class="sxs-lookup"><span data-stu-id="e565b-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="e565b-117">*factoryOptions*</span><span class="sxs-lookup"><span data-stu-id="e565b-117">*factoryOptions*</span></span> | <span data-ttu-id="e565b-118">提供給調試層的詳細資料層級。</span><span class="sxs-lookup"><span data-stu-id="e565b-118">The level of detail provided to the debugging layer.</span></span>                            |
| <span data-ttu-id="e565b-119">*工廠*</span><span class="sxs-lookup"><span data-stu-id="e565b-119">*factory*</span></span>        | <span data-ttu-id="e565b-120">當此方法傳回時，會包含指向新 factory 之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="e565b-120">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="e565b-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="e565b-121">Return Value</span></span>

<span data-ttu-id="e565b-122">如果方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e565b-122">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e565b-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e565b-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e565b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e565b-124">Requirements</span></span>



| <span data-ttu-id="e565b-125">需求</span><span class="sxs-lookup"><span data-stu-id="e565b-125">Requirement</span></span> | <span data-ttu-id="e565b-126">值</span><span class="sxs-lookup"><span data-stu-id="e565b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e565b-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e565b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e565b-128">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="e565b-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="e565b-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e565b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e565b-130">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e565b-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e565b-131">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="e565b-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="e565b-132">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e565b-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="e565b-133">標頭</span><span class="sxs-lookup"><span data-stu-id="e565b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e565b-134"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="e565b-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="e565b-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="e565b-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e565b-136"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e565b-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="e565b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e565b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e565b-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e565b-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

