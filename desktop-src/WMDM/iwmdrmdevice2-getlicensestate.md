---
title: IWMDRMDevice2 GetLicenseState 方法
description: GetLicenseState 方法會取得授權狀態。
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- GetLicenseState 方法 windows Media 裝置管理員
- GetLicenseState 方法 windows Media 裝置管理員，IWMDRMDevice2 介面
- IWMDRMDevice2 interface windows Media 裝置管理員，GetLicenseState 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991258"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a><span data-ttu-id="32553-106">IWMDRMDevice2：： GetLicenseState 方法</span><span class="sxs-lookup"><span data-stu-id="32553-106">IWMDRMDevice2::GetLicenseState method</span></span>

<span data-ttu-id="32553-107">**GetLicenseState** 方法會取得授權狀態。</span><span class="sxs-lookup"><span data-stu-id="32553-107">The **GetLicenseState** method gets the license state.</span></span>

## <a name="syntax"></a><span data-ttu-id="32553-108">語法</span><span class="sxs-lookup"><span data-stu-id="32553-108">Syntax</span></span>


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="32553-109">參數</span><span class="sxs-lookup"><span data-stu-id="32553-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32553-110">*pbStateQueryData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32553-110">*pbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32553-111">授權狀態的查詢資料指標。</span><span class="sxs-lookup"><span data-stu-id="32553-111">Pointer to the queried data of the license state.</span></span>

</dd> <dt>

<span data-ttu-id="32553-112">*cbStateQueryData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32553-112">*cbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32553-113">查詢的資料計數。</span><span class="sxs-lookup"><span data-stu-id="32553-113">Count of the queried data.</span></span>

</dd> <dt>

<span data-ttu-id="32553-114">*pdwCategory* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="32553-114">*pdwCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32553-115">類別的指標。</span><span class="sxs-lookup"><span data-stu-id="32553-115">Pointer to the category.</span></span>

</dd> <dt>

<span data-ttu-id="32553-116">*pcRemainingCounts* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="32553-116">*pcRemainingCounts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32553-117">剩餘計數的指標。</span><span class="sxs-lookup"><span data-stu-id="32553-117">Pointer to the remaining counts.</span></span>

</dd> <dt>

<span data-ttu-id="32553-118">*pcRemainingHours* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="32553-118">*pcRemainingHours* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32553-119">剩餘時數的指標。</span><span class="sxs-lookup"><span data-stu-id="32553-119">Pointer to the remaining hours.</span></span>

</dd> <dt>

<span data-ttu-id="32553-120">*pdwReserved* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="32553-120">*pdwReserved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32553-121">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="32553-121">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32553-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="32553-122">Return value</span></span>

<span data-ttu-id="32553-123">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="32553-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="32553-124">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="32553-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="32553-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="32553-125">Return code</span></span>                                                                          | <span data-ttu-id="32553-126">Description</span><span class="sxs-lookup"><span data-stu-id="32553-126">Description</span></span>                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="32553-127"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="32553-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="32553-128">方法成功。</span><span class="sxs-lookup"><span data-stu-id="32553-128">The method succeeds.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="32553-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="32553-129">Requirements</span></span>



| <span data-ttu-id="32553-130">需求</span><span class="sxs-lookup"><span data-stu-id="32553-130">Requirement</span></span> | <span data-ttu-id="32553-131">值</span><span class="sxs-lookup"><span data-stu-id="32553-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32553-132">標頭</span><span class="sxs-lookup"><span data-stu-id="32553-132">Header</span></span><br/>  | <dl> <span data-ttu-id="32553-133"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="32553-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="32553-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="32553-134">Library</span></span><br/> | <dl> <span data-ttu-id="32553-135"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="32553-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32553-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32553-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32553-137">**IWMDRMDevice2 介面**</span><span class="sxs-lookup"><span data-stu-id="32553-137">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





