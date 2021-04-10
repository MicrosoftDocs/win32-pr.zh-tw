---
description: COM + 物件的函式字串是由系統管理員為元件指定的初始化字串。
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: COM + 物件的函數位符串概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936184"
---
# <a name="com-object-constructor-strings-concepts"></a><span data-ttu-id="8a618-103">COM + 物件的函數位符串概念</span><span class="sxs-lookup"><span data-stu-id="8a618-103">COM+ Object Constructor Strings Concepts</span></span>

<span data-ttu-id="8a618-104">COM + 物件的函式字串是由系統管理員為元件指定的初始化字串。</span><span class="sxs-lookup"><span data-stu-id="8a618-104">COM+ object constructor strings are initialization strings that are administratively specified for a component.</span></span> <span data-ttu-id="8a618-105">您可以使用物件的函式字串來撰寫具有某種程度的單一元件，讓它可以在稍後針對特定工作進行自訂;也就是說，您可以執行參數化物件結構。</span><span class="sxs-lookup"><span data-stu-id="8a618-105">You can use object constructor strings to write a single component with a degree of generality that allows it to be later customized for a particular task; that is, you can perform parameterized object construction.</span></span>

<span data-ttu-id="8a618-106">例如，您可以使用這項功能來撰寫保存一般 ODBC 連接的元件，並于稍後為系統管理員指定元件的確切 DSN。</span><span class="sxs-lookup"><span data-stu-id="8a618-106">For example, you might use this feature to write a component that holds a generic ODBC connection and later specify an exact DSN for the component administratively.</span></span> <span data-ttu-id="8a618-107">如果系統組態變更，您可以據此變更函式字串。</span><span class="sxs-lookup"><span data-stu-id="8a618-107">If the system configuration changes, you can change the constructor string accordingly.</span></span>

> [!Note]  
> <span data-ttu-id="8a618-108">物件的函式字串不應該用來儲存安全性機密資訊。</span><span class="sxs-lookup"><span data-stu-id="8a618-108">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

<span data-ttu-id="8a618-109">您可以搭配 [物件](com--object-pooling.md) 共用使用物件的函式字串，以在您如何集區和重複使用資源的方式中達到更高程度的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="8a618-109">You can use object constructor strings in conjunction with [object pooling](com--object-pooling.md) to achieve a greater degree of granularity in how you pool and reuse resources.</span></span> <span data-ttu-id="8a618-110">例如，您可能會建立多個不同的元件（除了使用其他的函式字串和 Clsid），以維護不同的物件集區，以保留不同用戶端群組可用的連接。</span><span class="sxs-lookup"><span data-stu-id="8a618-110">For example, you might create several distinct components, identical except for constructor strings and CLSIDs, to maintain distinct pools of objects holding connections usable by distinct groups of clients.</span></span> <span data-ttu-id="8a618-111">如果連接是以系結至特定安全性角色的方式開啟，例如在資料庫上以特定的驗證開啟連接時（例如，在一般情況下將它們轉譯為不可重複使用），這會很有用。</span><span class="sxs-lookup"><span data-stu-id="8a618-111">This would be useful if connections are opened in a manner that binds them to particular security roles—such as when the connections are opened with some specific authentication at the database—rendering them non-reusable in the general case.</span></span>

<span data-ttu-id="8a618-112">若要這樣做，您可以使用 [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)撰寫依賴物件函式字串的單一泛型元件，並將它重新編譯以產生數個可自訂的元件，每個元件都有不同的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="8a618-112">To do this, you can write a single generic component that relies on object constructor strings, using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), and recompile it to produce several customizable components each with a distinct CLSID.</span></span> <span data-ttu-id="8a618-113">然後，您可以系統管理員量身打造每個元件，以開啟與函式字串的適當連線、將它們設定為集區，並將其保留在每個 CLSID 的相異集區中。</span><span class="sxs-lookup"><span data-stu-id="8a618-113">You can then administratively tailor each component to open an appropriate connection with a constructor string, configure them to be pooled, and they will be maintained in distinct pools per CLSID.</span></span>

<span data-ttu-id="8a618-114">明確撰寫元件以辨識您輸入的字串時，您可以指定一個函式字串。</span><span class="sxs-lookup"><span data-stu-id="8a618-114">You can specify a constructor string when a component has been written specifically to recognize the string that you enter.</span></span> <span data-ttu-id="8a618-115">元件可以使用 [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)，以程式設計方式存取這些字串。</span><span class="sxs-lookup"><span data-stu-id="8a618-115">Components can access these strings programmatically by using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span></span>

<span data-ttu-id="8a618-116">只有在物件結構已啟用系統管理的情況下，才會在物件建立時傳入函式字串。</span><span class="sxs-lookup"><span data-stu-id="8a618-116">Constructor strings are passed in at object creation time only when object construction is administratively enabled.</span></span> <span data-ttu-id="8a618-117">COM + 會呼叫它所執行的 [**IObjectConstruct：：構造**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) 方法。</span><span class="sxs-lookup"><span data-stu-id="8a618-117">COM+ calls the [**IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) method that it implements.</span></span> <span data-ttu-id="8a618-118">在該方法中，您可以使用 [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring)存取函式字串。</span><span class="sxs-lookup"><span data-stu-id="8a618-118">Within that method, you can access the constructor string by using [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span></span> <span data-ttu-id="8a618-119">空字串可以是有效的專案。</span><span class="sxs-lookup"><span data-stu-id="8a618-119">Empty strings can be valid entries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a618-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a618-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a618-121">COM + 物件共用</span><span class="sxs-lookup"><span data-stu-id="8a618-121">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="8a618-122">指定元件的物件表示函式字串</span><span class="sxs-lookup"><span data-stu-id="8a618-122">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="8a618-123">使用物件的函式字串來建立元件</span><span class="sxs-lookup"><span data-stu-id="8a618-123">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



