---
description: 在 TPM 上建立2048位簽署金鑰組。
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Win32_Tpm 類別的 CreateEndorsementKeyPair 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511159"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a><span data-ttu-id="8947a-103">Win32 Tpm 類別的 CreateEndorsementKeyPair 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8947a-103">CreateEndorsementKeyPair method of the Win32\_Tpm class</span></span>

<span data-ttu-id="8947a-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **CREATEENDORSEMENTKEYPAIR** 方法會在 Tpm 上建立2048位簽署金鑰組。</span><span class="sxs-lookup"><span data-stu-id="8947a-104">The **CreateEndorsementKeyPair** method of the [**Win32\_Tpm**](win32-tpm.md) class creates an 2048-bit endorsement key pair on the TPM.</span></span> <span data-ttu-id="8947a-105">簽署金鑰組必須可供 [**TakeOwnership**](takeownership-win32-tpm.md) 方法順利執行。</span><span class="sxs-lookup"><span data-stu-id="8947a-105">The endorsement key pair must be available for the [**TakeOwnership**](takeownership-win32-tpm.md) method to run successfully.</span></span> <span data-ttu-id="8947a-106">您可以使用 [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) 方法來偵測簽署金鑰是否已存在於 TPM 中。</span><span class="sxs-lookup"><span data-stu-id="8947a-106">You can use the [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) method to detect whether the endorsement key already exists on the TPM.</span></span>

## <a name="syntax"></a><span data-ttu-id="8947a-107">語法</span><span class="sxs-lookup"><span data-stu-id="8947a-107">Syntax</span></span>


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a><span data-ttu-id="8947a-108">參數</span><span class="sxs-lookup"><span data-stu-id="8947a-108">Parameters</span></span>

<span data-ttu-id="8947a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8947a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8947a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8947a-110">Return value</span></span>

<span data-ttu-id="8947a-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8947a-111">Type: **uint32**</span></span>

<span data-ttu-id="8947a-112">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8947a-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="8947a-113">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="8947a-113">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="8947a-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="8947a-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="8947a-115">Description</span><span class="sxs-lookup"><span data-stu-id="8947a-115">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="8947a-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8947a-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="8947a-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="8947a-117">The method was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="8947a-118"><dt> **TPM \_ E \_ 停用的 \_ CMD**</dt> <dt>2150105096 (0x80280008)</dt></span><span class="sxs-lookup"><span data-stu-id="8947a-118"><dt>**TPM\_E\_DISABLED\_CMD** </dt> <dt>2150105096 (0x80280008)</dt></span></span> </dl> | <span data-ttu-id="8947a-119">此 TPM 上已有簽署金鑰組。</span><span class="sxs-lookup"><span data-stu-id="8947a-119">An endorsement key pair already exists on this TPM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8947a-120">備註</span><span class="sxs-lookup"><span data-stu-id="8947a-120">Remarks</span></span>

<span data-ttu-id="8947a-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="8947a-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8947a-122">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8947a-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8947a-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="8947a-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8947a-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="8947a-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8947a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8947a-125">Requirements</span></span>



| <span data-ttu-id="8947a-126">需求</span><span class="sxs-lookup"><span data-stu-id="8947a-126">Requirement</span></span> | <span data-ttu-id="8947a-127">值</span><span class="sxs-lookup"><span data-stu-id="8947a-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8947a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8947a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8947a-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8947a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8947a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8947a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8947a-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8947a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8947a-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="8947a-132">Namespace</span></span><br/>                | <span data-ttu-id="8947a-133">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="8947a-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="8947a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8947a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8947a-135"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8947a-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="8947a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8947a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8947a-137"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8947a-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8947a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8947a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8947a-139">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="8947a-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
