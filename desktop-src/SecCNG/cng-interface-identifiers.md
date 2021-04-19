---
description: 下列識別碼用來識別 CNG 密碼編譯介面。
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: 'CNG 介面識別碼 (Bcrypt .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f75de82e198e0471b48175a080012b9b40eed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973007"
---
# <a name="cng-interface-identifiers"></a><span data-ttu-id="ff304-103">CNG 介面識別碼</span><span class="sxs-lookup"><span data-stu-id="ff304-103">CNG Interface Identifiers</span></span>

<span data-ttu-id="ff304-104">下列識別碼用來識別 CNG 密碼編譯介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-104">The following identifiers are used to identify a CNG cryptographic interface.</span></span> <span data-ttu-id="ff304-105">在 CNG 中，介面會識別提供者所支援的密碼編譯行為類型。</span><span class="sxs-lookup"><span data-stu-id="ff304-105">In CNG, an interface identifies the type of cryptographic behavior that a provider supports.</span></span> <span data-ttu-id="ff304-106">例如，提供者可以是亂數產生器，也可以是雜湊提供者。</span><span class="sxs-lookup"><span data-stu-id="ff304-106">For example, a provider may be a random number generator or it may be a hashing provider.</span></span>



| <span data-ttu-id="ff304-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="ff304-107">Constant/value</span></span>                                                                                                                                                                                                                                                                                             | <span data-ttu-id="ff304-108">Description</span><span class="sxs-lookup"><span data-stu-id="ff304-108">Description</span></span>                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <span data-ttu-id="ff304-109"><dt>**BCRYPT \_CIPHER \_ 介面**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-109"><dt>**BCRYPT\_CIPHER\_INTERFACE**</dt> <dt>0x00000001</dt></span></span> </dl>                                               | <span data-ttu-id="ff304-110">對稱式加密介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-110">The symmetric cipher interface.</span></span><br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <span data-ttu-id="ff304-111"><dt>**BCRYPT \_雜湊 \_ 介面**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-111"><dt>**BCRYPT\_HASH\_INTERFACE**</dt> <dt>0x00000002</dt></span></span> </dl>                                                     | <span data-ttu-id="ff304-112">雜湊介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-112">The hash interface.</span></span><br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <span data-ttu-id="ff304-113"><dt>**BCRYPT \_非對稱式 \_ 加密 \_ 介面**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-113"><dt>**BCRYPT\_ASYMMETRIC\_ENCRYPTION\_INTERFACE**</dt> <dt>0x00000003</dt></span></span> </dl> | <span data-ttu-id="ff304-114">非對稱式加密介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-114">The asymmetric encryption interface.</span></span><br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <span data-ttu-id="ff304-115"><dt>**BCRYPT \_秘密 \_ 合約 \_ 介面**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-115"><dt>**BCRYPT\_SECRET\_AGREEMENT\_INTERFACE**</dt> <dt>0x00000004</dt></span></span> </dl>                | <span data-ttu-id="ff304-116">秘密協定介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-116">The secret agreement interface.</span></span><br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <span data-ttu-id="ff304-117"><dt>**BCRYPT \_簽名 \_ 介面**</dt> <dt>0x00000005</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-117"><dt>**BCRYPT\_SIGNATURE\_INTERFACE**</dt> <dt>0x00000005</dt></span></span> </dl>                                      | <span data-ttu-id="ff304-118">簽名介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-118">The signature interface.</span></span><br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <span data-ttu-id="ff304-119"><dt>**BCRYPT \_RNG \_ 介面**</dt> <dt>0x00000006</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-119"><dt>**BCRYPT\_RNG\_INTERFACE**</dt> <dt>0x00000006</dt></span></span> </dl>                                                        | <span data-ttu-id="ff304-120">亂數產生器介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-120">The random number generator interface.</span></span><br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <span data-ttu-id="ff304-121"><dt>**NCRYPT \_金鑰 \_ 儲存 \_ 介面**</dt> <dt>0x00010001</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-121"><dt>**NCRYPT\_KEY\_STORAGE\_INTERFACE**</dt> <dt>0x00010001</dt></span></span> </dl>                               | <span data-ttu-id="ff304-122">金鑰儲存介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-122">The key storage interface.</span></span><br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <span data-ttu-id="ff304-123"><dt>**NCRYPT \_SCHANNEL \_ 介面**</dt> <dt>0x00010002</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-123"><dt>**NCRYPT\_SCHANNEL\_INTERFACE**</dt> <dt>0x00010002</dt></span></span> </dl>                                         | <span data-ttu-id="ff304-124">Schannel 簽章介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-124">The Schannel signature interface.</span></span><br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <span data-ttu-id="ff304-125"><dt>**NCRYPT \_SCHANNEL 簽章 \_ \_ 介面**</dt> <dt>0x00010003</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-125"><dt>**NCRYPT\_SCHANNEL\_SIGNATURE\_INTERFACE**</dt> <dt>0x00010003</dt></span></span> </dl>          | <span data-ttu-id="ff304-126">Schannel 加密套件介面。</span><span class="sxs-lookup"><span data-stu-id="ff304-126">The Schannel cipher suite interface.</span></span><br/> <span data-ttu-id="ff304-127">**Windows server 2008、Windows Vista、Windows server 2003、WINDOWS XP 及 windows 2000：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="ff304-127">**Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP and Windows 2000:** This value is not supported.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ff304-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff304-128">Requirements</span></span>



| <span data-ttu-id="ff304-129">需求</span><span class="sxs-lookup"><span data-stu-id="ff304-129">Requirement</span></span> | <span data-ttu-id="ff304-130">值</span><span class="sxs-lookup"><span data-stu-id="ff304-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff304-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff304-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ff304-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff304-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                      |
| <span data-ttu-id="ff304-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff304-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ff304-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff304-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                |
| <span data-ttu-id="ff304-135">標頭</span><span class="sxs-lookup"><span data-stu-id="ff304-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff304-136"><dt>Bcrypt .h;</dt><dt>Ncrypt .h</dt></span><span class="sxs-lookup"><span data-stu-id="ff304-136"><dt>Bcrypt.h; </dt> <dt>Ncrypt.h</dt></span></span> </dl> |



 

 




