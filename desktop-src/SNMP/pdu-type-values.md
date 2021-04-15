---
title: " (Snmp 的 PDU 類型值) "
description: Pdu 類型值會用在 PDU 的 [pdu \_ 類型] 欄位中，以描述其類型。
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466452"
---
# <a name="pdu-type-values"></a><span data-ttu-id="a1b5e-103">PDU 類型值</span><span class="sxs-lookup"><span data-stu-id="a1b5e-103">PDU Type Values</span></span>

<span data-ttu-id="a1b5e-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a1b5e-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a1b5e-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="a1b5e-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="a1b5e-107">Pdu 類型值會用在 PDU 的 [ **pdu \_ 類型** ] 欄位中，以描述其類型。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-107">The PDU type values are used in the **pdu\_type** field of the PDU to describe its type.</span></span>



| <span data-ttu-id="a1b5e-108">常數</span><span class="sxs-lookup"><span data-stu-id="a1b5e-108">Constant</span></span>                                                                                                                                                                   | <span data-ttu-id="a1b5e-109">描述</span><span class="sxs-lookup"><span data-stu-id="a1b5e-109">Description</span></span>                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <span data-ttu-id="a1b5e-110"><dt>**SNMP \_ PDU \_ GET**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-110"><dt>**SNMP\_PDU\_GET**</dt></span></span> </dl>                | <span data-ttu-id="a1b5e-111">搜尋並從指定的 SNMP 變數取得值。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-111">Search and retrieve a value from a specified SNMP variable.</span></span><br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <span data-ttu-id="a1b5e-112"><dt>**SNMP \_ PDU \_ GETNEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-112"><dt>**SNMP\_PDU\_GETNEXT**</dt></span></span> </dl>    | <span data-ttu-id="a1b5e-113">搜尋並取出 SNMP 變數的值，而不知道變數的確切名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-113">Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.</span></span><br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <span data-ttu-id="a1b5e-114"><dt>**SNMP \_ PDU \_ 回應**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-114"><dt>**SNMP\_PDU\_RESPONSE**</dt></span></span> </dl> | <span data-ttu-id="a1b5e-115">回復 SNMP \_ pdu \_ 取得或 snmp \_ pdu \_ GETNEXT 要求。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-115">Reply to an SNMP\_PDU\_GET or an SNMP\_PDU\_GETNEXT request.</span></span><br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <span data-ttu-id="a1b5e-116"><dt>**SNMP \_ PDU \_ 設定**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-116"><dt>**SNMP\_PDU\_SET**</dt></span></span> </dl>                | <span data-ttu-id="a1b5e-117">將值儲存在指定的 SNMP 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-117">Store a value in a specified SNMP variable.</span></span><br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <span data-ttu-id="a1b5e-118"><dt>**SNMP \_ PDU \_ V1TRAP**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-118"><dt>**SNMP\_PDU\_V1TRAP**</dt></span></span> </dl>       | <span data-ttu-id="a1b5e-119">指出 PDU 設陷格式化以符合 SNMPv1 標準。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-119">Indicates that the PDU trap is formatted to conform with the SNMPv1 standard.</span></span><br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <span data-ttu-id="a1b5e-120"><dt>**SNMP \_ PDU \_ GETBULK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-120"><dt>**SNMP\_PDU\_GETBULK**</dt></span></span> </dl>    | <span data-ttu-id="a1b5e-121">使用單一要求來搜尋和取出多個值。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-121">Search and retrieve multiple values with a single request.</span></span><br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <span data-ttu-id="a1b5e-122"><dt>**SNMP \_ PDU \_ 通知**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-122"><dt>**SNMP\_PDU\_INFORM**</dt></span></span> </dl>       | <span data-ttu-id="a1b5e-123">表示通知要求 PDU。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-123">Indicates an inform request PDU.</span></span><br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <span data-ttu-id="a1b5e-124"><dt>**SNMP \_ PDU \_ 陷阱**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-124"><dt>**SNMP\_PDU\_TRAP**</dt></span></span> </dl>             | <span data-ttu-id="a1b5e-125">警示管理系統在 SNMPv2C 下的特殊事件。</span><span class="sxs-lookup"><span data-stu-id="a1b5e-125">Alerts the management system to an extraordinary event under SNMPv2C.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="a1b5e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1b5e-126">Requirements</span></span>



| <span data-ttu-id="a1b5e-127">需求</span><span class="sxs-lookup"><span data-stu-id="a1b5e-127">Requirement</span></span> | <span data-ttu-id="a1b5e-128">值</span><span class="sxs-lookup"><span data-stu-id="a1b5e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a1b5e-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1b5e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b5e-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1b5e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="a1b5e-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1b5e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b5e-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1b5e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a1b5e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a1b5e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1b5e-134"><dt>Snmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b5e-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b5e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1b5e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b5e-136">Simple Network Management Protocol (SNMP) 概觀</span><span class="sxs-lookup"><span data-stu-id="a1b5e-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="a1b5e-137">SNMP 參考</span><span class="sxs-lookup"><span data-stu-id="a1b5e-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="a1b5e-138">SNMP 常數</span><span class="sxs-lookup"><span data-stu-id="a1b5e-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

