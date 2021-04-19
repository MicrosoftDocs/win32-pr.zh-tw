---
title: 'IWMDRMLicenseManagement CreateLicenseRevocationChallenge 方法 (Wmdrmsdk .h) '
description: CreateLicenseRevocationChallenge 方法會產生授權撤銷挑戰。
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- CreateLicenseRevocationChallenge 方法 windows Media 格式
- CreateLicenseRevocationChallenge 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，CreateLicenseRevocationChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977721"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a><span data-ttu-id="36822-106">IWMDRMLicenseManagement：： CreateLicenseRevocationChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="36822-106">IWMDRMLicenseManagement::CreateLicenseRevocationChallenge method</span></span>

<span data-ttu-id="36822-107">**CreateLicenseRevocationChallenge** 方法會產生授權撤銷挑戰。</span><span class="sxs-lookup"><span data-stu-id="36822-107">The **CreateLicenseRevocationChallenge** method generates a license revocation challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="36822-108">語法</span><span class="sxs-lookup"><span data-stu-id="36822-108">Syntax</span></span>


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a><span data-ttu-id="36822-109">參數</span><span class="sxs-lookup"><span data-stu-id="36822-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36822-110">*pbMachineID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36822-110">*pbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36822-111">使用者指定的機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="36822-111">User-specified machine identifier.</span></span> <span data-ttu-id="36822-112">此值可用來查詢伺服器上的授權，而且必須符合授權伺服器所使用的任何格式。</span><span class="sxs-lookup"><span data-stu-id="36822-112">This value is used to query for a license on the server and must conform to whatever format the license server uses.</span></span>

</dd> <dt>

<span data-ttu-id="36822-113">*cbMachineID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36822-113">*cbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36822-114">電腦識別碼的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36822-114">Size, in bytes, of the machine identifier.</span></span>

</dd> <dt>

<span data-ttu-id="36822-115">*pbChallenge* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36822-115">*pbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36822-116">使用者指定的挑戰資料。</span><span class="sxs-lookup"><span data-stu-id="36822-116">User-specified challenge data.</span></span> <span data-ttu-id="36822-117">除了電腦識別碼之外，還會使用此資料來查詢授權伺服器，以取得要撤銷的授權。</span><span class="sxs-lookup"><span data-stu-id="36822-117">This data, in addition to the machine identifier, is used to query the license server for licenses to be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="36822-118">*cbChallenge* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36822-118">*cbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36822-119">挑戰資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36822-119">Size, in bytes, of the challenge data.</span></span>

</dd> <dt>

<span data-ttu-id="36822-120">*ppbChallengeOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="36822-120">*ppbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36822-121">接收挑戰輸出位址之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="36822-121">Address of a pointer that receives the address of the challenge output.</span></span> <span data-ttu-id="36822-122">此緩衝區是傳送至授權撤銷服務的資料。</span><span class="sxs-lookup"><span data-stu-id="36822-122">This buffer is the data that is sent to the license revocation service.</span></span> <span data-ttu-id="36822-123">完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="36822-123">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="36822-124">*pcbChallengeOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="36822-124">*pcbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36822-125">接收配置之挑戰輸出資料大小的變數位址（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36822-125">Address of a variable that receives the size of the allocated challenge output data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36822-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="36822-126">Return value</span></span>

<span data-ttu-id="36822-127">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="36822-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="36822-128">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="36822-128">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="36822-129">傳回碼</span><span class="sxs-lookup"><span data-stu-id="36822-129">Return code</span></span>                                                                          | <span data-ttu-id="36822-130">Description</span><span class="sxs-lookup"><span data-stu-id="36822-130">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="36822-131"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="36822-131"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="36822-132">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="36822-132">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36822-133">備註</span><span class="sxs-lookup"><span data-stu-id="36822-133">Remarks</span></span>

<span data-ttu-id="36822-134">無。</span><span class="sxs-lookup"><span data-stu-id="36822-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="36822-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="36822-135">Requirements</span></span>



| <span data-ttu-id="36822-136">需求</span><span class="sxs-lookup"><span data-stu-id="36822-136">Requirement</span></span> | <span data-ttu-id="36822-137">值</span><span class="sxs-lookup"><span data-stu-id="36822-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36822-138">標頭</span><span class="sxs-lookup"><span data-stu-id="36822-138">Header</span></span><br/> | <dl> <span data-ttu-id="36822-139"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="36822-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36822-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36822-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36822-141">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="36822-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





