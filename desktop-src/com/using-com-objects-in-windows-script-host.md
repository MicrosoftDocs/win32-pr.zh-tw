---
title: 在 Windows Script Host 中使用 COM 物件
description: Microsoft Windows Script Host 是一個腳本公用程式，可讓您用來在基底作業系統內執行腳本。
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696341"
---
# <a name="using-com-objects-in-windows-script-host"></a><span data-ttu-id="b8ac4-103">在 Windows Script Host 中使用 COM 物件</span><span class="sxs-lookup"><span data-stu-id="b8ac4-103">Using COM Objects in Windows Script Host</span></span>

<span data-ttu-id="b8ac4-104">Microsoft Windows Script Host 是一個腳本公用程式，可讓您用來在基底作業系統內執行腳本。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-104">Microsoft Windows Script Host is a scripting utility you can use to run scripts within the base operating system.</span></span> <span data-ttu-id="b8ac4-105">您可以使用 Windows Script Host 將一般工作自動化，並建立功能強大的宏和登入腳本。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-105">You can use Windows Script Host to automate common tasks and to create powerful macros and logon scripts.</span></span> <span data-ttu-id="b8ac4-106">Windows Script Host 隨附于 VBScript 和 JScript ActiveX 腳本引擎。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-106">Windows Script Host comes with VBScript and JScript ActiveX scripting engines.</span></span> <span data-ttu-id="b8ac4-107">其他軟體公司則提供 ActiveX 腳本引擎，適用于 PerlScript、PScript、Python 等語言。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-107">Other software companies provide ActiveX scripting engines for languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="b8ac4-108">若要在 Windows Script Host 所執行的腳本中使用 COM 物件，您必須先建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-108">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="b8ac4-109">建立 COM 物件之後，您就可以在腳本中使用它。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-109">After a COM object has been created, you can then use it in scripts.</span></span>

<span data-ttu-id="b8ac4-110">Windows Script Host 包含兩個應用程式。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-110">Windows Script Host consists of two applications.</span></span> <span data-ttu-id="b8ac4-111">其中一個會從 Windows 桌面 () 執行腳本，另一個則是 `WScript.exe` 從命令提示字元 () 執行腳本 `CScript.exe` 。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-111">One runs scripts from the Windows desktop (`WScript.exe`); the other runs scripts from the command prompt (`CScript.exe`).</span></span>

<span data-ttu-id="b8ac4-112">若要從桌面執行腳本，只要按兩下腳本檔即可。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-112">To run a script from the desktop, simply double-click a script file.</span></span> <span data-ttu-id="b8ac4-113">指令檔是文字檔。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-113">Script files are text files.</span></span> <span data-ttu-id="b8ac4-114">依照慣例，VBScript 檔案具有副檔名 `.vbs` 和 JScript 檔案 `.js` 。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-114">By convention, VBScript files have the extension `.vbs` and JScript files `.js`.</span></span>

<span data-ttu-id="b8ac4-115">若要從命令提示字元執行腳本，請 `Cscript.exe` 使用命令列執行應用程式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b8ac4-115">To run a script from the command prompt, run the `Cscript.exe` application with a command line such as the following:</span></span>

```console
cscript "c:\\sample scripts\\chart.vbs"
```

<span data-ttu-id="b8ac4-116">其中 `c:\\sample scripts\\chart.vbs` 是包含腳本之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-116">where `c:\\sample scripts\\chart.vbs` is the path to the file containing the script.</span></span>

<span data-ttu-id="b8ac4-117">您可以輸入下列命令列，以列印 Cscript.exe 所支援的參數清單：</span><span class="sxs-lookup"><span data-stu-id="b8ac4-117">You can print out a list of the parameters supported by Cscript.exe by entering the following command line:</span></span>

```console
call cscript //?
```

<span data-ttu-id="b8ac4-118">若要在 Windows Script Host 所執行的腳本中使用 COM 物件，您必須先建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-118">To use a COM object in a script run by Windows Script Host, you must first create an instance of the object.</span></span> <span data-ttu-id="b8ac4-119">在 VBScript 中，您可以藉由呼叫方法來完成這項作業 `CreateObject()` 。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-119">In VBScript you can do this by calling the `CreateObject()` method.</span></span> <span data-ttu-id="b8ac4-120">在 JScript 中，您可以使用 `ActiveXObject` 物件或 `WScript.CreateObject()` 方法。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-120">In JScript one can use either the `ActiveXObject` object or the `WScript.CreateObject()` method.</span></span> <span data-ttu-id="b8ac4-121">下列範例說明如何 `CreateObject()` 使用 VBScript 呼叫：</span><span class="sxs-lookup"><span data-stu-id="b8ac4-121">The following example illustrates calling `CreateObject()` using VBScript:</span></span>


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



<span data-ttu-id="b8ac4-122">下列範例說明如何 `ActiveXObject` 使用 JScript 建立物件：</span><span class="sxs-lookup"><span data-stu-id="b8ac4-122">The following example illustrates creating an `ActiveXObject` object using JScript:</span></span>


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
<span data-ttu-id="b8ac4-123">或者，使用 `WScript.CreateObject()` JScript 內的方法：</span><span class="sxs-lookup"><span data-stu-id="b8ac4-123">Alternatively using `WScript.CreateObject()` method inside JScript:</span></span>

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


<span data-ttu-id="b8ac4-124">建立 COM 物件的實例之後，您可以撰寫使用物件的腳本，例如：</span><span class="sxs-lookup"><span data-stu-id="b8ac4-124">After you have created an instance of the COM object, you can write script that uses the object, for example:</span></span>


```VB
objXL.Visible = true;
 
```



<span data-ttu-id="b8ac4-125">除了 CreateObject 方法和 ActiveXObject 物件之外，VBScript 和 JScript 都提供 GetObject 的方法，後者會傳回物件實例。</span><span class="sxs-lookup"><span data-stu-id="b8ac4-125">In addition to the CreateObject method and ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8ac4-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8ac4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8ac4-127">使用 COM 物件編寫腳本</span><span class="sxs-lookup"><span data-stu-id="b8ac4-127">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




