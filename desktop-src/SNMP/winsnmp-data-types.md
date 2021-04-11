---
title: WinSNMP 資料類型
description: 標準的 WinSNMP 資料類型是在 WINSNMP 中定義。H file。
ms.assetid: 20f1bbc3-5a08-4206-980d-22a794cda402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7061ade6f9b69c63ba4718d9d79bbd4d39c67b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023971"
---
# <a name="winsnmp-data-types"></a><span data-ttu-id="6338b-103">WinSNMP 資料類型</span><span class="sxs-lookup"><span data-stu-id="6338b-103">WinSNMP Data Types</span></span>

<span data-ttu-id="6338b-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6338b-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6338b-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="6338b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6338b-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="6338b-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="6338b-107">標準的 WinSNMP 資料類型是在 WINSNMP 中定義。H file。</span><span class="sxs-lookup"><span data-stu-id="6338b-107">The standard WinSNMP data types are defined in the WINSNMP.H file.</span></span>

<span data-ttu-id="6338b-108">請注意，WinSNMP 指定一些具有帶正負號長整數類型 **smiINT** 的參數。</span><span class="sxs-lookup"><span data-stu-id="6338b-108">Note that WinSNMP specifies some parameters with the signed long integer type, **smiINT**.</span></span> <span data-ttu-id="6338b-109">這可讓 WinSNMP 符合相關 Rfc 中定義的資料元素，特別是 PDU 元件。</span><span class="sxs-lookup"><span data-stu-id="6338b-109">This enables WinSNMP to comply with the data elements, especially the PDU components, defined in the relevant RFCs.</span></span>

 

 