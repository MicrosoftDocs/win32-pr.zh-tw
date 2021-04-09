---
title: 'WINBIO_IDENTITY_TYPE 常數 (Winbio \_ 類型 .h) '
description: 指定 WINBIO 身分識別結構中所包含之身分識別資訊的格式 \_ 。
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934149"
---
# <a name="winbio_identity_type-constants"></a><span data-ttu-id="00317-103">WINBIO 身分 \_ 識別 \_ 類型常數</span><span class="sxs-lookup"><span data-stu-id="00317-103">WINBIO\_IDENTITY\_TYPE Constants</span></span>

<span data-ttu-id="00317-104">下列 **WINBIO \_ 識別 \_ 類型** 常數可用來指定 WINBIO 身分 [**\_ 識別**](winbio-identity.md) 結構中所包含之身分識別資訊的格式。</span><span class="sxs-lookup"><span data-stu-id="00317-104">The following **WINBIO\_IDENTITY\_TYPE** constants can be used to specify the format of the identity information contained in the [**WINBIO\_IDENTITY**](winbio-identity.md) structure.</span></span>



| <span data-ttu-id="00317-105">常數</span><span class="sxs-lookup"><span data-stu-id="00317-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="00317-106">描述</span><span class="sxs-lookup"><span data-stu-id="00317-106">Description</span></span>                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="00317-107"><dt>**WINBIO \_ 識別碼 \_ 類型 \_ Null**</dt></span><span class="sxs-lookup"><span data-stu-id="00317-107"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="00317-108">範本沒有相關聯的識別碼。</span><span class="sxs-lookup"><span data-stu-id="00317-108">The template has no associated ID.</span></span> <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="00317-109"><dt>**WINBIO \_ ID \_ 類型 \_ 萬用字元**</dt></span><span class="sxs-lookup"><span data-stu-id="00317-109"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="00317-110">結構符合所有範本識別。</span><span class="sxs-lookup"><span data-stu-id="00317-110">The structure matches all template identities.</span></span><br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="00317-111"><dt>**WINBIO \_ 識別碼 \_ 類型 \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="00317-111"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="00317-112">GUID 可識別範本。</span><span class="sxs-lookup"><span data-stu-id="00317-112">A GUID identifies the template.</span></span><br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="00317-113"><dt>**WINBIO \_ 識別碼 \_ 類型 \_ SID**</dt></span><span class="sxs-lookup"><span data-stu-id="00317-113"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="00317-114">帳戶 SID 會識別範本。</span><span class="sxs-lookup"><span data-stu-id="00317-114">An account SID identifies the template.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="00317-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="00317-115">Requirements</span></span>



| <span data-ttu-id="00317-116">需求</span><span class="sxs-lookup"><span data-stu-id="00317-116">Requirement</span></span> | <span data-ttu-id="00317-117">值</span><span class="sxs-lookup"><span data-stu-id="00317-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00317-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00317-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00317-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00317-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="00317-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00317-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00317-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00317-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="00317-122">標頭</span><span class="sxs-lookup"><span data-stu-id="00317-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00317-123"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="00317-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00317-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00317-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00317-125">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="00317-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="00317-126">**WINBIO 身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="00317-126">**WINBIO\_IDENTITY**</span></span>](winbio-identity.md)
</dt> </dl>

 

 





