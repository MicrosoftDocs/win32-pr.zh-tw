---
description: 定義與簽章相關聯的屬性類型。
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: 'CAPICOM_ATTRIBUTE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: b03f91d0737b29b98adeb7e6a56bf9eccd35cc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990779"
---
# <a name="capicom_attribute-enumeration"></a><span data-ttu-id="9ed83-103">CAPICOM \_ 屬性列舉</span><span class="sxs-lookup"><span data-stu-id="9ed83-103">CAPICOM\_ATTRIBUTE enumeration</span></span>

<span data-ttu-id="9ed83-104">**CAPICOM \_ 屬性** 列舉型別會定義與簽章相關 [*聯的屬性類型。*](../secgloss/d-gly.md)</span><span class="sxs-lookup"><span data-stu-id="9ed83-104">The **CAPICOM\_ATTRIBUTE** enumeration type defines the kind of attribute associated with a [*signature*](../secgloss/d-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="9ed83-105">成員</span><span class="sxs-lookup"><span data-stu-id="9ed83-105">Members</span></span>



| <span data-ttu-id="9ed83-106">member</span><span class="sxs-lookup"><span data-stu-id="9ed83-106">Member</span></span>                                                       | <span data-ttu-id="9ed83-107">描述</span><span class="sxs-lookup"><span data-stu-id="9ed83-107">Description</span></span>                                                                | <span data-ttu-id="9ed83-108">值</span><span class="sxs-lookup"><span data-stu-id="9ed83-108">Value</span></span> |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| <span data-ttu-id="9ed83-109">**CAPICOM \_ 驗證 \_ 屬性 \_ 簽署 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="9ed83-109">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</span></span>         | <span data-ttu-id="9ed83-110">屬性包含建立簽章的時間。</span><span class="sxs-lookup"><span data-stu-id="9ed83-110">The attribute contains the time that the signature was created.</span></span><br/> | <span data-ttu-id="9ed83-111">0</span><span class="sxs-lookup"><span data-stu-id="9ed83-111">0</span></span>     |
| <span data-ttu-id="9ed83-112">**CAPICOM \_ 驗證的 \_ 屬性 \_ 檔 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="9ed83-112">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</span></span>        | <span data-ttu-id="9ed83-113">屬性包含已簽署檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ed83-113">The attribute contains the name of the signed document.</span></span><br/>         | <span data-ttu-id="9ed83-114">1</span><span class="sxs-lookup"><span data-stu-id="9ed83-114">1</span></span>     |
| <span data-ttu-id="9ed83-115">**CAPICOM \_ 驗證的 \_ 屬性 \_ 檔 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="9ed83-115">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</span></span> | <span data-ttu-id="9ed83-116">屬性包含已簽署檔的描述。</span><span class="sxs-lookup"><span data-stu-id="9ed83-116">The attribute contains a description of the signed document.</span></span><br/>    | <span data-ttu-id="9ed83-117">2</span><span class="sxs-lookup"><span data-stu-id="9ed83-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="9ed83-118">備註</span><span class="sxs-lookup"><span data-stu-id="9ed83-118">Remarks</span></span>

<span data-ttu-id="9ed83-119">**CAPICOM \_ 屬性** 列舉類型是由 [**Attribute.Name**](attribute-name.md)屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="9ed83-119">The **CAPICOM\_ATTRIBUTE** enumeration type is used by the [**Attribute.Name**](attribute-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed83-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ed83-120">Requirements</span></span>



| <span data-ttu-id="9ed83-121">需求</span><span class="sxs-lookup"><span data-stu-id="9ed83-121">Requirement</span></span> | <span data-ttu-id="9ed83-122">值</span><span class="sxs-lookup"><span data-stu-id="9ed83-122">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed83-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9ed83-123">Redistributable</span></span><br/> | <span data-ttu-id="9ed83-124">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9ed83-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="9ed83-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9ed83-125">Header</span></span><br/>          | <dl> <span data-ttu-id="9ed83-126"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="9ed83-126"><dt>Capicom.h</dt></span></span> </dl> |



 

 
