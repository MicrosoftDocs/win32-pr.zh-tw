---
title: WinSNMP 結構
description: WinSNMP API 函數會使用下列結構。
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP 結構 SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842488"
---
# <a name="winsnmp-structures"></a><span data-ttu-id="5c27e-104">WinSNMP 結構</span><span class="sxs-lookup"><span data-stu-id="5c27e-104">WinSNMP Structures</span></span>

<span data-ttu-id="5c27e-105">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5c27e-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5c27e-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5c27e-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5c27e-107">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="5c27e-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="5c27e-108">WinSNMP API 函數會使用下列結構。</span><span class="sxs-lookup"><span data-stu-id="5c27e-108">The WinSNMP API functions use the following structures.</span></span>



| <span data-ttu-id="5c27e-109">結構</span><span class="sxs-lookup"><span data-stu-id="5c27e-109">Structure</span></span>                                  | <span data-ttu-id="5c27e-110">Description</span><span class="sxs-lookup"><span data-stu-id="5c27e-110">Description</span></span>                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c27e-111">**smiCNTR64**</span><span class="sxs-lookup"><span data-stu-id="5c27e-111">**smiCNTR64**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | <span data-ttu-id="5c27e-112">包含代表計數器的64位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="5c27e-112">Contains a 64-bit unsigned integer value that represents a counter.</span></span>                                                    |
| [<span data-ttu-id="5c27e-113">**smiOCTETS**</span><span class="sxs-lookup"><span data-stu-id="5c27e-113">**smiOCTETS**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | <span data-ttu-id="5c27e-114">包含變數長度的 SNMP 八位字串指標。</span><span class="sxs-lookup"><span data-stu-id="5c27e-114">Contains a pointer to an SNMP octet string of variable length.</span></span>                                                         |
| [<span data-ttu-id="5c27e-115">**smiOID**</span><span class="sxs-lookup"><span data-stu-id="5c27e-115">**smiOID**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | <span data-ttu-id="5c27e-116">包含與指定的命名物件相關聯之 subidentifiers 的可變長度陣列指標。</span><span class="sxs-lookup"><span data-stu-id="5c27e-116">Contains a pointer to a variable length array of the subidentifiers that are associated with a specified named object.</span></span> |
| [<span data-ttu-id="5c27e-117">**smiVALUE**</span><span class="sxs-lookup"><span data-stu-id="5c27e-117">**smiVALUE**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | <span data-ttu-id="5c27e-118">表示與變數系結專案中的變數名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="5c27e-118">Represents the value that is associated with a variable name in a variable binding entry.</span></span>                              |
| [<span data-ttu-id="5c27e-119">**smiVENDORINFO**</span><span class="sxs-lookup"><span data-stu-id="5c27e-119">**smiVENDORINFO**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | <span data-ttu-id="5c27e-120">包含 Microsoft 的 WinSNMP 執行相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5c27e-120">Contains information about the Microsoft implementation of WinSNMP.</span></span>                                                    |



 

 

 