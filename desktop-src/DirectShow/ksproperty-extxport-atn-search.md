---
description: 此屬性會將命令傳送至裝置，以搜尋 (ATN) 的絕對曲目編號。 UVC 設備磁碟機支援此屬性。
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972916"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="5d5ed-104">KSPROPERTY \_ EXTXPORT \_ ATN \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="5d5ed-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="5d5ed-105">此屬性會將命令傳送至裝置，以搜尋 (ATN) 的絕對曲目編號。</span><span class="sxs-lookup"><span data-stu-id="5d5ed-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="5d5ed-106">UVC 設備磁碟機支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="5d5ed-106">The UVC device driver supports this property.</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="5d5ed-107">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="5d5ed-107">Property Set GUID</span></span> | <span data-ttu-id="5d5ed-108">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="5d5ed-108">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="5d5ed-109">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="5d5ed-109">Property ID</span></span>       | <span data-ttu-id="5d5ed-110">KSPROPERTY \_ EXTXPORT \_ ATN \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="5d5ed-110">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="5d5ed-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="5d5ed-111">Data Type</span></span>         | <span data-ttu-id="5d5ed-112">**KSPROPERTY \_EXTXPORT \_ S** 結構</span><span class="sxs-lookup"><span data-stu-id="5d5ed-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5d5ed-113">備註</span><span class="sxs-lookup"><span data-stu-id="5d5ed-113">Remarks</span></span>

<span data-ttu-id="5d5ed-114">將 **KSPROPERTY \_ EXTXPORT \_ S** 結構的 **dwAbsTrackNumber** 成員設定為下列值：</span><span class="sxs-lookup"><span data-stu-id="5d5ed-114">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="5d5ed-115">UVC 規格不會定義裝置使用持續性位的方式。</span><span class="sxs-lookup"><span data-stu-id="5d5ed-115">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="5d5ed-116">Windows DDK 中說明了 **KSPROPERTY \_ EXTXPORT \_ S** 結構。</span><span class="sxs-lookup"><span data-stu-id="5d5ed-116">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d5ed-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d5ed-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d5ed-118">外部裝置傳輸屬性集</span><span class="sxs-lookup"><span data-stu-id="5d5ed-118">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



