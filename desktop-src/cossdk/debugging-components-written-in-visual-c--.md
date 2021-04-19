---
description: 當您準備好要在 Microsoft Visual C++ 元件中進行 COM + 功能的偵錯工具時，您可以設定 Visual C++ 專案或 [元件服務] 系統管理工具來啟動偵錯工具。
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: 調試 Visual C++ 中撰寫的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970313"
---
# <a name="debugging-components-written-in-visual-c"></a><span data-ttu-id="c3723-103">調試 Visual C++ 中撰寫的元件</span><span class="sxs-lookup"><span data-stu-id="c3723-103">Debugging Components Written in Visual C++</span></span>

<span data-ttu-id="c3723-104">當您準備好要在 Microsoft Visual C++ 元件中進行 COM + 功能的偵錯工具時，您可以設定 Visual C++ 專案或 [元件服務] 系統管理工具來啟動偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c3723-104">When you are ready to debug the COM+ functionality in your Microsoft Visual C++ components, you can configure Visual C++ project or the Component Services administrative tool to launch the debugger.</span></span> <span data-ttu-id="c3723-105">如果您使用 Visual C++，就可以使用 OLE RPC 和即時 (JIT) 的偵測，以遠端用戶端進行的調試。</span><span class="sxs-lookup"><span data-stu-id="c3723-105">If you are using Visual C++, you can debug with a remote client using OLE RPC and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="c3723-106">如果您無法在偵錯工具下執行用戶端，或者用戶端是在另一部電腦上執行，您可以在 **偵錯工具設定中** 使用 Com + 啟動。</span><span class="sxs-lookup"><span data-stu-id="c3723-106">If you are unable to run your client under the debugger or if the client is running on another machine, you can use the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="c3723-107">您可以在 [COM + 應用程式 **屬性**] 對話方塊的 [ **Advanced** ] 索引標籤上，于 [元件服務] 系統管理工具中找到這個核取方塊。</span><span class="sxs-lookup"><span data-stu-id="c3723-107">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span>

<span data-ttu-id="c3723-108">當您完成偵錯工具時，您應該關閉正在進行偵錯工具的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3723-108">When you are finished debugging, you should shut down the COM+ applications you are debugging.</span></span> <span data-ttu-id="c3723-109">如果伺服器進程仍在執行中，當您下次嘗試在記憶體中載入現有的 DLL 時，當您嘗試建立 DLL 時，您可能會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="c3723-109">If a server process is left running, you might get an error message the next time you try to build a DLL when the existing DLL is still loaded in memory.</span></span> <span data-ttu-id="c3723-110">若要關閉 COM + 應用程式，請在主控台樹中的應用程式上按一下滑鼠右鍵，然後按一下 [ **關閉**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-110">To shut down a COM+ application, right-click the application in the console tree and then click **Shut down**.</span></span>

> [!Note]  
> <span data-ttu-id="c3723-111">如果您使用交易，您可能也會想要增加交易超時時間（預設為60秒）。</span><span class="sxs-lookup"><span data-stu-id="c3723-111">If you are using transactions, you might also want to increase the transaction time-out, which defaults to 60 seconds.</span></span> <span data-ttu-id="c3723-112">您也可以指定0的值，有效地指定無限的交易超時時間。</span><span class="sxs-lookup"><span data-stu-id="c3723-112">You can also specify a value of 0, effectively specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="c3723-113">使用 [元件服務] 系統管理工具，變更 [**我的電腦屬性**] 視窗中 [**選項**] 索引標籤上的 [交易超時設定]。</span><span class="sxs-lookup"><span data-stu-id="c3723-113">Using the Component Services administrative tool, change the transaction time-out setting on the **Options** tab of the **My Computer Properties** window.</span></span>

 

## <a name="debugging-server-application-components-with-visual-c"></a><span data-ttu-id="c3723-114">使用 Visual C++ 來調試伺服器應用程式元件</span><span class="sxs-lookup"><span data-stu-id="c3723-114">Debugging Server Application Components with Visual C++</span></span>

