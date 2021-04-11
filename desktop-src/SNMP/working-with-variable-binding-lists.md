---
title: 使用變數系結清單
description: 變數系結是 SNMP 物件實例名稱與關聯值的配對。 變數系結清單是一系列的變數系結專案。 在 WinSNMP 中，通訊協定資料單位 (PDU) 包含變數系結清單。
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- 使用變數系結清單 SNMP
- 變數系結清單 SNMP，SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103681450"
---
# <a name="working-with-variable-binding-lists"></a><span data-ttu-id="235d6-107">使用變數系結清單</span><span class="sxs-lookup"><span data-stu-id="235d6-107">Working with Variable Binding Lists</span></span>

<span data-ttu-id="235d6-108">*變數* 系結是 SNMP 物件實例名稱與關聯值的配對。</span><span class="sxs-lookup"><span data-stu-id="235d6-108">A *variable binding* is the pairing of an SNMP object instance name with an associated value.</span></span> <span data-ttu-id="235d6-109">變數系結 *清單* 是一系列的變數系結專案。</span><span class="sxs-lookup"><span data-stu-id="235d6-109">A *variable binding list* is a series of variable binding entries.</span></span> <span data-ttu-id="235d6-110">在 WinSNMP 中，通訊協定資料單位 (PDU) 包含變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="235d6-110">In WinSNMP, a protocol data unit (PDU) includes a variable binding list.</span></span>

<span data-ttu-id="235d6-111">變數系結清單結構的詳細資料僅限於 Microsoft 的 WinSNMP 實行。</span><span class="sxs-lookup"><span data-stu-id="235d6-111">The details of the variable binding list structure are restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="235d6-112">WinSNMP 應用程式可以使用 **HSNMP \_ VBL** 類型的控制碼來存取變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="235d6-112">A WinSNMP application can access a variable binding list with a handle of type **HSNMP\_VBL**.</span></span> <span data-ttu-id="235d6-113">如需詳細資訊，請參閱 [資源控制碼物件](resource-handle-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="235d6-113">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="235d6-114">WinSNMP 應用程式可以建立和操作變數系結清單，並將它們包含在 Pdu 中。</span><span class="sxs-lookup"><span data-stu-id="235d6-114">The WinSNMP application can construct and manipulate variable binding lists, and include them in PDUs.</span></span> <span data-ttu-id="235d6-115">若要執行這些作業，應用程式會使用 WinSNMP [變數](winsnmp-functions.md)系結函式。</span><span class="sxs-lookup"><span data-stu-id="235d6-115">To perform these operations, the application uses the WinSNMP [variable binding functions](winsnmp-functions.md).</span></span> <span data-ttu-id="235d6-116">如需使用 WinSNMP 和變數系結清單的詳細資訊，請參閱下表所列的主題。</span><span class="sxs-lookup"><span data-stu-id="235d6-116">For more information about working with WinSNMP and variable binding lists, see the topics listed in the following table.</span></span>



| <span data-ttu-id="235d6-117">主題</span><span class="sxs-lookup"><span data-stu-id="235d6-117">Topic</span></span>                                                                    | <span data-ttu-id="235d6-118">描述</span><span class="sxs-lookup"><span data-stu-id="235d6-118">Description</span></span>                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="235d6-119">建立變數系結清單</span><span class="sxs-lookup"><span data-stu-id="235d6-119">Creating a Variable Binding List</span></span>](creating-a-variable-binding-list.md) | <span data-ttu-id="235d6-120">描述如何建立變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="235d6-120">Describes how to create a variable binding list.</span></span> |
| [<span data-ttu-id="235d6-121">管理變數系結清單</span><span class="sxs-lookup"><span data-stu-id="235d6-121">Managing a Variable Binding List</span></span>](managing-a-variable-binding-list.md) | <span data-ttu-id="235d6-122">說明如何管理變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="235d6-122">Describes how to manage a variable binding list.</span></span> |



 

<span data-ttu-id="235d6-123">如需變數系結和變數系結清單的詳細資訊，請參閱 [RFC1905](https://www.ietf.org/rfc/rfc1905.txt)「簡易網路管理通訊協定第2版的通訊協定作業 (SNMPv2) 」和「WinSNMP [變數](winsnmp-functions.md)系結函式」。</span><span class="sxs-lookup"><span data-stu-id="235d6-123">For more information about variable bindings and variable binding lists, see [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protocol Operations for Version 2 of the Simple Network Management Protocol (SNMPv2)," and the WinSNMP [Variable Binding Functions](winsnmp-functions.md).</span></span>

 

 




