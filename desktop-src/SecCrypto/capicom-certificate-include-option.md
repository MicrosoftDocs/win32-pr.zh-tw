---
description: 定義要儲存鏈中的哪些憑證。
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: 'CAPICOM_CERTIFICATE_INCLUDE_OPTION 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997011"
---
# <a name="capicom_certificate_include_option-enumeration"></a><span data-ttu-id="d3f57-103">CAPICOM \_ 憑證 \_ 包含 \_ 選項列舉</span><span class="sxs-lookup"><span data-stu-id="d3f57-103">CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION enumeration</span></span>

<span data-ttu-id="d3f57-104">**CAPICOM \_ 憑證 \_ 包含 \_ 選項** 列舉型別會定義要儲存鏈中的哪些憑證。</span><span class="sxs-lookup"><span data-stu-id="d3f57-104">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type defines which certificates in a chain are saved.</span></span> <span data-ttu-id="d3f57-105">此列舉類型是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="d3f57-105">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="d3f57-106">成員</span><span class="sxs-lookup"><span data-stu-id="d3f57-106">Members</span></span>



| <span data-ttu-id="d3f57-107">member</span><span class="sxs-lookup"><span data-stu-id="d3f57-107">Member</span></span>                                                 | <span data-ttu-id="d3f57-108">描述</span><span class="sxs-lookup"><span data-stu-id="d3f57-108">Description</span></span>                                                                           | <span data-ttu-id="d3f57-109">值</span><span class="sxs-lookup"><span data-stu-id="d3f57-109">Value</span></span> |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="d3f57-110">**\_ \_ \_ \_ 除了 \_ 根以外的 CAPICOM 憑證包含鏈**</span><span class="sxs-lookup"><span data-stu-id="d3f57-110">**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</span></span> | <span data-ttu-id="d3f57-111">將所有憑證儲存在鏈中，但根實體除外。</span><span class="sxs-lookup"><span data-stu-id="d3f57-111">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> | <span data-ttu-id="d3f57-112">0</span><span class="sxs-lookup"><span data-stu-id="d3f57-112">0</span></span>     |
| <span data-ttu-id="d3f57-113">**CAPICOM \_ 憑證 \_ 包含 \_ 整個 \_ 鏈**</span><span class="sxs-lookup"><span data-stu-id="d3f57-113">**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</span></span>        | <span data-ttu-id="d3f57-114">儲存完整的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="d3f57-114">Saves the complete certificate chain.</span></span><br/>                                      | <span data-ttu-id="d3f57-115">1</span><span class="sxs-lookup"><span data-stu-id="d3f57-115">1</span></span>     |
| <span data-ttu-id="d3f57-116">**\_ \_ 僅限 CAPICOM 憑證包含 \_ 結束 \_ 實體 \_**</span><span class="sxs-lookup"><span data-stu-id="d3f57-116">**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</span></span>   | <span data-ttu-id="d3f57-117">只儲存終端實體憑證。</span><span class="sxs-lookup"><span data-stu-id="d3f57-117">Saves only the end entity certificate.</span></span><br/>                                     | <span data-ttu-id="d3f57-118">2</span><span class="sxs-lookup"><span data-stu-id="d3f57-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="d3f57-119">備註</span><span class="sxs-lookup"><span data-stu-id="d3f57-119">Remarks</span></span>

<span data-ttu-id="d3f57-120">[ **CAPICOM \_ 憑證 \_ 包含] \_ 選項** 列舉類型是由 [**CERTIFICATE. Save**](certificate-save.md) 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="d3f57-120">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f57-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3f57-121">Requirements</span></span>



| <span data-ttu-id="d3f57-122">需求</span><span class="sxs-lookup"><span data-stu-id="d3f57-122">Requirement</span></span> | <span data-ttu-id="d3f57-123">值</span><span class="sxs-lookup"><span data-stu-id="d3f57-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f57-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d3f57-124">Redistributable</span></span><br/> | <span data-ttu-id="d3f57-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d3f57-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="d3f57-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d3f57-126">Header</span></span><br/>          | <dl> <span data-ttu-id="d3f57-127"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="d3f57-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




