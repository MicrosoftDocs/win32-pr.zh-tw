---
title: IWMDRMLicense GetOutputProtectionLevels 方法
description: GetOutputProtectionLevels 方法會抓取指派給授權 (OPLs) 所有輸出保護層級的相關資訊。
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- GetOutputProtectionLevels 方法 windows Media 格式
- GetOutputProtectionLevels 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetOutputProtectionLevels 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966219"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a><span data-ttu-id="4e274-106">IWMDRMLicense：： GetOutputProtectionLevels 方法</span><span class="sxs-lookup"><span data-stu-id="4e274-106">IWMDRMLicense::GetOutputProtectionLevels method</span></span>

<span data-ttu-id="4e274-107">**GetOutputProtectionLevels** 方法會抓取指派給授權 (OPLs) 所有輸出保護層級的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4e274-107">The **GetOutputProtectionLevels** method retrieves information about all output protection levels (OPLs) assigned to the license.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e274-108">語法</span><span class="sxs-lookup"><span data-stu-id="4e274-108">Syntax</span></span>


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a><span data-ttu-id="4e274-109">參數</span><span class="sxs-lookup"><span data-stu-id="4e274-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e274-110">*pOPLs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e274-110">*pOPLs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e274-111">接收 OPL 資訊之 [**WMDRM \_ 輸出 \_ 保護 \_ 層級**](wmdrm-output-protection-levels.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4e274-111">Pointer to a [**WMDRM\_OUTPUT\_PROTECTION\_LEVELS**](wmdrm-output-protection-levels.md) structure that receives the OPL information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e274-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e274-112">Return value</span></span>

<span data-ttu-id="4e274-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4e274-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4e274-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="4e274-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4e274-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4e274-115">Return code</span></span>                                                                          | <span data-ttu-id="4e274-116">Description</span><span class="sxs-lookup"><span data-stu-id="4e274-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4e274-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4e274-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4e274-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="4e274-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e274-119">備註</span><span class="sxs-lookup"><span data-stu-id="4e274-119">Remarks</span></span>

<span data-ttu-id="4e274-120">無。</span><span class="sxs-lookup"><span data-stu-id="4e274-120">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e274-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e274-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e274-122">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="4e274-122">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