<span data-ttu-id="c3723-115">在偵測 COM + 伺服器應用程式時，您可能會想要將用戶端和伺服器應用程式同時載入至偵錯工具，以進行遠端呼叫的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c3723-115">When debugging COM+ server applications, you may want to debug remote calls by loading both the client and the server application into the debugger.</span></span> <span data-ttu-id="c3723-116">使用 Visual C++，您可以透過即時 (JIT) 和 OLE RPC 設定，來對元件進行遠端呼叫的偵測。</span><span class="sxs-lookup"><span data-stu-id="c3723-116">With Visual C++, you can debug remote calls to your components through the just-in-time (JIT) and OLE RPC settings.</span></span> <span data-ttu-id="c3723-117">JIT 設定會導致編譯的元件在發生錯誤時啟動 Visual C++ 偵錯工具;當您逐步執行程式碼時，OLE RPC 設定可讓偵錯工具逐步執行用戶端與元件。</span><span class="sxs-lookup"><span data-stu-id="c3723-117">The JIT setting causes the compiled component to start the Visual C++ debugger when an error occurs; the OLE RPC setting enables the debugger to step from client to component as you step through your code.</span></span>

<span data-ttu-id="c3723-118">啟用這些功能時，您可以在偵錯工具下啟動您的用戶端。</span><span class="sxs-lookup"><span data-stu-id="c3723-118">When these features are enabled, you can start your client under the debugger.</span></span> <span data-ttu-id="c3723-119">當用戶端對您的元件進行呼叫時，偵錯工具會逐步執行伺服器進程中的元件程式碼，即使伺服器位於網路上的其他電腦上也一樣。</span><span class="sxs-lookup"><span data-stu-id="c3723-119">When the client makes a call to your component, the debugger will step into the component's code in the server process, even if the server is on a different computer on the network.</span></span> <span data-ttu-id="c3723-120">必要時，伺服器電腦上的偵錯工具會自動啟動。</span><span class="sxs-lookup"><span data-stu-id="c3723-120">A debugging session is automatically started on the server computer if necessary.</span></span> <span data-ttu-id="c3723-121">同樣地，在元件程式碼中的 return 語句之後的單一逐步執行，將會傳回用戶端程式代碼中下一個語句的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c3723-121">Similarly, single stepping past the return statement in the component's code will return debugging to the next statement in the client's code.</span></span>

> [!Note]  
> <span data-ttu-id="c3723-122">您可以使用 [COM + **啟動于偵錯工具** ] 設定來儲存幾個步驟。</span><span class="sxs-lookup"><span data-stu-id="c3723-122">You may be able to save a few steps by using the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="c3723-123">這可讓您指定 Visual C++ (或其他) 偵錯工具，而不需要在 Visual C++ 環境中進行特殊的偵錯工具設定。</span><span class="sxs-lookup"><span data-stu-id="c3723-123">This allows you to specify the Visual C++ (or other) debugger without having to make special debug settings in the Visual C++ environment.</span></span> <span data-ttu-id="c3723-124">您可以在 [COM + 應用程式 **屬性**] 對話方塊的 [ **Advanced** ] 索引標籤上，于 [元件服務] 系統管理工具中找到這個核取方塊。</span><span class="sxs-lookup"><span data-stu-id="c3723-124">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span> <span data-ttu-id="c3723-125">如需詳細資訊，請參閱本主題中的「不 Visual C++ 的偵錯工具」。</span><span class="sxs-lookup"><span data-stu-id="c3723-125">For more information, see "Debugging Without Visual C++" in this topic.</span></span>

 

<span data-ttu-id="c3723-126">當包含元件的 COM + 應用程式是伺服器應用程式時，您必須先使用 [元件服務] 系統管理工具來關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3723-126">When the COM+ application containing your component is a server application, you must begin by shutting down the application using the Component Services administrative tool.</span></span> <span data-ttu-id="c3723-127">若要這樣做，請在主控台樹中的 COM + 應用程式上按一下滑鼠右鍵，然後按一下 [ **關閉**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-127">To do this, right-click the COM+ application in the console tree and then click **Shut down**.</span></span>

<span data-ttu-id="c3723-128">**若要在 Visual C++ 中啟用 RPC 調試**</span><span class="sxs-lookup"><span data-stu-id="c3723-128">**To enable RPC debugging in Visual C++**</span></span>

