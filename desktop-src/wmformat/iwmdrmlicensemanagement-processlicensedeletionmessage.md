---
title: 'IWMDRMLicenseManagement ProcessLicenseDeletionMessage 方法 (Wmdrmsdk .h) '
description: ProcessLicenseDeletion 方法會刪除針對原始以其他內容保護系統保護的內容所匯入的授權。
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- ProcessLicenseDeletionMessage 方法 windows Media 格式
- ProcessLicenseDeletionMessage 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，ProcessLicenseDeletionMessage 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978690"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a><span data-ttu-id="cdb1f-106">IWMDRMLicenseManagement：:P rocessLicenseDeletionMessage 方法</span><span class="sxs-lookup"><span data-stu-id="cdb1f-106">IWMDRMLicenseManagement::ProcessLicenseDeletionMessage method</span></span>

<span data-ttu-id="cdb1f-107">**ProcessLicenseDeletion** 方法會刪除針對原始以其他內容保護系統保護的內容所匯入的授權。</span><span class="sxs-lookup"><span data-stu-id="cdb1f-107">The **ProcessLicenseDeletion** method deletes a license that was imported for content originally protected with another content protection system.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb1f-108">語法</span><span class="sxs-lookup"><span data-stu-id="cdb1f-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a><span data-ttu-id="cdb1f-109">參數</span><span class="sxs-lookup"><span data-stu-id="cdb1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdb1f-110">*bstrDeletionMessage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cdb1f-110">*bstrDeletionMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdb1f-111">識別要刪除之授權的訊息。</span><span class="sxs-lookup"><span data-stu-id="cdb1f-111">Message identifying the license to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdb1f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdb1f-112">Return value</span></span>

<span data-ttu-id="cdb1f-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="cdb1f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cdb1f-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="cdb1f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cdb1f-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cdb1f-115">Return code</span></span>                                                                          | <span data-ttu-id="cdb1f-116">Description</span><span class="sxs-lookup"><span data-stu-id="cdb1f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cdb1f-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cdb1f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cdb1f-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="cdb1f-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cdb1f-119">備註</span><span class="sxs-lookup"><span data-stu-id="cdb1f-119">Remarks</span></span>

<span data-ttu-id="cdb1f-120">無。</span><span class="sxs-lookup"><span data-stu-id="cdb1f-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdb1f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdb1f-121">Requirements</span></span>



| <span data-ttu-id="cdb1f-122">需求</span><span class="sxs-lookup"><span data-stu-id="cdb1f-122">Requirement</span></span> | <span data-ttu-id="cdb1f-123">值</span><span class="sxs-lookup"><span data-stu-id="cdb1f-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb1f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cdb1f-124">Header</span></span><br/> | <dl> <span data-ttu-id="cdb1f-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="cdb1f-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdb1f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdb1f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb1f-127">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="cdb1f-127">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





