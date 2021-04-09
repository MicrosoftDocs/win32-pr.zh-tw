---
title: 類別圖示
description: 用來代表類別物件的圖示可以在 DisplaySpecifiers 容器的 >iconpath 屬性中指定。
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- 類別顯示名稱廣告，圖示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933086"
---
# <a name="class-icons"></a><span data-ttu-id="fdd00-104">類別圖示</span><span class="sxs-lookup"><span data-stu-id="fdd00-104">Class Icons</span></span>

<span data-ttu-id="fdd00-105">用來代表類別物件的圖示可以在 DisplaySpecifiers 容器的 **>iconpath** 屬性中指定。</span><span class="sxs-lookup"><span data-stu-id="fdd00-105">The icon used to represent a class object can be specified in the **iconPath** attribute in the DisplaySpecifiers container.</span></span> <span data-ttu-id="fdd00-106">此外，每個類別都可以儲存多個圖示狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd00-106">Moreover, each class can store multiple icon states.</span></span> <span data-ttu-id="fdd00-107">例如，資料夾類別可以有開啟、關閉和停用狀態的圖示。</span><span class="sxs-lookup"><span data-stu-id="fdd00-107">For example, a folder class can have icons for the open, closed, and disabled states.</span></span> <span data-ttu-id="fdd00-108">目前的執行最多接受每個類別16個不同的圖示狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd00-108">The current implementation accepts a maximum of sixteen different icon states per class.</span></span>

<span data-ttu-id="fdd00-109">**>iconpath** 屬性可以用兩種方式之一來指定。</span><span class="sxs-lookup"><span data-stu-id="fdd00-109">The **iconPath** attribute can be specified in one of two ways.</span></span>


```C++
<state>,<icon file name>
```



<span data-ttu-id="fdd00-110">或</span><span class="sxs-lookup"><span data-stu-id="fdd00-110">or</span></span>


```C++
<state>,<module file name>,<resource ID>
```



<span data-ttu-id="fdd00-111">在這些範例中，「 &lt; 狀態」 &gt; 是一個整數，其值介於0到15之間。</span><span class="sxs-lookup"><span data-stu-id="fdd00-111">In these examples, the "&lt;state&gt;" is an integer with a value between 0 and 15.</span></span> <span data-ttu-id="fdd00-112">值0會定義為圖示的預設或關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd00-112">The value 0 is defined to be the default or closed state of the icon.</span></span> <span data-ttu-id="fdd00-113">值1定義為圖示的開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd00-113">The value 1 is defined to be the open state of the icon.</span></span> <span data-ttu-id="fdd00-114">值2是停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd00-114">The value 2 is the disabled state.</span></span> <span data-ttu-id="fdd00-115">所有其他值都是由應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="fdd00-115">All other values are application-defined.</span></span>

<span data-ttu-id="fdd00-116">「 &lt; 圖示檔名稱」 &gt; 是包含圖示影像的圖示檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="fdd00-116">The "&lt;icon file name&gt;" is the path and file name of an icon file that contains the icon image.</span></span>

<span data-ttu-id="fdd00-117">「 &lt; 模組檔案名」 &gt; 是模組（例如 EXE 或 DLL）的路徑和檔案名，其中包含資源中的圖示影像。</span><span class="sxs-lookup"><span data-stu-id="fdd00-117">The "&lt;module file name&gt;" is the path and file name of a module, such as an EXE or DLL, that contains the icon image in a resource.</span></span> <span data-ttu-id="fdd00-118">「 &lt; 資源識別碼」 &gt; 是一個整數，可指定模組內圖示資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fdd00-118">The "&lt;resource ID&gt;" is an integer that specifies the resource identifier of the icon resource within the module.</span></span>

## <a name="adding-a-value-to-the-iconpath-attribute"></a><span data-ttu-id="fdd00-119">將值加入至 **>iconpath** 屬性</span><span class="sxs-lookup"><span data-stu-id="fdd00-119">Adding a Value to the **iconPath** Attribute</span></span>

<span data-ttu-id="fdd00-120">若要將值新增至 **>iconpath** 屬性，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="fdd00-120">To add a value to the **iconPath** attribute, perform the following steps.</span></span>

1.  <span data-ttu-id="fdd00-121">判斷屬性的值是否存在。</span><span class="sxs-lookup"><span data-stu-id="fdd00-121">Determine if the value for the attribute exists.</span></span> <span data-ttu-id="fdd00-122">如果要取代某個值，請先使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法來刪除現有的值，並將 *lnControlCode* 參數設定為 **ADS \_ PROPERTY \_ delete** ，並將 *vProp* 參數設定為要移除的值。</span><span class="sxs-lookup"><span data-stu-id="fdd00-122">If a value is to be replaced, first, delete the existing value using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="fdd00-123">請勿使用 *lnControlCode* 的 **ads \_ 屬性 \_ CLEAR** 或 **ads \_ 屬性 \_ 更新**。</span><span class="sxs-lookup"><span data-stu-id="fdd00-123">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="fdd00-124">建立代表屬性圖示資料的字串。</span><span class="sxs-lookup"><span data-stu-id="fdd00-124">Create the string that represents the attribute icon data.</span></span> <span data-ttu-id="fdd00-125">如需範例，請參閱上面的格式。</span><span class="sxs-lookup"><span data-stu-id="fdd00-125">For an example, see the format above.</span></span>
3.  <span data-ttu-id="fdd00-126">若要加入新的值，請使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法，並將 *lnControlCode* 參數設定為 [ **ADS] 屬性 [ \_ \_ 附加**]。</span><span class="sxs-lookup"><span data-stu-id="fdd00-126">To add the new value, use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND**.</span></span>
4.  <span data-ttu-id="fdd00-127">若要認可目錄的變更，請呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)。</span><span class="sxs-lookup"><span data-stu-id="fdd00-127">To commit changes to the directory, call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 