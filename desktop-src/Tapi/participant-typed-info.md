---
description: 參與者具 \_ 類型資訊列舉的成員會 \_ 識別 ITParticipant：： get ParticipantTypedInfo 方法所抓取的參與者資訊類型 \_ 。 存取 IPConf MSP 的應用程式會使用這個列舉。
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: 'PARTICIPANT_TYPED_INFO 列舉 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994678"
---
# <a name="participant_typed_info-enumeration"></a><span data-ttu-id="9dd44-104">參與者 \_ 輸入 \_ 資訊列舉</span><span class="sxs-lookup"><span data-stu-id="9dd44-104">PARTICIPANT\_TYPED\_INFO enumeration</span></span>

<span data-ttu-id="9dd44-105">\[**參與者 \_在 \_** windows Vista、windows Server 2008 和後續版本的作業系統中，無法使用具類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="9dd44-105">\[**PARTICIPANT\_TYPED\_INFO** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9dd44-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9dd44-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9dd44-107">**參與者具 \_ 類型 \_ 資訊** 列舉的成員會識別 [**ITParticipant：： get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)方法所抓取的參與者資訊類型。</span><span class="sxs-lookup"><span data-stu-id="9dd44-107">The members of the **PARTICIPANT\_TYPED\_INFO** enum identify the type of participant information being retrieved by the [**ITParticipant::get\_ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) method.</span></span> <span data-ttu-id="9dd44-108">存取 [IPCONF MSP](ipconf-msp.md)的應用程式會使用這個列舉。</span><span class="sxs-lookup"><span data-stu-id="9dd44-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd44-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dd44-109">Syntax</span></span>


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a><span data-ttu-id="9dd44-110">常數</span><span class="sxs-lookup"><span data-stu-id="9dd44-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9dd44-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**</span><span class="sxs-lookup"><span data-stu-id="9dd44-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI\_CANONICALNAME**</span></span>
</dt> <dd>

<span data-ttu-id="9dd44-112">參與者的正式名稱，例如 someone@example.com 。</span><span class="sxs-lookup"><span data-stu-id="9dd44-112">Canonical name of participant, such as someone@example.com.</span></span>

</dd> <dt>

<span data-ttu-id="9dd44-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="9dd44-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI\_NAME**</span></span>
</dt> <dd>

<span data-ttu-id="9dd44-114">參與者的可顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9dd44-114">Displayable name of participant.</span></span>

</dd> <dt>

<span data-ttu-id="9dd44-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EMAILADDRESS**</span><span class="sxs-lookup"><span data-stu-id="9dd44-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI\_EMAILADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="9dd44-116">參與者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="9dd44-116">Participant's email address.</span></span>

</dd> <dt>

<span data-ttu-id="9dd44-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="9dd44-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI\_PHONENUMBER**</span></span>
</dt> <dd>

<span data-ttu-id="9dd44-118">參與者的電話位址。</span><span class="sxs-lookup"><span data-stu-id="9dd44-118">Participant's phone address.</span></span>

</dd> <dt>

<span data-ttu-id="9dd44-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="9dd44-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI\_LOCATION**</span></span>
</dt> <dd>

<span data-ttu-id="9dd44-120">參與者的地理位址。</span><span class="sxs-lookup"><span data-stu-id="9dd44-120">Participant's geographical address.</span></span>

</dd> <dt>

<span data-ttu-id="9dd44-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI \_ 工具**</span><span class="sxs-lookup"><span data-stu-id="9dd44-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI\_TOOL**</span></span>
</dt> <dd>

<span data-ttu-id="9dd44-122">參與者的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9dd44-122">Participant's application.</span></span>

</dd> <dt>

<span data-ttu-id="9dd44-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI \_ 注意事項**</span><span class="sxs-lookup"><span data-stu-id="9dd44-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI\_NOTES**</span></span>
</dt> <dd>

<span data-ttu-id="9dd44-124">有關參與者的附注。</span><span class="sxs-lookup"><span data-stu-id="9dd44-124">Notes concerning participant.</span></span>

</dd> <dt>

<span data-ttu-id="9dd44-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ 私用**</span><span class="sxs-lookup"><span data-stu-id="9dd44-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="9dd44-126">定義實驗性或應用程式特定的來源描述 (SDES) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="9dd44-126">Defines an experimental or application-specific Source Description (SDES) extension.</span></span> <span data-ttu-id="9dd44-127">如需詳細資訊，請參閱 RFC 1889。</span><span class="sxs-lookup"><span data-stu-id="9dd44-127">See RFC 1889 for details.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9dd44-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="9dd44-128">Requirements</span></span>



| <span data-ttu-id="9dd44-129">需求</span><span class="sxs-lookup"><span data-stu-id="9dd44-129">Requirement</span></span> | <span data-ttu-id="9dd44-130">值</span><span class="sxs-lookup"><span data-stu-id="9dd44-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd44-131">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9dd44-131">TAPI version</span></span><br/> | <span data-ttu-id="9dd44-132">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9dd44-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9dd44-133">標頭</span><span class="sxs-lookup"><span data-stu-id="9dd44-133">Header</span></span><br/>       | <dl> <span data-ttu-id="9dd44-134"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd44-134"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dd44-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dd44-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd44-136">**ITParticipant：： get \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="9dd44-136">**ITParticipant::get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[<span data-ttu-id="9dd44-137">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="9dd44-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="9dd44-138">IPConf MSP 介面</span><span class="sxs-lookup"><span data-stu-id="9dd44-138">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




