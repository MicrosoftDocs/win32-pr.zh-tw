---
title: 'SNMP 簡單語法值 (Snmp. h) '
description: SNMP 簡單語法值是用來表示 SNMP 變數類型。
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104375"
---
# <a name="snmp-simple-syntax-values"></a><span data-ttu-id="ead6d-103">SNMP 簡單語法值</span><span class="sxs-lookup"><span data-stu-id="ead6d-103">SNMP Simple Syntax Values</span></span>

<span data-ttu-id="ead6d-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ead6d-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ead6d-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ead6d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ead6d-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="ead6d-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="ead6d-107">SNMP 簡單語法值是用來表示 SNMP 變數類型。</span><span class="sxs-lookup"><span data-stu-id="ead6d-107">The SNMP Simple Syntax Values are used to indicate an SNMP variable type.</span></span>



| <span data-ttu-id="ead6d-108">常數</span><span class="sxs-lookup"><span data-stu-id="ead6d-108">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="ead6d-109">描述</span><span class="sxs-lookup"><span data-stu-id="ead6d-109">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <span data-ttu-id="ead6d-110"><dt>**ASN \_ 整數**</dt></span><span class="sxs-lookup"><span data-stu-id="ead6d-110"><dt>**ASN\_INTEGER**</dt></span></span> </dl>                            | <span data-ttu-id="ead6d-111">表示32位帶正負號的整數變數。</span><span class="sxs-lookup"><span data-stu-id="ead6d-111">Indicates a 32-bit signed integer variable.</span></span><br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <span data-ttu-id="ead6d-112"><dt>**ASN \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="ead6d-112"><dt>**ASN\_BITS**</dt></span></span> </dl>                                     | <span data-ttu-id="ead6d-113">表示變數，其為已命名位的列舉。</span><span class="sxs-lookup"><span data-stu-id="ead6d-113">Indicates a variable that is an enumeration of named bits.</span></span><br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <span data-ttu-id="ead6d-114"><dt>**ASN \_ OCTETSTRING**</dt></span><span class="sxs-lookup"><span data-stu-id="ead6d-114"><dt>**ASN\_OCTETSTRING**</dt></span></span> </dl>                | <span data-ttu-id="ead6d-115">表示八位字串變數。</span><span class="sxs-lookup"><span data-stu-id="ead6d-115">Indicates an octet string variable.</span></span><br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <span data-ttu-id="ead6d-116"><dt>**ASN \_ Null**</dt></span><span class="sxs-lookup"><span data-stu-id="ead6d-116"><dt>**ASN\_NULL**</dt></span></span> </dl>                                     | <span data-ttu-id="ead6d-117">表示 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="ead6d-117">Indicates a **NULL** value.</span></span><br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <span data-ttu-id="ead6d-118"><dt>**ASN \_ OBJECTIDENTIFIER**</dt></span><span class="sxs-lookup"><span data-stu-id="ead6d-118"><dt>**ASN\_OBJECTIDENTIFIER**</dt></span></span> </dl> | <span data-ttu-id="ead6d-119">指出物件識別碼變數。</span><span class="sxs-lookup"><span data-stu-id="ead6d-119">Indicates an object identifier variable.</span></span><br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <span data-ttu-id="ead6d-120"><dt>**ASN \_ INTEGER32**</dt></span><span class="sxs-lookup"><span data-stu-id="ead6d-120"><dt>**ASN\_INTEGER32**</dt></span></span> </dl>                      | <span data-ttu-id="ead6d-121">表示32位帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="ead6d-121">Indicates a 32-bit signed integer value.</span></span><br/>                   |



## <a name="requirements"></a><span data-ttu-id="ead6d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ead6d-122">Requirements</span></span>



| <span data-ttu-id="ead6d-123">需求</span><span class="sxs-lookup"><span data-stu-id="ead6d-123">Requirement</span></span> | <span data-ttu-id="ead6d-124">值</span><span class="sxs-lookup"><span data-stu-id="ead6d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ead6d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ead6d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ead6d-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ead6d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="ead6d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ead6d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ead6d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ead6d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ead6d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ead6d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead6d-130"><dt>Snmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ead6d-130"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead6d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ead6d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead6d-132">Simple Network Management Protocol (SNMP) 概觀</span><span class="sxs-lookup"><span data-stu-id="ead6d-132">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="ead6d-133">SNMP 參考</span><span class="sxs-lookup"><span data-stu-id="ead6d-133">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="ead6d-134">SNMP 常數</span><span class="sxs-lookup"><span data-stu-id="ead6d-134">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

