---
description: 設定或抓取指定 EKU 之 CAPICOM 名稱的列舉值。 這是預設屬性。
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: IEKU：： Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987879"
---
# <a name="iekuname-property"></a><span data-ttu-id="e434f-104">IEKU：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="e434f-104">IEKU::Name property</span></span>

<span data-ttu-id="e434f-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e434f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e434f-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="e434f-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e434f-107">**Name** 屬性會設定或抓取指定 EKU 之 CAPICOM 名稱的列舉值。</span><span class="sxs-lookup"><span data-stu-id="e434f-107">The **Name** property sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="e434f-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="e434f-108">This is the default property.</span></span>

<span data-ttu-id="e434f-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e434f-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e434f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e434f-110">Syntax</span></span>


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a><span data-ttu-id="e434f-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="e434f-111">Property value</span></span>

<span data-ttu-id="e434f-112">指定 EKU 之 CAPICOM 名稱的 [**CAPICOM \_ EKU**](capicom-eku.md) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="e434f-112">A value of the [**CAPICOM\_EKU**](capicom-eku.md) enumeration that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="e434f-113">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="e434f-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="e434f-114">值</span><span class="sxs-lookup"><span data-stu-id="e434f-114">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="e434f-115">意義</span><span class="sxs-lookup"><span data-stu-id="e434f-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <span data-ttu-id="e434f-116"><dt>**CAPICOM \_ EKU \_ 其他**</dt></span><span class="sxs-lookup"><span data-stu-id="e434f-116"><dt>**CAPICOM\_EKU\_OTHER**</dt></span></span> </dl>                                                      | <span data-ttu-id="e434f-117">憑證具有在本機原則中定義的使用方式。</span><span class="sxs-lookup"><span data-stu-id="e434f-117">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="e434f-118">如果需要的 EKU 未預先定義，而且應用程式必須設定 OID 值，就會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e434f-118">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <span data-ttu-id="e434f-119"><dt>**CAPICOM \_ EKU \_ 伺服器 \_ 驗證**</dt></span><span class="sxs-lookup"><span data-stu-id="e434f-119"><dt>**CAPICOM\_EKU\_SERVER\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="e434f-120">憑證可以用來驗證服務器。</span><span class="sxs-lookup"><span data-stu-id="e434f-120">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <span data-ttu-id="e434f-121"><dt>**CAPICOM \_ EKU \_ 用戶端 \_ 驗證**</dt></span><span class="sxs-lookup"><span data-stu-id="e434f-121"><dt>**CAPICOM\_EKU\_CLIENT\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="e434f-122">憑證可以用來驗證用戶端。</span><span class="sxs-lookup"><span data-stu-id="e434f-122">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <span data-ttu-id="e434f-123"><dt>**CAPICOM \_ EKU 程式 \_ 代碼 \_ 簽署**</dt></span><span class="sxs-lookup"><span data-stu-id="e434f-123"><dt>**CAPICOM\_EKU\_CODE\_SIGNING**</dt></span></span> </dl>                                | <span data-ttu-id="e434f-124">憑證可以用來建立數位簽章。</span><span class="sxs-lookup"><span data-stu-id="e434f-124">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <span data-ttu-id="e434f-125"><dt>**CAPICOM \_ EKU \_ 電子郵件 \_ 保護**</dt></span><span class="sxs-lookup"><span data-stu-id="e434f-125"><dt>**CAPICOM\_EKU\_EMAIL\_PROTECTION**</dt></span></span> </dl>                    | <span data-ttu-id="e434f-126">憑證可用於電子郵件保護。</span><span class="sxs-lookup"><span data-stu-id="e434f-126">Certificate can be used for email protection.</span></span><br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <span data-ttu-id="e434f-127"><dt>**CAPICOM \_ EKU \_ 智慧卡 \_ 登入**</dt></span><span class="sxs-lookup"><span data-stu-id="e434f-127"><dt>**CAPICOM\_EKU\_SMARTCARD\_LOGON**</dt></span></span> </dl>                       | <span data-ttu-id="e434f-128">憑證可用於智慧卡登入。</span><span class="sxs-lookup"><span data-stu-id="e434f-128">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="e434f-129">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="e434f-129">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <span data-ttu-id="e434f-130"><dt>**CAPICOM \_ EKU \_ 加密 \_ 檔 \_ 系統**</dt></span><span class="sxs-lookup"><span data-stu-id="e434f-130"><dt>**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</dt></span></span> </dl> | <span data-ttu-id="e434f-131">憑證可用於 EFS。</span><span class="sxs-lookup"><span data-stu-id="e434f-131">Certificate can be used for EFS.</span></span> <span data-ttu-id="e434f-132">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="e434f-132">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="e434f-133">備註</span><span class="sxs-lookup"><span data-stu-id="e434f-133">Remarks</span></span>

<span data-ttu-id="e434f-134">當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="e434f-134">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="e434f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e434f-135">Requirements</span></span>



| <span data-ttu-id="e434f-136">需求</span><span class="sxs-lookup"><span data-stu-id="e434f-136">Requirement</span></span> | <span data-ttu-id="e434f-137">值</span><span class="sxs-lookup"><span data-stu-id="e434f-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e434f-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e434f-138">End of client support</span></span><br/> | <span data-ttu-id="e434f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e434f-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e434f-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e434f-140">End of server support</span></span><br/> | <span data-ttu-id="e434f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e434f-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e434f-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e434f-142">Redistributable</span></span><br/>       | <span data-ttu-id="e434f-143">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e434f-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e434f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e434f-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e434f-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e434f-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
