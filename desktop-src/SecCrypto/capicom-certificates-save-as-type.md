---
description: 定義包含憑證資訊之檔案的格式。
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: 'CAPICOM_CERTIFICATES_SAVE_AS_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994704"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a><span data-ttu-id="b2936-103">\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="b2936-103">CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="b2936-104">[ **CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型** ] 列舉類型會定義包含憑證資訊之檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="b2936-104">The **CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificates information.</span></span> <span data-ttu-id="b2936-105">此列舉類型是由 CAPICOM 2.0 引進。</span><span class="sxs-lookup"><span data-stu-id="b2936-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="b2936-106">成員</span><span class="sxs-lookup"><span data-stu-id="b2936-106">Members</span></span>



| <span data-ttu-id="b2936-107">member</span><span class="sxs-lookup"><span data-stu-id="b2936-107">Member</span></span>                                          | <span data-ttu-id="b2936-108">描述</span><span class="sxs-lookup"><span data-stu-id="b2936-108">Description</span></span>                                          | <span data-ttu-id="b2936-109">值</span><span class="sxs-lookup"><span data-stu-id="b2936-109">Value</span></span> |
|-------------------------------------------------|------------------------------------------------------|-------|
| <span data-ttu-id="b2936-110">**\_將 CAPICOM 憑證 \_ 另存為已 \_ \_ 序列化**</span><span class="sxs-lookup"><span data-stu-id="b2936-110">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</span></span> | <span data-ttu-id="b2936-111">已儲存的憑證會進行序列化。</span><span class="sxs-lookup"><span data-stu-id="b2936-111">The saved certificates are serialized.</span></span><br/>    | <span data-ttu-id="b2936-112">0</span><span class="sxs-lookup"><span data-stu-id="b2936-112">0</span></span>     |
| <span data-ttu-id="b2936-113">**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PKCS7**</span><span class="sxs-lookup"><span data-stu-id="b2936-113">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</span></span>      | <span data-ttu-id="b2936-114">憑證會儲存為 PKCS \# 7。</span><span class="sxs-lookup"><span data-stu-id="b2936-114">The certificates are saved as a PKCS \#7.</span></span><br/> | <span data-ttu-id="b2936-115">1</span><span class="sxs-lookup"><span data-stu-id="b2936-115">1</span></span>     |
| <span data-ttu-id="b2936-116">**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX**</span><span class="sxs-lookup"><span data-stu-id="b2936-116">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</span></span>        | <span data-ttu-id="b2936-117">憑證會儲存為 PFX。</span><span class="sxs-lookup"><span data-stu-id="b2936-117">The certificates are saved as a PFX.</span></span><br/>      | <span data-ttu-id="b2936-118">2</span><span class="sxs-lookup"><span data-stu-id="b2936-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="b2936-119">備註</span><span class="sxs-lookup"><span data-stu-id="b2936-119">Remarks</span></span>

<span data-ttu-id="b2936-120">憑證所 \_ 使用的 CAPICOM 憑證 \_ 儲存 \_ 為 \_ 類型列舉類型。 [**儲存**](certificates-save.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b2936-120">The CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration type is used by the [**Certificates.Save**](certificates-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2936-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2936-121">Requirements</span></span>



| <span data-ttu-id="b2936-122">需求</span><span class="sxs-lookup"><span data-stu-id="b2936-122">Requirement</span></span> | <span data-ttu-id="b2936-123">值</span><span class="sxs-lookup"><span data-stu-id="b2936-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2936-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b2936-124">Redistributable</span></span><br/> | <span data-ttu-id="b2936-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b2936-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b2936-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b2936-126">Header</span></span><br/>          | <dl> <span data-ttu-id="b2936-127"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="b2936-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




