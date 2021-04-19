---
description: 定義包含憑證資訊之檔案的格式。
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: 'CAPICOM_CERTIFICATE_SAVE_AS_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989819"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a><span data-ttu-id="ebcfa-103">\_將 CAPICOM 憑證 \_ 儲存 \_ 為 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="ebcfa-103">CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="ebcfa-104">[ **CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型** ] 列舉類型會定義包含憑證資訊之檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="ebcfa-104">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificate information.</span></span> <span data-ttu-id="ebcfa-105">此列舉類型是由 CAPICOM 2.0 引進。</span><span class="sxs-lookup"><span data-stu-id="ebcfa-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="ebcfa-106">成員</span><span class="sxs-lookup"><span data-stu-id="ebcfa-106">Members</span></span>



| <span data-ttu-id="ebcfa-107">member</span><span class="sxs-lookup"><span data-stu-id="ebcfa-107">Member</span></span>                                  | <span data-ttu-id="ebcfa-108">描述</span><span class="sxs-lookup"><span data-stu-id="ebcfa-108">Description</span></span>                                                                                                                                   | <span data-ttu-id="ebcfa-109">值</span><span class="sxs-lookup"><span data-stu-id="ebcfa-109">Value</span></span> |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="ebcfa-110">**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX**</span><span class="sxs-lookup"><span data-stu-id="ebcfa-110">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</span></span> | <span data-ttu-id="ebcfa-111">輸出檔案將會格式化為 PFX (PKCS 12) 檔案，而且也會儲存任何可匯出的相關私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="ebcfa-111">The output file will be formatted as a PFX (PKCS 12) file and any associated private keys which are exportable will also be saved.</span></span><br/> | <span data-ttu-id="ebcfa-112">0</span><span class="sxs-lookup"><span data-stu-id="ebcfa-112">0</span></span>     |
| <span data-ttu-id="ebcfa-113">**\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ CER**</span><span class="sxs-lookup"><span data-stu-id="ebcfa-113">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</span></span> | <span data-ttu-id="ebcfa-114">輸出檔案將會格式化為 CER 檔案，且不會儲存任何私用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ebcfa-114">The output file will be formatted as a CER file with no private keys saved.</span></span><br/>                                                        | <span data-ttu-id="ebcfa-115">1</span><span class="sxs-lookup"><span data-stu-id="ebcfa-115">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="ebcfa-116">備註</span><span class="sxs-lookup"><span data-stu-id="ebcfa-116">Remarks</span></span>

<span data-ttu-id="ebcfa-117">[**憑證. save**](certificate-save.md)方法會使用 **CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型** 列舉類型。</span><span class="sxs-lookup"><span data-stu-id="ebcfa-117">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebcfa-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebcfa-118">Requirements</span></span>



| <span data-ttu-id="ebcfa-119">需求</span><span class="sxs-lookup"><span data-stu-id="ebcfa-119">Requirement</span></span> | <span data-ttu-id="ebcfa-120">值</span><span class="sxs-lookup"><span data-stu-id="ebcfa-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ebcfa-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ebcfa-121">Redistributable</span></span><br/> | <span data-ttu-id="ebcfa-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ebcfa-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="ebcfa-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ebcfa-123">Header</span></span><br/>          | <dl> <span data-ttu-id="ebcfa-124"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="ebcfa-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




