---
description: 列舉系統上符合指定準則的所有憑證，並傳回指紋清單。
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Win32_EncryptableVolume 類別的 FindValidCertificates 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319879"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a29c2-103">Win32 EncryptableVolume 類別的 FindValidCertificates 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a29c2-103">FindValidCertificates method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a29c2-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **FindValidCertificates** 方法會列舉系統上符合指定準則的所有憑證，並傳回指紋清單。</span><span class="sxs-lookup"><span data-stu-id="a29c2-104">The **FindValidCertificates** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enumerates all certificates on the system that match the indicated criteria and returns a list of thumbprints.</span></span> <span data-ttu-id="a29c2-105">傳回的清單只包含具有有效 [*物件識別碼*](../secgloss/o-gly.md) (OID) 的憑證。</span><span class="sxs-lookup"><span data-stu-id="a29c2-105">The returned list only contains certificates with a valid [*object identifier*](../secgloss/o-gly.md) (OID).</span></span> <span data-ttu-id="a29c2-106">OID 可以是預設值，也可以在群組原則中指定。</span><span class="sxs-lookup"><span data-stu-id="a29c2-106">The OID may be the default, or it may be specified in the Group Policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="a29c2-107">語法</span><span class="sxs-lookup"><span data-stu-id="a29c2-107">Syntax</span></span>


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a><span data-ttu-id="a29c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="a29c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a29c2-109">*CertificateThumbprint* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a29c2-109">*CertificateThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a29c2-110">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a29c2-110">Type: **string\[\]**</span></span>

<span data-ttu-id="a29c2-111">字串的陣列，其中包含有效憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="a29c2-111">An array of strings that contains the list of valid certificates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a29c2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a29c2-112">Return value</span></span>

<span data-ttu-id="a29c2-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a29c2-113">Type: **uint32**</span></span>

<span data-ttu-id="a29c2-114">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a29c2-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="a29c2-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="a29c2-115">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="a29c2-116">Description</span><span class="sxs-lookup"><span data-stu-id="a29c2-116">Description</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a29c2-117"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a29c2-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="a29c2-118">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="a29c2-118">The method was successful.</span></span><br/>                |
| <dl> <span data-ttu-id="a29c2-119"><dt>**FVE \_E \_ 不正確 \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="a29c2-119"><dt>**FVE\_E\_INVALID\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl> | <span data-ttu-id="a29c2-120">可用的 BitLocker OID 無效。</span><span class="sxs-lookup"><span data-stu-id="a29c2-120">The available BitLocker OID is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a29c2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a29c2-121">Requirements</span></span>



| <span data-ttu-id="a29c2-122">需求</span><span class="sxs-lookup"><span data-stu-id="a29c2-122">Requirement</span></span> | <span data-ttu-id="a29c2-123">值</span><span class="sxs-lookup"><span data-stu-id="a29c2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a29c2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a29c2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a29c2-125">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a29c2-125">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a29c2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a29c2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a29c2-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a29c2-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a29c2-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="a29c2-128">Namespace</span></span><br/>                | <span data-ttu-id="a29c2-129">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="a29c2-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a29c2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a29c2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a29c2-131"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="a29c2-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a29c2-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a29c2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a29c2-133">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="a29c2-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
