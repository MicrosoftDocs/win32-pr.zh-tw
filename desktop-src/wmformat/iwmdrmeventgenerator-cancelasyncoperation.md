---
title: 'IWMDRMEventGenerator CancelAsyncOperation 方法 (Wmdrmsdk .h) '
description: CancelAsyncOperation 方法會取消非同步作業。
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- CancelAsyncOperation 方法 windows Media 格式
- CancelAsyncOperation 方法 windows Media Format，IWMDRMEventGenerator 介面
- IWMDRMEventGenerator 介面 windows Media Format，CancelAsyncOperation 方法
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982629"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a><span data-ttu-id="268c8-106">IWMDRMEventGenerator：： CancelAsyncOperation 方法</span><span class="sxs-lookup"><span data-stu-id="268c8-106">IWMDRMEventGenerator::CancelAsyncOperation method</span></span>

<span data-ttu-id="268c8-107">**CancelAsyncOperation** 方法會取消非同步作業。</span><span class="sxs-lookup"><span data-stu-id="268c8-107">The **CancelAsyncOperation** method cancels an asynchronous operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="268c8-108">語法</span><span class="sxs-lookup"><span data-stu-id="268c8-108">Syntax</span></span>


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="268c8-109">參數</span><span class="sxs-lookup"><span data-stu-id="268c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="268c8-110">*punkCancelationCookie* \[在\]</span><span class="sxs-lookup"><span data-stu-id="268c8-110">*punkCancelationCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268c8-111">識別要取消之非同步作業的取消 cookie 指標。</span><span class="sxs-lookup"><span data-stu-id="268c8-111">Pointer to the cancellation cookie that identifies the asynchronous operation to be canceled.</span></span> <span data-ttu-id="268c8-112">此 cookie 是由用來啟動作業的方法所提供。</span><span class="sxs-lookup"><span data-stu-id="268c8-112">This cookie is provided by the method used to start the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="268c8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="268c8-113">Return value</span></span>

<span data-ttu-id="268c8-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="268c8-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="268c8-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="268c8-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="268c8-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="268c8-116">Return code</span></span>                                                                          | <span data-ttu-id="268c8-117">Description</span><span class="sxs-lookup"><span data-stu-id="268c8-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="268c8-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="268c8-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="268c8-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="268c8-119">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="268c8-120">備註</span><span class="sxs-lookup"><span data-stu-id="268c8-120">Remarks</span></span>

<span data-ttu-id="268c8-121">無。</span><span class="sxs-lookup"><span data-stu-id="268c8-121">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="268c8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="268c8-122">Requirements</span></span>



| <span data-ttu-id="268c8-123">需求</span><span class="sxs-lookup"><span data-stu-id="268c8-123">Requirement</span></span> | <span data-ttu-id="268c8-124">值</span><span class="sxs-lookup"><span data-stu-id="268c8-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="268c8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="268c8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="268c8-126"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="268c8-126"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="268c8-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="268c8-127">Library</span></span><br/> | <dl> <span data-ttu-id="268c8-128"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="268c8-128"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="268c8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="268c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268c8-130">**IWMDRMEventGenerator 介面**</span><span class="sxs-lookup"><span data-stu-id="268c8-130">**IWMDRMEventGenerator Interface**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





