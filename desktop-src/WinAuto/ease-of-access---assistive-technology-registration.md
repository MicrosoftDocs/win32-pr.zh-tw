---
title: 輕鬆存取輔助技術註冊
description: 本文說明如何使用輕鬆存取中心註冊協助工具應用程式。 它也會說明如何量身打造您的協助工具應用程式，使其可與安全桌面順利搭配運作。
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965247"
---
# <a name="ease-of-access---assistive-technology-registration"></a><span data-ttu-id="ce7fa-104">輕鬆存取輔助技術註冊</span><span class="sxs-lookup"><span data-stu-id="ce7fa-104">Ease of Access   Assistive Technology Registration</span></span>

<span data-ttu-id="ce7fa-105">本文說明如何使用輕鬆存取中心註冊協助工具應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-105">This article explains how to register an accessibility application with the Ease of Access Center.</span></span> <span data-ttu-id="ce7fa-106">它也會說明如何量身打造您的協助工具應用程式，使其可與安全桌面順利搭配運作。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-106">It also explains how to tailor your accessibility application so it works well with the secure desktop.</span></span>

<span data-ttu-id="ce7fa-107">輕鬆存取中心是適用于 Microsoft Windows 的主控台應用程式，結合了協助工具和易用性的功能。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-107">The Ease of Access Center is a Control Panel application for Microsoft Windows brings together functionality for accessibility and ease of use.</span></span> <span data-ttu-id="ce7fa-108">藉由使用輕鬆存取中心，使用者可以設定其電腦以符合其實體和認知需求。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-108">By using the Ease of Access Center, users can configure their computers to suit their physical and cognitive needs.</span></span>

<span data-ttu-id="ce7fa-109">輕鬆存取中心的其中一個功能是協助使用者啟動協助工具應用程式，包括 [朗讀程式]、[螢幕小鍵盤] 和 [放大鏡]。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-109">One function of the Ease of Access Center is to help users launch accessibility applications, including Narrator, On-Screen Keyboard, and Magnifier.</span></span> <span data-ttu-id="ce7fa-110">註冊的協力廠商應用程式也會出現在輕鬆存取中心中，並且可以直接從該處啟動。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-110">Registered third-party applications also appear in the Ease of Access Center and can be launched directly from there.</span></span>

<span data-ttu-id="ce7fa-111">協助工具應用程式需要與安全桌面順利搭配運作。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-111">Accessibility applications need to work smoothly with the secure desktop.</span></span> <span data-ttu-id="ce7fa-112">安全桌面是使用者介面，當 (電腦在登入時，或當使用者已鎖定桌面) ，而且系統提示使用者允許可能不安全的動作時，就會出現該介面。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-112">The secure desktop is the user interface that appears when the computer is locked (at log-on or when the user has locked the desktop), and when the user is prompted to allow a potentially unsafe action.</span></span> <span data-ttu-id="ce7fa-113">基於安全考慮，Windows 會限制在安全桌面上執行的協力廠商軟體。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-113">For security reasons, Windows places limits on third-party software running on the secure desktop.</span></span> <span data-ttu-id="ce7fa-114">如果您想要讓協助工具應用程式在安全桌面電腦上執行，您需要向輕鬆存取中心註冊應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-114">If you want your accessibility application to run on the secure desktop, you need to register the application with the Ease of Access Center.</span></span>

## <a name="registering-with-the-ease-of-access-center"></a><span data-ttu-id="ce7fa-115">向輕鬆存取中心註冊</span><span class="sxs-lookup"><span data-stu-id="ce7fa-115">Registering with the Ease of Access Center</span></span>

<span data-ttu-id="ce7fa-116">協助工具應用程式會在安裝應用程式時，藉由建立一或多個登錄機碼來向輕鬆存取中心註冊。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-116">Accessibility applications register with the Ease of Access Center by creating one or more registry keys when the application is installed.</span></span> <span data-ttu-id="ce7fa-117">下表列出登錄機碼中包含的資訊。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-117">The following table lists the information contained in the registry keys.</span></span>



