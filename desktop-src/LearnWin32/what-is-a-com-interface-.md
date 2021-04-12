---
title: 什麼是 COM 介面
description: 什麼是 COM 介面
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da703569beae7a9aa2fc41bcea0214cc9aa488ad
ms.sourcegitcommit: 8eac40ea4d87a85e036ed5bbffec7b7a3dab39ec
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/04/2019
ms.locfileid: "104372711"
---
# <a name="what-is-a-com-interface"></a><span data-ttu-id="ae05e-103">什麼是 COM 介面？</span><span class="sxs-lookup"><span data-stu-id="ae05e-103">What Is a COM Interface?</span></span>

<span data-ttu-id="ae05e-104">如果您知道 c # 或 JAVA，介面應該是熟悉的概念。</span><span class="sxs-lookup"><span data-stu-id="ae05e-104">If you know C# or Java, interfaces should be a familiar concept.</span></span> <span data-ttu-id="ae05e-105">*介面* 會定義一組物件可支援的方法，而不需聽寫任何有關執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="ae05e-105">An *interface* defines a set of methods that an object can support, without dictating anything about the implementation.</span></span> <span data-ttu-id="ae05e-106">介面會在呼叫方法的程式碼和執行方法的程式碼之間，標記清楚的界限。</span><span class="sxs-lookup"><span data-stu-id="ae05e-106">The interface marks a clear boundary between code that calls a method and the code that implements the method.</span></span> <span data-ttu-id="ae05e-107">在「電腦科學」詞彙中，呼叫端會從執行 *分離* 出來。</span><span class="sxs-lookup"><span data-stu-id="ae05e-107">In computer science terms, the caller is *decoupled* from the implementation.</span></span>

![顯示物件和應用程式之間介面界限的圖例](images/com01.png)

<span data-ttu-id="ae05e-109">在 c + + 中，最接近介面的相等是純虛擬類別，也就是只包含純虛擬方法且沒有其他成員的類別。</span><span class="sxs-lookup"><span data-stu-id="ae05e-109">In C++, the nearest equivalent to an interface is a pure virtual class—that is, a class that contains only pure virtual methods and no other members.</span></span> <span data-ttu-id="ae05e-110">以下是介面的假設範例：</span><span class="sxs-lookup"><span data-stu-id="ae05e-110">Here is a hypothetical example of an interface:</span></span>

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

<span data-ttu-id="ae05e-111">此範例的概念是，某些圖形程式庫中的一組物件是可繪製的。</span><span class="sxs-lookup"><span data-stu-id="ae05e-111">The idea of this example is that a set of objects in some graphics library are drawable.</span></span> <span data-ttu-id="ae05e-112">`IDrawable`介面會定義任何可繪製物件必須支援的作業。</span><span class="sxs-lookup"><span data-stu-id="ae05e-112">The `IDrawable` interface defines the operations that any drawable object must support.</span></span> <span data-ttu-id="ae05e-113">依慣例 (，介面名稱是以 "I" 開頭。在此範例中 ) ，此 `IDrawable` 介面會定義單一作業： `Draw` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-113">(By convention, interface names start with "I".) In this example, the `IDrawable` interface defines a single operation: `Draw`.</span></span>

<span data-ttu-id="ae05e-114">所有介面都是 *抽象* 的，因此程式無法建立物件的實例 `IDrawable` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-114">All interfaces are *abstract*, so a program could not create an instance of an `IDrawable` object as such.</span></span> <span data-ttu-id="ae05e-115">例如，下列程式碼不會進行編譯。</span><span class="sxs-lookup"><span data-stu-id="ae05e-115">For example, the following code would not compile.</span></span>

```C++
IDrawable draw;
draw.Draw();
```

<span data-ttu-id="ae05e-116">相反地，圖形程式庫會提供可 *執行* 介面的物件 `IDrawable` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-116">Instead, the graphics library provides objects that *implement* the `IDrawable` interface.</span></span> <span data-ttu-id="ae05e-117">例如，程式庫可能會提供繪圖物件來繪製圖形，以及繪製影像的點陣圖物件。</span><span class="sxs-lookup"><span data-stu-id="ae05e-117">For example, the library might provide a shape object for drawing shapes and a bitmap object for drawing images.</span></span> <span data-ttu-id="ae05e-118">在 c + + 中，這是藉由繼承自通用抽象基類來完成：</span><span class="sxs-lookup"><span data-stu-id="ae05e-118">In C++, this is done by inheriting from a common abstract base class:</span></span>

