---
title: 64位考慮
description: 隨著64位 Windows 的可用性增加，使用者預期的輸入方法（例如各種語言的國際鍵盤或輸入法編輯器） (Ime) 東亞語言，以符合32位和64位的應用程式。
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- 文字服務架構 (TSF) 、64位 Windows
- TSF (文字服務架構) ，64位 Windows
- 文字服務，64位 Windows
- 64 位元 Windows
- '文字服務架構 (TSF) 、輸入法編輯器 (IME) '
- 'TSF (文字服務架構) ，輸入法編輯器 (IME) '
- '文字服務、輸入法編輯器 (IME) '
- 輸入法 (IME)
- '輸入法 (輸入法編輯器) '
- 文字服務架構 (TSF) ，國際鍵盤
- TSF (文字服務架構) ，國際鍵盤
- 文字服務，國際鍵盤
- 國際鍵盤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045ec699c7a433f15b92467e3072d30acbf01936
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375645"
---
# <a name="64-bit-considerations"></a><span data-ttu-id="4cda2-116">64位考慮</span><span class="sxs-lookup"><span data-stu-id="4cda2-116">64-Bit Considerations</span></span>

<span data-ttu-id="4cda2-117">隨著64位 Windows 的可用性增加，使用者預期的輸入方法（例如各種語言的國際鍵盤或輸入法編輯器） (Ime) 東亞語言，以符合32位和64位的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4cda2-117">With the increasing availability of 64-bit Windows, users expect input methods, such as international keyboards in various languages or Input Method Editors (IMEs) in East Asian languages, to work properly with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="4cda2-118">開發 Microsoft Windows 的輸入方法元件或文字服務時，請務必將64位 Windows 視為產品的潛在目標平臺。</span><span class="sxs-lookup"><span data-stu-id="4cda2-118">When developing input method components or text services for Microsoft Windows, it is important to consider 64-bit Windows as a potential target platform for your product.</span></span>

