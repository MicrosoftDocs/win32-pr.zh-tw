---
description: 下列常數與認證的輸出保護通訊協定搭配使用 (COPP) 至特定的輸出保護機制。
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: 'COPP 保護類型旗標 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996102"
---
# <a name="copp-protection-type-flags"></a><span data-ttu-id="b6ab8-103">COPP 保護類型旗標</span><span class="sxs-lookup"><span data-stu-id="b6ab8-103">COPP Protection Type Flags</span></span>

<span data-ttu-id="b6ab8-104">下列常數與認證的輸出保護通訊協定搭配使用 (COPP) 至特定的輸出保護機制。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-104">The follow constants are used with Certified Output Protection Protocol (COPP) to specific output protection mechanisms.</span></span>



| <span data-ttu-id="b6ab8-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="b6ab8-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="b6ab8-106">Description</span><span class="sxs-lookup"><span data-stu-id="b6ab8-106">Description</span></span>                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <span data-ttu-id="b6ab8-107"><dt>**COPP \_Set-protectiontype \_ 不明**</dt>的 <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab8-107"><dt>**COPP\_ProtectionType\_Unknown**</dt> <dt>0x80000000</dt></span></span> </dl>     | <span data-ttu-id="b6ab8-108">未知的保護機制。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-108">Unknown protection mechanism.</span></span><br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <span data-ttu-id="b6ab8-109"><dt>**COPP \_Set-protectiontype \_ 無**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab8-109"><dt>**COPP\_ProtectionType\_None**</dt> <dt>0x00000000</dt></span></span> </dl>                 | <span data-ttu-id="b6ab8-110">沒有防護機制。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-110">No protection mechanisms.</span></span><br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <span data-ttu-id="b6ab8-111"><dt>**COPP \_Set-protectiontype \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab8-111"><dt>**COPP\_ProtectionType\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="b6ab8-112">High-Bandwidth 數位內容保護 (HDCP) 。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-112">High-Bandwidth Digital Content Protection (HDCP).</span></span><br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <span data-ttu-id="b6ab8-113"><dt>**COPP \_Set-protectiontype \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab8-113"><dt>**COPP\_ProtectionType\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                     | <span data-ttu-id="b6ab8-114">類比禁止複製 (ACP) 。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-114">Analog Copy Protection (ACP).</span></span><br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <span data-ttu-id="b6ab8-115"><dt>**COPP \_Set-protectiontype \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab8-115"><dt>**COPP\_ProtectionType\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="b6ab8-116">複製世代管理系統類比 (CGMS-A) 。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-116">Copy Generation Management System   Analog (CGMS-A).</span></span><br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <span data-ttu-id="b6ab8-117"><dt>**COPP \_Set-protectiontype \_ Mask**</dt> <dt>0x80000007</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab8-117"><dt>**COPP\_ProtectionType\_Mask**</dt> <dt>0x80000007</dt></span></span> </dl>                 | <span data-ttu-id="b6ab8-118">用來隔離有效旗標的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-118">Bitmask to isolate valid flags.</span></span><br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <span data-ttu-id="b6ab8-119"><dt>**COPP \_Set-protectiontype \_ 保留**</dt>的 <dt>0x7FFFFFF8</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab8-119"><dt>**COPP\_ProtectionType\_Reserved**</dt> <dt>0x7FFFFFF8</dt></span></span> </dl> | <span data-ttu-id="b6ab8-120">保留的。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-120">Reserved.</span></span> <span data-ttu-id="b6ab8-121">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-121">Must be zero.</span></span><br/>                              |



## <a name="remarks"></a><span data-ttu-id="b6ab8-122">備註</span><span class="sxs-lookup"><span data-stu-id="b6ab8-122">Remarks</span></span>

<span data-ttu-id="b6ab8-123">某些方法會從這個列舉型別傳回單一旗標，而某些方法會傳回一或多個旗標的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-123">Some methods return a single flag from this enumeration type, and some methods return a bitwise **OR** of one or more flags.</span></span>

<span data-ttu-id="b6ab8-124">下列 COPP 查詢和命令會使用這些旗標。</span><span class="sxs-lookup"><span data-stu-id="b6ab8-124">These flags are used in the following COPP queries and commands.</span></span>

-   <span data-ttu-id="b6ab8-125">全域保護等級</span><span class="sxs-lookup"><span data-stu-id="b6ab8-125">Global Protection Level</span></span>
-   <span data-ttu-id="b6ab8-126">本機保護層級</span><span class="sxs-lookup"><span data-stu-id="b6ab8-126">Local Protection Level</span></span>
-   <span data-ttu-id="b6ab8-127">保護類型</span><span class="sxs-lookup"><span data-stu-id="b6ab8-127">Protection Type</span></span>
-   <span data-ttu-id="b6ab8-128">設定保護層級</span><span class="sxs-lookup"><span data-stu-id="b6ab8-128">Set Protection Level</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ab8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6ab8-129">Requirements</span></span>



| <span data-ttu-id="b6ab8-130">需求</span><span class="sxs-lookup"><span data-stu-id="b6ab8-130">Requirement</span></span> | <span data-ttu-id="b6ab8-131">值</span><span class="sxs-lookup"><span data-stu-id="b6ab8-131">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b6ab8-132">標頭</span><span class="sxs-lookup"><span data-stu-id="b6ab8-132">Header</span></span><br/> | <dl> <span data-ttu-id="b6ab8-133"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6ab8-133"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ab8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6ab8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ab8-135">常數和 Guid</span><span class="sxs-lookup"><span data-stu-id="b6ab8-135">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="b6ab8-136">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="b6ab8-136">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




