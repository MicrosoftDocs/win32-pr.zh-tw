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
# <a name="what-is-a-com-interface"></a>什麼是 COM 介面？

如果您知道 c # 或 JAVA，介面應該是熟悉的概念。 *介面* 會定義一組物件可支援的方法，而不需聽寫任何有關執行的資訊。 介面會在呼叫方法的程式碼和執行方法的程式碼之間，標記清楚的界限。 在「電腦科學」詞彙中，呼叫端會從執行 *分離* 出來。

![顯示物件和應用程式之間介面界限的圖例](images/com01.png)

在 c + + 中，最接近介面的相等是純虛擬類別，也就是只包含純虛擬方法且沒有其他成員的類別。 以下是介面的假設範例：

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

此範例的概念是，某些圖形程式庫中的一組物件是可繪製的。 `IDrawable`介面會定義任何可繪製物件必須支援的作業。 依慣例 (，介面名稱是以 "I" 開頭。在此範例中 ) ，此 `IDrawable` 介面會定義單一作業： `Draw` 。

所有介面都是 *抽象* 的，因此程式無法建立物件的實例 `IDrawable` 。 例如，下列程式碼不會進行編譯。

```C++
IDrawable draw;
draw.Draw();
```

相反地，圖形程式庫會提供可 *執行* 介面的物件 `IDrawable` 。 例如，程式庫可能會提供繪圖物件來繪製圖形，以及繪製影像的點陣圖物件。 在 c + + 中，這是藉由繼承自通用抽象基類來完成：

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

`Shape`和 `Bitmap` 類別會定義兩種不同類型的可以繪製物件。 每個類別都會繼承自 `IDrawable` ，而且會提供它自己的方法實作為 `Draw` 。 當然，這兩個執行可能會有相當大的差異。 例如， `Shape::Draw` 方法可能會在一組線上進行柵格化，而 `Bitmap::Draw` array.blit 圖元的陣列。

使用這個圖形程式庫的程式會 `Shape` `Bitmap` 透過指標操作和物件 `IDrawable` ，而不是 `Shape` 直接使用或 `Bitmap` 指標。

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

以下是對指標陣列進行迴圈的範例 `IDrawable` 。 只要陣列中的每個物件都有繼承，陣列就可能包含圖形、點陣圖和其他繪圖物件的異類分類 `IDrawable` 。

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

COM 的重點是，呼叫程式碼絕不會看到衍生類別的型別。 換句話說，您絕對不會 `Shape` `Bitmap` 在程式碼中宣告類型或的變數。 圖形和點陣圖上的所有作業都是使用指標來執行 `IDrawable` 。 如此一來，COM 會在介面與執行之間維持嚴格的分隔。 和類別的執行詳細 `Shape` 資料 `Bitmap` 可以變更，例如修正錯誤或新增功能，而不會變更呼叫程式碼。

在 c + + 的執行中，會使用類別或結構來宣告介面。

> [!Note]  
> 本主題中的程式碼範例旨在傳達一般概念，而不是實際實務。 定義新的 COM 介面超出此系列的範圍，但您不會直接在標頭檔中定義介面。 相反地，COM 介面是使用稱為介面定義語言 (IDL) 的語言來定義。 Idl 檔案是由 IDL 編譯器處理，它會產生 c + + 標頭檔。

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

當您使用 COM 時，請務必記住，介面不是物件。 它們是物件必須執行的方法集合。 數個物件可以執行相同的介面，如 `Shape` 和範例所示 `Bitmap` 。 此外，一個物件可以執行數個介面。 例如，圖形程式庫可能會定義一個名為 `ISerializable` 的介面，該介面支援儲存和載入繪圖物件。 現在請考慮下列類別宣告：

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

在此範例中， `Bitmap` 類別會實行 `ISerializable` 。 程式可以使用這個方法來儲存或載入點陣圖。 不過，此 `Shape` 類別不會執行 `ISerializable` ，因此不會公開該功能。 下圖顯示此範例中的繼承關係。

![顯示介面繼承的圖例，圖形和點陣圖類別指向 idrawable，但只有指向 iserializable 的點陣圖](images/com02.png)

本節已檢查過介面的概念基礎，但目前我們並未看到實際的 COM 程式碼。 我們將從任何 COM 應用程式必須執行的第一件事開始：初始化 COM 程式庫。

## <a name="next"></a>下一個

[初始化 COM 程式庫](initializing-the-com-library.md)