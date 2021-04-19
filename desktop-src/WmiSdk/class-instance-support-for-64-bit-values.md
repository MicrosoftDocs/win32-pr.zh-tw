---
description: 提供在路徑中使用64位值的限制。
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: 64位值的類別實例支援
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988315"
---
# <a name="class-instance-support-for-64-bit-values"></a><span data-ttu-id="fdd2a-103">64位值的類別實例支援</span><span class="sxs-lookup"><span data-stu-id="fdd2a-103">Class Instance Support for 64-Bit Values</span></span>

<span data-ttu-id="fdd2a-104">您可以使用64位的索引鍵值作為路徑的一部分，但有下列限制：</span><span class="sxs-lookup"><span data-stu-id="fdd2a-104">You can use a 64-bit key value as part of a path, with the following restrictions:</span></span>

-   <span data-ttu-id="fdd2a-105">只要您未超過32位範圍，就可以從索引鍵指派和取出值，就像是32位屬性一樣。</span><span class="sxs-lookup"><span data-stu-id="fdd2a-105">As long as you do not exceed the 32-bit range, you can assign and retrieve values from the key as you would a 32-bit property.</span></span>
-   <span data-ttu-id="fdd2a-106">當您超過已簽署類型的 0x7FFFFFFF (的整數值時) 、 (不帶正負號類型的 0x80000000) 或32位，您必須使用引號。</span><span class="sxs-lookup"><span data-stu-id="fdd2a-106">After you exceed the integer value of 0x7FFFFFFF (for signed types), 0x80000000 (for unsigned types), or 32 bits, you must use quotation marks.</span></span>
-   <span data-ttu-id="fdd2a-107">64位值的唯一有效路徑位於實例的 **\_ \_ RELPATH** 或 **\_ \_ path** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="fdd2a-107">The only valid path for a 64-bit value is located in the **\_\_RELPATH** or **\_\_PATH** properties of the instance.</span></span> <span data-ttu-id="fdd2a-108">因此，WMI 不支援對等值的十六進位標記法。</span><span class="sxs-lookup"><span data-stu-id="fdd2a-108">As such, WMI does not support the hexadecimal notation for the equivalent value.</span></span>
-   <span data-ttu-id="fdd2a-109">如果 WMI 將實例索引鍵記錄為負數，則您必須使用原始數位來取得實例。</span><span class="sxs-lookup"><span data-stu-id="fdd2a-109">If WMI records the instance key as a negative number, then you must use the original number to retrieve the instance.</span></span>

<span data-ttu-id="fdd2a-110">查詢的語法不會受到影響，且行為會如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="fdd2a-110">Query semantics are unaffected and behave as expected.</span></span> <span data-ttu-id="fdd2a-111">這個行為只會影響物件路徑、 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)和 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 作業。</span><span class="sxs-lookup"><span data-stu-id="fdd2a-111">This behavior only affects the object path, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) operations.</span></span>

<span data-ttu-id="fdd2a-112">下列範例顯示類別實例可以有64位的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="fdd2a-112">The following example shows that class instances can have 64-bit key values.</span></span>

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