1.  <span data-ttu-id="c3723-129">在 Visual C++ 中，按一下 [ **工具** ] 功能表上的 [ **選項**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-129">In Visual C++, on the **Tools** menu, click **Options**.</span></span>

2.  <span data-ttu-id="c3723-130">在 [ **選項** ] 對話方塊的 [ **調試** ] 索引標籤上，選取 [ **OLE RPC 調試** 和 **即時調試** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="c3723-130">In the **Options** dialog box, on the **Debug** tab, select the **OLE RPC debugging** and **Just-in time debugging** check boxes.</span></span>

3.  <span data-ttu-id="c3723-131">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="c3723-131">Click **OK**.</span></span>

<span data-ttu-id="c3723-132">若要開始進行偵錯工具，請在偵錯工具中啟動您的用戶端專案。</span><span class="sxs-lookup"><span data-stu-id="c3723-132">To begin debugging, start your client project in the debugger.</span></span>

<span data-ttu-id="c3723-133">您也可以在偵錯工具中不啟動用戶端的情況下，對元件進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c3723-133">You can also debug your component without launching your client in the debugger.</span></span> <span data-ttu-id="c3723-134">在此情況下，您的元件必須自行啟動偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c3723-134">In this case, your component must launch the debugger on its own.</span></span> <span data-ttu-id="c3723-135">若要這樣做，您的元件專案必須針對 debug 會話指定可執行檔，以及 COM + 應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3723-135">To do this, your component project must specify an executable for the debug session, along with the COM+ application ID.</span></span>

<span data-ttu-id="c3723-136">**若要啟用伺服器應用程式元件以啟動 Visual C++ 偵錯工具**</span><span class="sxs-lookup"><span data-stu-id="c3723-136">**To enable a server application component to launch the Visual C++ debugger**</span></span>

1.  <span data-ttu-id="c3723-137">在 [ **專案** ] 功能表上，按一下 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-137">On the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="c3723-138">在 [ **專案設定** ] 對話方塊的 [ **設定** ] 方塊中，選取 [ **Win32 Debug**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-138">In the **Project Settings** dialog box, in the **Settings For** box, select **Win32 Debug**.</span></span>

3.  <span data-ttu-id="c3723-139">在 [ **調試** ] 索引標籤的 [ **類別目錄** ] 方塊中，選取 **[一般**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-139">On the **Debug** tab, in the **Category** box, select **General**.</span></span>

4.  <span data-ttu-id="c3723-140">在 [ **用於偵錯工具的可執行檔** ] 方塊中，輸入 Dllhost.exe 的完整路徑，後面接著一個引數，指定包含元件的 com + 應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3723-140">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the application ID of the COM+ application containing the component.</span></span>

    > [!Note]  
    > <span data-ttu-id="c3723-141">您可以使用 [元件服務] 系統管理工具，在 [COM + 應用程式的 **屬性**] 對話方塊的 [**一般**] 索引標籤上找到應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3723-141">Using the Component Services administrative tool, you will find the application ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="c3723-142">以下是範例：</span><span class="sxs-lookup"><span data-stu-id="c3723-142">Following is an example:</span></span>

     

    > [!Note]  
    > <span data-ttu-id="c3723-143">C： \\ Winnt \\ System32 \\Dllhost.exe/ProcessID： {applicationID}</span><span class="sxs-lookup"><span data-stu-id="c3723-143">C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{applicationID}</span></span>

     

5.  <span data-ttu-id="c3723-144">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="c3723-144">Click **OK**.</span></span>

<span data-ttu-id="c3723-145">您現在可以設定中斷點、啟動偵錯工具，以及開始對您的元件進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="c3723-145">You can now set breakpoints, start the debugger, and begin making calls to your component.</span></span>

## <a name="debugging-library-application-components-with-visual-c"></a><span data-ttu-id="c3723-146">使用 Visual C++ 偵錯工具程式庫應用程式元件</span><span class="sxs-lookup"><span data-stu-id="c3723-146">Debugging Library Application Components with Visual C++</span></span>

<span data-ttu-id="c3723-147">若要在程式庫應用程式中進行元件的偵錯工具，您必須設定用戶端的專案，因為用戶端的進程將裝載程式庫應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3723-147">To debug components in a library application, you must configure the client's project because the client's process will host the library application.</span></span>

<span data-ttu-id="c3723-148">**使用 Visual C++ 啟用程式庫應用程式偵錯工具**</span><span class="sxs-lookup"><span data-stu-id="c3723-148">**To enable library application debugging with Visual C++**</span></span>

1.  <span data-ttu-id="c3723-149">在 Visual C++ 的 [ **專案** ] 功能表上，按一下 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-149">In Visual C++, on the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="c3723-150">在 [ **專案設定** ] 對話方塊的 [ **設定** ] 方塊中，按一下 [ **Win32 Debug**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-150">In the **Project Settings** dialog box, in the **Settings For** box, click **Win32 Debug**.</span></span>

3.  <span data-ttu-id="c3723-151">在 [ **調試** ] 索引標籤的 [ **類別目錄** ] 方塊中，按一下 [ **其他 dll**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-151">On the **Debug** tab, in the **Category** box, click **Additional DLLs**.</span></span>

4.  <span data-ttu-id="c3723-152">在 **模組** 清單中，在您的程式庫應用程式中新增元件 dll。</span><span class="sxs-lookup"><span data-stu-id="c3723-152">In the **Modules** list, add the component DLLs in your library application.</span></span> <span data-ttu-id="c3723-153">這可讓您在實際載入 DLL 之前設定中斷點。</span><span class="sxs-lookup"><span data-stu-id="c3723-153">This allows you to set breakpoints before your DLL is actually loaded.</span></span>

5.  <span data-ttu-id="c3723-154">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="c3723-154">Click **OK**.</span></span>

## <a name="debugging-without-visual-c"></a><span data-ttu-id="c3723-155">不 Visual C++ 的調試</span><span class="sxs-lookup"><span data-stu-id="c3723-155">Debugging Without Visual C++</span></span>

<span data-ttu-id="c3723-156">無論您是否使用 Visual C++ 進行偵錯工具，都可以使用 [ **在偵錯工具中啟動** ] 設定來指定應在其中執行元件的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c3723-156">Whether or not you are using Visual C++ for debugging, you can use the **Launch in debugger** setting to specify the debugger in which your components should run.</span></span>

<span data-ttu-id="c3723-157">**從元件服務系統管理工具指定偵錯工具**</span><span class="sxs-lookup"><span data-stu-id="c3723-157">**To specify a debugger from the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="c3723-158">在主控台樹中，選取包含您想要進行偵錯工具之元件的 COM + 程式庫應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3723-158">In the console tree, select the COM+ library application containing the components you wish to debug.</span></span>

2.  <span data-ttu-id="c3723-159">以滑鼠右鍵按一下應用程式，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="c3723-159">Right-click the application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="c3723-160">在應用程式的 [ **屬性** ] 對話方塊中，按一下 [ **Advanced （Advanced** ）] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="c3723-160">In the application's **Properties** dialog box, click the **Advanced** tab.</span></span>

4.  <span data-ttu-id="c3723-161">在 [ **調試** 程式] 下，選取 [ **在偵錯工具中啟動** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="c3723-161">Under **Debugging**, select the **Launch in debugger** check box.</span></span>

5.  <span data-ttu-id="c3723-162">在 [ **偵錯工具路徑** ] 方塊中，輸入您要使用之偵錯工具的路徑。</span><span class="sxs-lookup"><span data-stu-id="c3723-162">In the **Debugger path** box, enter path to the debugger you want to use.</span></span> <span data-ttu-id="c3723-163">您也可以按一下 **[流覽]** 找出偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="c3723-163">You can also click **Browse** to locate the debugger.</span></span> <span data-ttu-id="c3723-164">以下是範例： C： \\ Winnt \\ System32 \\Ntsd.exe。</span><span class="sxs-lookup"><span data-stu-id="c3723-164">Following is an example: C:\\Winnt\\System32\\Ntsd.exe.</span></span>

6.  <span data-ttu-id="c3723-165">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="c3723-165">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3723-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3723-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3723-167">調試 Visual Basic 中撰寫的元件</span><span class="sxs-lookup"><span data-stu-id="c3723-167">Debugging Components Written in Visual Basic</span></span>](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



