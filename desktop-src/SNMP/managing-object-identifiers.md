---
title: 管理物件識別碼
description: WinSNMP API 提供數個可簡化對 WinSNMP 應用程式之物件識別碼操作的 WinSNMP 公用程式函式。
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462408"
---
# <a name="managing-object-identifiers"></a><span data-ttu-id="a45c3-103">管理物件識別碼</span><span class="sxs-lookup"><span data-stu-id="a45c3-103">Managing Object Identifiers</span></span>

<span data-ttu-id="a45c3-104">WinSNMP API 提供數個可簡化對 WinSNMP 應用程式之物件識別碼操作的 [winsnmp 公用程式](winsnmp-functions.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="a45c3-104">The WinSNMP API provides several [WinSNMP utility functions](winsnmp-functions.md) that simplify the manipulation of object identifiers for WinSNMP applications.</span></span>

<span data-ttu-id="a45c3-105">[**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)函式會將物件識別碼的內部二進位標記法轉換為其點數位字串格式。</span><span class="sxs-lookup"><span data-stu-id="a45c3-105">The [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) function converts the internal binary representation of an object identifier to its dotted numeric string format.</span></span> <span data-ttu-id="a45c3-106">當您呼叫 [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)時，請將 MAXOBJIDSTRSIZE 長度的字串緩衝區指定 (1408 個位元組) ，以確保輸出緩衝區夠大，足以容納轉換的字串。</span><span class="sxs-lookup"><span data-stu-id="a45c3-106">When you call [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specify a string buffer of MAXOBJIDSTRSIZE length (1408 bytes) to ensure that the output buffer is large enough to hold the converted string.</span></span> <span data-ttu-id="a45c3-107">若要將物件識別碼從點數位字串格式轉換為其內部二進位標記法，請呼叫 [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) 函式。</span><span class="sxs-lookup"><span data-stu-id="a45c3-107">To convert an object identifier from the dotted numeric string format to its internal binary representation, call the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) function.</span></span>

<span data-ttu-id="a45c3-108">若要複製 SNMP 物件識別碼，請呼叫 [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) 函數。</span><span class="sxs-lookup"><span data-stu-id="a45c3-108">To copy an SNMP object identifier call the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) function.</span></span> <span data-ttu-id="a45c3-109">此函式會為新的物件識別碼配置任何必要的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a45c3-109">This function allocates any necessary memory for the new object identifier.</span></span>

<span data-ttu-id="a45c3-110">WinSNMP 應用程式必須呼叫 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)函式，以釋出針對 [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)和 [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)函數所指定之 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)結構的 **ptr** 成員所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="a45c3-110">A WinSNMP application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free resources allocated for the **ptr** member of the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure specified by both the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) and the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) functions.</span></span>

<span data-ttu-id="a45c3-111">[**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)函式會比較兩個 SNMP 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a45c3-111">The [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) function compares two SNMP object identifiers.</span></span> <span data-ttu-id="a45c3-112">WinSNMP 應用程式可以指定要比較的 subidentifiers 數目。</span><span class="sxs-lookup"><span data-stu-id="a45c3-112">The WinSNMP application can specify the number of subidentifiers to compare.</span></span> <span data-ttu-id="a45c3-113">呼叫 **SnmpOidCompare** 來判斷兩個物件識別碼是否有常見的前置詞。</span><span class="sxs-lookup"><span data-stu-id="a45c3-113">Call **SnmpOidCompare** to determine whether two object identifiers have common prefixes.</span></span>

<span data-ttu-id="a45c3-114">如需管理配置給物件識別碼之記憶體的詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="a45c3-114">For additional information about managing the memory allocated for object identifiers, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




