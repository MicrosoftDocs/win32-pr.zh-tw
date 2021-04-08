---
description: 視圖提供者是實例和方法提供者，可根據其他類別的實例建立新的類別。
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: 視圖提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850747"
---
# <a name="view-provider"></a><span data-ttu-id="ff723-103">視圖提供者</span><span class="sxs-lookup"><span data-stu-id="ff723-103">View Provider</span></span>

<span data-ttu-id="ff723-104">視圖提供者是實例和方法提供者，可根據其他類別的實例建立新的類別。</span><span class="sxs-lookup"><span data-stu-id="ff723-104">The View provider is an instance and method provider that creates new classes based on instances of other classes.</span></span> <span data-ttu-id="ff723-105">您可以使用視圖提供者，從不同的來源類別、不同的命名空間或不同的電腦取得屬性，並將屬性結合成單一類別。</span><span class="sxs-lookup"><span data-stu-id="ff723-105">You can use the View provider to take properties from different source classes, different namespaces, or different computers and combine the properties as a single class.</span></span>

<span data-ttu-id="ff723-106">作為實例和方法提供者，視圖提供者支援標準 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面和下列 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 方法：</span><span class="sxs-lookup"><span data-stu-id="ff723-106">As an instance and method provider, the View provider supports the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface and the following [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="ff723-107">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="ff723-107">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="ff723-108">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="ff723-108">**ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="ff723-109">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="ff723-109">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="ff723-110">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="ff723-110">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="ff723-111">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="ff723-111">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="ff723-112">如需有關用來定義 View 提供者類別之限定詞的詳細資訊，請參閱 [View provider 的特定限定詞](qualifiers-specific-to-the-view-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="ff723-112">For more information about the qualifiers use to define View provider classes, see [Qualifiers Specific to the View Provider](qualifiers-specific-to-the-view-provider.md).</span></span>

<span data-ttu-id="ff723-113">如需有關 views 的詳細資訊，請參閱將 [類別連結在一起](linking-classes-together.md)。</span><span class="sxs-lookup"><span data-stu-id="ff723-113">For more information about views, see [Linking Classes Together](linking-classes-together.md).</span></span>

<span data-ttu-id="ff723-114">64位平臺上有兩個版本的 View provider。</span><span class="sxs-lookup"><span data-stu-id="ff723-114">Two versions of the View provider are available on 64-bit platforms.</span></span> <span data-ttu-id="ff723-115">如需詳細資訊，請參閱 [在64位電腦上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="ff723-115">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="ff723-116">視圖提供者會在 ViewProv.dll 中執行。</span><span class="sxs-lookup"><span data-stu-id="ff723-116">The View provider is implemented in ViewProv.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff723-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff723-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff723-118">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="ff723-118">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



