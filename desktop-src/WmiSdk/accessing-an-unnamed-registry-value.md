---
description: 存取未命名的登錄值
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: 存取未命名的登錄值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975469"
---
# <a name="accessing-an-unnamed-registry-value"></a><span data-ttu-id="a15b2-103">存取未命名的登錄值</span><span class="sxs-lookup"><span data-stu-id="a15b2-103">Accessing an Unnamed Registry Value</span></span>

<span data-ttu-id="a15b2-104">登錄機碼的預設值或未命名值，會顯示為 (預設) 或 <No Name> 在 Regedit 登錄編輯程式中。</span><span class="sxs-lookup"><span data-stu-id="a15b2-104">The default, or unnamed value of a registry key is shown as (Default) or <No Name> in the Regedit registry editor.</span></span> <span data-ttu-id="a15b2-105">您可以使用系統登錄提供者來存取未命名的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="a15b2-105">You can use the System Registry provider to access an unnamed registry key.</span></span> <span data-ttu-id="a15b2-106">同樣地，您也可以使用系統登錄提供者來存取點陣圖描述（定義為未命名值）。</span><span class="sxs-lookup"><span data-stu-id="a15b2-106">Similarly, you can also use the System Registry provider to access bitmap descriptions, which are defined as unnamed values.</span></span>

<span data-ttu-id="a15b2-107">下列程式描述如何取出未命名的登錄值。</span><span class="sxs-lookup"><span data-stu-id="a15b2-107">The following procedure describes how to retrieve an unnamed registry value.</span></span>

<span data-ttu-id="a15b2-108">**取出未命名的登錄值**</span><span class="sxs-lookup"><span data-stu-id="a15b2-108">**To retrieve an unnamed registry value**</span></span>

1.  <span data-ttu-id="a15b2-109">定義屬性，並將該屬性的 **PropertyCoNtext** 限定詞設定為空字串。</span><span class="sxs-lookup"><span data-stu-id="a15b2-109">Define a property and set the **PropertyContext** qualifier of that property to an empty string.</span></span>

    <span data-ttu-id="a15b2-110">下列程式碼範例會示範類別如何定義屬性來保存 **ClassCoNtext** 限定詞所指定之索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="a15b2-110">The following code example shows how the class defines properties to hold values for the key specified by the **ClassContext** qualifier.</span></span> <span data-ttu-id="a15b2-111">預設值會儲存在 **預設** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="a15b2-111">The default value is stored in the **Default** property.</span></span>

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    <span data-ttu-id="a15b2-112">傳輸索引鍵不會使用未命名的值，因此除非使用登錄編輯工具來變更未命名的值，否則此 MOF 檔案的編譯不會產生任何 **預設** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a15b2-112">The Transports key does not use the unnamed value, so compilation of this MOF file does not produce any value for the **Default** property unless a registry editing tool is used to change the unnamed value.</span></span>

2.  <span data-ttu-id="a15b2-113">若為點陣圖檔案，請定義屬性，並設定該屬性的 **PropertyCoNtext** 。</span><span class="sxs-lookup"><span data-stu-id="a15b2-113">For a bitmap file, define a property and set the **PropertyContext** of that property.</span></span>

    <span data-ttu-id="a15b2-114">下列程式碼範例顯示如何定義屬性。</span><span class="sxs-lookup"><span data-stu-id="a15b2-114">The following code example shows how to define a property.</span></span>

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



