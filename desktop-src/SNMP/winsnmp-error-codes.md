---
title: WinSNMP 錯誤碼
description: WinSNMP 錯誤碼
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- WinSNMP 錯誤碼 SNMP
- 錯誤碼 SNMP、WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463569"
---
# <a name="winsnmp-error-codes"></a><span data-ttu-id="6c5bc-105">WinSNMP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6c5bc-105">WinSNMP Error Codes</span></span>

<span data-ttu-id="6c5bc-106">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c5bc-107">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6c5bc-108">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="6c5bc-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

> [!Note]  
> <span data-ttu-id="6c5bc-109">本主題所述的錯誤與相關 Rfc 所定義的 SNMP 錯誤碼不同。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-109">The errors described in this topic are distinct from the SNMP error codes defined by the relevant RFCs.</span></span>

 

<span data-ttu-id="6c5bc-110">如果函式失敗，所有的 WinSNMP 函數都會傳回值 **SNMPAPI \_ 失敗** 。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-110">All WinSNMP functions return the value **SNMPAPI\_FAILURE** if the function fails.</span></span> <span data-ttu-id="6c5bc-111">當 WinSNMP 函式失敗時，WinSNMP 應用程式必須立即呼叫 [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) 函式，以取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-111">The WinSNMP application must immediately call the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function to retrieve extended error information when a WinSNMP function fails.</span></span> <span data-ttu-id="6c5bc-112">下表列出的主題會討論由 WinSNMP 函數傳回的擴充錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-112">The following table lists topics that discuss extended error codes returned by WinSNMP functions.</span></span>



| <span data-ttu-id="6c5bc-113">主題</span><span class="sxs-lookup"><span data-stu-id="6c5bc-113">Topic</span></span>                                                        | <span data-ttu-id="6c5bc-114">描述</span><span class="sxs-lookup"><span data-stu-id="6c5bc-114">Description</span></span>                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="6c5bc-115">WinSNMP 一般錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6c5bc-115">WinSNMP Common Error Codes</span></span>](winsnmp-common-error-codes.md) | <span data-ttu-id="6c5bc-116">描述適用于 WinSNMP API 的常見錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-116">Describes common error codes for the WinSNMP API.</span></span>       |
| [<span data-ttu-id="6c5bc-117">網路傳輸錯誤</span><span class="sxs-lookup"><span data-stu-id="6c5bc-117">Network Transport Errors</span></span>](network-transport-errors.md)     | <span data-ttu-id="6c5bc-118">說明 WinSNMP API 的網路傳輸錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-118">Describes network transport errors for the WinSNMP API.</span></span> |



 

<span data-ttu-id="6c5bc-119">傳遞內容特定資訊的 WinSNMP 錯誤會包含在 [函數參考] 頁面中。</span><span class="sxs-lookup"><span data-stu-id="6c5bc-119">The WinSNMP errors that convey context-specific information are included in the function reference page.</span></span>

 

 