---
description: 指出使用的編碼類型。
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: 'CAPICOM_ENCODING_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999486"
---
# <a name="capicom_encoding_type-enumeration"></a><span data-ttu-id="7a91d-103">CAPICOM \_ 編碼 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="7a91d-103">CAPICOM\_ENCODING\_TYPE enumeration</span></span>

<span data-ttu-id="7a91d-104">**CAPICOM \_ 編碼 \_ 類型** 列舉類型指出使用的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="7a91d-104">The **CAPICOM\_ENCODING\_TYPE** enumeration type indicates the encoding type used.</span></span>

## <a name="members"></a><span data-ttu-id="7a91d-105">成員</span><span class="sxs-lookup"><span data-stu-id="7a91d-105">Members</span></span>



| <span data-ttu-id="7a91d-106">member</span><span class="sxs-lookup"><span data-stu-id="7a91d-106">Member</span></span>                      | <span data-ttu-id="7a91d-107">描述</span><span class="sxs-lookup"><span data-stu-id="7a91d-107">Description</span></span>                                                                                                                                                                                 | <span data-ttu-id="7a91d-108">值</span><span class="sxs-lookup"><span data-stu-id="7a91d-108">Value</span></span>      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="7a91d-109">**CAPICOM \_ 編碼 \_ 任何**</span><span class="sxs-lookup"><span data-stu-id="7a91d-109">**CAPICOM\_ENCODE\_ANY**</span></span>    | <span data-ttu-id="7a91d-110">資料會儲存為 base64 編碼字串或純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="7a91d-110">Data is saved as a base64-encoded string or a pure binary sequence.</span></span> <span data-ttu-id="7a91d-111">此編碼類型只用于具有未知編碼類型的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="7a91d-111">This encoding type is used only for input data that has an unknown encoding type.</span></span> <span data-ttu-id="7a91d-112">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="7a91d-112">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="7a91d-113">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="7a91d-113">0xffffffff</span></span> |
| <span data-ttu-id="7a91d-114">**CAPICOM \_ 編碼 \_ BASE64**</span><span class="sxs-lookup"><span data-stu-id="7a91d-114">**CAPICOM\_ENCODE\_BASE64**</span></span> | <span data-ttu-id="7a91d-115">資料會儲存為 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="7a91d-115">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                        | <span data-ttu-id="7a91d-116">0</span><span class="sxs-lookup"><span data-stu-id="7a91d-116">0</span></span>          |
| <span data-ttu-id="7a91d-117">**CAPICOM \_ 編碼 \_ 二進位**</span><span class="sxs-lookup"><span data-stu-id="7a91d-117">**CAPICOM\_ENCODE\_BINARY**</span></span> | <span data-ttu-id="7a91d-118">資料會儲存為純二進位序列。</span><span class="sxs-lookup"><span data-stu-id="7a91d-118">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                         | <span data-ttu-id="7a91d-119">1</span><span class="sxs-lookup"><span data-stu-id="7a91d-119">1</span></span>          |



## <a name="remarks"></a><span data-ttu-id="7a91d-120">備註</span><span class="sxs-lookup"><span data-stu-id="7a91d-120">Remarks</span></span>

<span data-ttu-id="7a91d-121">下列 CAPICOM 方法和屬性會使用這個列舉類型：</span><span class="sxs-lookup"><span data-stu-id="7a91d-121">This enumeration type is used by the following CAPICOM methods and properties:</span></span>

-   <span data-ttu-id="7a91d-122">[**Certificate. Export**](certificate-export.md) 方法</span><span class="sxs-lookup"><span data-stu-id="7a91d-122">[**Certificate.Export**](certificate-export.md) method</span></span>
-   <span data-ttu-id="7a91d-123">[**EncodedData。 Value**](encodeddata-value.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="7a91d-123">[**EncodedData.Value**](encodeddata-value.md) property</span></span>
-   <span data-ttu-id="7a91d-124">[**A**](encrypteddata-encrypt.md) 方法</span><span class="sxs-lookup"><span data-stu-id="7a91d-124">[**EncryptedData.Encrypt**](encrypteddata-encrypt.md) method</span></span>
-   <span data-ttu-id="7a91d-125">[**EnvelopedData**](envelopeddata-encrypt.md) 方法</span><span class="sxs-lookup"><span data-stu-id="7a91d-125">[**EnvelopedData.Encrypt**](envelopeddata-encrypt.md) method</span></span>
-   <span data-ttu-id="7a91d-126">[**ExtendedProperty。 Value**](extendedproperty-value.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="7a91d-126">[**ExtendedProperty.Value**](extendedproperty-value.md) property</span></span>
-   <span data-ttu-id="7a91d-127">[**SignedData. Sign**](signeddata-sign.md) 方法</span><span class="sxs-lookup"><span data-stu-id="7a91d-127">[**SignedData.Sign**](signeddata-sign.md) method</span></span>
-   <span data-ttu-id="7a91d-128">[**SignedData. CoSign**](signeddata-cosign.md) 方法</span><span class="sxs-lookup"><span data-stu-id="7a91d-128">[**SignedData.CoSign**](signeddata-cosign.md) method</span></span>
-   <span data-ttu-id="7a91d-129">[**Store. Export**](store-export.md) 方法</span><span class="sxs-lookup"><span data-stu-id="7a91d-129">[**Store.Export**](store-export.md) method</span></span>
-   <span data-ttu-id="7a91d-130">[**GetRandom**](utilities-getrandom.md) 方法</span><span class="sxs-lookup"><span data-stu-id="7a91d-130">[**Utilities.GetRandom**](utilities-getrandom.md) method</span></span>

## <a name="requirements"></a><span data-ttu-id="7a91d-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a91d-131">Requirements</span></span>



| <span data-ttu-id="7a91d-132">需求</span><span class="sxs-lookup"><span data-stu-id="7a91d-132">Requirement</span></span> | <span data-ttu-id="7a91d-133">值</span><span class="sxs-lookup"><span data-stu-id="7a91d-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a91d-134">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7a91d-134">Redistributable</span></span><br/> | <span data-ttu-id="7a91d-135">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7a91d-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="7a91d-136">標頭</span><span class="sxs-lookup"><span data-stu-id="7a91d-136">Header</span></span><br/>          | <dl> <span data-ttu-id="7a91d-137"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="7a91d-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 




