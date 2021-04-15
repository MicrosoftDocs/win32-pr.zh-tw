---
title: 'Snmp 要求類型 (Snmp. h) '
description: SNMP 要求類型是用來描述 SNMP 服務要求擴充代理程式執行的操作。
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466449"
---
# <a name="snmp-request-types"></a><span data-ttu-id="5f112-103">SNMP 要求類型</span><span class="sxs-lookup"><span data-stu-id="5f112-103">SNMP Request Types</span></span>

<span data-ttu-id="5f112-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5f112-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5f112-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5f112-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5f112-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="5f112-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="5f112-107">SNMP 要求類型是用來描述 SNMP 服務要求擴充代理程式執行的操作。</span><span class="sxs-lookup"><span data-stu-id="5f112-107">The SNMP Request Types are used to describe the operation that the SNMP service is requesting the extension agent to perform.</span></span>



| <span data-ttu-id="5f112-108">常數/值</span><span class="sxs-lookup"><span data-stu-id="5f112-108">Constant/value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="5f112-109">Description</span><span class="sxs-lookup"><span data-stu-id="5f112-109">Description</span></span>                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <span data-ttu-id="5f112-110"><dt>**SNMP \_擴充功能 \_ 取得**</dt> <dt>SNMP \_ PDU \_ GET</dt></span><span class="sxs-lookup"><span data-stu-id="5f112-110"><dt>**SNMP\_EXTENSION\_GET**</dt> <dt>SNMP\_PDU\_GET</dt></span></span> </dl>                       | <span data-ttu-id="5f112-111">取出指定變數值的值。</span><span class="sxs-lookup"><span data-stu-id="5f112-111">Retrieve the value of values of the specified variables.</span></span><br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <span data-ttu-id="5f112-112"><dt>**SNMP \_擴充功能 \_ 取得 \_ 下一個**</dt> <dt>SNMP \_ PDU \_ GETNEXT</dt></span><span class="sxs-lookup"><span data-stu-id="5f112-112"><dt>**SNMP\_EXTENSION\_GET\_NEXT**</dt> <dt>SNMP\_PDU\_GETNEXT</dt></span></span> </dl>   | <span data-ttu-id="5f112-113">取得所指定變數的詞典編纂後置值。</span><span class="sxs-lookup"><span data-stu-id="5f112-113">Retrieve the value or values of the lexicographic successor of the specified variables.</span></span><br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <span data-ttu-id="5f112-114"><dt>**SNMP \_擴充功能 \_ 取得 \_ 大量**</dt> <dt>SNMP \_ PDU \_ GETBULK</dt></span><span class="sxs-lookup"><span data-stu-id="5f112-114"><dt>**SNMP\_EXTENSION\_GET\_BULK**</dt> <dt>SNMP\_PDU\_GETBULK</dt></span></span> </dl>   | <span data-ttu-id="5f112-115">使用單一要求來搜尋和取出多個值。</span><span class="sxs-lookup"><span data-stu-id="5f112-115">Search and retrieve multiple values with a single request.</span></span><br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <span data-ttu-id="5f112-116"><dt>**SNMP \_ 延伸模組 \_ 設定 \_ 測試**</dt></span><span class="sxs-lookup"><span data-stu-id="5f112-116"><dt>**SNMP\_EXTENSION\_SET\_TEST**</dt></span></span> </dl>                                                                           | <span data-ttu-id="5f112-117">驗證指定之變數的值。</span><span class="sxs-lookup"><span data-stu-id="5f112-117">Validate the values of the specified variables.</span></span> <span data-ttu-id="5f112-118">這項作業會將認可要求期間成功寫入作業的機率最大化。</span><span class="sxs-lookup"><span data-stu-id="5f112-118">This operation maximizes the probability of a successful write operation during the COMMIT request.</span></span> <span data-ttu-id="5f112-119">如需詳細資訊，請參閱 [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) 函數。</span><span class="sxs-lookup"><span data-stu-id="5f112-119">For more information, see the [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) function.</span></span><br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <span data-ttu-id="5f112-120"><dt>**SNMP \_延伸模組 \_ 設定 \_ 認可**</dt> <dt>SNMP \_ PDU \_ 設定</dt></span><span class="sxs-lookup"><span data-stu-id="5f112-120"><dt>**SNMP\_EXTENSION\_SET\_COMMIT**</dt> <dt>SNMP\_PDU\_SET</dt></span></span> </dl> | <span data-ttu-id="5f112-121">將新值寫入指定的變數。</span><span class="sxs-lookup"><span data-stu-id="5f112-121">Write the new values to the specified variables.</span></span><br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <span data-ttu-id="5f112-122"><dt>**SNMP \_ 延伸模組 \_ 設定 \_ 復原**</dt></span><span class="sxs-lookup"><span data-stu-id="5f112-122"><dt>**SNMP\_EXTENSION\_SET\_UNDO**</dt></span></span> </dl>                                                                           | <span data-ttu-id="5f112-123">將所指定變數的值重設為其在認可要求之前的值。</span><span class="sxs-lookup"><span data-stu-id="5f112-123">Reset the values of the specified variables to their values before the COMMIT request.</span></span><br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <span data-ttu-id="5f112-124"><dt>**SNMP \_ 延伸模組 \_ 設定 \_ 清除**</dt></span><span class="sxs-lookup"><span data-stu-id="5f112-124"><dt>**SNMP\_EXTENSION\_SET\_CLEANUP**</dt></span></span> </dl>                                                                  | <span data-ttu-id="5f112-125">釋放在先前的要求和作業中配置的資源。</span><span class="sxs-lookup"><span data-stu-id="5f112-125">Release the resources allocated in previous requests and operations.</span></span><br/>                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="5f112-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f112-126">Requirements</span></span>



| <span data-ttu-id="5f112-127">需求</span><span class="sxs-lookup"><span data-stu-id="5f112-127">Requirement</span></span> | <span data-ttu-id="5f112-128">值</span><span class="sxs-lookup"><span data-stu-id="5f112-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5f112-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f112-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5f112-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f112-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="5f112-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f112-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5f112-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f112-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5f112-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5f112-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f112-134"><dt>Snmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f112-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f112-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f112-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f112-136">Simple Network Management Protocol (SNMP) 概觀</span><span class="sxs-lookup"><span data-stu-id="5f112-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="5f112-137">SNMP 參考</span><span class="sxs-lookup"><span data-stu-id="5f112-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="5f112-138">SNMP 常數</span><span class="sxs-lookup"><span data-stu-id="5f112-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