<span data-ttu-id="4cda2-119">因為以文字服務架構) 為基礎的 Ime 和文字服務 (通常會實作為動態連結程式庫 (Dll) ，所以請務必注意，Dll 是專門針對32位環境或64位環境中的使用而建立的，64位應用程式不能使用針對32位環境所建立的 DLL，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="4cda2-119">Because IMEs and text services (based on the Text Services Framework) are typically implemented as dynamic-link libraries (DLLs), it is important to note that DLLs are built specifically for use in either 32-bit environments or 64-bit environments; a DLL built for use in 32-bit environments cannot be used by 64-bit applications, and vice versa.</span></span>

> [!Note]  
> <span data-ttu-id="4cda2-120">WOW64 無法減少此位特定的 DLL 限制。</span><span class="sxs-lookup"><span data-stu-id="4cda2-120">WOW64 does not mitigate this bit-specific DLL restriction.</span></span> <span data-ttu-id="4cda2-121">如需 WOW64 的詳細資訊，請參閱執行 [32 位應用程式](/windows/desktop/WinProg64/running-32-bit-applications)。</span><span class="sxs-lookup"><span data-stu-id="4cda2-121">For information about WOW64, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span>

 

<span data-ttu-id="4cda2-122">本主題將討論在64位 Windows 上開發 Ime 和文字服務的重要設計考慮。</span><span class="sxs-lookup"><span data-stu-id="4cda2-122">This topic discusses important design considerations for developing IMEs and text services for use on 64-bit Windows.</span></span>

## <a name="64-bit-considerations-for-imes"></a><span data-ttu-id="4cda2-123">64位的 Ime 考慮</span><span class="sxs-lookup"><span data-stu-id="4cda2-123">64-Bit Considerations for IMEs</span></span>

<span data-ttu-id="4cda2-124">本章節說明建立與64位 Windows 搭配使用之 Ime 時所牽涉到的特殊考慮。</span><span class="sxs-lookup"><span data-stu-id="4cda2-124">This section describes the special considerations involved with building IMEs for use with 64-bit Windows.</span></span> <span data-ttu-id="4cda2-125">如需有關輸入法的詳細資訊，請參閱 [輸入法編輯器](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility)。</span><span class="sxs-lookup"><span data-stu-id="4cda2-125">For information about IMEs, see [Input Method Editor](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility).</span></span>

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a><span data-ttu-id="4cda2-126">建立 IME 的32位和64位版本</span><span class="sxs-lookup"><span data-stu-id="4cda2-126">Building 32-Bit and 64-Bit Versions of an IME</span></span>

<span data-ttu-id="4cda2-127">由於先前提及 Dll 的32位/64 位相容性問題，因此必須採取一些預防措施，以確保在64位 Windows 上執行的任何應用程式 (32 位或64位) 都能以透明的方式運作。</span><span class="sxs-lookup"><span data-stu-id="4cda2-127">Because of the previously mentioned 32-bit/64-bit compatibility issue with DLLs, some precautions must be taken to ensure that IMEs work transparently with any application (32-bit or 64-bit) running on 64-bit Windows.</span></span> <span data-ttu-id="4cda2-128">針對64位平臺上的32位和64位應用程式，讓您的 IME 能以透明方式運作的建議解決方案，是建立並安裝平行的32位和64位版本的 IME DLL。</span><span class="sxs-lookup"><span data-stu-id="4cda2-128">The recommended solution for enabling your IME to work transparently with both 32-bit and 64-bit applications on a 64-bit platform is to build and install parallel 32-bit and 64-bit versions of the IME DLL.</span></span> <span data-ttu-id="4cda2-129">一般來說，開發人員會藉由調整其組建環境中的目標平臺設定，從單一來源建立平行 Dll。</span><span class="sxs-lookup"><span data-stu-id="4cda2-129">Typically, developers build parallel DLLs from a single source by adjusting the target platform settings in their build environment.</span></span> <span data-ttu-id="4cda2-130">如需有關單一來源的32位和64位應用程式的詳細資訊，請參閱 [準備取得64位 Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows)。</span><span class="sxs-lookup"><span data-stu-id="4cda2-130">For more information about single-sourcing 32-bit and 64-bit applications, see [Getting Ready for 64-bit Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).</span></span>

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a><span data-ttu-id="4cda2-131">64位和32位輸入方法編輯器的並存安裝</span><span class="sxs-lookup"><span data-stu-id="4cda2-131">Side-by-Side Installation of 64-Bit and 32-Bit Input Method Editors</span></span>

<span data-ttu-id="4cda2-132">Ime 和文字服務的開發人員應該留意本主題中所述的64位考慮。</span><span class="sxs-lookup"><span data-stu-id="4cda2-132">Developers of IMEs and text services should be aware of the 64-bit considerations described throughout this topic.</span></span> <span data-ttu-id="4cda2-133">幸運的是，這些服務的使用者不需要擔心這些執行特定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4cda2-133">Fortunately, end users of these services need not be concerned with these implementation-specific details.</span></span> <span data-ttu-id="4cda2-134">64位 Windows 的一項功能是能夠隱藏使用者的64位和32位特定版本的 IME Dll 需求。</span><span class="sxs-lookup"><span data-stu-id="4cda2-134">A feature of 64-bit Windows is the ability to hide the need for 64-bit and 32-bit-specific versions of the IME DLLs from end users.</span></span> <span data-ttu-id="4cda2-135">當兩個版本的 IME 都正確地以並存方式安裝時，64位的 Windows 會辨識 IME 的64位和32位版本是否存在，並將這些位特定的 Ime 呈現給終端使用者，作為單一 *邏輯* IME。</span><span class="sxs-lookup"><span data-stu-id="4cda2-135">When both versions of the IME are properly installed in a side-by-side manner, 64-bit Windows recognizes the presence of both 64-bit and 32-bit versions of the IME and presents these bit-specific IMEs to the end user as a single *logical* IME.</span></span> <span data-ttu-id="4cda2-136">當使用者需要使用 IME 時，64位的 Windows 會明確地選擇 (32 位或64位) 的輸入法版本，適用于指定的情況。</span><span class="sxs-lookup"><span data-stu-id="4cda2-136">When an end user needs to use an IME, 64-bit Windows transparently chooses the version of the IME (32-bit or 64-bit) that is appropriate for the given circumstances.</span></span>

<span data-ttu-id="4cda2-137">若要讓64位和32位 Ime 的並存安裝正常運作 (也就是，若要將兩個平臺特定的 Dll 表示為使用者) 的單一邏輯 IME，必須符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="4cda2-137">For side-by-side installations of 64-bit and 32-bit IMEs to function properly (that is, to represent the two platform-specific DLLs as a single logical IME to the user), the following conditions must be met:</span></span>

-   <span data-ttu-id="4cda2-138">開發人員必須建立一個適用于32位 Windows 的平臺特定 (版本，以及一個適用于64位 Windows) 的 IME DLL。</span><span class="sxs-lookup"><span data-stu-id="4cda2-138">Developers must build platform-specific versions (one for 32-bit Windows and one for 64-bit Windows) of the IME DLL.</span></span>
-   <span data-ttu-id="4cda2-139">32位和64位 Dll 必須共用相同的檔案名。</span><span class="sxs-lookup"><span data-stu-id="4cda2-139">The 32-bit and 64-bit DLLs must share the same file name.</span></span>
-   <span data-ttu-id="4cda2-140">必須遵循安裝目錄需求。</span><span class="sxs-lookup"><span data-stu-id="4cda2-140">Installation directory requirements must be followed.</span></span> <span data-ttu-id="4cda2-141">如需詳細資訊，請參閱安裝目錄需求。</span><span class="sxs-lookup"><span data-stu-id="4cda2-141">For more information, see Installation Directory Requirements.</span></span>

<span data-ttu-id="4cda2-142">32位和64位 IME Dll 的並存安裝會共用相同的登錄機碼來儲存設定資料 (包括 DLL 檔案名) ：</span><span class="sxs-lookup"><span data-stu-id="4cda2-142">Side-by-side installations of 32-bit and 64-bit IME DLLs share the same registry key for storing configuration data (including the DLL file name):</span></span>


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



<span data-ttu-id="4cda2-143">[**ImmInstallIME**](/windows/desktop/api/imm/nf-imm-imminstallimea)函式是用來建立此登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="4cda2-143">The [**ImmInstallIME**](/windows/desktop/api/imm/nf-imm-imminstallimea) function is used to create this registry key.</span></span> <span data-ttu-id="4cda2-144">IME 的安裝程式和安裝程式必須呼叫此函式，才能將 IME 註冊為支援的鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="4cda2-144">The setup and installation program for an IME must call this function to register the IME as a supported keyboard layout.</span></span> <span data-ttu-id="4cda2-145">**ImmInstallIME** 函式應該只呼叫一次，不論是從32位或64位版本的 IME DLL。</span><span class="sxs-lookup"><span data-stu-id="4cda2-145">The **ImmInstallIME** function should be called only once, either from the 32-bit or 64-bit version of the IME DLL.</span></span>

## <a name="mismatched-ime-dlls"></a><span data-ttu-id="4cda2-146">不相符的 IME Dll</span><span class="sxs-lookup"><span data-stu-id="4cda2-146">Mismatched IME DLLs</span></span>

<span data-ttu-id="4cda2-147">建議您在64位 Windows 上只安裝32位版本的輸入法，也不會受到支援。</span><span class="sxs-lookup"><span data-stu-id="4cda2-147">Installing only the 32-bit version of an IME on 64-bit Windows is neither recommended nor supported.</span></span> <span data-ttu-id="4cda2-148">如果64位應用程式嘗試載入32位的輸入法，則當應用程式嘗試載入相關聯的鍵盤配置時，IME 會無訊息地失敗。</span><span class="sxs-lookup"><span data-stu-id="4cda2-148">If a 64-bit application attempts to load a 32-bit IME, the IME fails silently when the application attempts to load the associated keyboard layout.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="4cda2-149">當發生64位應用程式/32 位的輸入法衝突錯誤時，不會顯示警告對話方塊或訊息。</span><span class="sxs-lookup"><span data-stu-id="4cda2-149">No warning dialog or message displays when a 64-bit application/32-bit IME conflict error occurs.</span></span>

 

<span data-ttu-id="4cda2-150">適用于文字服務的64位考慮</span><span class="sxs-lookup"><span data-stu-id="4cda2-150">64-Bit Considerations for Text Services</span></span>

<span data-ttu-id="4cda2-151">本節說明在64位環境中建立文字服務時所牽涉到的特殊考慮。</span><span class="sxs-lookup"><span data-stu-id="4cda2-151">This section describes the special considerations involved with building text services for use in 64-bit environments.</span></span> <span data-ttu-id="4cda2-152">如需文字服務和文字服務架構的詳細資訊，請參閱 [文字服務架構](text-services-framework.md)。</span><span class="sxs-lookup"><span data-stu-id="4cda2-152">For more information about text services and the Text Services Framework, see [Text Services Framework](text-services-framework.md).</span></span>

## <a name="building-32-bit-and-64-bit-text-services"></a><span data-ttu-id="4cda2-153">建立32位和64位文字服務</span><span class="sxs-lookup"><span data-stu-id="4cda2-153">Building 32-Bit and 64-Bit Text Services</span></span>

<span data-ttu-id="4cda2-154">文字服務會實作為元件物件模型， (在 DLL 上公開的 COM) 物件。</span><span class="sxs-lookup"><span data-stu-id="4cda2-154">A text service is implemented as a Component Object Model (COM) object exposed on a DLL.</span></span> <span data-ttu-id="4cda2-155">因此，在64位 Windows 上安裝的文字服務可能會發生32位/64 位 DLL 衝突。</span><span class="sxs-lookup"><span data-stu-id="4cda2-155">Consequently, 32-bit/64-bit DLL conflicts can occur with text services installed on 64-bit Windows.</span></span> <span data-ttu-id="4cda2-156">就像使用 Ime 一樣，可讓您的文字服務在64位平臺上以透明的方式與32位和64位應用程式一起運作的建議解決方案，是建立並安裝平行的32位和64位版本的文字服務 DLL。</span><span class="sxs-lookup"><span data-stu-id="4cda2-156">Just as with IMEs, the recommended solution for enabling your text service to work transparently with both 32-bit and 64-bit applications on a 64-bit platform is to build and install parallel 32-bit and 64-bit versions of the text service DLL.</span></span>

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a><span data-ttu-id="4cda2-157">64位和32位文字服務的並存安裝</span><span class="sxs-lookup"><span data-stu-id="4cda2-157">Side-by-Side Installation of 64-Bit and 32-Bit Text Services</span></span>

<span data-ttu-id="4cda2-158">若要將32位版本和64位版本的文字服務並行安裝，並以單一的邏輯文字服務的形式呈現給使用者，必須符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="4cda2-158">For a 32-bit version and a 64-bit version of a text service to be installed side-by-side and represented to the user as a single, logical text service, the following conditions must be met:</span></span>

-   <span data-ttu-id="4cda2-159">這兩個版本的文字服務會在向 COM 子系統註冊 (CLSID) 時，指定相同的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cda2-159">Both versions of the text service specify the same class identifier (CLSID) when they are registered with the COM subsystem.</span></span>
-   <span data-ttu-id="4cda2-160">這兩個版本的文字服務都是獨立註冊的。</span><span class="sxs-lookup"><span data-stu-id="4cda2-160">Both versions of the text service are registered independently.</span></span> <span data-ttu-id="4cda2-161">如需詳細資訊，請參閱 [註冊 COM 應用程式](/windows/desktop/com/registering-com-applications)。</span><span class="sxs-lookup"><span data-stu-id="4cda2-161">For more information, see [Registering COM Applications](/windows/desktop/com/registering-com-applications).</span></span>

<span data-ttu-id="4cda2-162">當32位文字服務向64位 Windows 註冊時，註冊作業會以透明方式重新導向至下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="4cda2-162">When a 32-bit text service is registered with 64-bit Windows, the registration operation is transparently redirected to the following registry key:</span></span>


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[<span data-ttu-id="4cda2-163">登錄重新導向程式</span><span class="sxs-lookup"><span data-stu-id="4cda2-163">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



<span data-ttu-id="4cda2-164">[ITfInputProcessorProfiles](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[文字服務註冊](text-service-registration.md)</span><span class="sxs-lookup"><span data-stu-id="4cda2-164">[ITfInputProcessorProfiles](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[Text Service Registration](text-service-registration.md)</span></span>

<span data-ttu-id="4cda2-165">64位版本和32位版本的文字服務可能會同時使用。</span><span class="sxs-lookup"><span data-stu-id="4cda2-165">The 64-bit version and the 32-bit version of a text service might be in use simultaneously.</span></span> <span data-ttu-id="4cda2-166">在兩個版本的文字服務都需要操作任何共用物件的情況下，應該將存取共用物件的協調設計成文字服務。</span><span class="sxs-lookup"><span data-stu-id="4cda2-166">In cases where both versions of a text service need to manipulate any shared objects, coordination for access shared objects should be designed into the text service.</span></span> <span data-ttu-id="4cda2-167">每個文字服務都負責管理任何已使用或需要的共用物件。</span><span class="sxs-lookup"><span data-stu-id="4cda2-167">Each text service is responsible for managing any shared objects that are used or needed.</span></span>

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a><span data-ttu-id="4cda2-168">在64位 Windows 上僅安裝32位文字服務</span><span class="sxs-lookup"><span data-stu-id="4cda2-168">Installing Only 32-Bit Text Services on 64-Bit Windows</span></span>

<span data-ttu-id="4cda2-169">不建議在64位 Windows 平臺上安裝32位版本的文字服務，也不會受到建議。</span><span class="sxs-lookup"><span data-stu-id="4cda2-169">Installing only the 32-bit version of a text service on a 64-bit Windows platform is neither recommended nor supported.</span></span> <span data-ttu-id="4cda2-170">由於註冊對應是在64位 Windows 平臺上完成，因此64位應用程式可以透過 **ITfInputProcessorProfiles** 介面列舉32位文字服務的服務。</span><span class="sxs-lookup"><span data-stu-id="4cda2-170">Because of the registration mapping that is done on 64-bit Windows platforms, a 64-bit application can enumerate the services of a 32-bit Text Service through the **ITfInputProcessorProfiles** interface.</span></span> <span data-ttu-id="4cda2-171">不過，如果64位應用程式嘗試載入32位文字服務，則載入會無訊息地失敗。</span><span class="sxs-lookup"><span data-stu-id="4cda2-171">However, if a 64-bit application attempts to load a 32-bit text service, the load fails silently.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="4cda2-172">當發生64位應用程式/32 位文字服務衝突錯誤時，不會顯示警告對話方塊或訊息。</span><span class="sxs-lookup"><span data-stu-id="4cda2-172">No warning dialog or message displays when a 64-bit application/32-bit text service conflict error occurs.</span></span>

 

<span data-ttu-id="4cda2-173">其他考量</span><span class="sxs-lookup"><span data-stu-id="4cda2-173">Other Considerations</span></span>

## <a name="installation-directory-requirements"></a><span data-ttu-id="4cda2-174">安裝目錄需求</span><span class="sxs-lookup"><span data-stu-id="4cda2-174">Installation Directory Requirements</span></span>

<span data-ttu-id="4cda2-175">本節說明如何安裝 IME 和 text service 二進位檔案的需求。</span><span class="sxs-lookup"><span data-stu-id="4cda2-175">This section describes requirements for where to install IME and text service binary files.</span></span> <span data-ttu-id="4cda2-176">如果未遵循這些需求，您的文字服務或 IME 可能無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4cda2-176">If these requirements are not followed, your text service or IME might not function correctly.</span></span>

<span data-ttu-id="4cda2-177">**IME Dll**</span><span class="sxs-lookup"><span data-stu-id="4cda2-177">**IME DLLs**</span></span>

<span data-ttu-id="4cda2-178">在64位的 Windows 平臺上，將32位和64位的 IME Dll 安裝在下列目錄中：</span><span class="sxs-lookup"><span data-stu-id="4cda2-178">On 64-bit Windows platforms, install the 32-bit and 64-bit IME DLLs in the following directories:</span></span>

-   <span data-ttu-id="4cda2-179">在 SysWOW64 系統目錄中安裝32位的 IME Dll;呼叫 [**GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)，或使用 **CSIDL \_ SYSTEMX86** [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ，以取得此目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="4cda2-179">Install 32-bit IME DLLs in the SysWOW64 system directory; call [**GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya), or [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with **CSIDL\_SYSTEMX86** to retrieve this directory path.</span></span> <span data-ttu-id="4cda2-180">或者，如果您使用 [Windows Installer](/windows/desktop/Msi/about-windows-installer)，請使用 [**SystemFolder**](/windows/desktop/Msi/systemfolder) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4cda2-180">Alternately, if you are using [Windows Installer](/windows/desktop/Msi/about-windows-installer), use the [**SystemFolder**](/windows/desktop/Msi/systemfolder) property.</span></span>
-   <span data-ttu-id="4cda2-181">在 System32 系統目錄中安裝64位的 IME Dll;呼叫 [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)或 **SHGetFolderPath** 與 [CSIDL \_ 系統](/windows/desktop/shell/csidl) ，以取得此目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="4cda2-181">Install 64-bit IME DLLs in the System32 system directory; call [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya), or **SHGetFolderPath** with [CSIDL\_SYSTEM](/windows/desktop/shell/csidl) to retrieve this directory path.</span></span> <span data-ttu-id="4cda2-182">或者，針對 Windows Installer，請使用 [**System64Folder**](/windows/desktop/Msi/system64folder) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4cda2-182">Or, for Windows Installer, use the [**System64Folder**](/windows/desktop/Msi/system64folder) property.</span></span>

<span data-ttu-id="4cda2-183">**文字服務 Dll 和相關二進位檔案**</span><span class="sxs-lookup"><span data-stu-id="4cda2-183">**Text Service DLLs and Related Binary Files**</span></span>

<span data-ttu-id="4cda2-184">在64位 Windows 平臺上，請在下列目錄中安裝32位和64位文字服務 Dll，以及與您的文字服務或 IME 相關的任何其他二進位檔案：</span><span class="sxs-lookup"><span data-stu-id="4cda2-184">On 64-bit Windows platforms, install the 32-bit and 64-bit text service DLLs, as well as any other binary files related to your text service or IME, in the following directories:</span></span>

-   <span data-ttu-id="4cda2-185">將32位文字服務 Dll 和任何其他32位二進位檔安裝在 Program Files (x86) 目錄的子目錄;使用 **CSIDL \_ PROGRAM \_ FILESX86** 呼叫 **SHGetFolderPath** ，以取得此目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="4cda2-185">Install 32-bit text service DLLs and any other 32-bit binary files in a subdirectory in the Program Files (x86) directory; call **SHGetFolderPath** with **CSIDL\_PROGRAM\_FILESX86** to retrieve this directory path.</span></span> <span data-ttu-id="4cda2-186">或者，針對 Windows Installer，請使用 [**ProgramFilesFolder**](/windows/desktop/Msi/programfilesfolder) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4cda2-186">Or, for Windows Installer, use the [**ProgramFilesFolder**](/windows/desktop/Msi/programfilesfolder) property.</span></span>
-   <span data-ttu-id="4cda2-187">在 Program Files 目錄下的子目錄中，安裝64位文字服務 Dll 和任何其他64位二進位檔案;使用 **CSIDL \_ PROGRAM \_ FILES** 呼叫 **SHGetFolderPath** ，以抓取此目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="4cda2-187">Install 64-bit text service DLLs and any other 64-bit binary files in a subdirectory under the Program Files directory; call **SHGetFolderPath** with **CSIDL\_PROGRAM\_FILES** to retrieve this directory path.</span></span> <span data-ttu-id="4cda2-188">或者，針對 Windows Installer，請使用 [**ProgramFiles64Folder**](/windows/desktop/Msi/programfiles64folder) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4cda2-188">Or, for Windows Installer, use the [**ProgramFiles64Folder**](/windows/desktop/Msi/programfiles64folder) property.</span></span>

<span data-ttu-id="4cda2-189">如果您不是使用 Windows Installer 套件來安裝 IME 或文字服務，則強烈 recommnded 您使用64位安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="4cda2-189">If you are not using a Windows Installer package to install your IME or text service, it is strongly recommnded that you use a 64-bit installation application.</span></span> <span data-ttu-id="4cda2-190">WOW64 檔案系統重新導向器可能會導致32位安裝程式將檔案放在錯誤的目錄中 (例如，WOW64 檔案系統重新導向可能會導致要將 System32 目錄的檔案安裝在 SysWOW64 目錄中，而不是) 。</span><span class="sxs-lookup"><span data-stu-id="4cda2-190">The WOW64 file system redirector might cause 32-bit installers to place files in the wrong directories (for example, WOW64 file system redirection might cause files intended for the System32 directory to be installed in the SysWOW64 directory instead).</span></span> <span data-ttu-id="4cda2-191">如果您必須使用32位的安裝程式，請在安裝程式期間停用 WOW64 檔案重新導向，以確保檔案重新導向程式服務不會在安裝過程中造成任何非預期的重新導向。</span><span class="sxs-lookup"><span data-stu-id="4cda2-191">If you must use a 32-bit installer, disable WOW64 file redirection during the installation process to ensure that the file-redirector service does not cause any unintended redirection during the installation process.</span></span> <span data-ttu-id="4cda2-192">如需 WOW64 檔案系統重新導向器的詳細資訊，請參閱 [檔案系統重定向](/windows/desktop/WinProg64/file-system-redirector)程式。</span><span class="sxs-lookup"><span data-stu-id="4cda2-192">For information about the WOW64 file system redirector, see [File System Redirector](/windows/desktop/WinProg64/file-system-redirector).</span></span> <span data-ttu-id="4cda2-193">如需有關如何停用或啟用 WOW64 檔案系統重新導向的詳細資訊，請參閱 [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)。</span><span class="sxs-lookup"><span data-stu-id="4cda2-193">For information about how to disable or enable WOW64 file system redirection, see [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection).</span></span>

> [!TIP]
>
> <span data-ttu-id="4cda2-194">避免硬式編碼的安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="4cda2-194">Avoid hard-coded installation paths.</span></span> <span data-ttu-id="4cda2-195">如需詳細資訊，請參閱 [使用未 Hard-Coded 路徑的應用程式設計介面尋找目錄](/previous-versions//ms675638(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4cda2-195">For more information, see [Locate Directories Using the Application Programming Interface Not Hard-Coded Paths](/previous-versions//ms675638(v=vs.85))</span></span>

 

> [!IMPORTANT]
>
> <span data-ttu-id="4cda2-196">請勿將任何 IME 或文字服務檔案安裝在特殊目錄% WINDIR% \\ IME (預設為 c： \\ Windows \\ IME ) 。</span><span class="sxs-lookup"><span data-stu-id="4cda2-196">Do not install any IME or text service files in the special directory %WINDIR%\\IME (by default, c:\\Windows\\IME ).</span></span> <span data-ttu-id="4cda2-197">此目錄包含支援文字服務和 Ime 的系統檔案;它不是用來包含任何協力廠商的 IME 或文字服務檔案，而且此目錄不支援 WOW64 檔案系統重新導向。</span><span class="sxs-lookup"><span data-stu-id="4cda2-197">This directory contains system files that support text services and IMEs; it is not intended to contain any third-party IME or text service files, and WOW64 file system redirection is not supported for this directory.</span></span>

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a><span data-ttu-id="4cda2-198">在64位 Windows 平臺上執行的雙重 Ctfmon.exe 進程</span><span class="sxs-lookup"><span data-stu-id="4cda2-198">Dual Ctfmon.exe Processes Run on 64-Bit Windows Platforms</span></span>

<span data-ttu-id="4cda2-199">ctfmon.exe 進程會管理桌面上的文字服務架構，也提供 (UI) 的語言列使用者介面。</span><span class="sxs-lookup"><span data-stu-id="4cda2-199">The ctfmon.exe process manages the Text Services Framework on the desktop and also provides the language bar user interface (UI).</span></span> <span data-ttu-id="4cda2-200">在64位的 Windows 上，ctfmon.exe 進程的32位版本和64位版本會同時執行。</span><span class="sxs-lookup"><span data-stu-id="4cda2-200">On 64-bit Windows, a 32-bit version and a 64-bit version of the ctfmon.exe process run simultaneously.</span></span> <span data-ttu-id="4cda2-201">64位的 ctfmon.exe 進程會管理64位文字服務，同樣地，32位 ctfmon.exe 進程會管理32位文字服務。</span><span class="sxs-lookup"><span data-stu-id="4cda2-201">The 64-bit ctfmon.exe process manages 64-bit text services, and, likewise, the 32-bit ctfmon.exe process manages 32-bit text services.</span></span>

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a><span data-ttu-id="4cda2-202">不同版本的語言列 UI 顯示行為</span><span class="sxs-lookup"><span data-stu-id="4cda2-202">Display Behavior for Different Versions of the Language Bar UI</span></span>

<span data-ttu-id="4cda2-203">在64位的 Windows 上，只會顯示與64位版本的文字服務相關聯的語言 bar UI。</span><span class="sxs-lookup"><span data-stu-id="4cda2-203">On 64-bit Windows, only the language bar UI associated with the 64-bit version of a text service is ever shown.</span></span> <span data-ttu-id="4cda2-204">在32位應用程式使用32位版本的文字服務的情況下，64位的 Windows 會自動為對等的64位文字服務插入語言列 UI。</span><span class="sxs-lookup"><span data-stu-id="4cda2-204">In cases where a 32-bit application is using the 32-bit version of a text service, 64-bit Windows automatically inserts the language bar UI for the equivalent 64-bit text service.</span></span> <span data-ttu-id="4cda2-205">這可確保32位文字服務不需要任何特殊的工作就會出現在64位版本的語言列中。</span><span class="sxs-lookup"><span data-stu-id="4cda2-205">This ensures that no special work is required for 32-bit text services to appear in the 64-bit version of the language bar.</span></span>

## <a name="control-panel-considerations-on-64-bit-windows"></a><span data-ttu-id="4cda2-206">64位 Windows 上的主控台考慮</span><span class="sxs-lookup"><span data-stu-id="4cda2-206">Control Panel Considerations on 64-Bit Windows</span></span>

<span data-ttu-id="4cda2-207">64位 Windows 可讓您透過主控台存取32位和64位版本的文字服務和 Ime。</span><span class="sxs-lookup"><span data-stu-id="4cda2-207">64-bit Windows provides access to both 32-bit and 64-bit versions of text services and IMEs through the Control Panel.</span></span> <span data-ttu-id="4cda2-208">若要存取特定版本的文字服務或 Ime 主控台設定，請查看下列位置。</span><span class="sxs-lookup"><span data-stu-id="4cda2-208">To access Control Panel settings for specific versions of text services or IMEs, look in the following locations.</span></span>

-   <span data-ttu-id="4cda2-209">**32 位文字服務和 ime 的主控台存取：** 開始 > 設定-> 主控台-> 觀看 x86 主控台圖示</span><span class="sxs-lookup"><span data-stu-id="4cda2-209">**Control Panel access for 32-bit Text Services and IMEs:** Start -> Settings -> Control Panel -> View x86 Control Panel Icons</span></span>
-   <span data-ttu-id="4cda2-210">**64 位文字服務和 ime 的主控台存取：** 開始 > 設定-> 主控台-> 地區及語言選項</span><span class="sxs-lookup"><span data-stu-id="4cda2-210">**Control Panel access for 64-bit Text Services and IMEs:** Start -> Settings -> Control Panel -> Regional and Language Options</span></span>

<span data-ttu-id="4cda2-211">在某些情況下，某些設定可能只會透過32位主控台提供。</span><span class="sxs-lookup"><span data-stu-id="4cda2-211">There may be circumstances where some settings might be available only through the 32-bit Control Panel.</span></span> <span data-ttu-id="4cda2-212">在這些情況下，請在您的64位設定介面中提供適當的檔或提供 UI 提示，以確定文字服務或 IME 的使用者知道這一點。</span><span class="sxs-lookup"><span data-stu-id="4cda2-212">In these cases, be sure that users of your text service or IME are aware of this, by providing appropriate documentation or offering UI hints in your 64-bit settings interface.</span></span>

 

 