---
title: 'SNMPv1 陷阱類型 (Snmp. h) '
description: SNMPv1 陷阱類型會描述一組預先定義的一般陷阱類型，其格式化為符合 SNMPv1 陷阱 PDU 標準。
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844327"
---
# <a name="snmpv1-trap-types"></a><span data-ttu-id="ebdc3-103">SNMPv1 陷阱類型</span><span class="sxs-lookup"><span data-stu-id="ebdc3-103">SNMPv1 Trap Types</span></span>

<span data-ttu-id="ebdc3-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ebdc3-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ebdc3-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="ebdc3-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="ebdc3-107">SNMPv1 陷阱類型會描述一組預先定義的一般陷阱類型，其格式化為符合 SNMPv1 陷阱 PDU 標準。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-107">The SNMPv1 trap types describe a predefined set of generic trap types that are formatted to comply with the SNMPv1 trap PDU standard.</span></span>



| <span data-ttu-id="ebdc3-108">常數</span><span class="sxs-lookup"><span data-stu-id="ebdc3-108">Constant</span></span>                                                                                                                                                                                                          | <span data-ttu-id="ebdc3-109">描述</span><span class="sxs-lookup"><span data-stu-id="ebdc3-109">Description</span></span>                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <span data-ttu-id="ebdc3-110"><dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc3-110"><dt>**SNMP\_GENERICTRAP\_COLDSTART**</dt></span></span> </dl>             | <span data-ttu-id="ebdc3-111">表示冷啟動陷阱。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-111">Indicates a cold start trap.</span></span> <span data-ttu-id="ebdc3-112">代理程式正在以 managed 模式初始化通訊協定實體。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-112">The agent is initializing protocol entities on the managed mode.</span></span> <span data-ttu-id="ebdc3-113">它可能會改變其視圖中的物件。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-113">It may alter objects in its view.</span></span><br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <span data-ttu-id="ebdc3-114"><dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc3-114"><dt>**SNMP\_GENERICTRAP\_WARMSTART**</dt></span></span> </dl>             | <span data-ttu-id="ebdc3-115">表示暖啟動陷阱。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-115">Indicates a warm start trap.</span></span> <span data-ttu-id="ebdc3-116">代理程式正在重新初始化本身，但是它不會改變其視圖中的物件。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-116">The agent is reinitializing itself but it will not alter objects in its view.</span></span><br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <span data-ttu-id="ebdc3-117"><dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc3-117"><dt>**SNMP\_GENERICTRAP\_LINKDOWN**</dt></span></span> </dl>                | <span data-ttu-id="ebdc3-118">表示連結中斷的陷阱。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-118">Indicates a link-down trap.</span></span> <span data-ttu-id="ebdc3-119">附加的介面已從 up 狀態變更為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-119">An attached interface has changed from the up state to the down state.</span></span> <span data-ttu-id="ebdc3-120">變數系結清單中的第一個變數會識別介面。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-120">The first variable in the variable bindings list identifies the interface.</span></span><br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <span data-ttu-id="ebdc3-121"><dt>**SNMP \_ GENERICTRAP \_ LINKUP**</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc3-121"><dt>**SNMP\_GENERICTRAP\_LINKUP**</dt></span></span> </dl>                      | <span data-ttu-id="ebdc3-122">指出連結的設陷。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-122">Indicates a link-up trap.</span></span> <span data-ttu-id="ebdc3-123">附加的介面已從下開始變更為啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-123">An attached interface has changed from the down start to the up state.</span></span> <span data-ttu-id="ebdc3-124">變數系結清單中的第一個變數會識別介面。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-124">The first variable in the variable bindings list identifies the interface.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <span data-ttu-id="ebdc3-125"><dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc3-125"><dt>**SNMP\_GENERICTRAP\_AUTHFAILURE**</dt></span></span> </dl>       | <span data-ttu-id="ebdc3-126">指出驗證失敗的陷阱。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-126">Indicates an authentication failure trap.</span></span> <span data-ttu-id="ebdc3-127">SNMP 實體已傳送 SNMP 訊息，但其已宣告為屬於已知的社區。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-127">An SNMP entity has sent an SNMP message, but it has falsely claimed to belong to a known community.</span></span><br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <span data-ttu-id="ebdc3-128"><dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc3-128"><dt>**SNMP\_GENERICTRAP\_EGPNEIGHLOSS**</dt></span></span> </dl>    | <span data-ttu-id="ebdc3-129">表示 EGP 鄰居遺失陷阱。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-129">Indicates an EGP neighbor loss trap.</span></span> <span data-ttu-id="ebdc3-130">EGP 對等已變更為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-130">An EGP peer has changed to the down state.</span></span> <span data-ttu-id="ebdc3-131">變數系結清單中的第一個變數會識別 EGP 對等互連的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-131">The first variable in the variable bindings list identifies the IP address of the EGP peer.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <span data-ttu-id="ebdc3-132"><dt>**SNMP \_ GENERICTRAP \_ ENTERSPECIFIC**</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc3-132"><dt>**SNMP\_GENERICTRAP\_ENTERSPECIFIC**</dt></span></span> </dl> | <span data-ttu-id="ebdc3-133">表示企業特定的陷阱。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-133">Indicates an enterprise-specific trap.</span></span> <span data-ttu-id="ebdc3-134">發生特殊事件。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-134">An extraordinary event has occurred.</span></span> <span data-ttu-id="ebdc3-135">它是在 *specificTrap* 參數中以企業特定值識別。</span><span class="sxs-lookup"><span data-stu-id="ebdc3-135">It is identified in the *specificTrap* parameter with an enterprise-specific value.</span></span><br/>               |



## <a name="requirements"></a><span data-ttu-id="ebdc3-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebdc3-136">Requirements</span></span>



| <span data-ttu-id="ebdc3-137">需求</span><span class="sxs-lookup"><span data-stu-id="ebdc3-137">Requirement</span></span> | <span data-ttu-id="ebdc3-138">值</span><span class="sxs-lookup"><span data-stu-id="ebdc3-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ebdc3-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebdc3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ebdc3-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebdc3-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="ebdc3-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebdc3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ebdc3-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebdc3-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ebdc3-143">標頭</span><span class="sxs-lookup"><span data-stu-id="ebdc3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebdc3-144"><dt>Snmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc3-144"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebdc3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebdc3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebdc3-146">Simple Network Management Protocol (SNMP) 概觀</span><span class="sxs-lookup"><span data-stu-id="ebdc3-146">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="ebdc3-147">SNMP 參考</span><span class="sxs-lookup"><span data-stu-id="ebdc3-147">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="ebdc3-148">SNMP 常數</span><span class="sxs-lookup"><span data-stu-id="ebdc3-148">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

