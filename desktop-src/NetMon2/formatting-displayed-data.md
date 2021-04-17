---
description: 網路監視器或剖析器 DLL 可以格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: 設定已顯示之資料的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510977"
---
# <a name="formatting-displayed-data"></a><span data-ttu-id="ca2ac-103">設定已顯示之資料的格式</span><span class="sxs-lookup"><span data-stu-id="ca2ac-103">Formatting Displayed Data</span></span>

<span data-ttu-id="ca2ac-104">網路監視器或剖析器 DLL 可以格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-104">Network Monitor or your parser DLL can format the data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="ca2ac-105">網路監視器提供一般格式器，提供顯示存在於通訊協定內的大部分資料類型所需的基本服務。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-105">Network Monitor provides a generic formatter that provides the basic services needed to display most data types that exist within a protocol.</span></span> <span data-ttu-id="ca2ac-106">不過，一般格式子不支援所有資料類型。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-106">However, the generic formatter does not support all data types.</span></span> <span data-ttu-id="ca2ac-107">例如，一般格式器不支援下列各項：</span><span class="sxs-lookup"><span data-stu-id="ca2ac-107">For example, the generic formatter does not support the following:</span></span>

-   <span data-ttu-id="ca2ac-108">數種地址類型。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-108">Several address types.</span></span>
-   <span data-ttu-id="ca2ac-109">來源和目的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-109">Source and destination-friendly names.</span></span>
-   <span data-ttu-id="ca2ac-110">物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-110">Object identifiers.</span></span>
-   <span data-ttu-id="ca2ac-111">大型整數資料類型。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-111">Large integer data types.</span></span>
-   <span data-ttu-id="ca2ac-112">可變長度的小整數資料類型。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-112">Variable length small integer data types.</span></span>

<span data-ttu-id="ca2ac-113">下列範例會識別許可權識別碼屬性的兩個格式化字串。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-113">The following example identifies two formatted strings for the Privilege ID property.</span></span>

-   <span data-ttu-id="ca2ac-114">第一行程式碼會顯示一般格式器的輸出。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-114">The first line of code shows the output of the generic formatter.</span></span> <span data-ttu-id="ca2ac-115">輸出是以資料類型為基礎。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-115">The output is based on the data type.</span></span>
-   <span data-ttu-id="ca2ac-116">第二行程式碼會顯示自訂格式器的輸出，以及屬性資料的字串。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-116">The second line of code shows the output of a custom formatter with a string to the property data.</span></span>

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> <span data-ttu-id="ca2ac-117">可能的話，請使用一般格式器來顯示您的資料，因為它可讓您控制剖析器 DLL 的大小，並為剖析器 DLL 提供更佳的跨平臺功能。</span><span class="sxs-lookup"><span data-stu-id="ca2ac-117">When possible, use the generic formatter to display your data because it allows you to control the size of your parser DLL, and provides better cross-platform capabilities for your parser DLL.</span></span>

 

 

 



