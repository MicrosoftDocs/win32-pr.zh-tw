---
description: 相互關聯會影響從 SMIR 傳回的一組類別。
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: WMI SNMP 類別相互關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192186"
---
# <a name="wmi-snmp-class-correlation"></a><span data-ttu-id="51ec8-103">WMI SNMP 類別相互關聯</span><span class="sxs-lookup"><span data-stu-id="51ec8-103">WMI SNMP Class Correlation</span></span>

<span data-ttu-id="51ec8-104">相互關聯會影響從 SMIR 傳回的一組類別。</span><span class="sxs-lookup"><span data-stu-id="51ec8-104">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="51ec8-105">相互關聯的類別是指定的 SNMP 裝置在發生列舉時所能支援的類別。</span><span class="sxs-lookup"><span data-stu-id="51ec8-105">Correlated classes are those that a given SNMP device is known to support at the time enumeration occurs.</span></span> <span data-ttu-id="51ec8-106">Noncorrelated 列舉會傳回 SMIR 中所有出現的類別，不論裝置是否支援它們。</span><span class="sxs-lookup"><span data-stu-id="51ec8-106">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="51ec8-107">相互關聯是 WMI SNMP 提供者的一項功能，可以關閉或 (預設) 。</span><span class="sxs-lookup"><span data-stu-id="51ec8-107">Correlation is a feature of the WMI SNMP provider and can be turned off or on (default).</span></span>

> [!Note]  
> <span data-ttu-id="51ec8-108">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="51ec8-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="51ec8-109">相互關聯可能會讓您無法看到裝置實際支援的所有類別。</span><span class="sxs-lookup"><span data-stu-id="51ec8-109">Correlation might prevent you from seeing all of the classes that are actually supported by a device.</span></span> <span data-ttu-id="51ec8-110">如果您知道特定類別受到支援，但不會出現在 SMIR 中，這可能是因為下列幾個原因所致：其中一個是相互關聯。</span><span class="sxs-lookup"><span data-stu-id="51ec8-110">If you know that a particular class is supported but it does not appear in the SMIR, this could be due to several reasons, one of which is correlation.</span></span> <span data-ttu-id="51ec8-111">在寫入至有問題的裝置之前，請考慮關閉相互關聯。</span><span class="sxs-lookup"><span data-stu-id="51ec8-111">Consider turning correlation off before writing to the device in question.</span></span> <span data-ttu-id="51ec8-112">不過，關閉相互關聯可能會導致裝置不支援的許多類別會出現在 SMIR 中。</span><span class="sxs-lookup"><span data-stu-id="51ec8-112">However, turning correlation off results in the likelihood that many classes not supported by the device will appear in the SMIR.</span></span> <span data-ttu-id="51ec8-113">此外，使用相互關聯會產生效能成本，因為會查詢裝置以查看它所支援的類別。</span><span class="sxs-lookup"><span data-stu-id="51ec8-113">Also, there is a performance cost in using correlation because the device is queried to see what classes it supports.</span></span> <span data-ttu-id="51ec8-114">當相互關聯開啟時，SNMP 提供者會導致裝置支援類別的列舉，類似于執行 *mib 逐步* 解說工具的結果。</span><span class="sxs-lookup"><span data-stu-id="51ec8-114">When correlation is turned on, the SNMP provider causes an enumeration of device-supported classes similar to the result of running a *mib walk* tool.</span></span>

<span data-ttu-id="51ec8-115">例如，網路系統管理員想要知道特定網路中所有受管理中樞的幾個重要資料片段。</span><span class="sxs-lookup"><span data-stu-id="51ec8-115">For example, a network manager wants to know several key pieces of data about all the managed hubs in a particular network.</span></span> <span data-ttu-id="51ec8-116">目前裝置的資料庫及其支援的 Mib 已存在，因此不需要依賴裝置的相互關聯功能來提供支援的資料元素。</span><span class="sxs-lookup"><span data-stu-id="51ec8-116">A database of the current devices and their supported MIBs already exists, so there is no need to rely on the correlation function of the device to provide the supported data elements.</span></span> <span data-ttu-id="51ec8-117">在此情況下，相互關聯可能會關閉。</span><span class="sxs-lookup"><span data-stu-id="51ec8-117">In this case, correlation could be turned off.</span></span>

<span data-ttu-id="51ec8-118">下列範例顯示如何關閉相互關聯。</span><span class="sxs-lookup"><span data-stu-id="51ec8-118">The following example shows how to turn off correlation.</span></span>


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



<span data-ttu-id="51ec8-119">另一方面，另一個網路系統管理員可能會想要監視網路上的所有 UNIX 機器磁片磁碟機，但不熟悉這些機器上的 MIB 資料。</span><span class="sxs-lookup"><span data-stu-id="51ec8-119">On the other hand, another network manager may want to monitor all the UNIX machine disk drives on the network but is unfamiliar with the MIB data on those machines.</span></span> <span data-ttu-id="51ec8-120">在此情況下，相互關聯會開啟。</span><span class="sxs-lookup"><span data-stu-id="51ec8-120">In that case, correlation would be turned on.</span></span>

 

 



