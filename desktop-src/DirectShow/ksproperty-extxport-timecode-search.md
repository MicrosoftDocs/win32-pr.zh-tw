---
description: 這個屬性會將命令傳送至裝置，以搜尋指定的時間代碼。 UVC 設備磁碟機支援此屬性。
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909436"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="5ca1b-104">KSPROPERTY \_ EXTXPORT 時間 \_ 碼 \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="5ca1b-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="5ca1b-105">這個屬性會將命令傳送至裝置，以搜尋指定的時間代碼。</span><span class="sxs-lookup"><span data-stu-id="5ca1b-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="5ca1b-106">UVC 設備磁碟機支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca1b-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="5ca1b-107">標籤</span><span class="sxs-lookup"><span data-stu-id="5ca1b-107">Label</span></span> | <span data-ttu-id="5ca1b-108">值</span><span class="sxs-lookup"><span data-stu-id="5ca1b-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="5ca1b-109">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="5ca1b-109">Property Set GUID</span></span> | <span data-ttu-id="5ca1b-110">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="5ca1b-110">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="5ca1b-111">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="5ca1b-111">Property ID</span></span>       | <span data-ttu-id="5ca1b-112">KSPROPERTY \_ EXTXPORT 時間 \_ 碼 \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="5ca1b-112">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="5ca1b-113">資料類型</span><span class="sxs-lookup"><span data-stu-id="5ca1b-113">Data Type</span></span>         | <span data-ttu-id="5ca1b-114">**KSPROPERTY \_EXTXPORT \_ S** 結構</span><span class="sxs-lookup"><span data-stu-id="5ca1b-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="5ca1b-115">備註</span><span class="sxs-lookup"><span data-stu-id="5ca1b-115">Remarks</span></span>

<span data-ttu-id="5ca1b-116">以所需的框架、秒、分鐘和小時填入 **KSPROPERTY \_ EXTXPORT \_ S** 結構的時間 **碼** 成員。</span><span class="sxs-lookup"><span data-stu-id="5ca1b-116">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="5ca1b-117">Windows DDK 中說明了 **KSPROPERTY \_ EXTXPORT \_ S** 結構。</span><span class="sxs-lookup"><span data-stu-id="5ca1b-117">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ca1b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ca1b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca1b-119">外部裝置傳輸屬性集</span><span class="sxs-lookup"><span data-stu-id="5ca1b-119">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



