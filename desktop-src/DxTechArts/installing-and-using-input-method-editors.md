---
title: 安裝和使用輸入法編輯器
description: 本文提供的教學課程將說明如何安裝和使用標準 Windows 輸入方法編輯器 (IME) 。
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6018b3a387a12409f9e46d0392bbd60015af29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982514"
---
# <a name="installing-and-using-input-method-editors"></a><span data-ttu-id="cc55a-103">安裝和使用輸入法編輯器</span><span class="sxs-lookup"><span data-stu-id="cc55a-103">Installing and Using Input Method Editors</span></span>

<span data-ttu-id="cc55a-104">本文提供的教學課程將說明如何安裝和使用標準 Windows 輸入方法編輯器 (IME) 。</span><span class="sxs-lookup"><span data-stu-id="cc55a-104">This article offers a tutorial for how to install and use the standard Windows Input Method Editor (IME).</span></span>

-   [<span data-ttu-id="cc55a-105">安裝輸入方法編輯器</span><span class="sxs-lookup"><span data-stu-id="cc55a-105">Installing an Input Method Editor</span></span>](#installing-an-input-method-editor)
-   [<span data-ttu-id="cc55a-106">簡體中文 IME</span><span class="sxs-lookup"><span data-stu-id="cc55a-106">Simplified Chinese IME</span></span>](#simplified-chinese-ime)
-   [<span data-ttu-id="cc55a-107">繁體中文 IME</span><span class="sxs-lookup"><span data-stu-id="cc55a-107">Traditional Chinese IME</span></span>](#traditional-chinese-ime)
-   [<span data-ttu-id="cc55a-108">日文輸入法</span><span class="sxs-lookup"><span data-stu-id="cc55a-108">Japanese IME</span></span>](#japanese-ime)
-   [<span data-ttu-id="cc55a-109">韓文輸入法</span><span class="sxs-lookup"><span data-stu-id="cc55a-109">Korean IME</span></span>](#korean-ime)
-   [<span data-ttu-id="cc55a-110">需求</span><span class="sxs-lookup"><span data-stu-id="cc55a-110">Requirements</span></span>](#requirements)

## <a name="installing-an-input-method-editor"></a><span data-ttu-id="cc55a-111">安裝輸入方法編輯器</span><span class="sxs-lookup"><span data-stu-id="cc55a-111">Installing an Input Method Editor</span></span>

<span data-ttu-id="cc55a-112">下列各節說明如何安裝和使用輸入法編輯器 (Ime) ，以四種不同的東亞語言輸入複雜字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-112">The following sections describe how to install and use Input Method Editors (IMEs) to enter complex characters in four different East Asian languages.</span></span> <span data-ttu-id="cc55a-113">本文將討論每種語言特有的功能。</span><span class="sxs-lookup"><span data-stu-id="cc55a-113">Features unique to each language are discussed.</span></span>

<span data-ttu-id="cc55a-114">若要在應用程式中執行輸入方法編輯器 (IME) 功能，請參閱 [在遊戲中使用輸入法編輯器](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game)。</span><span class="sxs-lookup"><span data-stu-id="cc55a-114">To implement Input Method Editor (IME) functionality in an application, see [Using an Input Method Editor in a Game](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game).</span></span>

<span data-ttu-id="cc55a-115">Microsoft Windows XP 系統預設不會安裝 IME。</span><span class="sxs-lookup"><span data-stu-id="cc55a-115">An IME is not installed on Microsoft Windows XP systems by default.</span></span> <span data-ttu-id="cc55a-116">若要安裝，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="cc55a-116">To install, complete the following steps.</span></span>

<span data-ttu-id="cc55a-117">**安裝 IME**</span><span class="sxs-lookup"><span data-stu-id="cc55a-117">**To install an IME**</span></span>

1.  <span data-ttu-id="cc55a-118">從主控台中，開啟 [地區及語言選項]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-118">From the Control Panel, open Regional and Language Options.</span></span>
2.  <span data-ttu-id="cc55a-119">在 [語言] 索引標籤上，選取 [安裝東亞語言的檔案] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="cc55a-119">On the Languages tab, select the Install files for East Asian languages checkbox.</span></span>

    ![地區和語言選項的 [語言] 索引標籤](images/ime-1.png)

    <span data-ttu-id="cc55a-121">[安裝補充語言支援] 對話方塊會出現，通知您語言檔案的儲存需求。</span><span class="sxs-lookup"><span data-stu-id="cc55a-121">An Install Supplemental Language Support dialog box appears informing you of the storage requirements for the language files.</span></span>

    ![安裝補充語言支援對話方塊](images/ime-install-lang-dialog.png)

3.  <span data-ttu-id="cc55a-123">按一下 [確定] 關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cc55a-123">Click OK to close the dialog box.</span></span>
4.  <span data-ttu-id="cc55a-124">按一下 [語言] 索引標籤上的 [確定]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-124">Click OK on the Languages tab.</span></span>
5.  <span data-ttu-id="cc55a-125">另一個對話方塊會出現，要求提供語言支援檔案所在的 Windows XP 安裝磁片或網路共用位置。</span><span class="sxs-lookup"><span data-stu-id="cc55a-125">Another dialog box appears requesting a Windows XP installation disk or network share location where the language support files are located.</span></span> <span data-ttu-id="cc55a-126">插入 Windows XP compact 磁片或流覽至適當的網路位置，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-126">Insert a Windows XP compact disk or browse to the appropriate network location, and click OK.</span></span> <span data-ttu-id="cc55a-127">Microsoft Windows 會安裝必要的檔案，並提示您重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="cc55a-127">Microsoft Windows installs the necessary files and prompts for you to restart the computer.</span></span>
6.  <span data-ttu-id="cc55a-128">按一下 [是] 以重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="cc55a-128">Click Yes to restart the computer.</span></span>
7.  <span data-ttu-id="cc55a-129">重新開機之後，再次開啟 [地區及語言選項] 控制台。</span><span class="sxs-lookup"><span data-stu-id="cc55a-129">After restarting, open the Regional and Language Options control panel once again.</span></span>
8.  <span data-ttu-id="cc55a-130">在 [語言] 索引標籤上，按一下 [詳細資料]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-130">On the Languages tab, click Details.</span></span> <span data-ttu-id="cc55a-131">[文字服務和輸入語言] 視窗隨即出現。</span><span class="sxs-lookup"><span data-stu-id="cc55a-131">The Text Services and Input Languages window appears.</span></span>

    ![ext services 和輸入語言視窗](images/ime-2.png)

9.  <span data-ttu-id="cc55a-133">在 [設定] 索引標籤上，按一下 [新增]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-133">On the Settings tab, click Add.</span></span> <span data-ttu-id="cc55a-134">[新增輸入語言] 視窗隨即出現。</span><span class="sxs-lookup"><span data-stu-id="cc55a-134">The Add Input Language window appears.</span></span>

    ![新增輸入語言視窗](images/ime-3.png)

10. <span data-ttu-id="cc55a-136">針對輸入語言選取中文 (臺灣) ，並針對鍵盤配置/IME 選取 Microsoft 新的語音輸入法2002a。</span><span class="sxs-lookup"><span data-stu-id="cc55a-136">Select Chinese (Taiwan) for input language and Microsoft New Phonetic IME 2002a for keyboard layout/IME.</span></span>
11. <span data-ttu-id="cc55a-137">按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-137">Click OK.</span></span> <span data-ttu-id="cc55a-138">現在您可以使用類似的方式來新增其他語言和 Ime。</span><span class="sxs-lookup"><span data-stu-id="cc55a-138">Now you can add additional languages and IMEs in a similar fashion.</span></span>
12. <span data-ttu-id="cc55a-139">再按一次 [新增]，選取 [中文 (PRC]) 輸入語言和中文 (簡化) -Microsoft 針對鍵盤配置/輸入法3.0 的拼音輸入法，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-139">Click Add again, select Chinese (PRC) for input language and Chinese (Simplified) - Microsoft Pinyin IME 3.0 for keyboard layout/IME, then click OK.</span></span>
13. <span data-ttu-id="cc55a-140">按一下 [新增]，選取 [日文] 作為輸入語言，並選取 [Microsoft IME 標準 2002 ver]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-140">Click Add again, select Japanese for input language and Microsoft IME Standard 2002 ver.</span></span> <span data-ttu-id="cc55a-141">8.1 針對鍵盤配置/輸入法，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-141">8.1 for keyboard layout/IME, then click OK.</span></span>
14. <span data-ttu-id="cc55a-142">再按一次 [新增]，選取 [韓文] 作為 [輸入語言] 和 [韓文輸入系統] (IME 2002) 的鍵盤配置/輸入，然後按一下 [確定]</span><span class="sxs-lookup"><span data-stu-id="cc55a-142">Click Add again, select Korean for input language and Korean Input System (IME 2002) for keyboard layout/IME, then click OK.</span></span> <span data-ttu-id="cc55a-143">在 [文字服務和輸入語言] 視窗中，[已安裝的服務] 清單方塊現在應該包含四個新加入的 Ime。</span><span class="sxs-lookup"><span data-stu-id="cc55a-143">In the Text Services and Input Languages window, the Installed services list box should now contain the four newly-added IMEs.</span></span>

    ![已安裝的服務清單方塊](images/ime-7.png)

15. <span data-ttu-id="cc55a-145">按一下 [確定] 以關閉 [文字服務和輸入語言] 視窗。</span><span class="sxs-lookup"><span data-stu-id="cc55a-145">Click OK to close the Text Services and Input Languages window.</span></span>
16. <span data-ttu-id="cc55a-146">按一下 [確定] 關閉 [地區及語言選項] 控制台。</span><span class="sxs-lookup"><span data-stu-id="cc55a-146">Click OK to close the Regional and Language Options control panel.</span></span> <span data-ttu-id="cc55a-147">Windows 工作列現在應該會包含以紅色圈起的輸入地區設定指標。</span><span class="sxs-lookup"><span data-stu-id="cc55a-147">The Windows taskbar should now contain an input locale indicator circled in red.</span></span> <span data-ttu-id="cc55a-148">指標是否存在表示系統上已安裝一個以上的輸入語言。</span><span class="sxs-lookup"><span data-stu-id="cc55a-148">The existence of the indicator signifies that more than one input language has been installed on the system.</span></span>

    ![表示系統上已安裝一個以上輸入語言的指標](images/ime-8.png)

## <a name="simplified-chinese-ime"></a><span data-ttu-id="cc55a-150">簡體中文 IME</span><span class="sxs-lookup"><span data-stu-id="cc55a-150">Simplified Chinese IME</span></span>

<span data-ttu-id="cc55a-151">本節說明如何使用簡體中文 IME (拼音) 搭配 Microsoft 記事本來輸入幾個中文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-151">This section describes how to use the Simplified Chinese IME (PinYin) with Microsoft Notepad to enter a few Chinese characters.</span></span>

1.  <span data-ttu-id="cc55a-152">啟動 [記事本] (可從 [開始] 按鈕取得，然後選取 [所有程式和附屬應用程式]) 。</span><span class="sxs-lookup"><span data-stu-id="cc55a-152">Launch Notepad (available from the Start button, then select All Programs and Accessories).</span></span> <span data-ttu-id="cc55a-153">在 [記事本] 中輸入一些字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-153">Type some characters in Notepad.</span></span> <span data-ttu-id="cc55a-154">這些字元將協助您在稍後更清楚地視覺化 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="cc55a-154">These characters will help you visualize the IME window better later.</span></span>

    ![螢幕擷取畫面，它會顯示一些字元，可協助您在稍後針對簡體中文將 I M E 視窗視覺化。](images/ime-sc1.png)

2.  <span data-ttu-id="cc55a-156">使用 [記事本] 作為作用中的應用程式，按一下輸入地區設定指標，然後選取 [中文 (PRC]) 。</span><span class="sxs-lookup"><span data-stu-id="cc55a-156">With Notepad as the active application, click the input locale indicator and select Chinese (PRC).</span></span> <span data-ttu-id="cc55a-157">指標顯示會變更為 CH，以反映新的輸入語言是中文 (PRC) 。</span><span class="sxs-lookup"><span data-stu-id="cc55a-157">The indicator display changes to CH to reflect that the new input language is Chinese (PRC).</span></span>

    ![顯示輸入地區設定指標以選取中文 (P R C) 的螢幕擷取畫面。](images/ime-sc2.png)

3.  <span data-ttu-id="cc55a-159">將游標放在 [記事本] 中。</span><span class="sxs-lookup"><span data-stu-id="cc55a-159">Place the cursor in Notepad.</span></span> <span data-ttu-id="cc55a-160">按下鍵盤上的 [首頁]，讓游標位於行的開頭。</span><span class="sxs-lookup"><span data-stu-id="cc55a-160">Press HOME on the keyboard so that the cursor is at the beginning of the line.</span></span> <span data-ttu-id="cc55a-161">在鍵盤上輸入 "N"，然後輸入 "I"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-161">On the keyboard type "N", then "I".</span></span> <span data-ttu-id="cc55a-162">下圖顯示顯示的外觀。</span><span class="sxs-lookup"><span data-stu-id="cc55a-162">The following figure shows the appearance of the display.</span></span> <span data-ttu-id="cc55a-163">小型水準矩形是讀取視窗，會顯示目前的讀取字串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-163">The small horizontal rectangle is the reading window, which displays the current reading string.</span></span> <span data-ttu-id="cc55a-164">目前，由於輸入 "N" 和 "I"，讀取字串是 "ni"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-164">Currently, the reading string is "ni" as a result of typing "N" and "I".</span></span>

    ![顯示讀取字串為 ' n ' 和 ' i ' 的螢幕擷取畫面。](images/ime-sc3.png)

4.  <span data-ttu-id="cc55a-166">輸入 "3"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-166">Type "3".</span></span> <span data-ttu-id="cc55a-167">現在記事本有下列顯示畫面。</span><span class="sxs-lookup"><span data-stu-id="cc55a-167">Now Notepad has the following display.</span></span> <span data-ttu-id="cc55a-168">因為 N + I + 3 是簡體中文拼音的完整發音，所以 IME 有足夠的資訊來預期使用者可能要輸入的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-168">Because N+I+3 is a complete pronunciation in Simplified Chinese Pinyin, the IME has enough information to anticipate the character that the user may have intended to enter.</span></span> <span data-ttu-id="cc55a-169">因為您輸入了完整的發音，所以讀取視窗消失。</span><span class="sxs-lookup"><span data-stu-id="cc55a-169">The reading window disappears because you have entered a complete pronunciation.</span></span> <span data-ttu-id="cc55a-170">字元會顯示在 [記事本] 游標上方。</span><span class="sxs-lookup"><span data-stu-id="cc55a-170">A character is displayed on top of the Notepad cursor.</span></span> <span data-ttu-id="cc55a-171">此字元不是 [記事本] 的一部分，而是在 [記事本] 頂端的另一個視窗中顯示，並隱藏下 [記事本] 中現有的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-171">This character is not part of Notepad, rather it is displayed in another window on top of Notepad and hides the existing characters in Notepad that are beneath.</span></span> <span data-ttu-id="cc55a-172">這個新視窗稱為組合視窗，其中的字串稱為組合字元串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-172">This new window is called the composition window, and the string in it is called the composition string.</span></span> <span data-ttu-id="cc55a-173">組合字元串會在顯示中加上底線。</span><span class="sxs-lookup"><span data-stu-id="cc55a-173">The composition string is underlined in the display.</span></span>

    ![顯示組合視窗的螢幕擷取畫面，其中包含單一字元的組合字元串。](images/ime-sc4.png)

5.  <span data-ttu-id="cc55a-175">現在輸入 "H"、"A"、"O"、"3" 來輸入另一個字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-175">Now type "H", "A", "O", "3" to enter another character.</span></span> <span data-ttu-id="cc55a-176">請注意，當輸入 "H" 時，讀取視窗會顯示，而且當輸入 "3" 時，會消失。</span><span class="sxs-lookup"><span data-stu-id="cc55a-176">Note that the reading window shows up when "H" is typed and disappears when "3" is typed.</span></span> <span data-ttu-id="cc55a-177">如下所示，組合字元串現在包含兩個字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-177">As shown below, the composition string now contains two characters.</span></span>

    ![顯示組合視窗的螢幕擷取畫面，其中包含兩個字元的組合字元串。](images/ime-sc5.png)

6.  <span data-ttu-id="cc55a-179">按下鍵盤上的向左鍵。</span><span class="sxs-lookup"><span data-stu-id="cc55a-179">Press the left arrow on the keyboard once.</span></span> <span data-ttu-id="cc55a-180">組合游標會在您輸入的第二個字元處向左移動一個字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-180">The composition cursor moves one character to the left, at the second character you typed.</span></span> <span data-ttu-id="cc55a-181">視窗會出現在 [記事本] 上方，如下所示。</span><span class="sxs-lookup"><span data-stu-id="cc55a-181">A window appears on top of Notepad as shown below.</span></span> <span data-ttu-id="cc55a-182">此視窗稱為候選視窗。</span><span class="sxs-lookup"><span data-stu-id="cc55a-182">This window is called the candidate window.</span></span> <span data-ttu-id="cc55a-183">它會顯示符合您所輸入發音的字元或片語清單。</span><span class="sxs-lookup"><span data-stu-id="cc55a-183">It displays a list of characters or phrases that match the pronunciation that you have typed.</span></span> <span data-ttu-id="cc55a-184">您可以從候選清單中的專案選取所需的文字。</span><span class="sxs-lookup"><span data-stu-id="cc55a-184">You can select the intended word from the entries in the candidate list.</span></span> <span data-ttu-id="cc55a-185">在此範例中，有兩個候選字元可用於相同的發音。</span><span class="sxs-lookup"><span data-stu-id="cc55a-185">In this example, two candidate characters are available with the same pronunciation.</span></span>

    ![有兩個可用於相同發音的候選字元](images/ime-sc6.png)

7.  <span data-ttu-id="cc55a-187">輸入 "2" 來選取第二個專案。</span><span class="sxs-lookup"><span data-stu-id="cc55a-187">Type "2" to select the second entry.</span></span> <span data-ttu-id="cc55a-188">候選視窗現在會關閉，然後以選取的字元更新撰寫字串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-188">The candidate window now closes, and the composition string is updated with the selected character.</span></span>

    ![顯示以選取的字元更新的組合字元串的螢幕擷取畫面。](images/ime-sc7.png)

8.  <span data-ttu-id="cc55a-190">按 ENTER 鍵。</span><span class="sxs-lookup"><span data-stu-id="cc55a-190">Press ENTER.</span></span> <span data-ttu-id="cc55a-191">這會告知 IME 組合已完成，而且應該將字串傳送至應用程式-在此範例中為「記事本」。</span><span class="sxs-lookup"><span data-stu-id="cc55a-191">This tells the IME that the composition is complete and the string should be sent to the application - Notepad in this example.</span></span> <span data-ttu-id="cc55a-192">組合視窗會關閉，而這兩個字元會透過 WM CHAR 傳送至「記事本」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cc55a-192">The composition window closes, and the two characters are sent to Notepad via WM\_CHAR.</span></span> <span data-ttu-id="cc55a-193">下圖中的底線如下圖所示，這兩個字元都是 [記事本] 中文字的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc55a-193">The underline is gone in the following figure because the two characters shown are part of the text in Notepad.</span></span> <span data-ttu-id="cc55a-194">[記事本] 中的現有文字 "ABCDEFG" 已移至右側，因為已插入兩個以上的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-194">The existing text "ABCDEFG" in Notepad is moved to the right because two more characters have been inserted.</span></span> <span data-ttu-id="cc55a-195">您現在已成功使用 IME 輸入兩個簡體中文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-195">You have now successfully entered two Simplified Chinese characters using an IME.</span></span>

    ![已成功使用 ime 輸入兩個簡體中文字元](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a><span data-ttu-id="cc55a-197">繁體中文 IME</span><span class="sxs-lookup"><span data-stu-id="cc55a-197">Traditional Chinese IME</span></span>

<span data-ttu-id="cc55a-198">本節說明如何使用繁體中文 IME (新的語音) 與「記事本」來輸入幾個中文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-198">This section describes how to use the Traditional Chinese IME (New Phonetic) with Notepad to enter a few Chinese characters.</span></span>

1.  <span data-ttu-id="cc55a-199">啟動 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-199">Launch Notepad.</span></span> <span data-ttu-id="cc55a-200">在 [記事本] 中輸入一些字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-200">Type some characters in Notepad.</span></span> <span data-ttu-id="cc55a-201">這些字元將協助您在稍後更清楚地視覺化 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="cc55a-201">These characters will help you visualize the IME window better later.</span></span>

    ![螢幕擷取畫面，其中顯示的字元可協助您在稍後針對繁體中文以更好的方式將 I M E 視窗視覺化。](images/ime-tc1.png)

2.  <span data-ttu-id="cc55a-203">按一下 Windows 工作列上的輸入地區設定指標，然後選取 [中文 (臺灣) 。</span><span class="sxs-lookup"><span data-stu-id="cc55a-203">Click the input locale indicator on the Windows taskbar, and select Chinese (Taiwan).</span></span> <span data-ttu-id="cc55a-204">指標顯示會變更為 CH，以反映新的輸入語言為中文 (臺灣) 。</span><span class="sxs-lookup"><span data-stu-id="cc55a-204">The indicator display changes to CH to reflect that the new input language is Chinese (Taiwan).</span></span>

    ![輸入地區設定指標以選取中文 (臺灣) ](images/ime-tc2.png)

3.  <span data-ttu-id="cc55a-206">將游標放在 [記事本] 中。</span><span class="sxs-lookup"><span data-stu-id="cc55a-206">Place the cursor in Notepad.</span></span> <span data-ttu-id="cc55a-207">按下鍵盤上的 [首頁]，讓游標位於行的開頭。</span><span class="sxs-lookup"><span data-stu-id="cc55a-207">Press HOME on the keyboard so that the cursor is at the beginning of the line.</span></span> <span data-ttu-id="cc55a-208">在鍵盤上輸入 "S"，然後輸入 "U"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-208">On the keyboard type "S", then "U".</span></span> <span data-ttu-id="cc55a-209">下圖顯示顯示的外觀。</span><span class="sxs-lookup"><span data-stu-id="cc55a-209">The following figure shows the appearance of the display.</span></span> <span data-ttu-id="cc55a-210">小型垂直矩形是讀取視窗，會顯示目前的讀取字串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-210">The small vertical rectangle is the reading window, which displays the current reading string.</span></span> <span data-ttu-id="cc55a-211">如下圖所示，因為輸入 "S" 和 "U"，所以讀取字串有兩個字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-211">As shown in the following figure, the reading string has two characters as a result of typing "S" and "U".</span></span>

    ![顯示具有兩個字元之讀取字串的螢幕擷取畫面。](images/ime-tc3.png)

4.  <span data-ttu-id="cc55a-213">輸入 "3"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-213">Type "3".</span></span> <span data-ttu-id="cc55a-214">現在記事本有下列顯示畫面。</span><span class="sxs-lookup"><span data-stu-id="cc55a-214">Now Notepad has the following display.</span></span> <span data-ttu-id="cc55a-215">因為 S + U + 3 是繁體中文中的完整發音，所以 IME 有足夠的資訊來預期使用者可能要輸入的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-215">Because S+U+3 is a complete pronunciation in Traditional Chinese, the IME has enough information to anticipate the character that the user may have intended to enter.</span></span> <span data-ttu-id="cc55a-216">因為您輸入了完整的發音，所以讀取視窗消失。</span><span class="sxs-lookup"><span data-stu-id="cc55a-216">The reading window disappears because you have entered a complete pronunciation.</span></span> <span data-ttu-id="cc55a-217">字元會顯示在 [記事本] 游標上方。</span><span class="sxs-lookup"><span data-stu-id="cc55a-217">A character is displayed on top of the Notepad cursor.</span></span> <span data-ttu-id="cc55a-218">此字元不是 [記事本] 的一部分，而是在 [記事本] 頂端的另一個視窗中顯示，並隱藏下 [記事本] 中現有的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-218">This character is not part of Notepad, rather it is displayed in another window on top of Notepad and hides the existing characters in Notepad that are beneath.</span></span> <span data-ttu-id="cc55a-219">這個新視窗稱為組合視窗，其中的字串稱為組合字元串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-219">This new window is called the composition window, and the string in it is called the composition string.</span></span> <span data-ttu-id="cc55a-220">組合字元串會在顯示中加上底線。</span><span class="sxs-lookup"><span data-stu-id="cc55a-220">The composition string is underlined in the display.</span></span>

    ![顯示撰寫字串加上底線的組合視窗的螢幕擷取畫面。](images/ime-tc4.png)

5.  <span data-ttu-id="cc55a-222">現在輸入 "C"、"L" 和 "3" 來輸入另一個字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-222">Now type "C", "L", and "3" to enter another character.</span></span> <span data-ttu-id="cc55a-223">請注意，當輸入 "C" 時，讀取視窗會顯示，而當輸入 "3" 時，會消失。</span><span class="sxs-lookup"><span data-stu-id="cc55a-223">Note that the reading window shows up when "C" is typed and disappears when "3" is typed.</span></span> <span data-ttu-id="cc55a-224">如下所示，組合字元串現在包含兩個字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-224">As shown below, the composition string now contains two characters.</span></span>

    ![顯示撰寫字串和兩個字元加上底線的組合視窗的螢幕擷取畫面。](images/ime-tc5.png)

6.  <span data-ttu-id="cc55a-226">輸入鍵盤上的向下箭號。</span><span class="sxs-lookup"><span data-stu-id="cc55a-226">Type the down arrow on the keyboard once.</span></span> <span data-ttu-id="cc55a-227">視窗會出現在 [記事本] 上方，如下所示。</span><span class="sxs-lookup"><span data-stu-id="cc55a-227">A window appears on top of Notepad as shown below.</span></span> <span data-ttu-id="cc55a-228">此視窗稱為候選視窗。</span><span class="sxs-lookup"><span data-stu-id="cc55a-228">This window is called the candidate window.</span></span> <span data-ttu-id="cc55a-229">它會顯示符合您所輸入發音的字元或片語清單。</span><span class="sxs-lookup"><span data-stu-id="cc55a-229">It displays a list of characters or phrases that match the pronunciation that you have typed.</span></span> <span data-ttu-id="cc55a-230">您可以從候選清單中的專案選取所需的文字。</span><span class="sxs-lookup"><span data-stu-id="cc55a-230">You can select the intended word from the entries in the candidate list.</span></span> <span data-ttu-id="cc55a-231">在此範例中，有三個候選字元可用於相同的發音。</span><span class="sxs-lookup"><span data-stu-id="cc55a-231">In this example, three candidate characters are available with the same pronunciation.</span></span>

    ![有三個可供相同發音使用的候選字元](images/ime-tc6.png)

7.  <span data-ttu-id="cc55a-233">輸入 "2" 來選取第二個專案。</span><span class="sxs-lookup"><span data-stu-id="cc55a-233">Type "2" to select the second entry.</span></span> <span data-ttu-id="cc55a-234">候選視窗現在會關閉，然後以選取的字元更新撰寫字串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-234">The candidate window now closes, and the composition string is updated with the selected character.</span></span>

    ![顯示以選取的字元更新的組合字元串的螢幕擷取畫面。](images/ime-tc7.png)

8.  <span data-ttu-id="cc55a-236">按 ENTER 鍵。</span><span class="sxs-lookup"><span data-stu-id="cc55a-236">Press ENTER.</span></span> <span data-ttu-id="cc55a-237">這會告知 IME 組合已完成，而且應該將字串傳送至應用程式-在此範例中為「記事本」。</span><span class="sxs-lookup"><span data-stu-id="cc55a-237">This tells the IME that the composition is complete and the string should be sent to the application - Notepad in this example.</span></span> <span data-ttu-id="cc55a-238">組合視窗會關閉，而這兩個字元會透過 [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)傳送至「記事本」。</span><span class="sxs-lookup"><span data-stu-id="cc55a-238">The composition window closes, and the two characters are sent to Notepad via [**WM\_CHAR**](/windows/desktop/inputdev/wm-char).</span></span> <span data-ttu-id="cc55a-239">下圖中的底線如下圖所示，這兩個字元都是 [記事本] 中文字的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc55a-239">The underline is gone in the following figure because the two characters shown are part of the text in Notepad.</span></span> <span data-ttu-id="cc55a-240">[記事本] 中的現有文字 "ABCDEFG" 已移至右側，因為已插入兩個以上的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-240">The existing text "ABCDEFG" in Notepad is moved to the right because two more characters have been inserted.</span></span> <span data-ttu-id="cc55a-241">您現在已成功使用 IME 輸入兩個繁體中文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-241">You have now successfully entered two Traditional Chinese characters using an IME.</span></span>

    ![已成功使用 ime 輸入兩個繁體中文字元](images/ime-tc8.png)

## <a name="japanese-ime"></a><span data-ttu-id="cc55a-243">日文輸入法</span><span class="sxs-lookup"><span data-stu-id="cc55a-243">Japanese IME</span></span>

<span data-ttu-id="cc55a-244">本節逐步解說如何使用日文 IME 搭配 Notepad 來輸入幾個日文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-244">This section is a walk-through of using the Japanese IME with Notepad to enter a few Japanese characters.</span></span>

1.  <span data-ttu-id="cc55a-245">啟動 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-245">Launch Notepad.</span></span> <span data-ttu-id="cc55a-246">在 [記事本] 中輸入一些字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-246">Type some characters in Notepad.</span></span> <span data-ttu-id="cc55a-247">這些字元將協助您在稍後更清楚地視覺化 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="cc55a-247">These characters will help you visualize the IME window better later.</span></span>

    ![顯示字元的螢幕擷取畫面，可協助您在稍後針對日文將 I M E 視窗視覺化。](images/ime-j1.png)

2.  <span data-ttu-id="cc55a-249">使用 [記事本] 作為作用中的應用程式，按一下輸入地區設定指標，然後選取 [日文]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-249">With Notepad as the active application, click the input locale indicator, and select Japanese.</span></span> <span data-ttu-id="cc55a-250">指標顯示會變更為 JP，以反映新的輸入語言是日文。</span><span class="sxs-lookup"><span data-stu-id="cc55a-250">The indicator display changes to JP to reflect that the new input language is Japanese.</span></span>

    ![輸入地區設定指標以選取日文](images/ime-j2.png)

3.  <span data-ttu-id="cc55a-252">將游標放在 [記事本] 中。</span><span class="sxs-lookup"><span data-stu-id="cc55a-252">Place the cursor in Notepad.</span></span> <span data-ttu-id="cc55a-253">按下鍵盤上的 [首頁]，讓游標位於行的開頭。</span><span class="sxs-lookup"><span data-stu-id="cc55a-253">Press HOME on the keyboard so that the cursor is at the beginning of the line.</span></span> <span data-ttu-id="cc55a-254">在鍵盤上輸入 "N"，然後輸入 "I"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-254">On the keyboard type "N", then "I".</span></span> <span data-ttu-id="cc55a-255">下圖顯示顯示的外觀。</span><span class="sxs-lookup"><span data-stu-id="cc55a-255">The following figure shows the appearance of the display.</span></span> <span data-ttu-id="cc55a-256">因為 N + I 是日文的完整發音，所以 IME 有足夠的資訊來預期使用者可能要輸入的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-256">Because N+I is a complete pronunciation in Japanese, the IME has enough information to anticipate the character that the user may have intended to enter.</span></span> <span data-ttu-id="cc55a-257">字元會顯示在 [記事本] 游標上方。</span><span class="sxs-lookup"><span data-stu-id="cc55a-257">A character is displayed on top of the Notepad cursor.</span></span> <span data-ttu-id="cc55a-258">此字元不是 [記事本] 的一部分，而是在 [記事本] 頂端的另一個視窗中顯示，並隱藏下 [記事本] 中現有的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-258">This character is not part of Notepad, rather it is displayed in another window on top of Notepad and hides the existing characters in Notepad that are beneath.</span></span> <span data-ttu-id="cc55a-259">這個新視窗稱為組合視窗，其中的字串稱為組合字元串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-259">This new window is called the composition window, and the string in it is called the composition string.</span></span> <span data-ttu-id="cc55a-260">組合字元串會在顯示中加上底線。</span><span class="sxs-lookup"><span data-stu-id="cc55a-260">The composition string is underlined in the display.</span></span>

    ![顯示組合字元串的螢幕擷取畫面，其中有一個日文字元加上底線。](images/ime-j3.png)

4.  <span data-ttu-id="cc55a-262">現在輸入 "H"、"O"、"N"、"G" 和 "O" 以輸入兩個字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-262">Now type "H", "O", "N", "G", and "O" to enter two more characters.</span></span> <span data-ttu-id="cc55a-263">組合字元串現在包含四個字元，如下所示。</span><span class="sxs-lookup"><span data-stu-id="cc55a-263">The composition string now contains four characters, as shown below.</span></span>

    ![顯示有四個日文字元的組合字元串的螢幕擷取畫面。](images/ime-j4.png)

5.  <span data-ttu-id="cc55a-265">按下空格鍵。</span><span class="sxs-lookup"><span data-stu-id="cc55a-265">Press the Space Bar.</span></span> <span data-ttu-id="cc55a-266">這會指示 IME 將輸入的文字轉換成子句。</span><span class="sxs-lookup"><span data-stu-id="cc55a-266">This instructs the IME to convert the entered text into clauses.</span></span> <span data-ttu-id="cc55a-267">在下圖中，IME 將發音 "Nihongo" 轉換成以日文漢字撰寫的子句，也就是「日文語言」。</span><span class="sxs-lookup"><span data-stu-id="cc55a-267">In the figure below, the IME converts the pronunciation "Nihongo" to a clause written in Kanji that means "Japanese Language."</span></span>

    ![ime 轉換日文發音](images/ime-j5.png)

6.  <span data-ttu-id="cc55a-269">按下鍵盤上的向下箭號一次。</span><span class="sxs-lookup"><span data-stu-id="cc55a-269">Press the down arrow on the keyboard once.</span></span> <span data-ttu-id="cc55a-270">視窗會出現在 [記事本] 上方，如下所示。</span><span class="sxs-lookup"><span data-stu-id="cc55a-270">A window appears on top of Notepad as shown below.</span></span> <span data-ttu-id="cc55a-271">此視窗稱為候選視窗。</span><span class="sxs-lookup"><span data-stu-id="cc55a-271">This window is called the candidate window.</span></span> <span data-ttu-id="cc55a-272">它會顯示符合您所輸入發音的子句清單。</span><span class="sxs-lookup"><span data-stu-id="cc55a-272">It displays a list of clauses that match the pronunciation that you have typed.</span></span> <span data-ttu-id="cc55a-273">您可以從候選清單中選取想要的字組。</span><span class="sxs-lookup"><span data-stu-id="cc55a-273">You can select the intended word from the list of candidates.</span></span> <span data-ttu-id="cc55a-274">在此範例中，有三個候選字元可用於相同的發音。</span><span class="sxs-lookup"><span data-stu-id="cc55a-274">In this example, three candidate characters are available with the same pronunciation.</span></span> <span data-ttu-id="cc55a-275">請注意，第二個專案已反白顯示，而且組合字元串會變更。</span><span class="sxs-lookup"><span data-stu-id="cc55a-275">Note that the second entry is highlighted, and the composition string changes.</span></span> <span data-ttu-id="cc55a-276">這是藉由輸入向下箭號所造成的，這會告知 IME 選取先前顯示的專案。</span><span class="sxs-lookup"><span data-stu-id="cc55a-276">This is caused by typing the down arrow, which tells the IME to select the entry after the one that was previously displayed.</span></span>

    ![顯示候選視窗的螢幕擷取畫面。](images/ime-j6.png)

7.  <span data-ttu-id="cc55a-278">輸入 "2" 來選取第二個專案。</span><span class="sxs-lookup"><span data-stu-id="cc55a-278">Type "2" to select the second entry.</span></span> <span data-ttu-id="cc55a-279">候選視窗現在會關閉，然後以選取的字元更新撰寫字串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-279">The candidate window now closes, and the composition string is updated with the selected character.</span></span>

    ![顯示以選取的日文字元更新的組合字元串的螢幕擷取畫面。](images/ime-j7.png)

8.  <span data-ttu-id="cc55a-281">按 ENTER 鍵。</span><span class="sxs-lookup"><span data-stu-id="cc55a-281">Press ENTER.</span></span> <span data-ttu-id="cc55a-282">這會告知 IME 組合已完成，而且應該將字串傳送至應用程式-在此範例中為「記事本」。</span><span class="sxs-lookup"><span data-stu-id="cc55a-282">This tells the IME that the composition is complete and the string should be sent to the application - Notepad in this example.</span></span> <span data-ttu-id="cc55a-283">組合視窗會關閉，而這兩個字元會透過 [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)傳送至「記事本」。</span><span class="sxs-lookup"><span data-stu-id="cc55a-283">The composition window closes, and the two characters are sent to Notepad via [**WM\_CHAR**](/windows/desktop/inputdev/wm-char).</span></span> <span data-ttu-id="cc55a-284">下圖中的底線如下圖所示，這兩個字元都是 [記事本] 中文字的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc55a-284">The underline is gone in the following figure because the two characters shown are part of the text in Notepad.</span></span> <span data-ttu-id="cc55a-285">[記事本] 中的現有文字 "ABCDEFG" 已移至右側，因為已插入兩個以上的字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-285">The existing text "ABCDEFG" in Notepad is moved to the right because two more characters have been inserted.</span></span> <span data-ttu-id="cc55a-286">您現在已成功使用 IME 輸入幾個日文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-286">You have now successfully entered a few Japanese characters using an IME.</span></span>

    ![使用 ime 成功輸入幾個日文字元](images/ime-j8.png)

## <a name="korean-ime"></a><span data-ttu-id="cc55a-288">韓文輸入法</span><span class="sxs-lookup"><span data-stu-id="cc55a-288">Korean IME</span></span>

<span data-ttu-id="cc55a-289">本節說明如何搭配使用韓文 IME 與 Notepad 來輸入幾個韓文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-289">This section describes how to use the Korean IME with Notepad to enter a few Korean characters.</span></span>

1.  <span data-ttu-id="cc55a-290">啟動 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-290">Launch Notepad.</span></span> <span data-ttu-id="cc55a-291">在 [記事本] 中輸入一些字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-291">Type some characters in Notepad.</span></span> <span data-ttu-id="cc55a-292">這些字元將協助您在稍後更清楚地視覺化 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="cc55a-292">These characters will help you visualize the IME window better later.</span></span>

    ![可協助您在稍後更方便視覺化 ime 視窗的字元](images/ime-k1.png)

2.  <span data-ttu-id="cc55a-294">使用 [記事本] 作為作用中的應用程式，按一下輸入地區設定指標，然後選取 [韓文]。</span><span class="sxs-lookup"><span data-stu-id="cc55a-294">With Notepad as the active application, click the input locale indicator, and select Korean.</span></span> <span data-ttu-id="cc55a-295">指標顯示會變更為 KO，以反映新的輸入語言是韓文。</span><span class="sxs-lookup"><span data-stu-id="cc55a-295">The indicator display changes to KO to reflect that the new input language is Korean.</span></span>

    ![輸入地區設定指標以選取韓文](images/ime-k2.png)

3.  <span data-ttu-id="cc55a-297">將游標放在 [記事本] 中。</span><span class="sxs-lookup"><span data-stu-id="cc55a-297">Place the cursor in Notepad.</span></span> <span data-ttu-id="cc55a-298">按下鍵盤上的 [首頁]，讓游標位於行的開頭，然後輸入 "G"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-298">Press HOME on the keyboard so that the cursor is at the beginning of the line, then type "G".</span></span> <span data-ttu-id="cc55a-299">下圖顯示顯示的外觀。</span><span class="sxs-lookup"><span data-stu-id="cc55a-299">The following figure shows the appearance of the display.</span></span> <span data-ttu-id="cc55a-300">對應到 "G" 的拼音專案會出現在 [記事本] 中，並以區塊游標反白顯示。</span><span class="sxs-lookup"><span data-stu-id="cc55a-300">The phonetic element corresponding to "G" appears on Notepad and is highlighted with a block cursor.</span></span> <span data-ttu-id="cc55a-301">此反白顯示的字元稱為組合字元串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-301">This highlighted character is called the composition string.</span></span> <span data-ttu-id="cc55a-302">請注意，與其他語言的輸入法不同的是，組合字元串會傳送至 [記事本]，並在使用者輸入單一拼音專案時，立即插入現有文字的左邊。</span><span class="sxs-lookup"><span data-stu-id="cc55a-302">Note that unlike the IME for other languages, the composition string is sent to Notepad and inserted to the left of the existing text as soon as the user enters a single phonetic element.</span></span>

    ![顯示組合字元串的螢幕擷取畫面，其中有一個字元插入至現有文字的左邊。](images/ime-k3.png)

4.  <span data-ttu-id="cc55a-304">目前，組合字元串是由過渡字元所組成，因為使用者輸入的任何其他拼音元素都會就地變更撰寫字串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-304">At this time, the composition string consists of an interim character because any additional phonetic elements entered by the user change the composition string in place.</span></span> <span data-ttu-id="cc55a-305">現在輸入 "K"，然後輸入 "S"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-305">Now type "K", then "S".</span></span> <span data-ttu-id="cc55a-306">請注意，每次擊鍵都會變更中間字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-306">Note that the interim character changes with each keystroke.</span></span>

    ![組合字元串](images/ime-k4.png)

5.  <span data-ttu-id="cc55a-308">現在按下 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="cc55a-308">Now press the right CTRL key.</span></span> <span data-ttu-id="cc55a-309">出現的候選視窗會列出您可以針對輸入的發音（G + K + S）選取的中文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-309">A candidate window appears that lists the Hanja characters you can select for the pronunciation entered, G+K+S.</span></span>

    ![顯示候選視窗的螢幕擷取畫面，其中包含您可以在視窗底部選取的中文字元清單。](images/ime-k5.png)

6.  <span data-ttu-id="cc55a-311">輸入數位 "1" 以選取清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="cc55a-311">Type the numeral "1" to select the first entry in the list.</span></span> <span data-ttu-id="cc55a-312">候選視窗會關閉，並使用選取的字元更新撰寫字串。</span><span class="sxs-lookup"><span data-stu-id="cc55a-312">The candidate window closes, and the composition string is updated with the character selected.</span></span>

    ![以選取的字元更新的組合字元串](images/ime-k6.png)

7.  <span data-ttu-id="cc55a-314">輸入 "R"、"N" 和 "R"。</span><span class="sxs-lookup"><span data-stu-id="cc55a-314">Type "R", "N", and "R".</span></span> <span data-ttu-id="cc55a-315">然後按向右鍵，輸入另一個字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-315">Then press the right CTRL key to enter another character.</span></span>

    ![候選視窗](images/ime-k7.png)

8.  <span data-ttu-id="cc55a-317">輸入 "1" 以選取第一個專案。</span><span class="sxs-lookup"><span data-stu-id="cc55a-317">Type "1" to select the first entry.</span></span> <span data-ttu-id="cc55a-318">您現在已成功使用 IME 輸入兩個韓文字元。</span><span class="sxs-lookup"><span data-stu-id="cc55a-318">You have now successfully entered two Korean characters using an IME.</span></span> <span data-ttu-id="cc55a-319">韓文字元已經是 [記事本] 中文字字串的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc55a-319">The Korean characters are already part of the text string in Notepad.</span></span>

    ![使用 ime 成功輸入兩個韓文字元](images/ime-k8.png)

## <a name="requirements"></a><span data-ttu-id="cc55a-321">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc55a-321">Requirements</span></span>



| <span data-ttu-id="cc55a-322">需求</span><span class="sxs-lookup"><span data-stu-id="cc55a-322">Requirement</span></span> | <span data-ttu-id="cc55a-323">值</span><span class="sxs-lookup"><span data-stu-id="cc55a-323">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc55a-324">**作業系統**</span><span class="sxs-lookup"><span data-stu-id="cc55a-324">**Operating System**</span></span>                | <span data-ttu-id="cc55a-325">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc55a-325">Windows XP</span></span>                                                                                                 |
| <span data-ttu-id="cc55a-326">**可用硬碟空間**</span><span class="sxs-lookup"><span data-stu-id="cc55a-326">**Available Hard Disk Space**</span></span>       | <span data-ttu-id="cc55a-327">至少 230 MB</span><span class="sxs-lookup"><span data-stu-id="cc55a-327">At least 230 MB</span></span>                                                                                            |
| <span data-ttu-id="cc55a-328">**外部語言檔案位置**</span><span class="sxs-lookup"><span data-stu-id="cc55a-328">**Foreign Language File Locations**</span></span> | <span data-ttu-id="cc55a-329">Windows XP 安裝 compact 磁片或具有 Windows XP 安裝檔案的網路位置</span><span class="sxs-lookup"><span data-stu-id="cc55a-329">Windows XP installation compact disk or network location with Windows XP installation files</span></span>                |
| <span data-ttu-id="cc55a-330">**Time**</span><span class="sxs-lookup"><span data-stu-id="cc55a-330">**Time**</span></span>                            | <span data-ttu-id="cc55a-331">安裝外部語言檔案大約需要10分鐘;大約十分鐘，以複習四個不同的 Ime。</span><span class="sxs-lookup"><span data-stu-id="cc55a-331">About ten minutes to install foreign language files; about ten minutes each to review four different IMEs.</span></span> |



 

 

 