| <span data-ttu-id="ce7fa-118">Name</span><span class="sxs-lookup"><span data-stu-id="ce7fa-118">Name</span></span>                        | <span data-ttu-id="ce7fa-119">描述</span><span class="sxs-lookup"><span data-stu-id="ce7fa-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="ce7fa-120">強制/選用</span><span class="sxs-lookup"><span data-stu-id="ce7fa-120">Mandatory/Optional</span></span> | <span data-ttu-id="ce7fa-121">語言</span><span class="sxs-lookup"><span data-stu-id="ce7fa-121">Language</span></span>      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| <span data-ttu-id="ce7fa-122">應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="ce7fa-122">Application Name</span></span>            | <span data-ttu-id="ce7fa-123">資源檔中的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-123">The name of the application, which is in a resource file.</span></span> <span data-ttu-id="ce7fa-124">此登錄值包含指定格式的字串。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-124">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="ce7fa-125">如果應用程式是以英文以外的語言當地語系化，則這可能是應用程式名稱的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-125">This could be a localized version of the application name, if the application is localized in languages other than English.</span></span> <span data-ttu-id="ce7fa-126">名稱會出現在輕鬆存取中心中。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-126">The name appears in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="ce7fa-127">強制性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-127">Mandatory</span></span>          | <span data-ttu-id="ce7fa-128">當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-128">Localized</span></span>     |
| <span data-ttu-id="ce7fa-129">ATExe</span><span class="sxs-lookup"><span data-stu-id="ce7fa-129">ATExe</span></span>                       | <span data-ttu-id="ce7fa-130">應用程式可執行檔或映射的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-130">The name of the application executable file or image.</span></span> <span data-ttu-id="ce7fa-131">Windows 會使用這個值來判斷協助工具應用程式是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-131">Windows uses this value to determine whether the accessibility application is running.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="ce7fa-132">強制性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-132">Mandatory</span></span>          | <span data-ttu-id="ce7fa-133">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-133">Not localized</span></span> |
| <span data-ttu-id="ce7fa-134">CopySettingsToLockedDesktop</span><span class="sxs-lookup"><span data-stu-id="ce7fa-134">CopySettingsToLockedDesktop</span></span> | <span data-ttu-id="ce7fa-135">**DWORD** 值，指出是否要將協助工具應用程式的設定複製到鎖定的桌面。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-135">A **DWORD** value that indicates whether to copy the accessibility application's settings to the locked desktop.</span></span><br/> <span data-ttu-id="ce7fa-136">如果這個值是1，則應用程式可以將設定寫入使用者登錄中的位置，而 Windows 會將設定複製到使用者登錄中鎖定桌面的相同位置。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-136">If this value is 1, the application can write settings to a location in the user registry, and Windows copies the settings to the same location in the user registry for the locked desktop.</span></span> <span data-ttu-id="ce7fa-137">這可讓應用程式將其狀態從「標準」桌面保存到鎖定的桌面。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-137">This enables the application to persist its state from the "normal" desktop to the locked desktop.</span></span><br/>                                                                                                                                                             | <span data-ttu-id="ce7fa-138">選擇性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-138">Optional</span></span>           | <span data-ttu-id="ce7fa-139">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-139">Not localized</span></span> |
| <span data-ttu-id="ce7fa-140">Description</span><span class="sxs-lookup"><span data-stu-id="ce7fa-140">Description</span></span>                 | <span data-ttu-id="ce7fa-141">應用程式的簡短描述，從資源檔。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-141">A brief description of the application, from a resource file.</span></span> <span data-ttu-id="ce7fa-142">此登錄值包含指定格式的字串。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-142">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="ce7fa-143">如果應用程式是以英文以外的語言當地語系化，則這可能是描述的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-143">This could be a localized version of the description, if the application is localized in languages other than English.</span></span> <span data-ttu-id="ce7fa-144">這個字串的長度必須小於512個字元。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-144">The length of this string must be less than 512 characters.</span></span><br/> <span data-ttu-id="ce7fa-145">此描述會出現在輕鬆存取中心中，以提供協助工具應用程式給使用者的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-145">The description appears in the Ease of Access Center to provide additional information about the accessibility application to the user.</span></span><br/> <span data-ttu-id="ce7fa-146">此值也可以用來通知使用者，應用程式不會在安全桌面上使用。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-146">This value can also be used to notify the user that the application is not used on the secure desktop.</span></span><br/>      | <span data-ttu-id="ce7fa-147">強制性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-147">Mandatory</span></span>          | <span data-ttu-id="ce7fa-148">當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-148">Localized</span></span>     |
| <span data-ttu-id="ce7fa-149">設定檔</span><span class="sxs-lookup"><span data-stu-id="ce7fa-149">Profile</span></span>                     | <span data-ttu-id="ce7fa-150">指定應用程式所提供之住宿的簡短 XML 片段。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-150">A short piece of XML that specifies the accommodations that the application provides.</span></span> <span data-ttu-id="ce7fa-151">它可確保應用程式會出現在輕鬆存取中心的正確類別下。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-151">It ensures that the application appears under the correct category in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="ce7fa-152">強制性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-152">Mandatory</span></span>          | <span data-ttu-id="ce7fa-153">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-153">Not localized</span></span> |
| <span data-ttu-id="ce7fa-154">PassiveAutoStartBehavior</span><span class="sxs-lookup"><span data-stu-id="ce7fa-154">PassiveAutoStartBehavior</span></span>    | <p><span data-ttu-id="ce7fa-155">**DWORD** 值，指出是否已啟用舊版自動啟動行為。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-155">A **DWORD** value that indicates whether legacy auto-start behavior is enabled.</span></span></p><p><span data-ttu-id="ce7fa-156">預設值為0，表示需要舊版自動啟動行為。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-156">The default value is 0, which indicates that an AT requires legacy auto-start behavior.</span></span> <span data-ttu-id="ce7fa-157">這會導致 [在登入後開始登入] 設定，以簽入現成體驗 (OOBE) 和主控台 (查看主控台 > 輕鬆存取 > 輕鬆存取中心 >) **變更登入設定** ，並在 UAC 和鎖定畫面之後自動啟動。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-157">This  causes the “Start after sign-in” setting for that AT to be checked in the Out Of Box Experience (OOBE) and Control Panel (see **Control Panel -> Ease of Access -> Ease of Access Center -> Change sign-in settings**), and automatically starts the AT after UAC and lock-screen.</span></span></p><p><span data-ttu-id="ce7fa-158">值為1時，表示應該使用新的自動啟動行為，其中的 [在登入後啟動] 設定不會簽入 (OOBE) 和主控台，而且只有在核取 [登入後啟動] 設定時，才會在登入) 針對每個使用者 (會話自動啟動一次。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-158">A value of 1 indicates that the AT should use the new auto-start behavior where the “Start after sign-in” setting for that AT is not checked in the Out Of Box Experience (OOBE) and Control Panel, and the AT is automatically started once per user session (at login) only if the “start after sign-in” setting is checked.</span></span></p>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="ce7fa-159">選擇性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-159">Optional</span></span>          | <span data-ttu-id="ce7fa-160">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-160">Not localized</span></span> |
| <span data-ttu-id="ce7fa-161">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="ce7fa-161">SecureDesktopAccommodation</span></span>  | <span data-ttu-id="ce7fa-162">替代協助工具應用程式的名稱，此應用程式會在安全桌面電腦上執行，以取代此應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-162">The name of an alternate accessibility application to run on the secure desktop in the place of this application.</span></span> <span data-ttu-id="ce7fa-163">替代項可以是不同的應用程式、相同應用程式的不同版本、Windows 所含的協助工具應用程式之一，如果您不想要在安全桌面上執行任何協助工具應用程式，則可以使用「無」。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-163">The alternate can be a different application, a different version of the same application, one of the accessibility applications that is included in Windows, or "none" if you do not want to run any accessibility application on the secure desktop.</span></span> <br/>                                                                                                                                                                                                               | <span data-ttu-id="ce7fa-164">選擇性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-164">Optional</span></span>           | <span data-ttu-id="ce7fa-165">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-165">Not localized</span></span> |
| <span data-ttu-id="ce7fa-166">簡單設定檔</span><span class="sxs-lookup"><span data-stu-id="ce7fa-166">Simple Profile</span></span>              | <span data-ttu-id="ce7fa-167">值，描述如何在一個或兩個字組中分類應用程式：螢幕閱讀程式、放大鏡或螢幕小鍵盤（例如）。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-167">A value that describes how to classify the application in a word or two: Screen reader, Magnifier, or On-screen keyboard, for example.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="ce7fa-168">強制性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-168">Mandatory</span></span>          | <span data-ttu-id="ce7fa-169">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-169">Not localized</span></span> |
| <span data-ttu-id="ce7fa-170">StartExe</span><span class="sxs-lookup"><span data-stu-id="ce7fa-170">StartExe</span></span>                    | <span data-ttu-id="ce7fa-171">可執行檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-171">The full path of the executable.</span></span> <span data-ttu-id="ce7fa-172">此值可用來啟動協助工具應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-172">This value is used to launch the accessibility application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="ce7fa-173">強制性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-173">Mandatory</span></span>          | <span data-ttu-id="ce7fa-174">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-174">Not localized</span></span> |
| <span data-ttu-id="ce7fa-175">StartParams</span><span class="sxs-lookup"><span data-stu-id="ce7fa-175">StartParams</span></span>                 | <span data-ttu-id="ce7fa-176">命令列引數。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-176">Command-line arguments.</span></span> <span data-ttu-id="ce7fa-177">這些值會與 StartExe 搭配使用，以啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-177">These values are used along with StartExe to start the application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="ce7fa-178">選擇性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-178">Optional</span></span>           | <span data-ttu-id="ce7fa-179">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-179">Not localized</span></span> |
| <span data-ttu-id="ce7fa-180">TerminateOnDesktopSwitch</span><span class="sxs-lookup"><span data-stu-id="ce7fa-180">TerminateOnDesktopSwitch</span></span>    | <span data-ttu-id="ce7fa-181">**DWORD** 值，指定協助工具應用程式如何回應安全桌面的轉換。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-181">A **DWORD** value that specifies how the accessibility application responds to transitions to or from the secure desktop.</span></span><br/> <span data-ttu-id="ce7fa-182">如果此值不存在或為1，則 Windows 會在每次與安全桌面的轉換之間終止並重新啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-182">If this value does not exist or is 1, Windows terminates and restarts the application on each transition to or from the secure desktop.</span></span> <span data-ttu-id="ce7fa-183">這是預設行為。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-183">This is the default behavior.</span></span><br/> <span data-ttu-id="ce7fa-184">如果此值為0，則 Windows 不會在桌面轉換時終止協助工具應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-184">If this value is 0, Windows does not terminate the accessibility application on a desktop transition.</span></span> <span data-ttu-id="ce7fa-185">應用程式會繼續在先前的桌面上執行，而且如果實例尚未執行，則 Windows 會在新的桌面上啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-185">The application continues to run on the previous desktop, and Windows starts a new instance on the new desktop if an instance is not already running there.</span></span><br/> | <span data-ttu-id="ce7fa-186">選擇性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-186">Optional</span></span>           | <span data-ttu-id="ce7fa-187">未當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-187">Not localized</span></span> |


 

