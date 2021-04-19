---
description: 取得 TPM 儲存根金鑰公開部分之指定模數的儲存根金鑰指紋。
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: Win32_Tpm：： GetSrkADThumbprint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973240"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a><span data-ttu-id="1f6ed-103">Win32 \_ Tpm：： GetSrkADThumbprint 方法</span><span class="sxs-lookup"><span data-stu-id="1f6ed-103">Win32\_Tpm::GetSrkADThumbprint method</span></span>

<span data-ttu-id="1f6ed-104">取得 TPM 儲存根金鑰公開部分之指定模數的儲存根金鑰指紋。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-104">Gets the Storage root key thumbprint for a given modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="1f6ed-105">如果透過群組原則設定啟用 TPM 擁有者授權資訊的 Active Directory 備份，則會使用指紋來為 Active Directory 伺服器上的儲存體根金鑰編制索引。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-105">The thumbprint is used to index the Storage Root Keys on the Active Directory server if the Active Directory backup of TPM owner authorization information is enabled through Group Policy setting.</span></span>

> [!Note]  
> <span data-ttu-id="1f6ed-106">從 Windows 10 1607 版開始，TPM 擁有者授權永遠不會備份到 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-106">Beginning with Windows 10, version 1607, the TPM owner authorization is never backed up to Active Directory.</span></span>

 

<span data-ttu-id="1f6ed-107">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6ed-108">語法</span><span class="sxs-lookup"><span data-stu-id="1f6ed-108">Syntax</span></span>


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a><span data-ttu-id="1f6ed-109">參數</span><span class="sxs-lookup"><span data-stu-id="1f6ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f6ed-110">*SrkPublicKeyModulus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f6ed-110">*SrkPublicKeyModulus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f6ed-111">TPM 儲存根金鑰之公開部分的模數。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-111">The modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="1f6ed-112">您也可以使用 [Win32 \_ TPM](win32-tpm.md)類別的 [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md)方法來取得它。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-112">It can also be obtained using the [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) method of the [Win32\_TPM](win32-tpm.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="1f6ed-113">*SrkADThumbprint* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1f6ed-113">*SrkADThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f6ed-114">傳回20位元組陣列，其中包含給定模數的儲存體根金鑰指紋。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-114">Returns a 20-byte array containing the storage root key thumbprint for the given modulus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f6ed-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f6ed-115">Return value</span></span>

<span data-ttu-id="1f6ed-116">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-116">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="1f6ed-117">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="1f6ed-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1f6ed-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="1f6ed-119">Description</span><span class="sxs-lookup"><span data-stu-id="1f6ed-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1f6ed-120"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ed-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="1f6ed-121">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f6ed-122">備註</span><span class="sxs-lookup"><span data-stu-id="1f6ed-122">Remarks</span></span>

<span data-ttu-id="1f6ed-123">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1f6ed-124">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1f6ed-125">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1f6ed-126">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="1f6ed-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6ed-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f6ed-127">Requirements</span></span>



| <span data-ttu-id="1f6ed-128">需求</span><span class="sxs-lookup"><span data-stu-id="1f6ed-128">Requirement</span></span> | <span data-ttu-id="1f6ed-129">值</span><span class="sxs-lookup"><span data-stu-id="1f6ed-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6ed-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f6ed-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6ed-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f6ed-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1f6ed-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f6ed-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6ed-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f6ed-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1f6ed-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="1f6ed-134">Namespace</span></span><br/>                | <span data-ttu-id="1f6ed-135">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="1f6ed-135">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="1f6ed-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1f6ed-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f6ed-137"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ed-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f6ed-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1f6ed-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f6ed-139"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ed-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f6ed-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f6ed-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f6ed-141">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="1f6ed-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
