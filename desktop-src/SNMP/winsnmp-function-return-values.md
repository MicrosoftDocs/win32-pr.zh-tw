---
title: WinSNMP 函數傳回值
description: 來自 WinSNMP 函式呼叫的傳回值可以是 Microsoft WinSNMP 執行為 WinSNMP 應用程式佈建之資源的控制碼。
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023970"
---
# <a name="winsnmp-function-return-values"></a><span data-ttu-id="b1911-103">WinSNMP 函數傳回值</span><span class="sxs-lookup"><span data-stu-id="b1911-103">WinSNMP Function Return Values</span></span>

<span data-ttu-id="b1911-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b1911-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b1911-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b1911-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b1911-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="b1911-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b1911-107">來自 WinSNMP 函式呼叫的傳回值可以是 Microsoft WinSNMP 執行為 WinSNMP 應用程式佈建之資源的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b1911-107">The return value from a WinSNMP function call can be a handle to a resource that the Microsoft WinSNMP implementation allocates for the WinSNMP application.</span></span>

<span data-ttu-id="b1911-108">下表列出此執行所配置的五種資源控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="b1911-108">The following table lists the five types of resource handles that the implementation allocates.</span></span>



| <span data-ttu-id="b1911-109">控制碼類型</span><span class="sxs-lookup"><span data-stu-id="b1911-109">Handle type</span></span>    | <span data-ttu-id="b1911-110">Description</span><span class="sxs-lookup"><span data-stu-id="b1911-110">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="b1911-111">HSNMP \_ 會話</span><span class="sxs-lookup"><span data-stu-id="b1911-111">HSNMP\_SESSION</span></span> | <span data-ttu-id="b1911-112">對 WinSNMP 會話的處理</span><span class="sxs-lookup"><span data-stu-id="b1911-112">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="b1911-113">HSNMP \_ 實體</span><span class="sxs-lookup"><span data-stu-id="b1911-113">HSNMP\_ENTITY</span></span>  | <span data-ttu-id="b1911-114">SNMP 實體的控制碼</span><span class="sxs-lookup"><span data-stu-id="b1911-114">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="b1911-115">HSNMP \_ 內容</span><span class="sxs-lookup"><span data-stu-id="b1911-115">HSNMP\_CONTEXT</span></span> | <span data-ttu-id="b1911-116">SNMP 內容的控制碼</span><span class="sxs-lookup"><span data-stu-id="b1911-116">Handle to an SNMP context</span></span>         |
| <span data-ttu-id="b1911-117">HSNMP \_ PDU</span><span class="sxs-lookup"><span data-stu-id="b1911-117">HSNMP\_PDU</span></span>     | <span data-ttu-id="b1911-118">通訊協定資料單位的控制碼</span><span class="sxs-lookup"><span data-stu-id="b1911-118">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="b1911-119">HSNMP \_ VBL</span><span class="sxs-lookup"><span data-stu-id="b1911-119">HSNMP\_VBL</span></span>     | <span data-ttu-id="b1911-120">變數系結清單的控制碼</span><span class="sxs-lookup"><span data-stu-id="b1911-120">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="b1911-121">如需詳細資訊，請參閱 [資源控制碼物件](resource-handle-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="b1911-121">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="b1911-122">傳回值也可以是代表 SNMPAPI 狀態值之 **smiUINT32** 類型的不帶正負號長整數值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b1911-122">The return value can also be an unsigned long integer value of the **smiUINT32** type that represents an SNMPAPI\_STATUS value.</span></span>

<span data-ttu-id="b1911-123">下表列出的是 WinSNMP 狀態值及其意義。</span><span class="sxs-lookup"><span data-stu-id="b1911-123">The following table lists the WinSNMP status values and their meaning.</span></span>



| <span data-ttu-id="b1911-124">狀態</span><span class="sxs-lookup"><span data-stu-id="b1911-124">Status</span></span>           | <span data-ttu-id="b1911-125">描述</span><span class="sxs-lookup"><span data-stu-id="b1911-125">Description</span></span>                                                                      |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b1911-126">SNMPAPI \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="b1911-126">SNMPAPI\_FAILURE</span></span> | <span data-ttu-id="b1911-127">表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b1911-127">Indicates an error.</span></span> <span data-ttu-id="b1911-128">等於0或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b1911-128">Equates to 0 or **NULL**.</span></span>                                    |
| <span data-ttu-id="b1911-129">SNMPAPI \_ 成功</span><span class="sxs-lookup"><span data-stu-id="b1911-129">SNMPAPI\_SUCCESS</span></span> | <span data-ttu-id="b1911-130">表示函式已順利完成。</span><span class="sxs-lookup"><span data-stu-id="b1911-130">Indicates the function completed successfully.</span></span> <span data-ttu-id="b1911-131">等於1或正計數。</span><span class="sxs-lookup"><span data-stu-id="b1911-131">Equates to 1 or a positive count.</span></span> |



 

 

 