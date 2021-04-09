---
description: 用來保存登錄資料的類別會以數個標準限定詞來定義。
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: 使用限定詞定義登錄類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848745"
---
# <a name="defining-a-registry-class-with-qualifiers"></a><span data-ttu-id="7a510-103">使用限定詞定義登錄類別</span><span class="sxs-lookup"><span data-stu-id="7a510-103">Defining a Registry Class With Qualifiers</span></span>

<span data-ttu-id="7a510-104">用來保存登錄資料的類別會以數個標準限定詞來定義。</span><span class="sxs-lookup"><span data-stu-id="7a510-104">The classes used to hold registry data are defined with several standard qualifiers.</span></span>

<span data-ttu-id="7a510-105">以下是標準限定詞的清單：</span><span class="sxs-lookup"><span data-stu-id="7a510-105">The following is a list of the standard qualifiers:</span></span>

-   <span data-ttu-id="7a510-106">[動態](standard-wmi-qualifiers.md) 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="7a510-106">[Dynamic](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>

    <span data-ttu-id="7a510-107">您可以將 **動態** 限定詞附加至類別或實例。</span><span class="sxs-lookup"><span data-stu-id="7a510-107">You can attach the **Dynamic** qualifier to either a class or an instance.</span></span> <span data-ttu-id="7a510-108">**動態** 辨識符號會將類別或實例標示為由提供者動態管理。</span><span class="sxs-lookup"><span data-stu-id="7a510-108">The **Dynamic** qualifier marks the class or instance as managed dynamically by a provider.</span></span> <span data-ttu-id="7a510-109">當 **動態** 出現在類別或實例上時，也必須顯示 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 限定詞。</span><span class="sxs-lookup"><span data-stu-id="7a510-109">When **Dynamic** appears on a class or instance, the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier must also appear.</span></span> <span data-ttu-id="7a510-110">**提供者** 辨識符號會識別必須管理動態類別或實例的特定提供者。</span><span class="sxs-lookup"><span data-stu-id="7a510-110">The **Provider** qualifier identifies the particular provider that must manage the dynamic class or instance.</span></span>

-   [<span data-ttu-id="7a510-111">ClassCoNtext</span><span class="sxs-lookup"><span data-stu-id="7a510-111">ClassContext</span></span>](standard-wmi-qualifiers.md)

    <span data-ttu-id="7a510-112">**ClassCoNtext** 限定詞會附加至類別。</span><span class="sxs-lookup"><span data-stu-id="7a510-112">The **ClassContext** qualifier is attached to a class.</span></span> <span data-ttu-id="7a510-113">它會指定包含類別所代表之資訊的登錄機碼路徑。</span><span class="sxs-lookup"><span data-stu-id="7a510-113">It specifies the path to the registry key that contains the information the class represents.</span></span>

    <span data-ttu-id="7a510-114">**ClassCoNtext** 限定詞的格式如下。</span><span class="sxs-lookup"><span data-stu-id="7a510-114">The **ClassContext** qualifier has the following format.</span></span>

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    <span data-ttu-id="7a510-115">如果 KeyPath 的值包含含有子機碼的索引鍵，則其值可能很長。</span><span class="sxs-lookup"><span data-stu-id="7a510-115">The value for KeyPath can be long if it includes keys with subkeys.</span></span>

    <span data-ttu-id="7a510-116">下列範例顯示包含特定電腦傳輸裝置路徑的 **ClassCoNtext** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="7a510-116">The following example shows the **ClassContext** qualifier that contains the path to a particular computer transport device.</span></span>

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

<span data-ttu-id="7a510-117">下列類別定義的範本說明如何使用 **動態**、 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)和 **ClassCoNtext** 的限定詞。</span><span class="sxs-lookup"><span data-stu-id="7a510-117">The following template for a class definition illustrates the use of the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **ClassContext** qualifiers.</span></span> <span data-ttu-id="7a510-118">**提供** 者辨識符號所命名的提供者是實例系統登錄提供者。</span><span class="sxs-lookup"><span data-stu-id="7a510-118">The provider named by the **Provider** qualifier is the instance System Registry provider.</span></span> <span data-ttu-id="7a510-119">請注意，登錄路徑不區分大小寫，如同辨識符號名稱。</span><span class="sxs-lookup"><span data-stu-id="7a510-119">Be aware that registry paths are case-insensitive, as are qualifier names.</span></span>

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

<span data-ttu-id="7a510-120">管理應用程式也可以使用系統登錄提供者來取得和修改特定金鑰的登錄資料。</span><span class="sxs-lookup"><span data-stu-id="7a510-120">Management applications can also use the System Registry provider to retrieve and modify registry data for a particular key.</span></span>

 

 



