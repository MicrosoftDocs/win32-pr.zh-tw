---
title: IWMDRMDevice GetSecureClockChallenge 方法
description: GetSecureClockChallenge 方法會捕獲安全的時鐘挑戰結果。
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- GetSecureClockChallenge 方法 windows Media 裝置管理員
- GetSecureClockChallenge 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetSecureClockChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974915"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a><span data-ttu-id="acfa8-106">IWMDRMDevice：： GetSecureClockChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="acfa8-106">IWMDRMDevice::GetSecureClockChallenge method</span></span>

<span data-ttu-id="acfa8-107">**GetSecureClockChallenge** 方法會捕獲安全的時鐘挑戰結果。</span><span class="sxs-lookup"><span data-stu-id="acfa8-107">The **GetSecureClockChallenge** method retrieves the secure clock challenge result.</span></span>

## <a name="syntax"></a><span data-ttu-id="acfa8-108">語法</span><span class="sxs-lookup"><span data-stu-id="acfa8-108">Syntax</span></span>


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="acfa8-109">參數</span><span class="sxs-lookup"><span data-stu-id="acfa8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acfa8-110">*ppbChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="acfa8-110">*ppbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acfa8-111">已取出挑戰結果。</span><span class="sxs-lookup"><span data-stu-id="acfa8-111">Retrieved challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="acfa8-112">*pcbChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="acfa8-112">*pcbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acfa8-113">挑戰結果的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="acfa8-113">Size of the challenge result, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acfa8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="acfa8-114">Return value</span></span>

<span data-ttu-id="acfa8-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="acfa8-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="acfa8-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="acfa8-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="acfa8-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="acfa8-117">Return code</span></span>                                                                          | <span data-ttu-id="acfa8-118">Description</span><span class="sxs-lookup"><span data-stu-id="acfa8-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="acfa8-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="acfa8-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="acfa8-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="acfa8-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="acfa8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="acfa8-121">Requirements</span></span>



| <span data-ttu-id="acfa8-122">需求</span><span class="sxs-lookup"><span data-stu-id="acfa8-122">Requirement</span></span> | <span data-ttu-id="acfa8-123">值</span><span class="sxs-lookup"><span data-stu-id="acfa8-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acfa8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="acfa8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="acfa8-125"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="acfa8-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="acfa8-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="acfa8-126">Library</span></span><br/> | <dl> <span data-ttu-id="acfa8-127"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="acfa8-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acfa8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acfa8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acfa8-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="acfa8-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="acfa8-130">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="acfa8-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





