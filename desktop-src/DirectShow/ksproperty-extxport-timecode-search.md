---
description: 這個屬性會將命令傳送至裝置，以搜尋指定的時間代碼。 UVC 設備磁碟機支援此屬性。
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025654"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="48755-104">KSPROPERTY \_ EXTXPORT 時間 \_ 碼 \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="48755-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="48755-105">這個屬性會將命令傳送至裝置，以搜尋指定的時間代碼。</span><span class="sxs-lookup"><span data-stu-id="48755-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="48755-106">UVC 設備磁碟機支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="48755-106">The UVC device driver supports this property.</span></span>



|                   |                                        |
|-------------------|----------------------------------------|
| <span data-ttu-id="48755-107">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="48755-107">Property Set GUID</span></span> | <span data-ttu-id="48755-108">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="48755-108">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="48755-109">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="48755-109">Property ID</span></span>       | <span data-ttu-id="48755-110">KSPROPERTY \_ EXTXPORT 時間 \_ 碼 \_ 搜尋</span><span class="sxs-lookup"><span data-stu-id="48755-110">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="48755-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="48755-111">Data Type</span></span>         | <span data-ttu-id="48755-112">**KSPROPERTY \_EXTXPORT \_ S** 結構</span><span class="sxs-lookup"><span data-stu-id="48755-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="48755-113">備註</span><span class="sxs-lookup"><span data-stu-id="48755-113">Remarks</span></span>

<span data-ttu-id="48755-114">以所需的框架、秒、分鐘和小時填入 **KSPROPERTY \_ EXTXPORT \_ S** 結構的時間 **碼** 成員。</span><span class="sxs-lookup"><span data-stu-id="48755-114">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="48755-115">Windows DDK 中說明了 **KSPROPERTY \_ EXTXPORT \_ S** 結構。</span><span class="sxs-lookup"><span data-stu-id="48755-115">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="48755-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48755-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48755-117">外部裝置傳輸屬性集</span><span class="sxs-lookup"><span data-stu-id="48755-117">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