### <a name="localization"></a><span data-ttu-id="ce7fa-188">當地語系化</span><span class="sxs-lookup"><span data-stu-id="ce7fa-188">Localization</span></span>

<span data-ttu-id="ce7fa-189">應用程式名稱和描述的登錄值必須可以當地語系化，以支援多語系消費者介面 (MUI) 。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-189">The registry values of Application Name and Description need to be localizable to support Multilingual User Interface (MUI).</span></span>

<span data-ttu-id="ce7fa-190">這些字串採用下列格式，其中角括弧表示必要的元素，而方括弧表示選擇性元素。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-190">These strings are in the following format, where angle brackets signify required elements and square brackets signify an optional element.</span></span>

<span data-ttu-id="ce7fa-191">*@ <ResDllPath \\ ResDLLFilename>，- <resID> \[ ;<comment>\]*</span><span class="sxs-lookup"><span data-stu-id="ce7fa-191">*@<ResDllPath\\ResDLLFilename>,-<resID>\[;<comment>\]*</span></span>

<span data-ttu-id="ce7fa-192">*<ResDllPath \\ResDLLFilename>* 是資源 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-192">*<ResDllPath\\ResDLLFilename>* is the path to the resource DLL.</span></span> <span data-ttu-id="ce7fa-193">路徑可以包含環境變數。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-193">The path can contain environmental variables.</span></span>

<span data-ttu-id="ce7fa-194">*<resID>* 這是字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-194">*<resID>* is the resource ID for the string.</span></span>

<span data-ttu-id="ce7fa-195">*\[ 批註 \]* 包含任何選擇性批註。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-195">*\[comment\]* contains any optional comments.</span></span>

<span data-ttu-id="ce7fa-196">請看以下範例：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-196">Here is an example:</span></span>


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



