---
title: 從 c + + 轉換成 JAVA
description: 使用 c + + 程式設計語言，開發人員可以直接存取儲存特定變數的記憶體。 記憶體指標可提供此直接存取。 在 JAVA 中，系統會為您處理指標。
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371903"
---
# <a name="translating-to-java-from-c"></a><span data-ttu-id="9dd80-105">從 c + + 轉換成 JAVA</span><span class="sxs-lookup"><span data-stu-id="9dd80-105">Translating to Java from C++</span></span>

<span data-ttu-id="9dd80-106">使用 c + + 程式設計語言，開發人員可以直接存取儲存特定變數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9dd80-106">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="9dd80-107">記憶體指標可提供此直接存取。</span><span class="sxs-lookup"><span data-stu-id="9dd80-107">Memory pointers provide this direct access.</span></span> <span data-ttu-id="9dd80-108">在 JAVA 中，系統會為您處理指標。</span><span class="sxs-lookup"><span data-stu-id="9dd80-108">In Java, pointers are handled for you.</span></span>

<span data-ttu-id="9dd80-109">在 JAVA 中，結構 **、等** 位和 **typedef** 複合資料型別只會透過使用類別來處理。</span><span class="sxs-lookup"><span data-stu-id="9dd80-109">In Java, **struct**, **union**, and **typedef** composite data types are handled exclusively through the use of classes.</span></span> <span data-ttu-id="9dd80-110">例如，c + + **VARIANT** 資料類型會對應至 JAVA 中的 .com.. **.com** 。</span><span class="sxs-lookup"><span data-stu-id="9dd80-110">For example, the C++ **VARIANT** data type maps to **com.ms.com.Variant** in Java.</span></span>

<span data-ttu-id="9dd80-111">在 c + + 中，字串是字元陣列。</span><span class="sxs-lookup"><span data-stu-id="9dd80-111">In C++, strings are an array of characters.</span></span> <span data-ttu-id="9dd80-112">在 JAVA 中，字串是物件。</span><span class="sxs-lookup"><span data-stu-id="9dd80-112">In Java, strings are objects.</span></span> <span data-ttu-id="9dd80-113">作用於字串的方法會將字串視為完整的物件。</span><span class="sxs-lookup"><span data-stu-id="9dd80-113">Methods that act on strings treat the string as a complete object.</span></span>

<span data-ttu-id="9dd80-114">COM 方法會傳回稱為 **HRESULT** 的值，這是32位的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9dd80-114">COM methods return a value known as a **HRESULT**, which is a 32-bit error code.</span></span> <span data-ttu-id="9dd80-115">適用于 Microsoft Internet Explorer 的 JAVA 支援會定義會包裝 **HRESULT** 錯誤碼的 **ComException** 類別。</span><span class="sxs-lookup"><span data-stu-id="9dd80-115">The Java support for Microsoft Internet Explorer defines a class, **com.ms.com.ComException**, which wraps the **HRESULT** error code.</span></span>

<span data-ttu-id="9dd80-116">JAVA 不支援不帶正負號的資料類型，除了 **char** 之外，也就是16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="9dd80-116">Java does not support unsigned data types except for **char**, which is a 16-bit unsigned integer.</span></span> <span data-ttu-id="9dd80-117">接受或傳回其他不帶正負號資料類型的方法，無法從 JAVA 使用。</span><span class="sxs-lookup"><span data-stu-id="9dd80-117">Methods that accept or return other unsigned data types cannot be used from Java.</span></span>

<span data-ttu-id="9dd80-118">JAVA 不支援多維陣列。</span><span class="sxs-lookup"><span data-stu-id="9dd80-118">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="9dd80-119">接受或傳回多維陣列的方法無法從 JAVA 使用。</span><span class="sxs-lookup"><span data-stu-id="9dd80-119">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="9dd80-120">JAVA 中的布林值不能轉換成0和1。</span><span class="sxs-lookup"><span data-stu-id="9dd80-120">Boolean values in Java cannot be cast to 0 and 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dd80-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="9dd80-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dd80-122">轉換成 JAVA</span><span class="sxs-lookup"><span data-stu-id="9dd80-122">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