```C++
class Shape : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};

class Bitmap : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};
```

<span data-ttu-id="ae05e-119">`Shape`和 `Bitmap` 類別會定義兩種不同類型的可以繪製物件。</span><span class="sxs-lookup"><span data-stu-id="ae05e-119">The `Shape` and `Bitmap` classes define two distinct types of drawable object.</span></span> <span data-ttu-id="ae05e-120">每個類別都會繼承自 `IDrawable` ，而且會提供它自己的方法實作為 `Draw` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-120">Each class inherits from `IDrawable` and provides its own implementation of the `Draw` method.</span></span> <span data-ttu-id="ae05e-121">當然，這兩個執行可能會有相當大的差異。</span><span class="sxs-lookup"><span data-stu-id="ae05e-121">Naturally, the two implementations might differ considerably.</span></span> <span data-ttu-id="ae05e-122">例如， `Shape::Draw` 方法可能會在一組線上進行柵格化，而 `Bitmap::Draw` array.blit 圖元的陣列。</span><span class="sxs-lookup"><span data-stu-id="ae05e-122">For example, the `Shape::Draw` method might rasterize a set of lines, while `Bitmap::Draw` would blit an array of pixels.</span></span>

<span data-ttu-id="ae05e-123">使用這個圖形程式庫的程式會 `Shape` `Bitmap` 透過指標操作和物件 `IDrawable` ，而不是 `Shape` 直接使用或 `Bitmap` 指標。</span><span class="sxs-lookup"><span data-stu-id="ae05e-123">A program using this graphics library would manipulate `Shape` and `Bitmap` objects through `IDrawable` pointers, rather than using `Shape` or `Bitmap` pointers directly.</span></span>

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

<span data-ttu-id="ae05e-124">以下是對指標陣列進行迴圈的範例 `IDrawable` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-124">Here is an example that loops over an array of `IDrawable` pointers.</span></span> <span data-ttu-id="ae05e-125">只要陣列中的每個物件都有繼承，陣列就可能包含圖形、點陣圖和其他繪圖物件的異類分類 `IDrawable` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-125">The array might contain a heterogeneous assortment of shapes, bitmaps, and other graphics objects, as long as each object in the array inherits `IDrawable`.</span></span>

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

<span data-ttu-id="ae05e-126">COM 的重點是，呼叫程式碼絕不會看到衍生類別的型別。</span><span class="sxs-lookup"><span data-stu-id="ae05e-126">A key point about COM is that the calling code never sees the type of the derived class.</span></span> <span data-ttu-id="ae05e-127">換句話說，您絕對不會 `Shape` `Bitmap` 在程式碼中宣告類型或的變數。</span><span class="sxs-lookup"><span data-stu-id="ae05e-127">In other words, you would never declare a variable of type `Shape` or `Bitmap` in your code.</span></span> <span data-ttu-id="ae05e-128">圖形和點陣圖上的所有作業都是使用指標來執行 `IDrawable` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-128">All operations on shapes and bitmaps are performed using `IDrawable` pointers.</span></span> <span data-ttu-id="ae05e-129">如此一來，COM 會在介面與執行之間維持嚴格的分隔。</span><span class="sxs-lookup"><span data-stu-id="ae05e-129">In this way, COM maintains a strict separation between interface and implementation.</span></span> <span data-ttu-id="ae05e-130">和類別的執行詳細 `Shape` 資料 `Bitmap` 可以變更，例如修正錯誤或新增功能，而不會變更呼叫程式碼。</span><span class="sxs-lookup"><span data-stu-id="ae05e-130">The implementation details of the `Shape` and `Bitmap` classes can change—for example, to fix bugs or add new capabilities—with no changes to the calling code.</span></span>

<span data-ttu-id="ae05e-131">在 c + + 的執行中，會使用類別或結構來宣告介面。</span><span class="sxs-lookup"><span data-stu-id="ae05e-131">In a C++ implementation, interfaces are declared using a class or structure.</span></span>

