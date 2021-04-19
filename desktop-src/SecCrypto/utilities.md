---
description: 提供從 base64 產生亂數、轉換及編碼和解碼的功能。
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: 公用程式物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979520"
---
# <a name="utilities-object"></a><span data-ttu-id="30b8e-103">公用程式物件</span><span class="sxs-lookup"><span data-stu-id="30b8e-103">Utilities object</span></span>

<span data-ttu-id="30b8e-104">\[**公用程式** 物件可在 [需求] 區段中指定的作業系統中使用。\]</span><span class="sxs-lookup"><span data-stu-id="30b8e-104">\[The **Utilities** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="30b8e-105">**公用程式** 物件提供從 base64 產生亂數、轉換及編碼和解碼的功能。</span><span class="sxs-lookup"><span data-stu-id="30b8e-105">The **Utilities** object provides functionality for random number generation, conversions, and encoding and decoding from base64.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="30b8e-106">使用時機</span><span class="sxs-lookup"><span data-stu-id="30b8e-106">When to use</span></span>

<span data-ttu-id="30b8e-107">**公用程式** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="30b8e-107">The **Utilities** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="30b8e-108">以 base64 編碼字串，或從 base64 解碼字串。</span><span class="sxs-lookup"><span data-stu-id="30b8e-108">Encode a string as base64 or decode a string from base64.</span></span>
-   <span data-ttu-id="30b8e-109">將二進位壓縮的字串轉換成位元組陣列，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="30b8e-109">Convert a binary-packed string to a byte array and vice versa.</span></span>
-   <span data-ttu-id="30b8e-110">將二進位壓縮的字串轉換成十六進位字串，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="30b8e-110">Convert a binary-packed string to a hexadecimal string and vice versa.</span></span>
-   <span data-ttu-id="30b8e-111">產生安全的亂數字。</span><span class="sxs-lookup"><span data-stu-id="30b8e-111">Generate a secure random number.</span></span>
-   <span data-ttu-id="30b8e-112">將當地時間轉換為國際標準時間 (格林威治標準時間) ，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="30b8e-112">Convert local time to Coordinated Universal Time (Greenwich Mean Time) and vice versa.</span></span>

## <a name="members"></a><span data-ttu-id="30b8e-113">成員</span><span class="sxs-lookup"><span data-stu-id="30b8e-113">Members</span></span>

<span data-ttu-id="30b8e-114">**公用程式** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="30b8e-114">The **Utilities** object has these types of members:</span></span>

-   [<span data-ttu-id="30b8e-115">方法</span><span class="sxs-lookup"><span data-stu-id="30b8e-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="30b8e-116">方法</span><span class="sxs-lookup"><span data-stu-id="30b8e-116">Methods</span></span>

<span data-ttu-id="30b8e-117">**公用程式** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="30b8e-117">The **Utilities** object has these methods.</span></span>



| <span data-ttu-id="30b8e-118">方法</span><span class="sxs-lookup"><span data-stu-id="30b8e-118">Method</span></span>                                                               | <span data-ttu-id="30b8e-119">描述</span><span class="sxs-lookup"><span data-stu-id="30b8e-119">Description</span></span>                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="30b8e-120">**Base64Decode**</span><span class="sxs-lookup"><span data-stu-id="30b8e-120">**Base64Decode**</span></span>](utilities-base64decode.md)                       | <span data-ttu-id="30b8e-121">從 base64 解碼字串。</span><span class="sxs-lookup"><span data-stu-id="30b8e-121">Decodes a string from base64.</span></span><br/>                                     |
| [<span data-ttu-id="30b8e-122">**Base64Encode**</span><span class="sxs-lookup"><span data-stu-id="30b8e-122">**Base64Encode**</span></span>](utilities-base64encode.md)                       | <span data-ttu-id="30b8e-123">以 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="30b8e-123">Encodes a string as base64.</span></span><br/>                                       |
| [<span data-ttu-id="30b8e-124">**BinaryStringToByteArray**</span><span class="sxs-lookup"><span data-stu-id="30b8e-124">**BinaryStringToByteArray**</span></span>](utilities-binarystringtobytearray.md) | <span data-ttu-id="30b8e-125">將二進位壓縮的字串轉換成位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="30b8e-125">Converts a binary-packed string to an array of bytes.</span></span><br/>             |
| [<span data-ttu-id="30b8e-126">**BinaryToHex**</span><span class="sxs-lookup"><span data-stu-id="30b8e-126">**BinaryToHex**</span></span>](utilities-binarytohex.md)                         | <span data-ttu-id="30b8e-127">將二進位壓縮的字串轉換成十六進位字串。</span><span class="sxs-lookup"><span data-stu-id="30b8e-127">Converts a binary-packed string to a hexadecimal string.</span></span><br/>          |
| [<span data-ttu-id="30b8e-128">**ByteArrayToBinaryString**</span><span class="sxs-lookup"><span data-stu-id="30b8e-128">**ByteArrayToBinaryString**</span></span>](utilities-bytearraytobinarystring.md) | <span data-ttu-id="30b8e-129">將位元組陣列轉換為二進位壓縮的字串。</span><span class="sxs-lookup"><span data-stu-id="30b8e-129">Converts an array of bytes to a binary-packed string.</span></span><br/>             |
| [<span data-ttu-id="30b8e-130">**GetRandom**</span><span class="sxs-lookup"><span data-stu-id="30b8e-130">**GetRandom**</span></span>](utilities-getrandom.md)                             | <span data-ttu-id="30b8e-131">產生安全的亂數字。</span><span class="sxs-lookup"><span data-stu-id="30b8e-131">Generates a secure random number.</span></span><br/>                                 |
| [<span data-ttu-id="30b8e-132">**HexToBinary**</span><span class="sxs-lookup"><span data-stu-id="30b8e-132">**HexToBinary**</span></span>](utilities-hextobinary.md)                         | <span data-ttu-id="30b8e-133">將十六進位字串轉換為二進位壓縮的字串。</span><span class="sxs-lookup"><span data-stu-id="30b8e-133">Converts a hexadecimal string to a binary-packed string.</span></span><br/>          |
| [<span data-ttu-id="30b8e-134">**LocalTimeToUTCTime**</span><span class="sxs-lookup"><span data-stu-id="30b8e-134">**LocalTimeToUTCTime**</span></span>](utilities-localtimetoutctime.md)           | <span data-ttu-id="30b8e-135">將電腦的當地時間轉換成國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="30b8e-135">Converts the computer's local time to Coordinated Universal Time.</span></span><br/> |
| [<span data-ttu-id="30b8e-136">**UTCTimeToLocalTime**</span><span class="sxs-lookup"><span data-stu-id="30b8e-136">**UTCTimeToLocalTime**</span></span>](utilities-utctimetolocaltime.md)           | <span data-ttu-id="30b8e-137">將國際標準時間轉換為電腦的本地時間。</span><span class="sxs-lookup"><span data-stu-id="30b8e-137">Converts Coordinated Universal Time to the computer's local time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30b8e-138">備註</span><span class="sxs-lookup"><span data-stu-id="30b8e-138">Remarks</span></span>

<span data-ttu-id="30b8e-139">您可以建立 **公用程式** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="30b8e-139">The **Utilities** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="30b8e-140">**公用程式** 物件的 PROGID 為 CAPICOM。公用事業。1。</span><span class="sxs-lookup"><span data-stu-id="30b8e-140">The ProgID for the **Utilities** object is CAPICOM.Utilities.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b8e-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="30b8e-141">Requirements</span></span>



| <span data-ttu-id="30b8e-142">需求</span><span class="sxs-lookup"><span data-stu-id="30b8e-142">Requirement</span></span> | <span data-ttu-id="30b8e-143">值</span><span class="sxs-lookup"><span data-stu-id="30b8e-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30b8e-144">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="30b8e-144">Redistributable</span></span><br/> | <span data-ttu-id="30b8e-145">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="30b8e-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="30b8e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="30b8e-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="30b8e-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30b8e-147"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




