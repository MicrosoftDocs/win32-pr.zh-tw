---
title: 'IWMDRMSecurity GetSecurityVersion 方法 (Wmdrmsdk .h) '
description: GetSecurityVersion 方法會在用戶端電腦上抓取 DRM 子系統的版本。
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- GetSecurityVersion 方法 windows Media 格式
- GetSecurityVersion 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetSecurityVersion 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984034"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a><span data-ttu-id="db5d4-106">IWMDRMSecurity：： GetSecurityVersion 方法</span><span class="sxs-lookup"><span data-stu-id="db5d4-106">IWMDRMSecurity::GetSecurityVersion method</span></span>

<span data-ttu-id="db5d4-107">**GetSecurityVersion** 方法會在用戶端電腦上抓取 DRM 子系統的版本。</span><span class="sxs-lookup"><span data-stu-id="db5d4-107">The **GetSecurityVersion** method retrieves the version of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="db5d4-108">語法</span><span class="sxs-lookup"><span data-stu-id="db5d4-108">Syntax</span></span>


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a><span data-ttu-id="db5d4-109">參數</span><span class="sxs-lookup"><span data-stu-id="db5d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db5d4-110">*pbstrVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="db5d4-110">*pbstrVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db5d4-111">接收 DRM 子系統版本號碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="db5d4-111">Address of a variable that receives the DRM subsystem version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db5d4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="db5d4-112">Return value</span></span>

<span data-ttu-id="db5d4-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="db5d4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="db5d4-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="db5d4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="db5d4-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="db5d4-115">Return code</span></span>                                                                          | <span data-ttu-id="db5d4-116">Description</span><span class="sxs-lookup"><span data-stu-id="db5d4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="db5d4-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="db5d4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="db5d4-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="db5d4-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db5d4-119">備註</span><span class="sxs-lookup"><span data-stu-id="db5d4-119">Remarks</span></span>

<span data-ttu-id="db5d4-120">版本號碼會以字串表示，由四個以句點分隔的數位所組成。</span><span class="sxs-lookup"><span data-stu-id="db5d4-120">The version number is expressed as a string consisting of four numbers separated by periods.</span></span> <span data-ttu-id="db5d4-121">第一個數位是主要版本號碼，通常是設定為2。</span><span class="sxs-lookup"><span data-stu-id="db5d4-121">The first number is the major version number, which is usually set to 2.</span></span> <span data-ttu-id="db5d4-122">第二個數字是次要版本號碼，範圍介於2到10之間。</span><span class="sxs-lookup"><span data-stu-id="db5d4-122">The second number is the minor version number, ranging from 2 to 10.</span></span> <span data-ttu-id="db5d4-123">第三個數字一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="db5d4-123">The third number is always set to 0.</span></span> <span data-ttu-id="db5d4-124">第四個數字設定為0或1，且為布林值，指出子系統是否已個別化。</span><span class="sxs-lookup"><span data-stu-id="db5d4-124">The fourth number is set to 0 or 1, and is a Boolean value indicating whether the subsystem has been individualized.</span></span> <span data-ttu-id="db5d4-125">例如，"2.4.0.1" 的版本號碼表示第二個主要版本的個別第四個次要版本。</span><span class="sxs-lookup"><span data-stu-id="db5d4-125">For example, a version number of "2.4.0.1" indicates the individualized fourth minor version of the second major version.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5d4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="db5d4-126">Requirements</span></span>



| <span data-ttu-id="db5d4-127">需求</span><span class="sxs-lookup"><span data-stu-id="db5d4-127">Requirement</span></span> | <span data-ttu-id="db5d4-128">值</span><span class="sxs-lookup"><span data-stu-id="db5d4-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db5d4-129">標頭</span><span class="sxs-lookup"><span data-stu-id="db5d4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="db5d4-130"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="db5d4-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="db5d4-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="db5d4-131">Library</span></span><br/> | <dl> <span data-ttu-id="db5d4-132"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="db5d4-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5d4-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db5d4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5d4-134">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="db5d4-134">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





