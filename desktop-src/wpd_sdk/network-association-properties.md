---
description: Windows 可攜式裝置支援下列網路關聯屬性。
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: '網路關聯屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976094"
---
# <a name="network-association-properties"></a><span data-ttu-id="bd64b-103">網路關聯屬性</span><span class="sxs-lookup"><span data-stu-id="bd64b-103">Network Association Properties</span></span>

<span data-ttu-id="bd64b-104">Windows 可攜式裝置支援下列網路關聯屬性。</span><span class="sxs-lookup"><span data-stu-id="bd64b-104">Windows Portable Devices supports the following network association properties.</span></span>



| <span data-ttu-id="bd64b-105">屬性</span><span class="sxs-lookup"><span data-stu-id="bd64b-105">Property</span></span>                                                  | <span data-ttu-id="bd64b-106">VarType</span><span class="sxs-lookup"><span data-stu-id="bd64b-106">VarType</span></span>                   | <span data-ttu-id="bd64b-107">Description</span><span class="sxs-lookup"><span data-stu-id="bd64b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd64b-108">**WPD \_ 網路 \_ 關聯 \_ 主機 \_ 網路 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="bd64b-108">**WPD\_NETWORK\_ASSOCIATION\_HOST\_NETWORK\_IDENTIFIERS**</span></span> | <span data-ttu-id="bd64b-109">**VT \_ 向量 \| vt \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="bd64b-109">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="bd64b-110">適用于此關聯的 EUI-64 主機識別碼清單。這是位元組陣列，其中包含一組整數的 EUI-64 實體網路位址。</span><span class="sxs-lookup"><span data-stu-id="bd64b-110">The list of EUI-64 host identifiers valid for this association.This is an array of bytes that contains an integral number of EUI-64 physical network addresses.</span></span> <span data-ttu-id="bd64b-111">這些 EUI-64 值是主機上網路關聯時間可用的實體網路位址。</span><span class="sxs-lookup"><span data-stu-id="bd64b-111">These EUI-64 values are the physical network addresses available on the host at Network Association time.</span></span> <span data-ttu-id="bd64b-112">如果主機具有 MAC-48 實體網路位址 (一般的 IPv4 網路) ，則每個 MAC-48 位址都會以 EUI-64 位址編碼，並以 FF-FF 分隔的兩個 MAC-48 位址。</span><span class="sxs-lookup"><span data-stu-id="bd64b-112">If the host has MAC-48 physical network addresses (typical of IPv4 networks), each MAC-48 address will be encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span><br/> |
| <span data-ttu-id="bd64b-113">**WPD \_ 網路 \_ 關聯 \_ X509V3SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="bd64b-113">**WPD\_NETWORK\_ASSOCIATION\_X509V3SEQUENCE**</span></span>             | <span data-ttu-id="bd64b-114">**VT \_ 向量 \| vt \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="bd64b-114">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="bd64b-115">要提供給 TLS 伺服器驗證的 x.509 v3 憑證順序。</span><span class="sxs-lookup"><span data-stu-id="bd64b-115">The sequence of X.509 v3 certificates to be provided for TLS server authentication.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="bd64b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd64b-116">Requirements</span></span>



| <span data-ttu-id="bd64b-117">需求</span><span class="sxs-lookup"><span data-stu-id="bd64b-117">Requirement</span></span> | <span data-ttu-id="bd64b-118">值</span><span class="sxs-lookup"><span data-stu-id="bd64b-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd64b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="bd64b-119">Header</span></span><br/> | <dl> <span data-ttu-id="bd64b-120"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd64b-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd64b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd64b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd64b-122">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="bd64b-122">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




