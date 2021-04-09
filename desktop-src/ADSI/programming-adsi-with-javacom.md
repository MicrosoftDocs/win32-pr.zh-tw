---
title: 使用 JAVA/COM 編寫 ADSI 程式設計
description: 您可以使用 Microsoft virtual machine for JAVA (Microsoft VM) 和 Microsoft JAVA 編譯器，從 JAVA/COM 應用程式存取所有透過任何 ADSI COM 元件公開的 ADSI 功能。
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- 使用 JAVA/COM AD 撰寫 ADSI 程式設計
- ADSI ADSI、使用、JAVA/COM 程式設計
- ADSI ADSI，範例程式碼 JAVA
- ADSI ADSI，範例程式碼 JAVA，系結至 ADSI 物件，並在該物件上叫用方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839151"
---
# <a name="programming-adsi-with-javacom"></a><span data-ttu-id="694bb-107">使用 JAVA/COM 編寫 ADSI 程式設計</span><span class="sxs-lookup"><span data-stu-id="694bb-107">Programming ADSI with Java/COM</span></span>

<span data-ttu-id="694bb-108">您可以使用 Microsoft virtual machine for JAVA (Microsoft VM) 和 Microsoft JAVA 編譯器，從 JAVA/COM 應用程式存取所有透過任何 ADSI COM 元件公開的 ADSI 功能。</span><span class="sxs-lookup"><span data-stu-id="694bb-108">Using the Microsoft virtual machine for Java (Microsoft VM) and Microsoft Java Compiler, you have access to all the ADSI features exposed through any ADSI COM components, from a Java/COM application.</span></span> <span data-ttu-id="694bb-109">下列 JAVA 程式碼範例顯示系結至 ADSI 物件，並在該物件上叫用方法所需的元素。</span><span class="sxs-lookup"><span data-stu-id="694bb-109">The following Java code example shows the elements necessary to bind to an ADSI object and invoke methods on that object.</span></span> <span data-ttu-id="694bb-110">必要的 ADSI API 函數和物件方法會透過 Activeds.dll 公開。</span><span class="sxs-lookup"><span data-stu-id="694bb-110">The required ADSI API functions and object methods are exposed through Activeds.dll.</span></span>


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



<span data-ttu-id="694bb-111">第一個 **import** 語句中的引數是指封裝于 Activeds.dll 中的 JAVA 包裝函式類別。</span><span class="sxs-lookup"><span data-stu-id="694bb-111">The argument in the first **import** statement refers to Java Wrapper classes packaged in Activeds.dll.</span></span> <span data-ttu-id="694bb-112">使用 Visual c + + 來建立包裝函式類別，並將它們包含在您的專案中，請遵循下列程式。</span><span class="sxs-lookup"><span data-stu-id="694bb-112">Use Visual J++ to create the wrapper classes and include them in your project, following the procedure below.</span></span>

<span data-ttu-id="694bb-113">**建立包裝函式類別，並將它們包含在您的專案中**</span><span class="sxs-lookup"><span data-stu-id="694bb-113">**To create wrapper classes and include them in your project**</span></span>

1.  <span data-ttu-id="694bb-114">在 Visual c + + 專案中，從 [**專案**] 功能表選取 [**加入 Com 包裝** 函式 ...]。</span><span class="sxs-lookup"><span data-stu-id="694bb-114">In a Visual J++ project, select **Add Com Wrapper...** from the **Project** menu.</span></span>
2.  <span data-ttu-id="694bb-115">從 [COM 包裝函式] 對話方塊的 [ **已安裝的元件** ] 中選取 [Active DS 類型程式庫]。</span><span class="sxs-lookup"><span data-stu-id="694bb-115">Select "Active DS Type Library" from the **Installed Components:** from the COM Wrappers dialog.</span></span> <span data-ttu-id="694bb-116">如果清單方塊中未顯示類型程式庫，請按一下 [ **流覽 ...]** 按鈕，流覽至儲存 Activeds 的目錄，然後選取類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="694bb-116">If the type library is not shown in the list box, click the **Browse...** button, navigate to the directory where Activeds.tlb is stored, and then select the type library.</span></span>

