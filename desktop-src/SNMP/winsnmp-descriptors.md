---
title: WinSNMP 描述項
description: 在 WinSNMP 程式設計環境中，描述項是下列兩個結構的其中一個。
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300280"
---
# <a name="winsnmp-descriptors"></a><span data-ttu-id="63362-103">WinSNMP 描述項</span><span class="sxs-lookup"><span data-stu-id="63362-103">WinSNMP Descriptors</span></span>

<span data-ttu-id="63362-104">在 WinSNMP 程式設計環境中， *描述* 項是下列兩個結構的其中一個：</span><span class="sxs-lookup"><span data-stu-id="63362-104">In the WinSNMP programming environment a *descriptor* is one of the following two structures:</span></span>

-   <span data-ttu-id="63362-105">描述八進位字串變數的 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 結構</span><span class="sxs-lookup"><span data-stu-id="63362-105">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure which describes an octet string variable</span></span>
-   <span data-ttu-id="63362-106">描述 SNMP 物件識別碼變數的 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 結構</span><span class="sxs-lookup"><span data-stu-id="63362-106">An [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure which describes an SNMP object identifier variable</span></span>

<span data-ttu-id="63362-107">WinSNMP 描述元是具有兩個成員的結構：長度成員、 **len** 和指標成員、 **ptr**。</span><span class="sxs-lookup"><span data-stu-id="63362-107">A WinSNMP descriptor is a structure that has two members: a length member, **len**, and a pointer member, **ptr**.</span></span> <span data-ttu-id="63362-108">**Ptr** 成員指向所需的八位字串或物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="63362-108">The **ptr** member points to the octet string or object identifier of interest.</span></span> <span data-ttu-id="63362-109">**Ptr** 成員可以是 **smiLPBYTE** 或 **smiLPUINT32** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="63362-109">The **ptr** member can be either the **smiLPBYTE** or **smiLPUINT32** data type.</span></span>

<span data-ttu-id="63362-110">[**SmiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)描述元或 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)描述元可以是 **smiVALUE** 結構的 **值** 成員。</span><span class="sxs-lookup"><span data-stu-id="63362-110">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor or an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) descriptor can be the **value** member of an **smiVALUE** structure.</span></span> <span data-ttu-id="63362-111">[**SmiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)結構描述與變數系結專案中的變數名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="63362-111">The [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure describes the value associated with a variable name in a variable binding entry.</span></span>

<span data-ttu-id="63362-112">Microsoft WinSNMP 執行會為所有輸出 **smiOCTETS** 和 **smiOID** 結構配置和解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="63362-112">The Microsoft WinSNMP implementation allocates and deallocates memory for all output **smiOCTETS** and **smiOID** structures.</span></span> <span data-ttu-id="63362-113">因此，應用程式必須呼叫 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) 函式，以釋放這些結構的 **ptr** 成員記憶體。</span><span class="sxs-lookup"><span data-stu-id="63362-113">Therefore, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free the memory for the **ptr** member of these structures.</span></span>

<span data-ttu-id="63362-114">描述項中的字串成員不需要 **Null** 終止位元組。</span><span class="sxs-lookup"><span data-stu-id="63362-114">String members in descriptors do not require a **NULL** terminating byte.</span></span> <span data-ttu-id="63362-115">如需管理配置給描述項之記憶體的詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="63362-115">For additional information about managing the memory allocated for descriptors, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




