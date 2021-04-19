---
description: 表示單一驗證的屬性。
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984755"
---
# <a name="attribute-object"></a><span data-ttu-id="d163a-103">Attribute 物件</span><span class="sxs-lookup"><span data-stu-id="d163a-103">Attribute object</span></span>

<span data-ttu-id="d163a-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d163a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d163a-105">請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObject 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="d163a-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="d163a-106">**Attribute** 物件代表單一已驗證的屬性。</span><span class="sxs-lookup"><span data-stu-id="d163a-106">The **Attribute** object represents a single authenticated attribute.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d163a-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="d163a-107">When to use</span></span>

<span data-ttu-id="d163a-108">**屬性** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="d163a-108">The **Attribute** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d163a-109">設定或取出屬性的 CAPICOM 名稱。</span><span class="sxs-lookup"><span data-stu-id="d163a-109">Set or retrieve the CAPICOM name of the attribute.</span></span>
-   <span data-ttu-id="d163a-110">設定或取得屬性的值，例如簽署時間、簽署的檔案名稱，或檔的描述。</span><span class="sxs-lookup"><span data-stu-id="d163a-110">Set or retrieve the value of the attribute, such as signing time, the name of the document signed, or a description of the document signed.</span></span>

## <a name="members"></a><span data-ttu-id="d163a-111">成員</span><span class="sxs-lookup"><span data-stu-id="d163a-111">Members</span></span>

<span data-ttu-id="d163a-112">**Attribute** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d163a-112">The **Attribute** object has these types of members:</span></span>

-   [<span data-ttu-id="d163a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d163a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d163a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d163a-114">Properties</span></span>

<span data-ttu-id="d163a-115">**Attribute** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d163a-115">The **Attribute** object has these properties.</span></span>



| <span data-ttu-id="d163a-116">屬性</span><span class="sxs-lookup"><span data-stu-id="d163a-116">Property</span></span>                                    | <span data-ttu-id="d163a-117">存取類型</span><span class="sxs-lookup"><span data-stu-id="d163a-117">Access type</span></span>           | <span data-ttu-id="d163a-118">Description</span><span class="sxs-lookup"><span data-stu-id="d163a-118">Description</span></span>                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d163a-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="d163a-119">**Name**</span></span>](attribute-name.md)<br/>   | <span data-ttu-id="d163a-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d163a-120">Read/write</span></span><br/> | <span data-ttu-id="d163a-121">設定或抓取屬性的 CAPICOM 名稱。</span><span class="sxs-lookup"><span data-stu-id="d163a-121">Sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="d163a-122">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="d163a-122">This is the default property.</span></span><br/> |
| [<span data-ttu-id="d163a-123">**值**</span><span class="sxs-lookup"><span data-stu-id="d163a-123">**Value**</span></span>](attribute-value.md)<br/> | <span data-ttu-id="d163a-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d163a-124">Read/write</span></span><br/> | <span data-ttu-id="d163a-125">設定或抓取屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d163a-125">Sets or retrieves the value of the attribute.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="d163a-126">備註</span><span class="sxs-lookup"><span data-stu-id="d163a-126">Remarks</span></span>

<span data-ttu-id="d163a-127">您可以建立 **屬性** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="d163a-127">The **Attribute** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="d163a-128">**屬性** 物件的 PROGID 為 CAPICOM。屬性。1。</span><span class="sxs-lookup"><span data-stu-id="d163a-128">The ProgID for the **Attribute** object is CAPICOM.Attribute.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="d163a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d163a-129">Requirements</span></span>



| <span data-ttu-id="d163a-130">需求</span><span class="sxs-lookup"><span data-stu-id="d163a-130">Requirement</span></span> | <span data-ttu-id="d163a-131">值</span><span class="sxs-lookup"><span data-stu-id="d163a-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d163a-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d163a-132">End of client support</span></span><br/> | <span data-ttu-id="d163a-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d163a-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d163a-134">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d163a-134">End of server support</span></span><br/> | <span data-ttu-id="d163a-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d163a-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d163a-136">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d163a-136">Redistributable</span></span><br/>       | <span data-ttu-id="d163a-137">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d163a-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d163a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d163a-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d163a-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d163a-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d163a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d163a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d163a-141">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="d163a-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
