---
description: 封裝許多 NDIS 6.0 結構中所需的物件類型、版本和大小資訊。
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: 'NDIS_OBJECT_HEADER 結構 (Ntddndis .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983482"
---
# <a name="ndis_object_header-structure"></a><span data-ttu-id="99f42-103">NDIS \_ 物件 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="99f42-103">NDIS\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="99f42-104">**Ndis \_ 物件 \_ 標頭** 結構會封裝許多 NDIS 6.0 結構中所需的物件類型、版本和大小資訊。</span><span class="sxs-lookup"><span data-stu-id="99f42-104">The **NDIS\_OBJECT\_HEADER** structure packages the object type, version, and size information that is required in many NDIS 6.0 structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f42-105">語法</span><span class="sxs-lookup"><span data-stu-id="99f42-105">Syntax</span></span>


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="99f42-106">成員</span><span class="sxs-lookup"><span data-stu-id="99f42-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="99f42-107">**型別**</span><span class="sxs-lookup"><span data-stu-id="99f42-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="99f42-108">指定結構所描述之 NDIS 物件的型別。</span><span class="sxs-lookup"><span data-stu-id="99f42-108">Specifies the type of NDIS object that a structure describes.</span></span>

</dd> <dt>

<span data-ttu-id="99f42-109">**修訂**</span><span class="sxs-lookup"><span data-stu-id="99f42-109">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="99f42-110">指定此結構的修訂編號。</span><span class="sxs-lookup"><span data-stu-id="99f42-110">Specifies the revision number of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="99f42-111">**大小**</span><span class="sxs-lookup"><span data-stu-id="99f42-111">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="99f42-112">指定包含 **ndis \_ 物件 \_ 標頭** 之 ndis 結構的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="99f42-112">Specifies the total size, in bytes, of the NDIS structure that contains the **NDIS\_OBJECT\_HEADER**.</span></span> <span data-ttu-id="99f42-113">此大小包含 **NDIS \_ 物件 \_ 標頭** 成員的大小，以及結構的所有其他成員。</span><span class="sxs-lookup"><span data-stu-id="99f42-113">This size includes the size of the **NDIS\_OBJECT\_HEADER** member and all other members of the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99f42-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="99f42-114">Requirements</span></span>



| <span data-ttu-id="99f42-115">需求</span><span class="sxs-lookup"><span data-stu-id="99f42-115">Requirement</span></span> | <span data-ttu-id="99f42-116">值</span><span class="sxs-lookup"><span data-stu-id="99f42-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99f42-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99f42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="99f42-118">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99f42-118">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99f42-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99f42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="99f42-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99f42-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="99f42-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="99f42-121">Redistributable</span></span><br/>          | <span data-ttu-id="99f42-122">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="99f42-122">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="99f42-123">標頭</span><span class="sxs-lookup"><span data-stu-id="99f42-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="99f42-124"><dt>Ntddndis (包含 Windot11) </dt></span><span class="sxs-lookup"><span data-stu-id="99f42-124"><dt>Ntddndis.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99f42-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99f42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f42-126">**DOT11 \_ BSSID \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="99f42-126">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> </dl>

 

 




