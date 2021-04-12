---
title: 'SNMP 的函式語法值 (Snmp. h) '
description: SNMP 的函式語法值描述項合抽象語法標記法 (一)  (asn.1) 編碼標準的類型。
ms.assetid: 8e3b6e00-51cf-4e39-a68e-dcf8fbe8ab3b
topic_type:
- apiref
api_name:
- ASN_SEQUENCE
- ASN_SEQUENCEOF
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484e58d7a92a3c75408db3160362d84e7891b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094371"
---
# <a name="snmp-constructor-syntax-values"></a><span data-ttu-id="c8fd2-103">SNMP 函數語法值</span><span class="sxs-lookup"><span data-stu-id="c8fd2-103">SNMP Constructor Syntax Values</span></span>

<span data-ttu-id="c8fd2-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c8fd2-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c8fd2-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="c8fd2-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="c8fd2-107">SNMP 的函式語法值描述項合抽象語法標記法 (一)  (asn.1) 編碼標準的類型。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-107">The SNMP Constructor Syntax Values describe types that are compliant with the Abstract Syntax Notation One (ASN.1) encoding standard.</span></span>



| <span data-ttu-id="c8fd2-108">常數</span><span class="sxs-lookup"><span data-stu-id="c8fd2-108">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="c8fd2-109">描述</span><span class="sxs-lookup"><span data-stu-id="c8fd2-109">Description</span></span>                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="ASN_SEQUENCE"></span><span id="asn_sequence"></span><dl> <span data-ttu-id="c8fd2-110"><dt>**ASN \_ 序列**</dt></span><span class="sxs-lookup"><span data-stu-id="c8fd2-110"><dt>**ASN\_SEQUENCE**</dt></span></span> </dl>       | <span data-ttu-id="c8fd2-111">指出訊息為 ASN 序列。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-111">Indicates that the message is an ASN sequence.</span></span><br/> |
| <span id="ASN_SEQUENCEOF"></span><span id="asn_sequenceof"></span><dl> <span data-ttu-id="c8fd2-112"><dt>**ASN \_ SEQUENCEOF**</dt></span><span class="sxs-lookup"><span data-stu-id="c8fd2-112"><dt>**ASN\_SEQUENCEOF**</dt></span></span> </dl> | <span data-ttu-id="c8fd2-113">請參閱 ASN \_ 序列。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-113">See ASN\_SEQUENCE.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="c8fd2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8fd2-114">Requirements</span></span>



| <span data-ttu-id="c8fd2-115">需求</span><span class="sxs-lookup"><span data-stu-id="c8fd2-115">Requirement</span></span> | <span data-ttu-id="c8fd2-116">值</span><span class="sxs-lookup"><span data-stu-id="c8fd2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c8fd2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8fd2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c8fd2-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8fd2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="c8fd2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8fd2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c8fd2-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8fd2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c8fd2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c8fd2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8fd2-122"><dt>Snmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8fd2-122"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8fd2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8fd2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8fd2-124">Simple Network Management Protocol (SNMP) 概觀</span><span class="sxs-lookup"><span data-stu-id="c8fd2-124">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="c8fd2-125">SNMP 參考</span><span class="sxs-lookup"><span data-stu-id="c8fd2-125">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="c8fd2-126">SNMP 常數</span><span class="sxs-lookup"><span data-stu-id="c8fd2-126">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

