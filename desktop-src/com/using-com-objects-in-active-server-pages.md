---
title: 使用 Active Server Pages 中的 COM 物件
description: 您可以在 Active Server Pages (ASP) 應用程式中編寫 COM 物件的腳本。
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300196"
---
# <a name="using-com-objects-in-active-server-pages"></a><span data-ttu-id="e5e48-103">使用 Active Server Pages 中的 COM 物件</span><span class="sxs-lookup"><span data-stu-id="e5e48-103">Using COM Objects in Active Server Pages</span></span>

<span data-ttu-id="e5e48-104">您可以在 Active Server Pages (ASP) 應用程式中編寫 COM 物件的腳本。</span><span class="sxs-lookup"><span data-stu-id="e5e48-104">You can script COM objects in Active Server Pages (ASP) applications.</span></span> <span data-ttu-id="e5e48-105">若要這樣做，您必須先使用物件標記或呼叫 ASP Server 物件的 CreateObject 方法，建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="e5e48-105">To do so, you must first create an instance of the object either by using the OBJECT tag or by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="e5e48-106">一旦建立 COM 物件之後，您就可以在 ASP 頁面的後續腳本中使用它。</span><span class="sxs-lookup"><span data-stu-id="e5e48-106">Once a COM object has been created, you can use it in subsequent scripts on the ASP page.</span></span>

<span data-ttu-id="e5e48-107">您可以使用 ASP 來處理許多不同類型的腳本引擎，每種引擎都支援不同的指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="e5e48-107">Using ASP, you can work with many different types of scripting engines, each of which supports a different scripting language.</span></span> <span data-ttu-id="e5e48-108">ASP 隨附 VBScript 和 JScript 腳本引擎。</span><span class="sxs-lookup"><span data-stu-id="e5e48-108">ASP comes with VBScript and JScript scripting engines.</span></span> <span data-ttu-id="e5e48-109">您也可以插入由其他公司開發的腳本引擎，以支援 PerlScript、PScript、Python 等語言。</span><span class="sxs-lookup"><span data-stu-id="e5e48-109">You can also plug in scripting engines developed by other companies to support languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="e5e48-110">如果您未設定 ASP 頁面的指令碼語言，則預設值為 VBScript。</span><span class="sxs-lookup"><span data-stu-id="e5e48-110">If you do not set the scripting language for an ASP page, VBScript is the default.</span></span> <span data-ttu-id="e5e48-111">若要指定 VBScript 以外的指令碼語言，請在每個 ASP 頁面頂端加入一行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e5e48-111">To specify a scripting language other than VBScript, include a line such as the following at the top of each ASP page:</span></span>

``` syntax
<%@ LANGUAGE=JScript %>
 
```

<span data-ttu-id="e5e48-112">若要在 ASP 頁面中使用 COM 物件，您必須先建立該物件的實例。</span><span class="sxs-lookup"><span data-stu-id="e5e48-112">To use a COM object in an ASP page, you must first create an instance of that object.</span></span> <span data-ttu-id="e5e48-113">若要這麼做，請使用物件標記並為 RUNAT 屬性指定 "SERVER" 值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="e5e48-113">You do this by using the OBJECT tag and specifying the value "SERVER" for the RUNAT attribute, as shown in the following example.</span></span> <span data-ttu-id="e5e48-114">根據預設，物件標記會在用戶端上建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="e5e48-114">By default, the OBJECT tag creates an instance of the object on the client.</span></span> <span data-ttu-id="e5e48-115">將 RUNAT 屬性設定為 [伺服器] 會在伺服器上建立物件。</span><span class="sxs-lookup"><span data-stu-id="e5e48-115">Setting the RUNAT attribute to SERVER causes the object to be created on the server.</span></span> <span data-ttu-id="e5e48-116">物件必須在伺服器上執行，ASP 才能使用。</span><span class="sxs-lookup"><span data-stu-id="e5e48-116">The object must run on the server in order to be used by ASP.</span></span>

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

<span data-ttu-id="e5e48-117">您也可以藉由呼叫 ASP 伺服器物件的 CreateObject 方法，在 ASP 頁面上建立 COM 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="e5e48-117">You can also create an instance of a COM object on an ASP page by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="e5e48-118">使用 CreateObject 比使用物件標記建立物件慢，但是它會稍微更容易讀取，因為它會指定程式設計的識別碼，而不是 COM 物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5e48-118">Using Server.CreateObject is slower than creating the object using an OBJECT tag, but it is slightly more readable because it specifies the programmatic identifier instead of the class identifier of the COM object.</span></span> <span data-ttu-id="e5e48-119">伺服器物件是由 ASP 公開，不需要建立。</span><span class="sxs-lookup"><span data-stu-id="e5e48-119">The Server object is exposed by ASP and does not need to be created.</span></span> <span data-ttu-id="e5e48-120">如何呼叫 CreateObject，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="e5e48-120">How to call Server.CreateObject is illustrated in the following examples.</span></span> <span data-ttu-id="e5e48-121">第一個範例是 VBScript：</span><span class="sxs-lookup"><span data-stu-id="e5e48-121">The first example is VBScript:</span></span>

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="e5e48-122">下一個範例是 JScript：</span><span class="sxs-lookup"><span data-stu-id="e5e48-122">The next example is JScript:</span></span>

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="e5e48-123">呼叫 CreateObject 比使用物件標記來建立 COM 物件慢。</span><span class="sxs-lookup"><span data-stu-id="e5e48-123">Calling CreateObject is slower than using the OBJECT tag to create a COM object.</span></span> <span data-ttu-id="e5e48-124">在效能很重要的應用程式中，您應該使用物件標記。</span><span class="sxs-lookup"><span data-stu-id="e5e48-124">In applications where performance is critical, you should use the OBJECT tag.</span></span>

<span data-ttu-id="e5e48-125">建立 COM 物件的實例之後，您可以在腳本中使用它。</span><span class="sxs-lookup"><span data-stu-id="e5e48-125">After you have created an instance of the COM object, you can use it in scripts.</span></span> <span data-ttu-id="e5e48-126">這會在下列 VBScript 範例中說明，此範例會設定 COM 物件的 Border 屬性值。</span><span class="sxs-lookup"><span data-stu-id="e5e48-126">Doing this is illustrated in the VBScript example following, which sets the value of the COM object's Border property.</span></span>

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a><span data-ttu-id="e5e48-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5e48-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5e48-128">使用 COM 物件編寫腳本</span><span class="sxs-lookup"><span data-stu-id="e5e48-128">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




