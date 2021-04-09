---
description: 您可以使用下列方法來為您的 COM + 應用程式設定應用程式回收值。
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: 設定 COM + 應用程式回收值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111444"
---
# <a name="configuring-com-application-recycling-values"></a><span data-ttu-id="5ea80-103">設定 COM + 應用程式回收值</span><span class="sxs-lookup"><span data-stu-id="5ea80-103">Configuring COM+ Application Recycling Values</span></span>

<span data-ttu-id="5ea80-104">您可以使用下列方法來為您的 COM + 應用程式設定應用程式回收值。</span><span class="sxs-lookup"><span data-stu-id="5ea80-104">You can use the following methods to configure application recycling values for your COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="5ea80-105">您無法回收已設定為以 Windows 服務形式執行的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5ea80-105">You cannot recycle a COM+ application that has been configured to run as a Windows service.</span></span> <span data-ttu-id="5ea80-106">此外，程式庫應用程式具有其主機進程的回收和共用屬性。</span><span class="sxs-lookup"><span data-stu-id="5ea80-106">Also, library applications have the recycling and pooling properties of their host process.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="5ea80-107">元件服務系統管理工具</span><span class="sxs-lookup"><span data-stu-id="5ea80-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="5ea80-108">若要設定 COM + 應用程式的應用程式回收，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="5ea80-108">To configure application recycling for a COM+ application, use the following steps:</span></span>

1.  <span data-ttu-id="5ea80-109">在 [元件服務] 系統管理工具的主控台樹中，以滑鼠右鍵按一下您要回收的 COM + 伺服器應用程式，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="5ea80-109">In the console tree of the Component Services administrative tool, right-click the COM+ server application you want to be recycled and then click **Properties**.</span></span>

2.  <span data-ttu-id="5ea80-110">在 [共用 **& 回收** ] 索引標籤上，根據您要使用的準則，輸入 **存留期限制 (分鐘** 的值) 、 **記憶體限制 (KB)**、 **到期時間 (分鐘**) 、 **通話限制** 和 **啟用限制**。</span><span class="sxs-lookup"><span data-stu-id="5ea80-110">On the **Pooling & Recycling** tab, enter values for **Lifetime Limit (minutes)**, **Memory Limit (KB)**, **Expiration Timeout (minutes)**, **Call Limit**, and **Activation Limit**, depending on the criteria you want to use.</span></span>

    -   <span data-ttu-id="5ea80-111">**存留期限制** 表示進程在回收之前可執行檔最大分鐘數。</span><span class="sxs-lookup"><span data-stu-id="5ea80-111">**Lifetime Limit** indicates the maximum number of minutes a process can run before it's recycled.</span></span> <span data-ttu-id="5ea80-112">有效範圍是從0到30240分鐘 (21 天) 。</span><span class="sxs-lookup"><span data-stu-id="5ea80-112">The valid range is 0 through 30,240 minutes (21 days).</span></span> <span data-ttu-id="5ea80-113">預設分鐘數為0。</span><span class="sxs-lookup"><span data-stu-id="5ea80-113">The default number of minutes is 0.</span></span>
    -   <span data-ttu-id="5ea80-114">**記憶體限制** 表示回收進程之前，進程記憶體使用量的最大數量 (以 kb) 。</span><span class="sxs-lookup"><span data-stu-id="5ea80-114">**Memory Limit** indicates the maximum amount of process memory usage (in kilobytes) before recycling the process.</span></span> <span data-ttu-id="5ea80-115">如果處理程序的記憶體使用量超出指定的數量達一分鐘以上，就會回收處理程序。</span><span class="sxs-lookup"><span data-stu-id="5ea80-115">If the process's memory usage exceeds the specified number for longer than one minute, the process is recycled.</span></span> <span data-ttu-id="5ea80-116">有效範圍是0到 1048576 KB，預設記憶體使用量數量為 0 KB。</span><span class="sxs-lookup"><span data-stu-id="5ea80-116">The valid range is 0 through 1,048,576 KB, and the default amount of memory usage is 0 KB.</span></span>
    -   <span data-ttu-id="5ea80-117">**到期時間** 表示在強制關機之前，要等候的分鐘數，以釋放進程中物件的所有外部參考。</span><span class="sxs-lookup"><span data-stu-id="5ea80-117">**Expiration Timeout** indicates the number of minutes to wait, before being forcibly shut down, for the release of all external references to objects in the process.</span></span> <span data-ttu-id="5ea80-118">有效範圍是從1到1440分鐘 (24 小時) ，而預設到期時間為15分鐘。</span><span class="sxs-lookup"><span data-stu-id="5ea80-118">The valid range is 1 through 1440 minutes (24 hours), and the default expiration time-out is 15 minutes.</span></span> <span data-ttu-id="5ea80-119">只有當已根據其他條件決定將回收處理程序時，才會使用此值。</span><span class="sxs-lookup"><span data-stu-id="5ea80-119">This value is used only when it is already determined that a process will be recycled based on the other criteria.</span></span>
    -   <span data-ttu-id="5ea80-120">[**通話限制**] 表示在回收進程之前，應用程式物件可以接受的呼叫數上限。</span><span class="sxs-lookup"><span data-stu-id="5ea80-120">**Call Limit** indicates the maximum number of calls that application objects can accept before recycling the process.</span></span> <span data-ttu-id="5ea80-121">有效範圍是從0到1048576的呼叫，而預設的呼叫數目為0。</span><span class="sxs-lookup"><span data-stu-id="5ea80-121">The valid range is 0 through 1,048,576 calls, and the default number of calls is 0.</span></span>
    -   <span data-ttu-id="5ea80-122">**啟用限制** 表示回收進程之前，要接受的應用程式物件啟用數目上限。</span><span class="sxs-lookup"><span data-stu-id="5ea80-122">**Activation Limit** indicates the maximum number of application object activations to accept before recycling the process.</span></span> <span data-ttu-id="5ea80-123">有效範圍是0到1048576的啟用，而啟用的預設數目為0。</span><span class="sxs-lookup"><span data-stu-id="5ea80-123">The valid range is 0 through 1,048,576 activations, and the default number of activations is 0.</span></span>

    > [!Note]  
    > <span data-ttu-id="5ea80-124">如果 **存留期限制**、 **記憶體限制**、 **通話限制** 或 **啟用限制** 值設定為 0 (預設值) ，則會停用該準則的應用程式回收。</span><span class="sxs-lookup"><span data-stu-id="5ea80-124">When the **Lifetime Limit**, **Memory Limit**, **Call Limit**, or **Activation Limit** value is set to 0 (the default value), application recycling for that criterion is disabled.</span></span> <span data-ttu-id="5ea80-125">當這四個準則都設定為0時，會停用所選應用程式的應用程式回收。</span><span class="sxs-lookup"><span data-stu-id="5ea80-125">When all four of these criteria are set to 0, application recycling is disabled for the selected application.</span></span>

     

