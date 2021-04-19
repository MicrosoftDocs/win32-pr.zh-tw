---
description: 定義基本服務集 (BSS) 網路類型。
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: 'DOT11_BSS_TYPE 列舉 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 7815e75f3ef7ef8d908b7d2b26f2e5f9d3630009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982491"
---
# <a name="dot11_bss_type-enumeration"></a><span data-ttu-id="9712d-103">DOT11 \_ BSS \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="9712d-103">DOT11\_BSS\_TYPE enumeration</span></span>

<span data-ttu-id="9712d-104">**DOT11 \_ bss \_ 型** 別列舉型別會定義基本的服務集 (BSS) 網路類型。</span><span class="sxs-lookup"><span data-stu-id="9712d-104">The **DOT11\_BSS\_TYPE** enumerated type defines a basic service set (BSS) network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9712d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9712d-105">Syntax</span></span>


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="9712d-106">常數</span><span class="sxs-lookup"><span data-stu-id="9712d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9712d-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11 \_ BSS \_ 類型 \_ 基礎結構**</span><span class="sxs-lookup"><span data-stu-id="9712d-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11\_BSS\_type\_infrastructure**</span></span>
</dt> <dd>

<span data-ttu-id="9712d-108">指定基礎結構 BSS 網路。</span><span class="sxs-lookup"><span data-stu-id="9712d-108">Specifies an infrastructure BSS network.</span></span>

</dd> <dt>

<span data-ttu-id="9712d-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**\_獨立 dot11 BSS \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="9712d-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11\_BSS\_type\_independent**</span></span>
</dt> <dd>

<span data-ttu-id="9712d-110">指定獨立的 BSS (IBSS) 網路。</span><span class="sxs-lookup"><span data-stu-id="9712d-110">Specifies an independent BSS (IBSS) network.</span></span>

</dd> <dt>

<span data-ttu-id="9712d-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11 \_ BSS \_ 類型 \_ any**</span><span class="sxs-lookup"><span data-stu-id="9712d-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11\_BSS\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="9712d-112">指定基礎結構或 IBSS 網路。</span><span class="sxs-lookup"><span data-stu-id="9712d-112">Specifies either infrastructure or IBSS network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9712d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9712d-113">Requirements</span></span>



| <span data-ttu-id="9712d-114">需求</span><span class="sxs-lookup"><span data-stu-id="9712d-114">Requirement</span></span> | <span data-ttu-id="9712d-115">值</span><span class="sxs-lookup"><span data-stu-id="9712d-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9712d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9712d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9712d-117">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9712d-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9712d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9712d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9712d-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9712d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="9712d-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9712d-120">Redistributable</span></span><br/>          | <span data-ttu-id="9712d-121">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="9712d-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="9712d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9712d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9712d-123"><dt>Wlantypes (包含 Windot11) </dt></span><span class="sxs-lookup"><span data-stu-id="9712d-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9712d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9712d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9712d-125">**WLAN \_ BSS \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="9712d-125">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[<span data-ttu-id="9712d-126">**WLAN \_ 連接 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="9712d-126">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="9712d-127">**WlanGetNetworkBssList**</span><span class="sxs-lookup"><span data-stu-id="9712d-127">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




