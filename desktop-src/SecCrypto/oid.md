---
description: 代表數個 CAPICOM 屬性所使用 (OID) 的物件識別碼。
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: OID 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994908"
---
# <a name="oid-object"></a><span data-ttu-id="b43a8-103">OID 物件</span><span class="sxs-lookup"><span data-stu-id="b43a8-103">OID object</span></span>

<span data-ttu-id="b43a8-104">\[**OID** 物件可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="b43a8-104">\[The **OID** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b43a8-105">相反地，請在 [**system.object**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)命名空間中使用 [**Oid 類別**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="b43a8-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b43a8-106">**Oid** 物件代表數個 CAPICOM 屬性所使用 (OID) 的 [*物件識別碼*](../secgloss/o-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b43a8-106">The **OID** object represents an [*object identifier*](../secgloss/o-gly.md) (OID) that is used by several CAPICOM properties.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b43a8-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="b43a8-107">When to use</span></span>

<span data-ttu-id="b43a8-108">**OID** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="b43a8-108">The **OID** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b43a8-109">設定或取得 OID 名稱和 OID 的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b43a8-109">Set or retrieve a CAPICOM name and display name for the OID.</span></span>
-   <span data-ttu-id="b43a8-110">設定或取出 OID 的點號。</span><span class="sxs-lookup"><span data-stu-id="b43a8-110">Set or retrieve the dotted number for the OID.</span></span>

## <a name="members"></a><span data-ttu-id="b43a8-111">成員</span><span class="sxs-lookup"><span data-stu-id="b43a8-111">Members</span></span>

<span data-ttu-id="b43a8-112">**OID** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b43a8-112">The **OID** object has these types of members:</span></span>

-   [<span data-ttu-id="b43a8-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b43a8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b43a8-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b43a8-114">Properties</span></span>

<span data-ttu-id="b43a8-115">**OID** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b43a8-115">The **OID** object has these properties.</span></span>



| <span data-ttu-id="b43a8-116">屬性</span><span class="sxs-lookup"><span data-stu-id="b43a8-116">Property</span></span>                                            | <span data-ttu-id="b43a8-117">存取類型</span><span class="sxs-lookup"><span data-stu-id="b43a8-117">Access type</span></span>           | <span data-ttu-id="b43a8-118">Description</span><span class="sxs-lookup"><span data-stu-id="b43a8-118">Description</span></span>                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b43a8-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="b43a8-119">**FriendlyName**</span></span>](oid-friendlyname.md)<br/> | <span data-ttu-id="b43a8-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b43a8-120">Read/write</span></span><br/> | <span data-ttu-id="b43a8-121">設定或抓取 OID 的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b43a8-121">Sets or retrieves the display name for the OID.</span></span><br/>                                       |
| [<span data-ttu-id="b43a8-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="b43a8-122">**Name**</span></span>](oid-name.md)<br/>                 | <span data-ttu-id="b43a8-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b43a8-123">Read/write</span></span><br/> | <span data-ttu-id="b43a8-124">為 OID 設定或抓取 CAPICOM 定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="b43a8-124">Sets or retrieves the CAPICOM-defined name for the OID.</span></span> <span data-ttu-id="b43a8-125">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="b43a8-125">This is the default property.</span></span><br/> |
| [<span data-ttu-id="b43a8-126">**值**</span><span class="sxs-lookup"><span data-stu-id="b43a8-126">**Value**</span></span>](oid-value.md)<br/>               | <span data-ttu-id="b43a8-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b43a8-127">Read/write</span></span><br/> | <span data-ttu-id="b43a8-128">設定或抓取 OID 的 OID 點值。</span><span class="sxs-lookup"><span data-stu-id="b43a8-128">Sets or retrieves the value of the OID dotted number of the OID.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="b43a8-129">備註</span><span class="sxs-lookup"><span data-stu-id="b43a8-129">Remarks</span></span>

<span data-ttu-id="b43a8-130">您可以建立 **OID** 物件，並且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="b43a8-130">The **OID** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="b43a8-131">**OID** 物件的 PROGID 是 CAPICOM。OID. 1。</span><span class="sxs-lookup"><span data-stu-id="b43a8-131">The ProgID for the **OID** object is CAPICOM.OID.1.</span></span>

<span data-ttu-id="b43a8-132">下列的 CAPICOM 物件屬性會傳回 **OID** 物件：</span><span class="sxs-lookup"><span data-stu-id="b43a8-132">The following CAPICOM object properties return an **OID** object:</span></span>

-   [<span data-ttu-id="b43a8-133">**PolicyInformation OID**</span><span class="sxs-lookup"><span data-stu-id="b43a8-133">**PolicyInformation.OID**</span></span>](policyinformation-oid.md)
-   [<span data-ttu-id="b43a8-134">**限定詞。 OID**</span><span class="sxs-lookup"><span data-stu-id="b43a8-134">**Qualifier.OID**</span></span>](qualifier-oid.md)
-   [<span data-ttu-id="b43a8-135">**副檔名 OID**</span><span class="sxs-lookup"><span data-stu-id="b43a8-135">**Extension.OID**</span></span>](extension-oid.md)
-   [<span data-ttu-id="b43a8-136">**範本 OID**</span><span class="sxs-lookup"><span data-stu-id="b43a8-136">**Template.OID**</span></span>](template-oid.md)

## <a name="requirements"></a><span data-ttu-id="b43a8-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="b43a8-137">Requirements</span></span>



| <span data-ttu-id="b43a8-138">需求</span><span class="sxs-lookup"><span data-stu-id="b43a8-138">Requirement</span></span> | <span data-ttu-id="b43a8-139">值</span><span class="sxs-lookup"><span data-stu-id="b43a8-139">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b43a8-140">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b43a8-140">Redistributable</span></span><br/> | <span data-ttu-id="b43a8-141">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b43a8-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b43a8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b43a8-142">DLL</span></span><br/>             | <dl> <span data-ttu-id="b43a8-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b43a8-143"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
