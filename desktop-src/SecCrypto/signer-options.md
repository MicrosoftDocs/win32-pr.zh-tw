---
description: 設定或抓取簽署者的憑證選項。
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: 簽署者. 選項屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995373"
---
# <a name="signeroptions-property"></a><span data-ttu-id="6ca51-103">簽署者. 選項屬性</span><span class="sxs-lookup"><span data-stu-id="6ca51-103">Signer.Options property</span></span>

<span data-ttu-id="6ca51-104">\[[ **選項** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6ca51-104">\[The **Options** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ca51-105">相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="6ca51-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6ca51-106">**Options** 屬性會設定或抓取簽署者的憑證選項。</span><span class="sxs-lookup"><span data-stu-id="6ca51-106">The **Options** property sets or retrieves the signer's certificate option.</span></span>

<span data-ttu-id="6ca51-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ca51-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca51-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ca51-108">Syntax</span></span>


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a><span data-ttu-id="6ca51-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="6ca51-109">Property value</span></span>

<span data-ttu-id="6ca51-110">CAPICOM 憑證的值包含指定簽署者憑證選項的 [**\_ \_ \_ 選項**](capicom-certificate-include-option.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="6ca51-110">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies the signer's certificate option.</span></span> <span data-ttu-id="6ca51-111">預設值為 [ \_ \_ \_ \_ 除了根以外的 CAPICOM 憑證包含鏈] \_ 。</span><span class="sxs-lookup"><span data-stu-id="6ca51-111">The default value is CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT.</span></span> <span data-ttu-id="6ca51-112">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="6ca51-112">The following table shows the possible values.</span></span>



| <span data-ttu-id="6ca51-113">值</span><span class="sxs-lookup"><span data-stu-id="6ca51-113">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="6ca51-114">意義</span><span class="sxs-lookup"><span data-stu-id="6ca51-114">Meaning</span></span>                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="6ca51-115"><dt>**\_ \_ \_ \_ 除了 \_ 根以外的 CAPICOM 憑證包含鏈**</dt></span><span class="sxs-lookup"><span data-stu-id="6ca51-115"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="6ca51-116">將所有憑證儲存在鏈中，但根實體除外。</span><span class="sxs-lookup"><span data-stu-id="6ca51-116">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="6ca51-117"><dt>**CAPICOM \_ 憑證 \_ 包含 \_ 整個 \_ 鏈**</dt></span><span class="sxs-lookup"><span data-stu-id="6ca51-117"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="6ca51-118">儲存完整的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="6ca51-118">Saves the complete certificate chain.</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="6ca51-119"><dt>**\_ \_ 僅限 CAPICOM 憑證包含 \_ 結束 \_ 實體 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ca51-119"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="6ca51-120">只儲存終端實體憑證。</span><span class="sxs-lookup"><span data-stu-id="6ca51-120">Saves only the end entity certificate.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="6ca51-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ca51-121">Requirements</span></span>



| <span data-ttu-id="6ca51-122">需求</span><span class="sxs-lookup"><span data-stu-id="6ca51-122">Requirement</span></span> | <span data-ttu-id="6ca51-123">值</span><span class="sxs-lookup"><span data-stu-id="6ca51-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca51-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6ca51-124">Redistributable</span></span><br/> | <span data-ttu-id="6ca51-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6ca51-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6ca51-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6ca51-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="6ca51-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ca51-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca51-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ca51-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca51-129">**簽署者**</span><span class="sxs-lookup"><span data-stu-id="6ca51-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
