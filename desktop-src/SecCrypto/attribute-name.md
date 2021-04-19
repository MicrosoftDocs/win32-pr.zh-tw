---
description: 設定或抓取屬性的 CAPICOM 名稱。 這是預設屬性。
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Attribute.Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995190"
---
# <a name="attributename-property"></a><span data-ttu-id="d034c-104">Attribute.Name 屬性</span><span class="sxs-lookup"><span data-stu-id="d034c-104">Attribute.Name property</span></span>

<span data-ttu-id="d034c-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d034c-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d034c-106">請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObject 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="d034c-106">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="d034c-107">**Name** 屬性會設定或抓取屬性的 CAPICOM 名稱。</span><span class="sxs-lookup"><span data-stu-id="d034c-107">The **Name** property sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="d034c-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="d034c-108">This is the default property.</span></span>

<span data-ttu-id="d034c-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d034c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d034c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d034c-110">Syntax</span></span>


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a><span data-ttu-id="d034c-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="d034c-111">Property value</span></span>

<span data-ttu-id="d034c-112">指定屬性之 CAPICOM 名稱的 [**capicom \_ 屬性**](capicom-attribute.md) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="d034c-112">A value of the [**CAPICOM\_ATTRIBUTE**](capicom-attribute.md) enumeration that specifies the CAPICOM name of the attribute.</span></span> <span data-ttu-id="d034c-113">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="d034c-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="d034c-114">值</span><span class="sxs-lookup"><span data-stu-id="d034c-114">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="d034c-115">意義</span><span class="sxs-lookup"><span data-stu-id="d034c-115">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <span data-ttu-id="d034c-116"><dt>**CAPICOM \_ 驗證 \_ 屬性 \_ 簽署 \_ 時間**</dt></span><span class="sxs-lookup"><span data-stu-id="d034c-116"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</dt></span></span> </dl>                         | <span data-ttu-id="d034c-117">屬性包含建立簽章的時間。</span><span class="sxs-lookup"><span data-stu-id="d034c-117">The attribute contains the time that the signature was created.</span></span><br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <span data-ttu-id="d034c-118"><dt>**CAPICOM \_ 驗證的 \_ 屬性 \_ 檔 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="d034c-118"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</dt></span></span> </dl>                      | <span data-ttu-id="d034c-119">屬性包含已簽署檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="d034c-119">The attribute contains the name of the signed document.</span></span><br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <span data-ttu-id="d034c-120"><dt>**CAPICOM \_ 驗證的 \_ 屬性 \_ 檔 \_ 描述**</dt></span><span class="sxs-lookup"><span data-stu-id="d034c-120"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</dt></span></span> </dl> | <span data-ttu-id="d034c-121">屬性包含已簽署檔的描述。</span><span class="sxs-lookup"><span data-stu-id="d034c-121">The attribute contains a description of the signed document.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="d034c-122">備註</span><span class="sxs-lookup"><span data-stu-id="d034c-122">Remarks</span></span>

<span data-ttu-id="d034c-123">當這個屬性的值是直接或間接重設時，會重設物件的整個狀態。</span><span class="sxs-lookup"><span data-stu-id="d034c-123">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="d034c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d034c-124">Requirements</span></span>



| <span data-ttu-id="d034c-125">需求</span><span class="sxs-lookup"><span data-stu-id="d034c-125">Requirement</span></span> | <span data-ttu-id="d034c-126">值</span><span class="sxs-lookup"><span data-stu-id="d034c-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d034c-127">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d034c-127">End of client support</span></span><br/> | <span data-ttu-id="d034c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d034c-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d034c-129">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d034c-129">End of server support</span></span><br/> | <span data-ttu-id="d034c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d034c-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d034c-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d034c-131">Redistributable</span></span><br/>       | <span data-ttu-id="d034c-132">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d034c-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d034c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d034c-133">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d034c-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d034c-134"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d034c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d034c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d034c-136">**屬性**</span><span class="sxs-lookup"><span data-stu-id="d034c-136">**Attribute**</span></span>](attribute.md)
</dt> </dl>

 

 
