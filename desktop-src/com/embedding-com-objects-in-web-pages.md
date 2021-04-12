---
title: 在網頁中內嵌 COM 物件
description: 您可以在網頁中使用 COM 物件。 若要這樣做，請先建立該 COM 物件的實例。 建立物件實例之後，您可以在該網頁的後續腳本中使用它。
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300567"
---
# <a name="embedding-com-objects-in-web-pages"></a><span data-ttu-id="e3bf8-105">在網頁中內嵌 COM 物件</span><span class="sxs-lookup"><span data-stu-id="e3bf8-105">Embedding COM Objects in Web Pages</span></span>

<span data-ttu-id="e3bf8-106">您可以在網頁中使用 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-106">You can use COM objects in webpages.</span></span> <span data-ttu-id="e3bf8-107">若要這樣做，請先建立該 COM 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-107">To do this, first create an instance of that COM object.</span></span> <span data-ttu-id="e3bf8-108">建立物件實例之後，您可以在該網頁的後續腳本中使用它。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-108">After an object instance is created, you can use it in subsequent scripts on that webpage.</span></span>

<span data-ttu-id="e3bf8-109">若要在網頁中建立 COM 物件實例，您可以使用物件標記。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-109">To create a COM object instance in a webpage, you can use an OBJECT tag.</span></span> <span data-ttu-id="e3bf8-110">或者，如果您的指令碼語言提供原生的方式來建立 COM 物件，您就可以使用腳本來建立物件實例。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-110">Alternatively, if your scripting language provides a native way to create COM objects, you can create an object instance using script.</span></span>

<span data-ttu-id="e3bf8-111">請注意，在網頁中內嵌 COM 物件只適用于支援 ActiveX 和 COM 的瀏覽器，例如 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-111">Note that embedding COM objects in webpages only works with browsers that support ActiveX and COM, for example Internet Explorer.</span></span>

<span data-ttu-id="e3bf8-112">下列範例說明如何使用物件標記，在網頁中內嵌 COM 物件：</span><span class="sxs-lookup"><span data-stu-id="e3bf8-112">The following example illustrates using the OBJECT tag to embed a COM object in a webpage:</span></span>

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

<span data-ttu-id="e3bf8-113">如果您的指令碼語言提供建立 COM 物件的方法，您也可以在腳本中建立 COM 物件實例。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-113">You can also create a COM object instance in script, if your scripting language provides a way to create COM objects.</span></span> <span data-ttu-id="e3bf8-114">例如，VBScript 提供 CreateObject 方法，而 JScript 則提供 ActiveXObject 物件。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-114">For example, VBScript provides the CreateObject method and JScript provides the ActiveXObject object.</span></span> <span data-ttu-id="e3bf8-115">下列範例說明如何在腳本中建立物件。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-115">Creating objects in script is illustrated in the following examples.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

<span data-ttu-id="e3bf8-116">除了 CreateObject 方法和 ActiveXObject 物件之外，VBScript 和 JScript 都會提供 GetObject 的方法，以傳回物件實例。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-116">In addition to the CreateObject method and the ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

<span data-ttu-id="e3bf8-117">建立 COM 物件之後，您可以使用物件標記識別項屬性中指定的識別碼，在後續的腳本中參考它。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-117">After a COM object has been created, you can reference it in subsequent scripts by using the identifier specified in the OBJECT tag's ID attribute.</span></span> <span data-ttu-id="e3bf8-118">在上述範例中，此識別碼已指定為「vid」。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-118">In the preceding example, this identifier was specified as "vid."</span></span> <span data-ttu-id="e3bf8-119">請注意，使用 COM 物件的腳本必須出現在建立物件實例的物件標記或腳本之後;否則，物件識別碼是未定義的。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-119">Note that the script that uses the COM object must appear after the OBJECT tag or script that creates the object instance; otherwise, the object identifier is undefined.</span></span> <span data-ttu-id="e3bf8-120">下列腳本會使用 objXL 物件來顯示 Microsoft Excel 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-120">The following script uses the objXL object to display the version information for Microsoft Excel.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

<span data-ttu-id="e3bf8-121">如果您要撰寫內嵌于網頁的腳本，則瀏覽器也會公開您的腳本可以存取的物件模型。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-121">If you are writing scripts embedded in a webpage, the browser also exposes an object model that your scripts can access.</span></span> <span data-ttu-id="e3bf8-122">Internet Explorer 所使用的模型符合全球資訊網協會 (W3C) 所建議的檔物件模型 (DOM) 。</span><span class="sxs-lookup"><span data-stu-id="e3bf8-122">The model used by Internet Explorer conforms to the Document Object Model (DOM) proposed by the World Wide Web Consortium (W3C).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3bf8-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3bf8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3bf8-124">使用 COM 物件編寫腳本</span><span class="sxs-lookup"><span data-stu-id="e3bf8-124">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