<span data-ttu-id="694bb-117">Visual c + + 會建立 JAVA 包裝函式類別的 activeds 封裝，並將封裝包含在專案的預設路徑中。</span><span class="sxs-lookup"><span data-stu-id="694bb-117">Visual J++ creates the activeds package for the Java Wrapper classes and include the package into the project's default path.</span></span> <span data-ttu-id="694bb-118">如需詳細資訊，請參閱 Visual c + + 視窗上 [ **專案探索** ] 窗格中的 activeds 套件。</span><span class="sxs-lookup"><span data-stu-id="694bb-118">For more information, see the activeds package in the **Project Explore** pane on the Visual J++ window.</span></span>

<span data-ttu-id="694bb-119">若要取得無法 cocreated 的 ADSI 物件，請使用其中一個已公開的 ADSI API 函式，例如 [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) 或 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)，這些函式也會封裝在 Activeds.dll 中。</span><span class="sxs-lookup"><span data-stu-id="694bb-119">To get an ADSI object that cannot be cocreated, use one of the exposed ADSI API functions, for example, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), which are also packaged in Activeds.dll.</span></span> <span data-ttu-id="694bb-120">Microsoft J/Direct 提供這些和其他原生 Api 的存取權。</span><span class="sxs-lookup"><span data-stu-id="694bb-120">Microsoft J/Direct provides access to these and other native APIs.</span></span> <span data-ttu-id="694bb-121">上述程式碼範例的最後兩行說明這一點。</span><span class="sxs-lookup"><span data-stu-id="694bb-121">This is illustrated by the last two lines of the code example, above.</span></span>

<span data-ttu-id="694bb-122">在編譯時，請確定已啟用 Microsoft 語言延伸模組。</span><span class="sxs-lookup"><span data-stu-id="694bb-122">When compiling, ensure that Microsoft Language Extension is enabled.</span></span> <span data-ttu-id="694bb-123">若要這樣做，請從 [Visual j + + 專案] 視窗中的 [**專案**] 功能表選取 [ **<project> 屬性 ...** ]。</span><span class="sxs-lookup"><span data-stu-id="694bb-123">To do this, select **<project> Properties...** from the **Project** menu in the Visual J++ project window.</span></span> <span data-ttu-id="694bb-124">然後，按一下 [ **<project> 屬性**] 對話方塊中的 [**編譯**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="694bb-124">Then, click the **Compile** tab in the **<project> Properties** dialog.</span></span> <span data-ttu-id="694bb-125">清除 [ **停用 Microsoft 語言擴充** 功能] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="694bb-125">Clear the **Disable Microsoft Language Extensions** check box.</span></span> <span data-ttu-id="694bb-126">如果是從命令列編譯，請使用 "/x-" 參數，例如：</span><span class="sxs-lookup"><span data-stu-id="694bb-126">If compiling from the command line, use "/x-" switch, for example:</span></span>

<span data-ttu-id="694bb-127">**jvc/x-SimpleADSI .java**</span><span class="sxs-lookup"><span data-stu-id="694bb-127">**jvc /x- SimpleADSI.java**</span></span>

<span data-ttu-id="694bb-128">最後，為了讓虛擬機器載入 COM 元件，必須在系統路徑上看到動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="694bb-128">Finally, in order for the virtual machine to load the COM component, the dynamic-link library (DLL) must be visible on the system path.</span></span> <span data-ttu-id="694bb-129">如果傳回 "UnsatisfiedLinkError" 錯誤，請將路徑設定為包含所需 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="694bb-129">If a "java.lang.UnsatisfiedLinkError" error is returned, set the PATH to include the path that contains the required DLL.</span></span> <span data-ttu-id="694bb-130">例如，如果 Activeds.dll 已安裝在 c： \\ adsi lib 中 \\ ，請從命令列發出下列命令：</span><span class="sxs-lookup"><span data-stu-id="694bb-130">For example, if Activeds.dll has been installed in c:\\adsi\\lib, issue the following command from the command line:</span></span>

<span data-ttu-id="694bb-131">**set PATH =% PATH%;c： \\ adsi \\ lib**</span><span class="sxs-lookup"><span data-stu-id="694bb-131">**set PATH = %PATH%; c:\\adsi\\lib**</span></span>

 

 




