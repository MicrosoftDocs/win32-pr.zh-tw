---
description: BLOB \_ 字元集 \_ 列舉指出目前的會議 BLOB 所使用的字元集。
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: 'BLOB_CHARACTER_SET 列舉 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995776"
---
# <a name="blob_character_set-enumeration"></a><span data-ttu-id="a0425-103">BLOB \_ 字元集 \_ 列舉</span><span class="sxs-lookup"><span data-stu-id="a0425-103">BLOB\_CHARACTER\_SET enumeration</span></span>

<span data-ttu-id="a0425-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="a0425-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0425-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="a0425-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a0425-106">**BLOB \_ 字元集 \_** 列舉指出目前的會議 BLOB 所使用的字元集。</span><span class="sxs-lookup"><span data-stu-id="a0425-106">The **BLOB\_CHARACTER\_SET** enum indicates the character set used by the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0425-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0425-107">Syntax</span></span>


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a><span data-ttu-id="a0425-108">常數</span><span class="sxs-lookup"><span data-stu-id="a0425-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a0425-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS \_ ASCII**</span><span class="sxs-lookup"><span data-stu-id="a0425-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS\_ASCII**</span></span>
</dt> <dd>

<span data-ttu-id="a0425-110">標準 ASCII 格式。</span><span class="sxs-lookup"><span data-stu-id="a0425-110">Standard ASCII format.</span></span>

</dd> <dt>

<span data-ttu-id="a0425-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS \_ UTF7**</span><span class="sxs-lookup"><span data-stu-id="a0425-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS\_UTF7**</span></span>
</dt> <dd>

<span data-ttu-id="a0425-112">Unicode 的七位轉換格式。</span><span class="sxs-lookup"><span data-stu-id="a0425-112">Seven-bit transformation format of Unicode.</span></span> <span data-ttu-id="a0425-113">如需此格式的詳細資訊，請進行網際網路搜尋以取得 RFC 1642。</span><span class="sxs-lookup"><span data-stu-id="a0425-113">For details on this format, conduct an Internet search for RFC 1642.</span></span>

</dd> <dt>

<span data-ttu-id="a0425-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS \_ UTF8**</span><span class="sxs-lookup"><span data-stu-id="a0425-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS\_UTF8**</span></span>
</dt> <dd>

<span data-ttu-id="a0425-115">UCS 轉換格式8。</span><span class="sxs-lookup"><span data-stu-id="a0425-115">UCS Transformation Format 8.</span></span> <span data-ttu-id="a0425-116">如需此格式的詳細資訊，請使用網際網路搜尋 ISO (國際標準組織) 和 IEC (國際電子電機委員會) 檔 ISO/IEC JTC1/SC2/WG2 N 1036 （日期為1994年8月1日） WG2 專案編輯器。</span><span class="sxs-lookup"><span data-stu-id="a0425-116">For details on this format, conduct an Internet search for ISO (the International Organization for Standardization) and IEC (the International Electrotechnical Commission) document ISO/IEC JTC1/SC2/WG2 N 1036, dated August 1, 1994, by WG2 Project Editor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0425-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0425-117">Requirements</span></span>



| <span data-ttu-id="a0425-118">需求</span><span class="sxs-lookup"><span data-stu-id="a0425-118">Requirement</span></span> | <span data-ttu-id="a0425-119">值</span><span class="sxs-lookup"><span data-stu-id="a0425-119">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0425-120">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="a0425-120">TAPI version</span></span><br/> | <span data-ttu-id="a0425-121">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a0425-121">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="a0425-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a0425-122">Header</span></span><br/>       | <dl> <span data-ttu-id="a0425-123"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0425-123"><dt>Sdpblb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0425-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0425-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0425-125">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="a0425-125">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[<span data-ttu-id="a0425-126">**取得 \_ CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="a0425-126">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)
</dt> <dt>

[<span data-ttu-id="a0425-127">**Init**</span><span class="sxs-lookup"><span data-stu-id="a0425-127">**Init**</span></span>](itconferenceblob-init.md)
</dt> <dt>

[<span data-ttu-id="a0425-128">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="a0425-128">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




