---
description: 方法提供者應該將 IWbemServices 實作為主要介面。 不過，純方法提供者只需要您執行 IWbemServices：： ExecMethodAsync 方法。
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: 執行方法提供者的主要介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998308"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a><span data-ttu-id="44ef2-104">執行方法提供者的主要介面</span><span class="sxs-lookup"><span data-stu-id="44ef2-104">Implementing the Primary Interface for a Method Provider</span></span>

<span data-ttu-id="44ef2-105">方法提供者應該將 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 實作為主要介面。</span><span class="sxs-lookup"><span data-stu-id="44ef2-105">A method provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="44ef2-106">不過，純方法提供者只需要您執行 [**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="44ef2-106">However, a pure method provider requires only that you implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method.</span></span>

<span data-ttu-id="44ef2-107">由於其他提供者會使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)，因此介面包含許多與純方法提供者無關的方法。</span><span class="sxs-lookup"><span data-stu-id="44ef2-107">Because other providers use [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), the interface contains many methods that are irrelevant to a pure method provider.</span></span> <span data-ttu-id="44ef2-108">單純的方法提供者應該提供存根執行，以傳回 \_ \_ \_ 無法 \_ 用於 [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)以外所有其他 **IWbemServices** 方法的 WBEM E 提供者。</span><span class="sxs-lookup"><span data-stu-id="44ef2-108">Your pure method provider should supply a stub implementation that returns WBEM\_E\_PROVIDER\_NOT\_CAPABLE for all of other **IWbemServices** methods besides [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span> <span data-ttu-id="44ef2-109">不過，許多方法提供者也會作為實例或類別提供者。</span><span class="sxs-lookup"><span data-stu-id="44ef2-109">However, many method providers also serve as instance or class providers.</span></span> <span data-ttu-id="44ef2-110">組合方法和執行個體提供者必須支援更多的 **IWbemServices** 方法。</span><span class="sxs-lookup"><span data-stu-id="44ef2-110">Combination method and instance providers must support more of the **IWbemServices** methods.</span></span>

 

 