> [!Note]  
> <span data-ttu-id="ae05e-132">本主題中的程式碼範例旨在傳達一般概念，而不是實際實務。</span><span class="sxs-lookup"><span data-stu-id="ae05e-132">The code examples in this topic are meant to convey general concepts, not real-world practice.</span></span> <span data-ttu-id="ae05e-133">定義新的 COM 介面超出此系列的範圍，但您不會直接在標頭檔中定義介面。</span><span class="sxs-lookup"><span data-stu-id="ae05e-133">Defining new COM interfaces is beyond the scope of this series, but you would not define an interface directly in a header file.</span></span> <span data-ttu-id="ae05e-134">相反地，COM 介面是使用稱為介面定義語言 (IDL) 的語言來定義。</span><span class="sxs-lookup"><span data-stu-id="ae05e-134">Instead, a COM interface is defined using a language called Interface Definition Language (IDL).</span></span> <span data-ttu-id="ae05e-135">Idl 檔案是由 IDL 編譯器處理，它會產生 c + + 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="ae05e-135">The IDL file is processed by an IDL compiler, which generates a C++ header file.</span></span>

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

<span data-ttu-id="ae05e-136">當您使用 COM 時，請務必記住，介面不是物件。</span><span class="sxs-lookup"><span data-stu-id="ae05e-136">When you work with COM, it is important to remember that interfaces are not objects.</span></span> <span data-ttu-id="ae05e-137">它們是物件必須執行的方法集合。</span><span class="sxs-lookup"><span data-stu-id="ae05e-137">They are collections of methods that objects must implement.</span></span> <span data-ttu-id="ae05e-138">數個物件可以執行相同的介面，如 `Shape` 和範例所示 `Bitmap` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-138">Several objects can implement the same interface, as shown with the `Shape` and `Bitmap` examples.</span></span> <span data-ttu-id="ae05e-139">此外，一個物件可以執行數個介面。</span><span class="sxs-lookup"><span data-stu-id="ae05e-139">Moreover, one object can implement several interfaces.</span></span> <span data-ttu-id="ae05e-140">例如，圖形程式庫可能會定義一個名為 `ISerializable` 的介面，該介面支援儲存和載入繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="ae05e-140">For example, the graphics library might define an interface named `ISerializable` that supports saving and loading graphics objects.</span></span> <span data-ttu-id="ae05e-141">現在請考慮下列類別宣告：</span><span class="sxs-lookup"><span data-stu-id="ae05e-141">Now consider the following class declarations:</span></span>

```C++
// An interface for serialization.
class ISerializable
{
public:
    virtual void Load(PCWSTR filename) = 0;    // Load from file.
    virtual void Save(PCWSTR filename) = 0;    // Save to file.
};

// Declarations of drawable object types.

class Shape : public IDrawable
{
    ...
};

class Bitmap : public IDrawable, public ISerializable
{
    ...
};
```

<span data-ttu-id="ae05e-142">在此範例中， `Bitmap` 類別會實行 `ISerializable` 。</span><span class="sxs-lookup"><span data-stu-id="ae05e-142">In this example, the `Bitmap` class implements `ISerializable`.</span></span> <span data-ttu-id="ae05e-143">程式可以使用這個方法來儲存或載入點陣圖。</span><span class="sxs-lookup"><span data-stu-id="ae05e-143">The program could use this method to save or load the bitmap.</span></span> <span data-ttu-id="ae05e-144">不過，此 `Shape` 類別不會執行 `ISerializable` ，因此不會公開該功能。</span><span class="sxs-lookup"><span data-stu-id="ae05e-144">However, the `Shape` class does not implement `ISerializable`, so it does not expose that functionality.</span></span> <span data-ttu-id="ae05e-145">下圖顯示此範例中的繼承關係。</span><span class="sxs-lookup"><span data-stu-id="ae05e-145">The following diagram shows the inheritance relations in this example.</span></span>

![顯示介面繼承的圖例，圖形和點陣圖類別指向 idrawable，但只有指向 iserializable 的點陣圖](images/com02.png)

<span data-ttu-id="ae05e-147">本節已檢查過介面的概念基礎，但目前我們並未看到實際的 COM 程式碼。</span><span class="sxs-lookup"><span data-stu-id="ae05e-147">This section has examined the conceptual basis of interfaces, but so far we have not seen actual COM code.</span></span> <span data-ttu-id="ae05e-148">我們將從任何 COM 應用程式必須執行的第一件事開始：初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="ae05e-148">We'll start with the first thing that any COM application must do: Initialize the COM library.</span></span>

## <a name="next"></a><span data-ttu-id="ae05e-149">下一個</span><span class="sxs-lookup"><span data-stu-id="ae05e-149">Next</span></span>

[<span data-ttu-id="ae05e-150">初始化 COM 程式庫</span><span class="sxs-lookup"><span data-stu-id="ae05e-150">Initializing the COM Library</span></span>](initializing-the-com-library.md)