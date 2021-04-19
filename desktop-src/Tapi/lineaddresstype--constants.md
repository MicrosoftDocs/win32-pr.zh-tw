---
description: 網址類別型會識別位址格式，例如標準電話號碼或電子郵件地址。 只有協商 TAPI 3.0 版或更新版本的應用程式可以使用網址類別型。
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: 'LINEADDRESSTYPE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998399"
---
# <a name="lineaddresstype_-constants"></a><span data-ttu-id="23f62-104">LINEADDRESSTYPE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="23f62-104">LINEADDRESSTYPE\_ Constants</span></span>

<span data-ttu-id="23f62-105">網址類別型會識別位址格式，例如標準電話號碼或電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="23f62-105">The address type identifies address format, such as standard phone number or e-mail address.</span></span> <span data-ttu-id="23f62-106">只有協商 TAPI 3.0 版或更新版本的應用程式可以使用網址類別型。</span><span class="sxs-lookup"><span data-stu-id="23f62-106">Only applications that negotiate TAPI version 3.0 or higher can use address types.</span></span>

<dl> <dt>

<span data-ttu-id="23f62-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="23f62-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE\_PHONENUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f62-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="23f62-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="23f62-109">網址類別型是標準的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="23f62-109">Address type is a standard phone number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="23f62-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE \_ SDP**</span><span class="sxs-lookup"><span data-stu-id="23f62-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE\_SDP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f62-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="23f62-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="23f62-112">網址類別型為 Session Description Protocol (SDP) 會議。</span><span class="sxs-lookup"><span data-stu-id="23f62-112">Address type is Session Description Protocol (SDP) conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="23f62-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EMAILNAME**</span><span class="sxs-lookup"><span data-stu-id="23f62-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE\_EMAILNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f62-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="23f62-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="23f62-115">網址類別型是電子郵件名稱。</span><span class="sxs-lookup"><span data-stu-id="23f62-115">Address type is an e-mail name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="23f62-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ DOMAINNAME**</span><span class="sxs-lookup"><span data-stu-id="23f62-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f62-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="23f62-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="23f62-118">網址類別型是功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="23f62-118">Address type is a domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="23f62-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="23f62-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE\_IPADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23f62-120">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23f62-120">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="23f62-121">網址類別型是 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="23f62-121">Address type is an IP address.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23f62-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="23f62-122">Requirements</span></span>



| <span data-ttu-id="23f62-123">需求</span><span class="sxs-lookup"><span data-stu-id="23f62-123">Requirement</span></span> | <span data-ttu-id="23f62-124">值</span><span class="sxs-lookup"><span data-stu-id="23f62-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="23f62-125">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="23f62-125">TAPI version</span></span><br/> | <span data-ttu-id="23f62-126">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="23f62-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="23f62-127">標頭</span><span class="sxs-lookup"><span data-stu-id="23f62-127">Header</span></span><br/>       | <dl> <span data-ttu-id="23f62-128"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="23f62-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




