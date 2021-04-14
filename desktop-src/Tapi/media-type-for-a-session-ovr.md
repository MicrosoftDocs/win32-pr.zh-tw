---
description: 媒體類型 (或模式) 描述要交換的資訊類型，例如互動式語音。 給定的通訊會話可能牽涉到數種媒體類型。
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: 會話的媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514336"
---
# <a name="media-type-for-a-session"></a><span data-ttu-id="9a2b2-104">會話的媒體類型</span><span class="sxs-lookup"><span data-stu-id="9a2b2-104">Media Type for a Session</span></span>

<span data-ttu-id="9a2b2-105">媒體類型 (或模式) 描述要交換的資訊類型，例如互動式語音。</span><span class="sxs-lookup"><span data-stu-id="9a2b2-105">The media type (or mode) describes the type of information being exchanged, such as interactive voice.</span></span> <span data-ttu-id="9a2b2-106">給定的通訊會話可能牽涉到數種媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9a2b2-106">A given communications session may involve several media types.</span></span>

<span data-ttu-id="9a2b2-107">服務提供者會向 TAPI 和應用程式提供支援的媒體類型或類型。</span><span class="sxs-lookup"><span data-stu-id="9a2b2-107">Service providers expose to TAPI and to applications the media type or types they support.</span></span> <span data-ttu-id="9a2b2-108">如需取得此資料的詳細資訊，請參閱裝置 [媒體類型](media-type-ovr.md) 總覽。</span><span class="sxs-lookup"><span data-stu-id="9a2b2-108">See the device [media type](media-type-ovr.md) overview for information on acquiring this data.</span></span>

<span data-ttu-id="9a2b2-109">**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode)、 [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)、 [**LINE \_ MONITORMEDIA**](./line-monitormedia.md) message、 [LINEMEDIAMODE \_ 常數](./linemediamode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9a2b2-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**LINE\_MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="9a2b2-110">**TAPI 3.x：** 請參閱使用 **cil \_ MEDIATYPESAVAILABLE** 的 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) 、 [**ITCallInfo：:p \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **Cil \_ MEDIATYPESAVAILABLE**、 [**ITCallInfoChangeEvent：： get \_ 原因**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (傳回 **CALLINFOCHANGE \_ 媒體媒體** 的 [**CIC \_ 原因**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause)) 、 [TAPIMEDIATYPE \_ 常數](tapimediatype--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9a2b2-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (returns [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC\_MEDIATYPE**), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>

 

 
