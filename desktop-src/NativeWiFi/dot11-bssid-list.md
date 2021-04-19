---
description: 包含基本服務集 (BSS) 識別碼的清單。
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: 'DOT11_BSSID_LIST 結構 (Windot11 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977998"
---
# <a name="dot11_bssid_list-structure"></a><span data-ttu-id="f9bb6-103">DOT11 \_ BSSID \_ 清單結構</span><span class="sxs-lookup"><span data-stu-id="f9bb6-103">DOT11\_BSSID\_LIST structure</span></span>

<span data-ttu-id="f9bb6-104">**DOT11 \_ BSSID \_ 清單** 結構包含基本服務集 (BSS) 識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="f9bb6-104">The **DOT11\_BSSID\_LIST** structure contains a list of basic service set (BSS) identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9bb6-105">語法</span><span class="sxs-lookup"><span data-stu-id="f9bb6-105">Syntax</span></span>


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a><span data-ttu-id="f9bb6-106">成員</span><span class="sxs-lookup"><span data-stu-id="f9bb6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9bb6-107">**標頭**</span><span class="sxs-lookup"><span data-stu-id="f9bb6-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="f9bb6-108">[**Ndis \_ 物件 \_ 標頭**](ndis-object-header.md)結構，包含 ndis 結構的類型、版本和大小資訊。</span><span class="sxs-lookup"><span data-stu-id="f9bb6-108">An [**NDIS\_OBJECT\_HEADER**](ndis-object-header.md) structure that contains the type, version, and, size information of an NDIS structure.</span></span> <span data-ttu-id="f9bb6-109">對於大部分的 **DOT11 \_ BSSID \_ 清單** 結構，請 **將類型** 成員設定為 **NDIS \_ 物件 \_ 類型 \_ 預設值**、將 **修訂** 成員設定為 **DOT11 \_ BSSID \_ 清單 \_ 修訂版 \_ 1**，然後將 **Size** 成員設為 **sizeof (DOT11 \_ BSSID \_ 清單)**。</span><span class="sxs-lookup"><span data-stu-id="f9bb6-109">For most **DOT11\_BSSID\_LIST** structures, set the **Type** member to **NDIS\_OBJECT\_TYPE\_DEFAULT**, set the **Revision** member to **DOT11\_BSSID\_LIST\_REVISION\_1**, and set the **Size** member to **sizeof(DOT11\_BSSID\_LIST)**.</span></span>

</dd> <dt>

<span data-ttu-id="f9bb6-110">**uNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="f9bb6-110">**uNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="f9bb6-111">此結構中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f9bb6-111">The number of entries in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9bb6-112">**uTotalNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="f9bb6-112">**uTotalNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="f9bb6-113">支援的專案總數。</span><span class="sxs-lookup"><span data-stu-id="f9bb6-113">The total number of entries supported.</span></span>

</dd> <dt>

<span data-ttu-id="f9bb6-114">**BSSIDs**</span><span class="sxs-lookup"><span data-stu-id="f9bb6-114">**BSSIDs**</span></span>
</dt> <dd>

<span data-ttu-id="f9bb6-115">BSS 識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="f9bb6-115">A list of BSS identifiers.</span></span> <span data-ttu-id="f9bb6-116">BSS 識別碼會儲存為 [**DOT11 \_ MAC \_ 位址**](dot11-mac-address-type.md) 類型。</span><span class="sxs-lookup"><span data-stu-id="f9bb6-116">A BSS identifier is stored as a [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9bb6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9bb6-117">Requirements</span></span>



| <span data-ttu-id="f9bb6-118">需求</span><span class="sxs-lookup"><span data-stu-id="f9bb6-118">Requirement</span></span> | <span data-ttu-id="f9bb6-119">值</span><span class="sxs-lookup"><span data-stu-id="f9bb6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9bb6-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9bb6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9bb6-121">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9bb6-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9bb6-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9bb6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9bb6-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9bb6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f9bb6-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f9bb6-124">Redistributable</span></span><br/>          | <span data-ttu-id="f9bb6-125">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="f9bb6-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="f9bb6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f9bb6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9bb6-127"><dt>Windot11 (包含 Windot11) </dt></span><span class="sxs-lookup"><span data-stu-id="f9bb6-127"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9bb6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9bb6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9bb6-129">**WLAN \_ 連接 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="f9bb6-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




