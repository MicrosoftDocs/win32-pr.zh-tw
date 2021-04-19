---
title: 'IWMDRMNonSilentLicenseAquisition GetChallenge 方法 (Wmdrmsdk .h) '
description: GetChallenge 方法會抓取應張貼至授權伺服器的授權挑戰。
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- GetChallenge 方法 windows Media 格式
- GetChallenge 方法 windows Media Format，IWMDRMNonSilentLicenseAquisition 介面
- IWMDRMNonSilentLicenseAquisition 介面 windows Media Format，GetChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983014"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a><span data-ttu-id="5c99b-106">IWMDRMNonSilentLicenseAquisition：： GetChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="5c99b-106">IWMDRMNonSilentLicenseAquisition::GetChallenge method</span></span>

<span data-ttu-id="5c99b-107">**GetChallenge** 方法會抓取應張貼至授權伺服器的授權挑戰。</span><span class="sxs-lookup"><span data-stu-id="5c99b-107">The **GetChallenge** method retrieves the license challenge that should be posted to the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c99b-108">語法</span><span class="sxs-lookup"><span data-stu-id="5c99b-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="5c99b-109">參數</span><span class="sxs-lookup"><span data-stu-id="5c99b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c99b-110">*pbstrChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5c99b-110">*pbstrChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c99b-111">接收授權挑戰之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="5c99b-111">Address of a variable that receives the license challenge.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c99b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c99b-112">Return value</span></span>

<span data-ttu-id="5c99b-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="5c99b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5c99b-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="5c99b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5c99b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5c99b-115">Return code</span></span>                                                                          | <span data-ttu-id="5c99b-116">Description</span><span class="sxs-lookup"><span data-stu-id="5c99b-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5c99b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5c99b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5c99b-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="5c99b-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c99b-119">備註</span><span class="sxs-lookup"><span data-stu-id="5c99b-119">Remarks</span></span>

<span data-ttu-id="5c99b-120">無。</span><span class="sxs-lookup"><span data-stu-id="5c99b-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c99b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c99b-121">Requirements</span></span>



| <span data-ttu-id="5c99b-122">需求</span><span class="sxs-lookup"><span data-stu-id="5c99b-122">Requirement</span></span> | <span data-ttu-id="5c99b-123">值</span><span class="sxs-lookup"><span data-stu-id="5c99b-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c99b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5c99b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5c99b-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c99b-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c99b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="5c99b-126">Library</span></span><br/> | <dl> <span data-ttu-id="5c99b-127"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c99b-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c99b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c99b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c99b-129">**IWMDRMNonSilentLicenseAquisition 介面**</span><span class="sxs-lookup"><span data-stu-id="5c99b-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





