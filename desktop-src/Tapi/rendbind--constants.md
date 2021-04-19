---
description: RENDBIND 常數是 ITDirectory：： Bind 方法用來指出所提供驗證類型的旗標。
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: 'RENDBIND_ 常數 (Rend) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990934"
---
# <a name="rendbind_-constants"></a><span data-ttu-id="1fd16-103">RENDBIND \_ 常數</span><span class="sxs-lookup"><span data-stu-id="1fd16-103">RENDBIND\_ Constants</span></span>

<span data-ttu-id="1fd16-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="1fd16-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1fd16-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="1fd16-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1fd16-106">RENDBIND 常數是 [**ITDirectory：： Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) 方法用來指出所提供驗證類型的旗標。</span><span class="sxs-lookup"><span data-stu-id="1fd16-106">The RENDBIND constants are flags used by the [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) method to indicate types of authentication supplied.</span></span>

<dl> <dt>

<span data-ttu-id="1fd16-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="1fd16-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="1fd16-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1fd16-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="1fd16-109">驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="1fd16-109">Authenticate user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fd16-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTDOMAINNAME**</span><span class="sxs-lookup"><span data-stu-id="1fd16-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND\_DEFAULTDOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="1fd16-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1fd16-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="1fd16-112">使用 [預設功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="1fd16-112">Use default domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fd16-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTUSERNAME**</span><span class="sxs-lookup"><span data-stu-id="1fd16-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND\_DEFAULTUSERNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="1fd16-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1fd16-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="1fd16-115">使用預設的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="1fd16-115">Use default user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fd16-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="1fd16-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND\_DEFAULTPASSWORD**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="1fd16-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="1fd16-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="1fd16-118">使用預設密碼。</span><span class="sxs-lookup"><span data-stu-id="1fd16-118">Use default password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fd16-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTCREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="1fd16-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND\_DEFAULTCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="1fd16-120">0x0000000e</span><span class="sxs-lookup"><span data-stu-id="1fd16-120">0x0000000e</span></span>
</dt> <dt>



<span data-ttu-id="1fd16-121">為了方便起見，上述三個 Or 運算在一起。</span><span class="sxs-lookup"><span data-stu-id="1fd16-121">The previous three ORed together for convenience.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fd16-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fd16-122">Requirements</span></span>



| <span data-ttu-id="1fd16-123">需求</span><span class="sxs-lookup"><span data-stu-id="1fd16-123">Requirement</span></span> | <span data-ttu-id="1fd16-124">值</span><span class="sxs-lookup"><span data-stu-id="1fd16-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1fd16-125">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="1fd16-125">TAPI version</span></span><br/> | <span data-ttu-id="1fd16-126">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1fd16-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1fd16-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1fd16-127">Header</span></span><br/>       | <dl> <span data-ttu-id="1fd16-128"><dt>Rend。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fd16-128"><dt>Rend.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fd16-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fd16-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd16-130">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="1fd16-130">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="1fd16-131">**ITDirectory：： Bind**</span><span class="sxs-lookup"><span data-stu-id="1fd16-131">**ITDirectory::Bind**</span></span>](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