3.  <span data-ttu-id="5ea80-126">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="5ea80-126">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="5ea80-127">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5ea80-127">Visual Basic</span></span>

<span data-ttu-id="5ea80-128">Microsoft Visual Basic 中的下列函式示範如何為您選擇的任何 COM + 伺服器應用程式設定應用程式回收值。</span><span class="sxs-lookup"><span data-stu-id="5ea80-128">The following function in Microsoft Visual Basic demonstrates how you can set the application recycling values for any COM+ server application that you choose.</span></span> <span data-ttu-id="5ea80-129">若要從 Visual Basic 使用它，請將參考新增至 COM + 系統管理員類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="5ea80-129">To use it from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



<span data-ttu-id="5ea80-130">若要使用函式，請提供應用程式名稱的字串值，以及所需應用程式回收設定的整數值。</span><span class="sxs-lookup"><span data-stu-id="5ea80-130">To use the function, provide a string value for the application name and integer values for the desired application recycling settings.</span></span> <span data-ttu-id="5ea80-131">下列 Visual Basic 程式碼示範如何將 **RecycleLifetimeLimit** 值設定為5、將 **RecycleMemoryLimit** 值設定為10、將 **RecycleCallLimit** 值設定為9、將 **RecycleActivationLimit** 值設定為100，以及將 **RecycleExpirationTimeout** 值設定為15。</span><span class="sxs-lookup"><span data-stu-id="5ea80-131">The following Visual Basic code shows how to set the **RecycleLifetimeLimit** value to 5, the **RecycleMemoryLimit** value to 10, the **RecycleCallLimit** value to 9, the **RecycleActivationLimit** value to 100, and the **RecycleExpirationTimeout** value to 15.</span></span>


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a><span data-ttu-id="5ea80-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ea80-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ea80-133">COM + 應用程式回收概念</span><span class="sxs-lookup"><span data-stu-id="5ea80-133">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



