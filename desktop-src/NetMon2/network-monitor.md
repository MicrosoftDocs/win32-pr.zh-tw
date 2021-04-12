---
description: 網路監視器會捕捉顯示和分析的網路流量。 它可讓您執行工作，例如分析先前在使用者定義方法中所捕獲的資料，以及從定義的通訊協定剖析器中提取資料。
ms.assetid: a70b6e22-e744-4760-b878-9ee35428fed5
title: 網路監視器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51a57dd2373d7a10fedd68a72dbc4021efdb921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513824"
---
# <a name="network-monitor"></a><span data-ttu-id="02440-104">網路監視器</span><span class="sxs-lookup"><span data-stu-id="02440-104">Network Monitor</span></span>

## <a name="purpose"></a><span data-ttu-id="02440-105">目的</span><span class="sxs-lookup"><span data-stu-id="02440-105">Purpose</span></span>

<span data-ttu-id="02440-106">網路監視器會捕捉顯示和分析的網路流量。</span><span class="sxs-lookup"><span data-stu-id="02440-106">Network Monitor captures network traffic for display and analysis.</span></span> <span data-ttu-id="02440-107">它可讓您執行工作，例如分析先前在使用者定義方法中所捕獲的資料，以及從定義的通訊協定剖析器中提取資料。</span><span class="sxs-lookup"><span data-stu-id="02440-107">It enables you to perform tasks such as analyzing previously captured data in user-defined methods and extract data from defined protocol parsers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="02440-108">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="02440-108">Developer audience</span></span>

<span data-ttu-id="02440-109">您可以使用 C/c + + 存取網路監視器所提供的所有 API 集。</span><span class="sxs-lookup"><span data-stu-id="02440-109">All API sets provided by Network Monitor can be accessed using C/C++.</span></span> <span data-ttu-id="02440-110">也可以使用網路封 [*包提供者*](n.md) 的開發人員也必須熟悉 COM。</span><span class="sxs-lookup"><span data-stu-id="02440-110">Those developers also working with [*network packet providers*](n.md) must also be familiar with COM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="02440-111">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="02440-111">Run-time requirements</span></span>

<span data-ttu-id="02440-112">若要從網路監視器 API 呼叫，您必須在 Windows NT Server 4.0、Windows 2000 Server 或 Windows Server 2003 上執行，或已安裝 Microsoft Systems Management Server。</span><span class="sxs-lookup"><span data-stu-id="02440-112">To call from the Network Monitor API, you must be running on Windows NT Server 4.0, Windows 2000 Server, or Windows Server 2003, or have Microsoft Systems Management Server installed.</span></span>

<span data-ttu-id="02440-113">NPP 驅動程式和支援的功能包括所有版本的 Windows NT 4.0 和 Windows 2000 伺服器。</span><span class="sxs-lookup"><span data-stu-id="02440-113">The NPP driver and supported features include all versions of Windows NT 4.0 and Windows 2000 Server.</span></span>

> [!Note]  
> <span data-ttu-id="02440-114">Windows Vista 和更新版本不支援網路監視器2.1 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="02440-114">Network Monitor 2.1 and earlier are not supported on Windows Vista and later.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="02440-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="02440-115">In this section</span></span>



| <span data-ttu-id="02440-116">主題</span><span class="sxs-lookup"><span data-stu-id="02440-116">Topic</span></span>                                                                 | <span data-ttu-id="02440-117">描述</span><span class="sxs-lookup"><span data-stu-id="02440-117">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02440-118">網路監視器 SDK</span><span class="sxs-lookup"><span data-stu-id="02440-118">The Network Monitor SDK</span></span>](the-network-monitor-sdk.md)<br/>     | <span data-ttu-id="02440-119">網路監視器 SDK 簡介。</span><span class="sxs-lookup"><span data-stu-id="02440-119">Introduction to the Network Monitor SDK.</span></span><br/>                                                   |
| [<span data-ttu-id="02440-120">關於網路監視器2。1</span><span class="sxs-lookup"><span data-stu-id="02440-120">About Network Monitor 2.1</span></span>](about-network-monitor-2-1.md)<br/> | <span data-ttu-id="02440-121">網路監視器的概念和服務。</span><span class="sxs-lookup"><span data-stu-id="02440-121">Network Monitor concepts and services.</span></span><br/>                                                     |
| [<span data-ttu-id="02440-122">使用網路監視器2。1</span><span class="sxs-lookup"><span data-stu-id="02440-122">Using Network Monitor 2.1</span></span>](using-network-monitor-2-1.md)<br/> | <span data-ttu-id="02440-123">工作相關的主題，描述如何使用網路監視器函式和 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="02440-123">Task-related topics that describe how to use Network Monitor functions and COM components.</span></span><br/> |
| [<span data-ttu-id="02440-124">參考</span><span class="sxs-lookup"><span data-stu-id="02440-124">Reference</span></span>](reference.md)<br/>                                 | <span data-ttu-id="02440-125">網路監視器的參考主題。</span><span class="sxs-lookup"><span data-stu-id="02440-125">Reference topics for Network Monitor.</span></span><br/>                                                      |
| [<span data-ttu-id="02440-126">詞彙</span><span class="sxs-lookup"><span data-stu-id="02440-126">Glossary</span></span>](glossary.md)<br/>                                   | <span data-ttu-id="02440-127">網路監視器的定義和術語。</span><span class="sxs-lookup"><span data-stu-id="02440-127">Definitions and terminology for Network Monitor.</span></span><br/>                                           |



 

 

 