<span data-ttu-id="ce7fa-197">如需 MUI 的詳細資訊，請參閱 [WINDOWS Mui 知識中心](../intl/about-multilingual-user-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-197">For more information about MUI, see [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span></span>

### <a name="hci-profile"></a><span data-ttu-id="ce7fa-198">HCI 設定檔</span><span class="sxs-lookup"><span data-stu-id="ce7fa-198">HCI Profile</span></span>

<span data-ttu-id="ce7fa-199">電腦 (HCI) 設定檔的互動方式，是根據使用者的需求來決定要提供哪些住宿。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-199">The Human Computer Interaction (HCI) profile is a way to determine what accommodations to provide based on the needs of the user.</span></span> <span data-ttu-id="ce7fa-200">協助工具應用程式應該註冊應用程式有助於容納的殘障類型相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-200">Accessibility applications should register information about the kind of disability the application helps to accommodate.</span></span>

<span data-ttu-id="ce7fa-201">設定檔登錄值包含 XML，可描述協助工具應用程式的目標殘障類型。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-201">The Profile registry value contains XML that describes the kind of disability targeted by the accessibility application.</span></span> <span data-ttu-id="ce7fa-202">此 XML 的格式如下：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-202">This XML has the following format:</span></span>


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



<span data-ttu-id="ce7fa-203">[ **便利設施類型** ] 屬性的有效值如下所示：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-203">The valid values for the **Accommodation type** attribute are as follows:</span></span>

-   <span data-ttu-id="ce7fa-204">輕度視覺</span><span class="sxs-lookup"><span data-stu-id="ce7fa-204">mild vision</span></span>
-   <span data-ttu-id="ce7fa-205">嚴重願景</span><span class="sxs-lookup"><span data-stu-id="ce7fa-205">severe vision</span></span>
-   <span data-ttu-id="ce7fa-206">輕度認知</span><span class="sxs-lookup"><span data-stu-id="ce7fa-206">mild cognitive</span></span>
-   <span data-ttu-id="ce7fa-207">嚴重認知</span><span class="sxs-lookup"><span data-stu-id="ce7fa-207">severe cognitive</span></span>
-   <span data-ttu-id="ce7fa-208">輕度的靈活性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-208">mild dexterity</span></span>
-   <span data-ttu-id="ce7fa-209">嚴重的靈活性</span><span class="sxs-lookup"><span data-stu-id="ce7fa-209">severe dexterity</span></span>
-   <span data-ttu-id="ce7fa-210">輕度聽力</span><span class="sxs-lookup"><span data-stu-id="ce7fa-210">mild hearing</span></span>
-   <span data-ttu-id="ce7fa-211">嚴重聽力</span><span class="sxs-lookup"><span data-stu-id="ce7fa-211">severe hearing</span></span>
-   <span data-ttu-id="ce7fa-212">輕度語音</span><span class="sxs-lookup"><span data-stu-id="ce7fa-212">mild speech</span></span>
-   <span data-ttu-id="ce7fa-213">嚴重語音</span><span class="sxs-lookup"><span data-stu-id="ce7fa-213">severe speech</span></span>

> [!Note]  
> <span data-ttu-id="ce7fa-214">這些值區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-214">These values are case sensitive.</span></span>

 

<span data-ttu-id="ce7fa-215">如果協助工具應用程式支援多個住宿，設定檔登錄值應該包含每個住宿的 **便利型** 別屬性。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-215">If an accessibility application supports multiple accommodations, the Profile registry value should include an **Accommodation type** attribute for each accommodation.</span></span>

### <a name="ease-of-access-registry-details"></a><span data-ttu-id="ce7fa-216">輕鬆存取登錄詳細資料</span><span class="sxs-lookup"><span data-stu-id="ce7fa-216">Ease of Access registry details</span></span>

<span data-ttu-id="ce7fa-217">若要註冊您的協助工具應用程式，您必須在下列登錄位置為您的應用程式建立金鑰，並以名稱/值組填入。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-217">To register your accessibility application, you need to create a key for your application at the following registry location and populate it with name-value pairs.</span></span>

<span data-ttu-id="ce7fa-218">**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ ATs\\**</span><span class="sxs-lookup"><span data-stu-id="ce7fa-218">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\**</span></span>

<span data-ttu-id="ce7fa-219">使用下列格式來命名您應用程式的登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-219">Name your application's registry key using the following format:</span></span>

<span data-ttu-id="ce7fa-220">*"公司版 \_ ProductName \_ v \# "*</span><span class="sxs-lookup"><span data-stu-id="ce7fa-220">*"CompanyName\_ProductName\_v\#"*</span></span>

<span data-ttu-id="ce7fa-221">例如「Contoso \_ 放大鏡2.0」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-221">For example, "Contoso\_Magnifier\_v2.0".</span></span>

<span data-ttu-id="ce7fa-222">若要新增登錄值，您的安裝程式必須以較高的許可權執行。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-222">To add registry values, your installation program must be running with elevated privileges.</span></span>

### <a name="secure-desktop-accommodation"></a><span data-ttu-id="ce7fa-223">安全桌面的住宿</span><span class="sxs-lookup"><span data-stu-id="ce7fa-223">Secure desktop accommodation</span></span>

<span data-ttu-id="ce7fa-224">**SecureDesktopAccommodation** 登錄機碼可讓您指定協助工具應用程式對安全桌面的回應方式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-224">The **SecureDesktopAccommodation** registry key lets you specify how your accessibility application responds to the secure desktop.</span></span> <span data-ttu-id="ce7fa-225">根據預設，輕鬆存取中心會在安全桌面電腦上啟動您的應用程式（如果它已在一般桌上型電腦上執行），或已設定為在登入桌面上執行。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-225">By default, the Ease of Access Center launches your application on the secure desktop if it was already running on the normal desktop, or if it is configured to run on the logon desktop.</span></span> <span data-ttu-id="ce7fa-226">藉由使用 **SecureDesktopAccommodation** 機碼，您可以：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-226">By using the **SecureDesktopAccommodation** key, you can:</span></span>

-   <span data-ttu-id="ce7fa-227">指定要在安全桌面上使用的應用程式替代版本。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-227">Specify an alternate version of your application for use on the secure desktop.</span></span> <span data-ttu-id="ce7fa-228">例如，您可能會有停用不安全功能的替代版本，或已優化為使用較少的記憶體，且更快啟動。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-228">For example, you might have an alternate version that disables unsecured features, or is optimized to use less memory and launch faster.</span></span>

    <span data-ttu-id="ce7fa-229">若要指定替代版本，請將 **SecureDesktopAccommodation** 索引鍵設定為替代版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-229">To specify the alternate version, set the **SecureDesktopAccommodation** key to the name of the alternate version.</span></span> <span data-ttu-id="ce7fa-230">例如，如果您在 Contoso 螢幕讀取器 v1.0 金鑰註冊您的應用程式 \_ \_ ，您可以在 Contoso screen ReaderSecure v1.0 註冊替代版本 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-230">For example, if you registered your application at the Contoso\_Screen Reader\_v1.0 key, you could register the alternate version at Contoso\_Screen ReaderSecure\_v1.0.</span></span> <span data-ttu-id="ce7fa-231">然後，將 Contoso  \_ 螢幕讀取器1.0 版的 SecureDesktopAccommodation 機碼設定 \_ 為 "contoso \_ screen ReaderSecure v1.0 \_ "。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-231">Then, set the **SecureDesktopAccommodation** key of Contoso\_Screen Reader\_v1.0 to "Contoso\_Screen ReaderSecure\_v1.0".</span></span>

-   <span data-ttu-id="ce7fa-232">指定要在安全桌面上使用的 Microsoft 協助工具應用程式來取代您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-232">Specify a Microsoft accessibility application to use on the secure desktop in place of your application.</span></span> <span data-ttu-id="ce7fa-233">針對此選項，請將 **SecureDesktopAccommodation** 設定為特定 Microsoft 協助工具應用程式的名稱： "osk"、"magnifierpane" 或 "朗讀程式"。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-233">For this option, set **SecureDesktopAccommodation** to the name of the particular Microsoft accessibility application: "osk", "magnifierpane", or "Narrator".</span></span>
-   <span data-ttu-id="ce7fa-234">指定您的應用程式不應該在安全桌面電腦上執行，也不應該在任何替代的應用程式上執行。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-234">Specify that your application should not run on the secure desktop, and neither should any alternate application.</span></span> <span data-ttu-id="ce7fa-235">針對此選項，請將 **SecureDesktopAccommodation** 設定為 "none" (建議) 或不存在的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-235">For this option, set **SecureDesktopAccommodation** to "none" (recommend) or the name of a nonexistent application.</span></span>

<span data-ttu-id="ce7fa-236">如果協助工具應用程式的 **SecureDesktopAccommodation** 登錄機碼指定要在安全桌面上執行的 Microsoft 協助工具應用程式來取代您的應用程式，則 Windows 會在轉換至安全桌面時通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-236">If the **SecureDesktopAccommodation** registry key for your accessibility application specifies a Microsoft accessibility application to run on the secure desktop in place of your application, Windows notifies the user of this when making the transition to the secure desktop.</span></span> <span data-ttu-id="ce7fa-237">為了通知使用者，Windows 會顯示您應用程式的描述登錄機碼中指定的字串。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-237">To notify the user, Windows displays the string specified in the Description registry key for your application.</span></span> <span data-ttu-id="ce7fa-238">例如，如果 ScreenReader Deluxe 1.0 應用程式在安全桌面上使用 Microsoft 朗讀程式，則會包含描述字串，例如：「Microsoft 朗讀程式將用於鎖定、登入及其他安全的桌面，以取代 ScreenReader Deluxe 1.0」。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-238">For example, if the ScreenReader Deluxe 1.0 application uses Microsoft Narrator on the secure desktop, it would include a Description string such as, "Microsoft Narrator will be used in the locked, logon, and other secure desktops in place of ScreenReader Deluxe 1.0."</span></span>

<span data-ttu-id="ce7fa-239">如果您應用程式的 **SecureDesktopAccommodation** 機碼設定為「無」，請使用 **Description** 金鑰告訴使用者您的應用程式無法在安全桌面上使用，也沒有提供任何替代方法。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-239">If your application's **SecureDesktopAccommodation** key is set to "none", use the **Description** key to tell the user your application is not available on the secure desktop and no alternative is provided.</span></span>

<span data-ttu-id="ce7fa-240">Windows 會顯示輕鬆存取中心中相關位置的描述文字。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-240">Windows displays the Description text in the relevant locations in the Ease of Access Center.</span></span>

### <a name="running-at-installation-and-on-the-logon-desktop"></a><span data-ttu-id="ce7fa-241">在安裝和登入桌面上執行</span><span class="sxs-lookup"><span data-stu-id="ce7fa-241">Running at installation and on the logon desktop</span></span>

<span data-ttu-id="ce7fa-242">如果您在下列登錄位置將協助工具應用程式的已註冊金鑰名稱附加至字串，Windows 會在安裝後立即啟動您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-242">If you append your accessibility application's registered key name to the string at the following registry location, Windows will launch your application immediately after it is installed.</span></span> <span data-ttu-id="ce7fa-243">此外，每當登入桌面為使用中時，Windows 就會自動執行您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-243">Also, Windows will automatically run your application whenever the logon desktop is active.</span></span>

<span data-ttu-id="ce7fa-244">**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ 設定**</span><span class="sxs-lookup"><span data-stu-id="ce7fa-244">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\Configuration**</span></span>

<span data-ttu-id="ce7fa-245">設定金鑰是以逗號分隔的字串。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-245">The Configuration key is a comma-delimited string.</span></span> <span data-ttu-id="ce7fa-246">若要新增應用程式，請將與您應用程式登錄機碼相同的字串附加到 HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ ATs \\ 。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-246">To add your application, append a string that is the same as your application's registry key at HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\.</span></span>

### <a name="running-in-a-job"></a><span data-ttu-id="ce7fa-247">在作業中執行</span><span class="sxs-lookup"><span data-stu-id="ce7fa-247">Running in a job</span></span>

<span data-ttu-id="ce7fa-248">如果 **TerminateOnDesktopSwitch** 登錄機碼不存在或設定為非零，則 Windows 會在作業的內容中執行應用程式，並在每個桌面轉換時終止並重新啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-248">If the **TerminateOnDesktopSwitch** registry key is not present or is set to non-zero, Windows runs the application in the context of a job, terminating and restarting the application with each desktop transition.</span></span> <span data-ttu-id="ce7fa-249">在作業中執行可確保只有應用程式的單一實例會在特定時間執行，並讓應用程式不需要監視桌面狀態。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-249">Running in a job ensures that only a single instance of the application is running at a particular time, and frees the application from having to monitor the desktop state.</span></span> <span data-ttu-id="ce7fa-250">在作業中執行的缺點包括：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-250">The disadvantages of running in a job include:</span></span>

-   <span data-ttu-id="ce7fa-251">應用程式會在每一部桌上型電腦轉換時產生啟動成本。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-251">The application incurs a startup cost with each desktop transition.</span></span>
-   <span data-ttu-id="ce7fa-252">只能透過輕鬆存取中心啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-252">The application can be started only through the Ease of Access Center.</span></span>
-   <span data-ttu-id="ce7fa-253">應用程式必須持續儲存其設定，因為桌面轉換可以隨時終止。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-253">The application must continually save its settings because it can be terminated at any time by a desktop transition.</span></span>

<span data-ttu-id="ce7fa-254">如果 **TerminateOnDesktopSwitch** 索引鍵存在且設為0，則 Windows 不會在作業中執行協助工具應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-254">If the **TerminateOnDesktopSwitch** key exists and is set to 0, Windows doesn't run the accessibility application in a job.</span></span> <span data-ttu-id="ce7fa-255">這有下列優點：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-255">This has the following advantages:</span></span>

-   <span data-ttu-id="ce7fa-256">沒有任何啟動成本與桌面轉換相關聯。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-256">No startup costs are associated with desktop transitions.</span></span>
-   <span data-ttu-id="ce7fa-257">您可以在輕鬆存取中心之外啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-257">The application can be started outside of the Ease of Access Center.</span></span>

<span data-ttu-id="ce7fa-258">未在作業中執行的缺點包括：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-258">The disadvantages of not running in a job include:</span></span>

-   <span data-ttu-id="ce7fa-259">因為應用程式不會在桌面轉換時重新開機，所以它必須偵測目前的桌面何時處於非使用中狀態，並適當地回應。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-259">Because the application isn t restarted on desktop transitions, it must detect when the current desktop is inactive and respond appropriately.</span></span> <span data-ttu-id="ce7fa-260">例如，應用程式必須放棄硬體的控制權，如此一來，應用程式的安全桌面版本才能使用它，而且應用程式應該進入睡眠模式，以避免使用處理器資源。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-260">For example, the application must relinquish control of hardware so the secure desktop version of the application can use it, and the application should enter sleep mode to avoid using processor resources.</span></span>
-   <span data-ttu-id="ce7fa-261">如果可以透過 [開始] 功能表、Windows 檔案總管或命令列來啟動應用程式，則必須通知輕鬆存取中心。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-261">If the application can be started through the Start menu, Windows Explorer, or the command line, the Ease of Access Center needs to be informed.</span></span> <span data-ttu-id="ce7fa-262">如需詳細資訊，請參閱 **Windows 標誌鍵 + U**。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-262">For more information, see **Windows Logo key + U**.</span></span>
-   <span data-ttu-id="ce7fa-263">由於應用程式的多個複本可以同時在不同的桌上型電腦上執行，因此必須撰寫應用程式，以支援多個執行中的複本。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-263">Because multiple copies of the application can run simultaneously on different desktops, the application must be written to support multiple running copies.</span></span>

### <a name="windows-logo-key--u"></a><span data-ttu-id="ce7fa-264">Windows 標誌鍵 + U</span><span class="sxs-lookup"><span data-stu-id="ce7fa-264">Windows Logo key + U</span></span>

<span data-ttu-id="ce7fa-265">如果您的協助工具應用程式設定為在作業中執行，則應用程式的啟動程式碼應該包含對 [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) 函式的呼叫，以判斷應用程式是否正在作業中啟動。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-265">If your accessibility application is configured to run in a job, your application's startup code should include a call to the [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) function to determine whether the application is starting in a job.</span></span> <span data-ttu-id="ce7fa-266">如果是，應用程式應該啟動輕鬆存取中心然後結束。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-266">If it is, the application should start the Ease of Access Center and then exit.</span></span> <span data-ttu-id="ce7fa-267">下列範例顯示如何呼叫 **IsProcessInJob**。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-267">The following example shows how to call **IsProcessInJob**.</span></span>


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



<span data-ttu-id="ce7fa-268">如果協助工具應用程式設定為在作業之外執行，則應該通知輕鬆存取中心應用程式正在啟動，並正常繼續。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-268">If the accessibility application is configured to run outside of a job, it should notify the Ease of Access Center that the application is starting and continue as normal.</span></span>

<span data-ttu-id="ce7fa-269">無論應用程式的設定方式為何，如果它提供從應用程式中結束的方法（例如 [關閉] 按鈕），則應用程式必須通知輕鬆存取中心正在結束。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-269">Regardless of how the application is configured, if it provides a way to exit from within the application, such as a Close button, the application must notify the Ease of Access Center that it is exiting.</span></span>

<span data-ttu-id="ce7fa-270">應用程式會藉由設定暫存登錄機碼，然後將 Windows 標誌鍵 + U 按鍵組合插入輸入資料流程，來通知輕鬆存取中心。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-270">An application notifies the Ease of Access Center by setting a temporary registry key and then injecting the Windows Logo key + U key combination into the input stream.</span></span>

<span data-ttu-id="ce7fa-271">應用程式應該在下列位置建立暫存金鑰。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-271">The application should create the temporary key at the following location.</span></span>

<span data-ttu-id="ce7fa-272">**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**</span><span class="sxs-lookup"><span data-stu-id="ce7fa-272">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\AccessibilityTemp**</span></span>

<span data-ttu-id="ce7fa-273">暫存索引鍵的名稱應該與註冊的應用程式名稱相同，例如 "Contoso \_ Screen Reader v1.0 \_ "。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-273">The temporary key should have the same name as the registered application name, such as "Contoso\_Screen Reader\_v1.0".</span></span> <span data-ttu-id="ce7fa-274">索引鍵的值是在啟動時設定為0x0003 的 **DWORD** ，或在應用程式結束時0x0002 的值。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-274">The value of the key is a **DWORD** set to 0x0003 when it is starting, or 0x0002 when the application is exiting.</span></span>


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a><span data-ttu-id="ce7fa-275">Windows 標誌鍵 + 向上音量</span><span class="sxs-lookup"><span data-stu-id="ce7fa-275">Windows Logo key + Volume Up</span></span>

<span data-ttu-id="ce7fa-276">當使用者按下 Windows 標誌鍵 + 音量按鍵組合 (（例如 tablet 裝置) ）來啟動協助工具應用程式時，輕鬆存取中心會將下列命令列引數傳遞至應用程式：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-276">When the user starts your accessibility application by pressing the Windows Logo key + Volume Up key combination (such as on a tablet device), the Ease of Access Center passes the following command-line argument to the application:</span></span>

<span data-ttu-id="ce7fa-277">**/hardwarebuttonlaunch**</span><span class="sxs-lookup"><span data-stu-id="ce7fa-277">**/hardwarebuttonlaunch**</span></span>

<span data-ttu-id="ce7fa-278">您的應用程式可以使用這個引數來判斷是要正常啟動，還是要據以調整行為。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-278">Your application can use this argument to determine whether to start normally, or to adjust behavior accordingly.</span></span>

### <a name="transferring-secure-desktop-settings"></a><span data-ttu-id="ce7fa-279">傳送安全桌面設定</span><span class="sxs-lookup"><span data-stu-id="ce7fa-279">Transferring secure desktop settings</span></span>

<span data-ttu-id="ce7fa-280">如果您的協助工具應用程式支援安全桌面，您可以在應用程式轉換至安全桌面時，使用登錄來複製設定。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-280">If your accessibility application supports the secure desktop, you can use the registry to copy settings when the application transitions to the secure desktop.</span></span> <span data-ttu-id="ce7fa-281">複製設定有助於讓使用者更順暢地轉換至安全桌面。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-281">Copying settings helps makes the transition to the secure desktop more seamless for the user.</span></span>

<span data-ttu-id="ce7fa-282">若要複製設定，請將應用程式的 CopySettingsToLockedDesktop 登錄機碼設定為1，並將設定儲存在下列登錄位置中。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-282">To copy settings, set the application's CopySettingsToLockedDesktop registry key to 1, and store the settings in the following registry location.</span></span>

<span data-ttu-id="ce7fa-283">**HKCU \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ ATConfig\\<AT Key Name>**</span><span class="sxs-lookup"><span data-stu-id="ce7fa-283">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATConfig\\<AT Key Name>**</span></span>

<span data-ttu-id="ce7fa-284">當應用程式正在執行時，輕鬆存取中心會監視此登錄位置。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-284">The Ease of Access Center monitors this registry location while the application is running.</span></span> <span data-ttu-id="ce7fa-285">當轉換到安全桌面時，輕鬆存取中心會將設定複製到安全桌面 HKCU hive 中的相同位置。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-285">When a transition to the secure desktop occurs, the Ease of Access Center copies the settings to the same location in the secure desktop s HKCU hive.</span></span> <span data-ttu-id="ce7fa-286">然後，應用程式可以讀取設定並繼續其狀態。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-286">The application can then read the settings and resume its state.</span></span>

<span data-ttu-id="ce7fa-287">您的協助工具應用程式應該定期寫入其設定，或每當值變更時。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-287">Your accessibility application should write its settings at regular intervals or whenever the values change.</span></span> <span data-ttu-id="ce7fa-288">在應用程式結束時寫入設定將無法運作。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-288">Writing settings on application exit will not work.</span></span> <span data-ttu-id="ce7fa-289">如果應用程式是在作業中執行，則會在結束程式碼有機會執行之前，從安全桌面的轉換結束。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-289">If the application is running in a job, it is terminated on the transition away from the secure desktop, before the exit code has a chance to run.</span></span> <span data-ttu-id="ce7fa-290">如果應用程式不是在作業中執行，則應用程式不會在離開安全桌面的轉換時終止。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-290">If the application is not running in a job, the application is not terminated on the transition away from the secure desktop.</span></span>

### <a name="caution"></a><span data-ttu-id="ce7fa-291">警告</span><span class="sxs-lookup"><span data-stu-id="ce7fa-291">Caution</span></span>

<span data-ttu-id="ce7fa-292">因為此處所述的登錄機碼是以使用者模式撰寫，所以並不安全。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-292">Because the registry keys described here are written in user mode, they are not secure.</span></span> <span data-ttu-id="ce7fa-293">如果您的協助工具應用程式會讀取這些機碼的內容，則應謹慎檢查資料並謹慎使用。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-293">If your accessibility application reads the contents of these keys, it should carefully check the data and use it with caution.</span></span> <span data-ttu-id="ce7fa-294">具體來說，您的應用程式應該對 **DWORD** 值進行界限檢查、謹慎使用字串長度、不應讀取外掛程式 DLL 名稱，而且不應該執行字串中找到的任何命令。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-294">Specifically, your application should do a bounds check on **DWORD** values, be careful with string lengths, should not read plug-in DLL names, and should not execute any commands found in strings.</span></span>

## <a name="registry-examples"></a><span data-ttu-id="ce7fa-295">登錄範例</span><span class="sxs-lookup"><span data-stu-id="ce7fa-295">Registry Examples</span></span>

<span data-ttu-id="ce7fa-296">下列範例顯示名為 Contoso ScreenReader 2.0 版之虛構產品的可能登錄值，其當地語系化名稱會儲存為資源。</span><span class="sxs-lookup"><span data-stu-id="ce7fa-296">The following example shows the possible registry values for a fictitious product called Contoso ScreenReader version 2.0, whose localized name is stored as a resource.</span></span>

<span data-ttu-id="ce7fa-297">資料表中的值位於下列索引鍵底下：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-297">The values in the table are under the following key:</span></span>

<span data-ttu-id="ce7fa-298">**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 協助工具 \\ ATs \\ Contoso \_ Screen Reader \_ 2.0 版**</span><span class="sxs-lookup"><span data-stu-id="ce7fa-298">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\Contoso\_Screen Reader\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce7fa-299">名稱</span><span class="sxs-lookup"><span data-stu-id="ce7fa-299">Name</span></span></th>
<th><span data-ttu-id="ce7fa-300">類型</span><span class="sxs-lookup"><span data-stu-id="ce7fa-300">Type</span></span></th>
<th><span data-ttu-id="ce7fa-301">資料</span><span class="sxs-lookup"><span data-stu-id="ce7fa-301">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce7fa-302">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ce7fa-302">ApplicationName</span></span></td>
<td><span data-ttu-id="ce7fa-303">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-303">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-304">@% SystemRoot% \system32\ContosoRes.dll，-5020</span><span class="sxs-lookup"><span data-stu-id="ce7fa-304">@%SystemRoot%\system32\ContosoRes.dll,-5020</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-305">Description</span><span class="sxs-lookup"><span data-stu-id="ce7fa-305">Description</span></span></td>
<td><span data-ttu-id="ce7fa-306">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-306">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-307">@% SystemRoot% \system32\ContosoRes.dll，-5040</span><span class="sxs-lookup"><span data-stu-id="ce7fa-307">@%SystemRoot%\system32\ContosoRes.dll,-5040</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce7fa-308">設定檔</span><span class="sxs-lookup"><span data-stu-id="ce7fa-308">Profile</span></span></td>
<td><span data-ttu-id="ce7fa-309">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-309">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce7fa-310">XML</span><span class="sxs-lookup"><span data-stu-id="ce7fa-310">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-311">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="ce7fa-311">SimpleProfile</span></span></td>
<td><span data-ttu-id="ce7fa-312">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-312">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-313">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="ce7fa-313">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce7fa-314">StartExe</span><span class="sxs-lookup"><span data-stu-id="ce7fa-314">StartExe</span></span></td>
<td><span data-ttu-id="ce7fa-315">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-315">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-316">C:\ContosoTools\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="ce7fa-316">C:\ContosoTools\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-317">StartParams</span><span class="sxs-lookup"><span data-stu-id="ce7fa-317">StartParams</span></span></td>
<td><span data-ttu-id="ce7fa-318">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-318">REG_SZ</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ce7fa-319">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="ce7fa-319">SecureDesktopAccommodation</span></span></td>
<td><span data-ttu-id="ce7fa-320">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-320">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-321">Narrator</span><span class="sxs-lookup"><span data-stu-id="ce7fa-321">Narrator</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce7fa-322">如果應用程式同時在單一可執行檔中提供螢幕閱讀程式和螢幕放大鏡，螢幕讀取器元件的值可能如下所示：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-322">If the application provides both a screen reader and a screen magnifier in a single executable, the values for the screen reader component might look like this:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce7fa-323">名稱</span><span class="sxs-lookup"><span data-stu-id="ce7fa-323">Name</span></span></th>
<th><span data-ttu-id="ce7fa-324">類型</span><span class="sxs-lookup"><span data-stu-id="ce7fa-324">Type</span></span></th>
<th><span data-ttu-id="ce7fa-325">資料</span><span class="sxs-lookup"><span data-stu-id="ce7fa-325">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce7fa-326">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ce7fa-326">ApplicationName</span></span></td>
<td><span data-ttu-id="ce7fa-327">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-327">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-328">@C:\Program Files\Contoso\Contosores.dll，-30</span><span class="sxs-lookup"><span data-stu-id="ce7fa-328">@C:\Program Files\Contoso\Contosores.dll,-30</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-329">Description</span><span class="sxs-lookup"><span data-stu-id="ce7fa-329">Description</span></span></td>
<td><span data-ttu-id="ce7fa-330">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-330">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-331">@C:\Program Files\Contoso\Contosores.dll、-32</span><span class="sxs-lookup"><span data-stu-id="ce7fa-331">@C:\Program Files\Contoso\Contosores.dll,-32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce7fa-332">設定檔</span><span class="sxs-lookup"><span data-stu-id="ce7fa-332">Profile</span></span></td>
<td><span data-ttu-id="ce7fa-333">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-333">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce7fa-334">XML</span><span class="sxs-lookup"><span data-stu-id="ce7fa-334">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-335">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="ce7fa-335">SimpleProfile</span></span></td>
<td><span data-ttu-id="ce7fa-336">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-336">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-337">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="ce7fa-337">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce7fa-338">StartExe</span><span class="sxs-lookup"><span data-stu-id="ce7fa-338">StartExe</span></span></td>
<td><span data-ttu-id="ce7fa-339">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-339">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="ce7fa-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-341">StartParams</span><span class="sxs-lookup"><span data-stu-id="ce7fa-341">StartParams</span></span></td>
<td><span data-ttu-id="ce7fa-342">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-342">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-343">/r</span><span class="sxs-lookup"><span data-stu-id="ce7fa-343">/r</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce7fa-344">放大鏡元件的值會在下列機碼中：</span><span class="sxs-lookup"><span data-stu-id="ce7fa-344">The values for the magnifier component would be in the following key:</span></span>

<span data-ttu-id="ce7fa-345">**HKLM \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATs \\ Contoso \_ 放大鏡 \_ 2.0 版**</span><span class="sxs-lookup"><span data-stu-id="ce7fa-345">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Contosoibility\\ATs\\Contoso\_Magnifier\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce7fa-346">名稱</span><span class="sxs-lookup"><span data-stu-id="ce7fa-346">Name</span></span></th>
<th><span data-ttu-id="ce7fa-347">類型</span><span class="sxs-lookup"><span data-stu-id="ce7fa-347">Type</span></span></th>
<th><span data-ttu-id="ce7fa-348">資料</span><span class="sxs-lookup"><span data-stu-id="ce7fa-348">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce7fa-349">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ce7fa-349">ApplicationName</span></span></td>
<td><span data-ttu-id="ce7fa-350">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-350">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-351">@c:\Program Files\Contoso\Contosores.dll，-31</span><span class="sxs-lookup"><span data-stu-id="ce7fa-351">@c:\Program Files\Contoso\Contosores.dll,-31</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-352">Description</span><span class="sxs-lookup"><span data-stu-id="ce7fa-352">Description</span></span></td>
<td><span data-ttu-id="ce7fa-353">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-353">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-354">@c:\Program Files\Contoso\Contosores.dll、-42</span><span class="sxs-lookup"><span data-stu-id="ce7fa-354">@c:\Program Files\Contoso\Contosores.dll,-42</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce7fa-355">設定檔</span><span class="sxs-lookup"><span data-stu-id="ce7fa-355">Profile</span></span></td>
<td><span data-ttu-id="ce7fa-356">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-356">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce7fa-357">XML</span><span class="sxs-lookup"><span data-stu-id="ce7fa-357">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-358">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="ce7fa-358">SimpleProfile</span></span></td>
<td><span data-ttu-id="ce7fa-359">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-359">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-360">放大</span><span class="sxs-lookup"><span data-stu-id="ce7fa-360">Magnification</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce7fa-361">StartExe</span><span class="sxs-lookup"><span data-stu-id="ce7fa-361">StartExe</span></span></td>
<td><span data-ttu-id="ce7fa-362">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-362">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="ce7fa-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce7fa-364">StartParams</span><span class="sxs-lookup"><span data-stu-id="ce7fa-364">StartParams</span></span></td>
<td><span data-ttu-id="ce7fa-365">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ce7fa-365">REG_SZ</span></span></td>
<td><span data-ttu-id="ce7fa-366">/m</span><span class="sxs-lookup"><span data-stu-id="ce7fa-366">/m</span></span></td>
</tr>
</tbody>
</table>



 

 

