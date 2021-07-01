---
title: 適用於 Windows 的遊戲測試案例：Windows XP、Windows Vista、Windows 7 和 Windows 8 上遊戲的最佳作法
description: 本文提供適用于 Windows 遊戲的測試案例。
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120273"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="e4d4d-103">Windows 測試案例的遊戲： Windows XP、Windows Vista、Windows 7 和 Windows 8 遊戲的最佳作法</span><span class="sxs-lookup"><span data-stu-id="e4d4d-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="e4d4d-104">本文提供適用于 Windows 遊戲的測試案例。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="e4d4d-105">如何使用本文</span><span class="sxs-lookup"><span data-stu-id="e4d4d-105">How to Use This Article</span></span>

<span data-ttu-id="e4d4d-106">本文有三個主要區段：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="e4d4d-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**測試需求**</span><span class="sxs-lookup"><span data-stu-id="e4d4d-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-108">這份檔中的每項測試需求都有四個主要區段：標題和資料表，其中有三個值得注意的區段 (左欄、右上角) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="e4d4d-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>標題</span><span class="sxs-lookup"><span data-stu-id="e4d4d-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-110">測試案例的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="e4d4d-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box、最左邊的資料行</span><span class="sxs-lookup"><span data-stu-id="e4d4d-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-112">測試案例所套用的作業系統名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="e4d4d-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box、右上角</span><span class="sxs-lookup"><span data-stu-id="e4d4d-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-114">測試案例的簡短摘要。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="e4d4d-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box、右下角</span><span class="sxs-lookup"><span data-stu-id="e4d4d-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-116">實際測試案例的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e4d4d-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**範例測試腳本**</span><span class="sxs-lookup"><span data-stu-id="e4d4d-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-118">如果使用測試需求做為指南，此區段是一般測試階段將遵循的順序範例。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="e4d4d-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**測試控管注意事項**</span><span class="sxs-lookup"><span data-stu-id="e4d4d-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-120">本章節包含每個測試控管的詳細資訊，這些工具可用來確認測試需求中的通過或失敗狀況。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="e4d4d-121">測試需求</span><span class="sxs-lookup"><span data-stu-id="e4d4d-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="e4d4d-122">1. 遊戲需求</span><span class="sxs-lookup"><span data-stu-id="e4d4d-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="e4d4d-123">1.1 Windows 遊戲瀏覽器</span><span class="sxs-lookup"><span data-stu-id="e4d4d-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-124">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="e4d4d-126">遊戲必須在 Windows Vista 和 Windows 7 上的遊戲瀏覽器中顯示。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="e4d4d-127">選取時，遊戲也必須顯示正確的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="e4d4d-128">安裝不能建立快捷方式來啟動桌面、[開始] 功能表或任何其他位置中的遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="e4d4d-129">不得建立移除的工作和快捷方式。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-130">安裝遊戲之後，請開啟 [遊戲瀏覽器]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="e4d4d-131">確認 [遊戲瀏覽器] 中顯示遊戲圖示。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="e4d4d-132">以滑鼠右鍵按一下圖示，並測試每個應用程式定義的 play & 支援工作。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="e4d4d-133">按一下圖示，並確認底部的 [發行者]、[開發人員]、[內容類型]、[發行日期]、[版本])  (的中繼資料都是正確的。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="e4d4d-134">確認遊戲圖示 Windows 體驗指數 (WEI) 資訊顯示在 [遊戲] Explorer 中。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="e4d4d-135">確認在 [遊戲瀏覽器] 中，中繼資料的遊戲超連結可正常運作。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="e4d4d-136"> (如果未顯示超連結，則這是未簽署 exe 的可能正負號;請參閱 <a href="#23-sign-files">2.3 章節</a>的 ) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="e4d4d-137">確認遊戲在 [遊戲瀏覽器] 中顯示正確的 [家長監護] 控制項評等。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="e4d4d-138"> (如果指出未分級，請確認這是未分級的遊戲;否則，這是未簽署 exe 的指標;請參閱 <a href="#23-sign-files">2.3 章節</a>的 ) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="e4d4d-139">確認遊戲未在使用者桌面上放置啟動快捷方式。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="e4d4d-140">按一下 [開始]-> [所有程式]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="e4d4d-141">確認遊戲未在 [開始] 功能表中放置啟動快捷方式。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="e4d4d-142">確認該遊戲不會在主控台以外的 [開始] 功能表中放置卸載快捷方式。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="e4d4d-143">如果遊戲是以數位方式散佈，請確認服務提供者出現在 Windows 遊戲瀏覽器中。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="e4d4d-144">1.2 Windows 系列安全性/家長監護控制項</span><span class="sxs-lookup"><span data-stu-id="e4d4d-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-145">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="e4d4d-147">遊戲必須在標準使用者的內容中執行 &quot; &quot; 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="e4d4d-148">家長監護必須能夠封鎖遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="e4d4d-149">確認 GDF 具有 EXE 名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-150">在 Windows Vista 或 Windows 7 中建立名為 Toby 的標準使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="e4d4d-151">啟動-> 主控台-> 新增或移除使用者帳戶-> 建立新帳戶</span><span class="sxs-lookup"><span data-stu-id="e4d4d-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="e4d4d-152">和 Jane 一樣，從系統管理員帳戶設定遊戲的家長監護。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="e4d4d-153">開始 > 主控台-> 為任何使用者 > 設定家長監護 Toby</span><span class="sxs-lookup"><span data-stu-id="e4d4d-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="e4d4d-154">確認已從 [遊戲瀏覽器] 圖示啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="e4d4d-155">確認該遊戲在 [家長監護] 主控台中的 [遊戲] 標題下方，顯示正確的 [家長監護] 評等。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="e4d4d-156">套用家長監護之前，請確認遊戲不會在啟動時提示輸入系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="e4d4d-157">將家長監護設定為 &quot; On &quot; 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="e4d4d-158">在 [Windows 設定] 區段中，按一下 [遊戲]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="e4d4d-159">按一下 [確定] (設定現在應該是 &quot; AO/所有遊戲 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="e4d4d-160">確認遊戲以使用者 Jane 的方式執行這些設定。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="e4d4d-161">以 Jane 的形式登出，並以 Toby 登入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="e4d4d-162">確認遊戲以這些設定做為使用者 Toby 來執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="e4d4d-163">以 Toby 的形式登出，並以 Jane 的身份登入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="e4d4d-164">返回至上一個畫面，然後選取 [ &quot; 設定遊戲分級] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="e4d4d-165">選取低於遊戲 ESRB 評等的評等。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-166">如果遊戲未分級，請略過此步驟，並移至此測試的下一個部分。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="e4d4d-167">視所測試 SKU 的語言地區設定而定，可能需要選擇不同的評等系統來尋找遊戲評等。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="e4d4d-168">以 Jane 的形式登出，並以 Toby 登入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="e4d4d-169">確認使用者 Jane 封鎖 ESRB 時，不會啟動使用者 Toby 的遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="e4d4d-170">以 Toby 的形式登出，並以 Jane 的身份登入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="e4d4d-171">如果之前有變更，請還原 ESRB 設定。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="e4d4d-172">如果沒有任何 ESRB 設定，請選取 &quot; [封鎖] 或 [允許特定遊戲]， &quot; 然後依名稱選取遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="e4d4d-173">以 Jane 的形式登出，並以 Toby 登入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="e4d4d-174">確認使用者 Jane 封鎖 EXE/名稱時，不會啟動使用者 Toby 的遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="e4d4d-175">以 Jane 的形式登出 Toby，然後再登入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="e4d4d-176">就像 Jane 一樣，開啟使用者控制項-> 的應用程式限制。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="e4d4d-177">按一下 [ &quot; Toby 只能使用我允許的程式 &quot; ]，然後按一下 [確定] (也就是不允許 exe) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="e4d4d-178">移至使用者控制項 |遊戲使用 ESRB 評等來控制及允許特定遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="e4d4d-179">以 Jane 的形式登出，並以 Toby 登入，然後嘗試播放遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="e4d4d-180">確認遊戲未遭到封鎖，且 Toby 可以在 [ &quot; 允許無 exe] 設定時播放 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="e4d4d-181">1.3 Windows Vista 豐富儲存的遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="e4d4d-182">這項需求已淘汰。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="e4d4d-183">1.4 Xbox 360 Windows 條件式需求的通用控制器 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-184">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-185">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-187">支援遊戲台控制器的遊戲必須支援使用 XInput API 的適用于 Windows 的 Xbox 360 控制器。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="e4d4d-188">所有對通用控制器觸發程式和按鈕的參考都必須使用 Xbox 360 名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-189">啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-189">Launch the game.</span></span></li>
<li><span data-ttu-id="e4d4d-190">移至控制器選項。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="e4d4d-191">確認遊戲可將 Windows Xbox 360 控制器辨識為輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="e4d4d-192">玩遊戲並確認遊戲和功能表系統可控制適用于 Windows 的 Xbox 360 控制器。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="e4d4d-193">確認適用于 Windows 的 Xbox 360 控制器根據接受的標準行為。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="e4d4d-194"> (B 代表上一頁、A for accept、Start for 遊戲功能表/暫停或接受等 ) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="e4d4d-195">確認遊戲是使用 Xbox 360 名稱來參考控制器按鈕和觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-196">如果遊戲不支援遊戲控制器及/或僅支援鍵盤/滑鼠，則略過此測試案例。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="e4d4d-197">\* \* 控制器的設定可能位於遊戲之外。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="e4d4d-198">1.5 多重外觀比例和解析度</span><span class="sxs-lookup"><span data-stu-id="e4d4d-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-199">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-200">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-202">遊戲必須至少支援下列外觀比例和相關聯的螢幕解析度：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="e4d4d-203">4:3 &quot; 標準 &quot; (800 600 或 1024 768) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="e4d4d-204">16:9 &quot; 寬銀幕 &quot; (1280 720) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="e4d4d-205">16:10 &quot; 寬銀幕 &quot; (1152 720、1680 1050 或 800 480) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="e4d4d-206">找出遊戲的影片選項 (這可能是) 的遊戲中。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-207">下列測試必須在寬螢幕監視器上完成。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="e4d4d-208">在 [影片解析度] 區段中，選取 [800 600] 或 [1024 768]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="e4d4d-209">確認遊戲以4:3 的外觀比例解析度執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="e4d4d-210">在 [影片解析度] 區段中，選取 [1280 720]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="e4d4d-211">確認遊戲以16:9 的外觀比例解析度執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="e4d4d-212">在 [影片解析度] 區段中，選取 [1680 1050]、[800 480] 或 [1152 720]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="e4d4d-213">確認遊戲以16:10 的外觀比例解析度執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="e4d4d-214">確認遊戲不會延展圖片，而是會顯示更廣泛的觀點。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="e4d4d-215">確認當解決問題發生變更時，遊戲會提示使用者。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="e4d4d-216">如果使用者未在15秒內接受，請確認顯示器會還原為先前的設定。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="e4d4d-217">確認遊戲未在遊戲播放區域的左側和右側新增黑色橫條。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="e4d4d-218"> (在這種情況下，您會在畫面中間看到遊戲區域仍處於4:3 的比例。 ) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="e4d4d-219">1.6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="e4d4d-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="e4d4d-220">這項需求已淘汰。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="e4d4d-221">1.7 Direct3D \[ 條件式需求\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



| <span data-ttu-id="e4d4d-222">OS</span><span class="sxs-lookup"><span data-stu-id="e4d4d-222">OS</span></span>                                                                    | <span data-ttu-id="e4d4d-223">需求</span><span class="sxs-lookup"><span data-stu-id="e4d4d-223">Requirement</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d4d-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-224">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-225">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-226">Windows XP</span></span><br/> | <span data-ttu-id="e4d4d-227">如果遊戲使用 Direct3D，支援的最低版本必須是 Direct3D 9，而且 Direct3D 必須是任何顯示設定選項的預設值。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-227">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <span data-ttu-id="e4d4d-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>手動</dt></span><span class="sxs-lookup"><span data-stu-id="e4d4d-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="e4d4d-229">啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-229">Launch the game.</span></span> <span data-ttu-id="e4d4d-230">在影片選項中，檢查是否有呈現選項、D3D 和/或 OpenGL。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-230">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="e4d4d-231">如果有的話，請確認遊戲轉譯選項預設為 Direct3D。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-231">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="e4d4d-232">如果您無法確認 D3D9 是所使用的 DirectX 版本，請繼續進行自動化測試。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-232">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="e4d4d-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>自動化測試</dt></span><span class="sxs-lookup"><span data-stu-id="e4d4d-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="e4d4d-234">使用工具： Depends.exe</span><span class="sxs-lookup"><span data-stu-id="e4d4d-234">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="e4d4d-235">1.8 啟用高 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="e4d4d-235">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-236">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-236">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-237">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="e4d4d-238">在啟用 DPI 縮放比例的情況下，遊戲和其安裝程式必須正確執行，而且沒有視覺問題。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-238">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="e4d4d-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>手動</dt> </span><span class="sxs-lookup"><span data-stu-id="e4d4d-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="e4d4d-240">將系統設定為 DPI 150%：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-240">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="e4d4d-241">Windows Vista：主控台：個人化、調整字型大小 (DPI) 、自訂 DPI。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-241">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="e4d4d-242">設定為150%。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-242">Set to 150%.</span></span><br/> <span data-ttu-id="e4d4d-243">Windows 7：主控台：顯示，設定為較大-150%。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-243">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="e4d4d-244">執行安裝程式和遊戲，確認裁剪的畫面或對話方塊沒有任何問題。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-244">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="e4d4d-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>自動化測試</dt> </span><span class="sxs-lookup"><span data-stu-id="e4d4d-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="e4d4d-246">確認元素 <dpiAware>true</dpiAware> 包含在內嵌資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-246">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="e4d4d-247">使用工具： Mt.exe</span><span class="sxs-lookup"><span data-stu-id="e4d4d-247">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="e4d4d-248">2. 安全性和相容性</span><span class="sxs-lookup"><span data-stu-id="e4d4d-248">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="e4d4d-249">2.1 遵循使用者帳戶控制指導方針</span><span class="sxs-lookup"><span data-stu-id="e4d4d-249">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-250">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-250">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-251">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-251">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="e4d4d-252">應用程式所包含的每個可執行檔 (.EXE 擴充) 都必須有定義其執行層級的內嵌資訊清單：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-252">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-253">若為遊戲和遊戲安裝程式，uiAccess 應一律設為 &quot; false &quot; 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-253">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-254">確認遊戲可執行檔包含資訊清單。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-254">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="e4d4d-255">確認遊戲可執行檔資訊清單並無 requestedexecutionlevel 是 &quot; AsInvoker &quot; 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-255">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="e4d4d-256">使用工具： Mt.exe</span><span class="sxs-lookup"><span data-stu-id="e4d4d-256">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="e4d4d-257">2.2 支援 x64 版本的 Windows</span><span class="sxs-lookup"><span data-stu-id="e4d4d-257">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-258">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-258">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-259">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-259">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="e4d4d-260">若要維持與 x64 版 Windows 的相容性：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-260">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="e4d4d-261">標題和標題安裝程式不得包含任何16位程式碼，或依賴任何16位元件。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-261">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="e4d4d-262">如果遊戲相依于操作的核心模式驅動程式，則必須提供這些驅動程式的 x64 版本。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-262">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="e4d4d-263">遊戲安裝程式必須偵測並安裝適用于64位版本 Windows 的適當驅動程式和元件。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-263">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-264">64位版 Windows XP Professional 的支援是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-264">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="e4d4d-265">手動測試</span><span class="sxs-lookup"><span data-stu-id="e4d4d-265">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="e4d4d-266">在64位版本的 Windows 上執行遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-266">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="e4d4d-267">確認遊戲安裝程式在 Windows Vista 或 Windows 7 的64位版本上正常執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-267">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="e4d4d-268">確認遊戲未在64位版本的 Windows Vista 或 Windows 7 上執行16位可執行檔時遇到錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-268">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="e4d4d-269">錯誤會在錯誤視窗中提及16位應用程式。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-269">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="e4d4d-270">如果遊戲有原生的64位可執行檔，則也請使用它。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-270">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="e4d4d-271">2.3 簽署檔案</span><span class="sxs-lookup"><span data-stu-id="e4d4d-271">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-272">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-273">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-273">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-274">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-274">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-275">所有可執行程式碼檔案 (例如，.exe 和 .dll 延伸模組) 必須使用 Authenticode 憑證進行簽署。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-275">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="e4d4d-276">如果您使用 Windows Installer，則必須簽署安裝程式 (.msi 檔案) 的封裝檔案。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-276">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="e4d4d-277">手動測試</span><span class="sxs-lookup"><span data-stu-id="e4d4d-277">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="e4d4d-278">流覽至遊戲目錄。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-278">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="e4d4d-279">找出所有 .exe 和 .dll 檔案。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-279">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="e4d4d-280">以滑鼠右鍵按一下每個檔案的 [屬性]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-280">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="e4d4d-281">確認遊戲可執行檔包含數位簽章。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-281">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="e4d4d-282">2.4 簽署驅動程式</span><span class="sxs-lookup"><span data-stu-id="e4d4d-282">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-283">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-283">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-284">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-284">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-285">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-285">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-286">遊戲所安裝的任何核心模式驅動程式都必須使用公開有效的 Authenticode 憑證進行簽署。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-286">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="e4d4d-287">遊戲所安裝的任何核心模式硬體設備磁碟機都必須有透過 Windows 硬體品質實驗室 (WHQL) 或驅動程式可靠性簽章 (DRS) 程式取得的 Microsoft 簽名。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-287">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="e4d4d-288">手動測試</span><span class="sxs-lookup"><span data-stu-id="e4d4d-288">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="e4d4d-289">安裝遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-289">Install the game.</span></span></li>
<li><span data-ttu-id="e4d4d-290">確認遊戲安裝程式未顯示未簽署的驅動程式對話方塊 (s) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-290">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="e4d4d-291">2.5 正確執行版本檢查</span><span class="sxs-lookup"><span data-stu-id="e4d4d-291">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-292">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-292">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-293">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-293">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-294">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-294">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-295">除非使用者授權合約禁止在未來的作業系統上使用，否則遊戲不能在未來的作業系統上執行，如 Windows 版本號碼的變更所述。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-295">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="e4d4d-296">如果遊戲應該會失敗，就必須向使用者顯示訊息，以正常方式進行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-296">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="e4d4d-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>手動</dt> </span><span class="sxs-lookup"><span data-stu-id="e4d4d-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="e4d4d-298">在 windows XP、windows Vista 和 Windows 7 的32位版本，以及在64位版本的 Windows Vista 和 Windows 7 上安裝遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-298">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="e4d4d-299">確認遊戲安裝程式未遇到關於 OS 版本的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-299">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="e4d4d-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>自動化測試</dt> </span><span class="sxs-lookup"><span data-stu-id="e4d4d-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="e4d4d-301">使用工具：應用程式驗證器</span><span class="sxs-lookup"><span data-stu-id="e4d4d-301">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="e4d4d-302">啟動應用程式驗證器。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-302">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="e4d4d-303">選取 INSTALL.EXE 之後，請啟用 [相容性： HighVersionLie 測試]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-303">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="e4d4d-304">安裝遊戲，並確定不會根據作業系統版本封鎖安裝。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-304">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="e4d4d-305">選取 GAME.EXE 之後，請啟用 [相容性： HighVersionLie 測試]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-305">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="e4d4d-306">執行遊戲，並確定它不會根據作業系統版本封鎖執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-306">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="e4d4d-307">2.6 支援並行使用者會話</span><span class="sxs-lookup"><span data-stu-id="e4d4d-307">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-308">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-308">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-309">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-310">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-310">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-311">遊戲必須支援標準 Windows 多工案例。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-311">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="e4d4d-312">在 Windows Vista 或 Windows 7 中建立名為 Toby 的標準使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-312">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="e4d4d-313">啟動-> 主控台-> 新增或移除使用者帳戶-> 建立新帳戶</span><span class="sxs-lookup"><span data-stu-id="e4d4d-313">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="e4d4d-314">以使用者 Jane 的形式啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-314">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="e4d4d-315">ALT + TAB 回到桌面上。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-315">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="e4d4d-316">確認遊戲正確地將 ALT + Tab 切換至 Windows 桌面。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-316">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="e4d4d-317">按一下 [開始-> [鎖定右邊的箭號]-> 切換使用者]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-317">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="e4d4d-318">以使用者 Toby 登入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-318">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="e4d4d-319">確認該遊戲在以使用者 Jane 的方式執行時，以使用者 Toby 的形式啟動。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-319">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="e4d4d-320">確認在使用者切換程式期間，此遊戲不會遇到使用者 Toby 或使用者 Jane 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-320">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="e4d4d-321">如果您可以啟動其他遊戲會話，請確認您無法從原始的遊戲會話聽到音訊。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-321">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="e4d4d-322">關閉遊戲並切換回原始的使用者和遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-322">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="e4d4d-323">2.7 支援長名稱</span><span class="sxs-lookup"><span data-stu-id="e4d4d-323">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-324">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-324">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-325">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-325">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-326">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-326">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-327">如果遊戲支援儲存檔案，它必須能夠儲存具有完整名稱和路徑的檔案。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-327">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="e4d4d-328">遊戲必須適當地處理特殊檔案系統字元，例如 \/： \*？</span><span class="sxs-lookup"><span data-stu-id="e4d4d-328">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="e4d4d-329">&quot; 在用來建立檔案名或路徑的任何使用者輸入欄位中，< 或 >。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-329">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-330">啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-330">Launch the game.</span></span></li>
<li><span data-ttu-id="e4d4d-331">開始新的遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-331">Start a new game.</span></span></li>
<li><span data-ttu-id="e4d4d-332">儲存遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-332">Save the game.</span></span> <span data-ttu-id="e4d4d-333">在儲存過程中，請使用 [儲存名稱：我的第一個儲存] 遊戲來確認遊戲是否儲存。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-333">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="e4d4d-334">退出主功能表。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-334">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="e4d4d-335">嘗試載入新儲存的遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-335">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="e4d4d-336">確認在處理不受支援的檔案系統字元（例如 \/： \*）時，此遊戲不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-336">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="e4d4d-337">&quot; < 或 > 如果遊戲允許您，請為已儲存的遊戲命名。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-337">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="e4d4d-338">如果允許使用者命名其設定檔及（或）字元或儲存遊戲，請在這裡使用長檔名時，確認遊戲不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-338">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="e4d4d-339">3. 安裝</span><span class="sxs-lookup"><span data-stu-id="e4d4d-339">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="e4d4d-340">3.1 簡易安裝</span><span class="sxs-lookup"><span data-stu-id="e4d4d-340">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-341">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-341">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-342">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-342">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-343">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-343">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-344">使用傳統安裝的遊戲必須在其安裝程式使用者介面中提供簡化的路徑。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-344">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-345">插入遊戲光碟。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-345">Insert the game disc.</span></span></li>
<li><span data-ttu-id="e4d4d-346">確認該遊戲未顯示 End-User 授權合約 (EULA) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-346">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="e4d4d-347">如果遊戲支援自訂或 advanced 安裝選項，請確認此選項可在安裝過程中存取。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-347">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="e4d4d-348">確認 [預設安裝] 選項會略過安裝程式的所有使用者輸入選項， (選取 [安裝資料夾]、[元件選取] 等) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-348">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="e4d4d-349">確認遊戲安裝程式不會提示 OS 元件安裝 (DirectX 安裝程式、Visual C 執行時間等) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-349">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="e4d4d-350">確認遊戲安裝程式未提示防火牆互動。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-350">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="e4d4d-351">確認遊戲會自動執行，或在安裝程式結束時出現啟動器功能表。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-351">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="e4d4d-352">確認遊戲卸載程式會移除所有已安裝、未轉散發的作業系統元件檔案，並清除所有設定。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-352">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="e4d4d-353">不需要清除每一使用者的設定和資料 (例如儲存的遊戲) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-353">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="e4d4d-354">3.2 支援安裝的使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="e4d4d-354">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-355">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-355">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-356">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-356">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="e4d4d-357">遊戲安裝程式不能假設它是在與使用者相同的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-357">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="e4d4d-358">因此，遊戲必須在第一次執行時，與安裝分開執行每個使用者的工作。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-358">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-359">確認您可以將遊戲安裝為使用者 Jane。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-359">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="e4d4d-360"> (在安裝/安裝程式期間，這會需要更高的許可權。 ) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-360">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="e4d4d-361">確認遊戲安裝程式會提示使用者 Jane 透過系統管理員認證來提升許可權。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-361">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="e4d4d-362"> (要提升的提示會在使用者嘗試安裝時出現。 ) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-362">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="e4d4d-363">選擇在安裝結束時自動執行遊戲（如果尚未這麼做），或從出現的功能表中啟動。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-363">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="e4d4d-364">一旦遊戲中，請建立新的設定檔，並玩遊戲並加以儲存。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-364">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="e4d4d-365">離開遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-365">Exit the game.</span></span></li>
<li><span data-ttu-id="e4d4d-366">重新開機遊戲，並確認使用者 Jane 帳戶可以存取使用者設定檔和儲存的遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-366">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="e4d4d-367">3.3 安裝到正確的資料夾</span><span class="sxs-lookup"><span data-stu-id="e4d4d-367">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-368">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-368">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-369">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-370">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-370">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-371">根據預設，遊戲必須安裝至 Program Files 資料夾。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-371">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="e4d4d-372">使用者資料必須在第一次執行時寫入，而不是在安裝期間寫入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-372">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-373">使用預設的安裝類型來安裝遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-373">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="e4d4d-374">確認已將遊戲安裝至 Program Files。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-374">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-375">如果此測試失敗，請確認該遊戲是否適用于所有使用者的安裝。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-375">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="e4d4d-376">如果是，就會發生失敗。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-376">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="e4d4d-377">3.4 正確安裝 Windows 資源</span><span class="sxs-lookup"><span data-stu-id="e4d4d-377">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-378">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-378">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-379">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-380">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-380">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-381">應用程式不能嘗試安裝受 Windows 資源保護 (WRP) 保護的檔案或登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-381">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="e4d4d-382">確認安裝程式期間沒有出現任何 Windows 資源保護 WRP] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-382">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="e4d4d-383">3.5 避免在安裝期間重新開機</span><span class="sxs-lookup"><span data-stu-id="e4d4d-383">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-384">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-384">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-385">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-385">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-386">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-386">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-387">遊戲安裝程式不應假設重新發佈套件的 Windows 元件安裝需要重新開機，除非重新開機是由傳回結果或 Microsoft 檔所表示。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-387">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-388">安裝遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-388">Install the game.</span></span></li>
<li><span data-ttu-id="e4d4d-389">確認遊戲不需要在安裝後重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-389">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-390">如果 Microsoft 系統更新可轉散發套件需要重新開機，請執行下列動作：完成遊戲安裝、卸載遊戲，然後再次安裝遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-390">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="e4d4d-391">在第二次安裝時，遊戲安裝程式不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-391">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="e4d4d-392">3.6 使用正確的檔案版本控制</span><span class="sxs-lookup"><span data-stu-id="e4d4d-392">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-393">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-393">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-394">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-394">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-395">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-395">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-396">遊戲安裝程式必須正確檢查，以確定已安裝最新的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-396">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="e4d4d-397">安裝遊戲絕不能回歸您不會產生的任何檔案，或是由您未產生的應用程式所共用的檔案。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-397">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-398">在安裝遊戲之前，請先建立 System32 的預先安裝快照集。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-398">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="e4d4d-399">建立名為 G4Wtest 的目錄。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-399">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="e4d4d-400">啟動命令視窗， (啟動-> 執行-> cmd) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-400">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="e4d4d-401">流覽至 c:\windows\system32。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-401">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="e4d4d-402">輸入 dir/o：-g/o：-d >> c:\G4Wtest\pregame.txt。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-402">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="e4d4d-403">建立 System32 的後置安裝快照集。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-403">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="e4d4d-404">啟動命令視窗， (啟動-> 執行-> cmd) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-404">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="e4d4d-405">流覽至 c:\windows\system32。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-405">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="e4d4d-406">輸入 dir/o：-g/o：-d >> c:\G4Wtest\postgame.txt。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-406">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="e4d4d-407">確認遊戲未回歸任何檔案版本的遊戲未產生的檔案 ( .。。在兩份檔中列出的檔案，其方式是比較 pregame.txt 與 postgame.txt) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-407">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="e4d4d-408">3.7 支援自動運行 \[ 條件需求\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-408">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-409">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-409">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-410">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-410">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-411">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-411">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-412">針對在 CD、DVD 或其他支援自動執行的卸載式媒體上散佈的遊戲，當光碟第一次插入時，應用程式必須自動執行或提示使用者安裝遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-412">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-413">為了在 windows Vista 之前的 Windows 版本上使用而撰寫的自動執行程式，不應該使用 .NET 執行時間，因為這項技術並不包含在 Windows XP 或舊版的 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-413">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="e4d4d-414">如需進一步指引，請參閱 <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Windows 技術需求</a> 3.7 的遊戲，支援自動執行時間。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-414">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="e4d4d-415">插入遊戲光碟或媒體。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-415">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="e4d4d-416">確認 [安裝/執行] 對話方塊已自動啟動。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-416">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="e4d4d-417">Windows Vista 或 Windows 7：確認遊戲自動執行程式本身不會提示使用者 Jane 透過系統管理員認證來提升許可權。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-417">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="e4d4d-418">確認自動執行的可執行檔不需要現成可轉散發元件，例如 .NET 3.5、C Run-Time 程式庫等等。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-418">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="e4d4d-419">請確認在安裝後重新插入磁片磁碟機中的光碟，不會再次自動開始安裝。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-419">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="e4d4d-420">4. 可靠性</span><span class="sxs-lookup"><span data-stu-id="e4d4d-420">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="e4d4d-421">4.1 消除不必要的重新開機</span><span class="sxs-lookup"><span data-stu-id="e4d4d-421">4.1 Eliminate Unnecessary Reboots</span></span>



| <span data-ttu-id="e4d4d-422">OS</span><span class="sxs-lookup"><span data-stu-id="e4d4d-422">OS</span></span>                                              | <span data-ttu-id="e4d4d-423">需求</span><span class="sxs-lookup"><span data-stu-id="e4d4d-423">Requirement</span></span>                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d4d-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-424">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-425">Windows Vista</span></span><br/> | <span data-ttu-id="e4d4d-426">所有應用程式安裝程式都必須利用重新開機管理員 Api 來避免系統重新開機 (請參閱 [需求 3.5](#35-avoid-reboots-during-installation)) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-426">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="e4d4d-427">4.2 消除應用程式驗證器失敗</span><span class="sxs-lookup"><span data-stu-id="e4d4d-427">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-428">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-428">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-429">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-430">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-430">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-431">在下列測試中，遊戲必須不會在 Microsoft 應用程式驗證器 (AppVerifier) 4.0 版或更新版本下產生任何失敗：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-431">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="e4d4d-432">基本概念：控制碼、堆積、鎖定、記憶體、TLS</span><span class="sxs-lookup"><span data-stu-id="e4d4d-432">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="e4d4d-433">其他： DangerousAPIs、DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="e4d4d-433">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="e4d4d-434">使用工具： AppVerifier 4.0 (或更新版本) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-434">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="e4d4d-435">安裝 AppVerifier。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-435">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="e4d4d-436">啟動 AppVerifier，然後選取 [檔案-> 新增應用程式]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-436">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="e4d4d-437">找出遊戲可執行檔，選取它，然後按一下 [ &quot; 開啟] &quot; 按鈕。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-437">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="e4d4d-438">在 [ &quot; 應用程式] &quot; 區段中，選取 [遊戲可執行檔]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-438">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="e4d4d-439">在 [ &quot; 測試] &quot; 區段中，選取 [分類基本和其他] 底下列出的測試 (取消核取 [ &quot; ThreadPool] 和 [TimeRollOver] &quot; &quot; &quot;) ，並確定未選取所有其他測試。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-439">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="e4d4d-440">啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-440">Launch the game.</span></span></li>
<li><span data-ttu-id="e4d4d-441">確認遊戲在應用程式驗證器下執行時，不會產生失敗。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-441">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="e4d4d-442">有些測試需要完整執行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-442">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="e4d4d-443">這可能需要不受保護的遊戲可執行檔版本，因為反盜版/反盜版技術可能會干擾 AppVerifer。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-443">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="e4d4d-444">4.3 支援 Windows 錯誤報告</span><span class="sxs-lookup"><span data-stu-id="e4d4d-444">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-445">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-446">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-447">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-448">遊戲必須只處理已知和預期的例外狀況，Windows 錯誤報告不得停用。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-448">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="e4d4d-449">如果將錯誤 (（例如存取違規) ）插入遊戲中，則必須允許 Windows 錯誤報告報告損毀。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-449">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="e4d4d-450">使用工具：執行緒劫匪</span><span class="sxs-lookup"><span data-stu-id="e4d4d-450">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="e4d4d-451">如果應用程式在測試時當機，請確認該遊戲已正確顯示 Windows 錯誤報告，並收集損毀資料。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-451">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-452">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-452">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-453">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-454">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-454">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-455">所有可執行檔 (例如，.exe 或 .dll 檔案) 必須包含正確的產品名稱、公司名稱和檔案版本。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-455">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="e4d4d-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>手動測試：</dt> </span><span class="sxs-lookup"><span data-stu-id="e4d4d-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="e4d4d-457">在安裝媒體上，以滑鼠右鍵按一下遊戲的可執行檔 (s) ，然後安裝在電腦硬碟上。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-457">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="e4d4d-458">選取 [屬性]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-458">Select Properties.</span></span></li>
<li><span data-ttu-id="e4d4d-459">Windows XP：按一下 [ <strong>版本</strong> ] 索引標籤。確認已正確填入 [產品名稱]、[公司名稱] 和 [檔案版本] 欄位。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-459">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="e4d4d-460">Windows Vista 或 Windows 7：按一下 [ <strong>詳細資料</strong> ] 索引標籤。確認 [產品名稱] 和 [檔案版本] 欄位已正確填入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-460">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="e4d4d-461">在 Windows Vista 或 Windows 7 的 [屬性] 頁面中看不到公司名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-461">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="e4d4d-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>自動化測試：</dt> </span><span class="sxs-lookup"><span data-stu-id="e4d4d-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="e4d4d-463">使用 Microsoft 遊戲進行 Windows 測試控管;請參閱 <a href="#64-microsoft-games-for-windows-test-tool">第6.4 節</a>。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-463">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e4d4d-464">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4d4d-464">Windows 7</span></span><br/> <span data-ttu-id="e4d4d-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4d4d-465">Windows Vista</span></span><br/> <span data-ttu-id="e4d4d-466">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d4d-466">Windows XP</span></span><br/></td>
<td><span data-ttu-id="e4d4d-467">正常結束遊戲時，不能造成不明的例外狀況錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-467">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="e4d4d-468">播放正常遊戲會話的遊戲之後，請確認遊戲未在結束時產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-468">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="e4d4d-469">5. 範例測試腳本</span><span class="sxs-lookup"><span data-stu-id="e4d4d-469">5. Sample Test Script</span></span>

<span data-ttu-id="e4d4d-470">這是使用上述測試需求作為指南的一般測試階段範例。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-470">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="e4d4d-471">5.1 工具</span><span class="sxs-lookup"><span data-stu-id="e4d4d-471">5.1 Tools</span></span>

-   <span data-ttu-id="e4d4d-472">Windows Vista SP1 和（或） Windows 7 在 AMD CPU 上的32位版本</span><span class="sxs-lookup"><span data-stu-id="e4d4d-472">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="e4d4d-473">Intel CPU 上的 Windows Vista SP1 和（或） Windows 7 的32位版本</span><span class="sxs-lookup"><span data-stu-id="e4d4d-473">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="e4d4d-474">Windows Vista SP1 和（或） Windows 7 在 AMD CPU 上的64位版本</span><span class="sxs-lookup"><span data-stu-id="e4d4d-474">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="e4d4d-475">Intel CPU 上的 Windows Vista SP1 和（或） Windows 7 的64位版本</span><span class="sxs-lookup"><span data-stu-id="e4d4d-475">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="e4d4d-476">AMD CPU 上的32位 edition Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="e4d4d-476">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="e4d4d-477">Intel CPU 上的32位版 Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="e4d4d-477">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="e4d4d-478">支援 1680 1050 的全螢幕監視器</span><span class="sxs-lookup"><span data-stu-id="e4d4d-478">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="e4d4d-479">適用于 Windows 的 Xbox 360 控制器</span><span class="sxs-lookup"><span data-stu-id="e4d4d-479">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="e4d4d-480">5.2 預先安裝</span><span class="sxs-lookup"><span data-stu-id="e4d4d-480">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="e4d4d-481">Windows Vista 和 Windows 7：建立兩位標準使用者： Jane 和 Toby</span><span class="sxs-lookup"><span data-stu-id="e4d4d-481">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="e4d4d-482">Windows Vista 和 Windows 7：確定已啟用使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="e4d4d-482">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="e4d4d-483">建立 System32 的預先安裝快照集</span><span class="sxs-lookup"><span data-stu-id="e4d4d-483">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="e4d4d-484">建立名為 G4Wtest 的目錄</span><span class="sxs-lookup"><span data-stu-id="e4d4d-484">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="e4d4d-485">顯示命令視窗 (啟動-> 執行-> cmd) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-485">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="e4d4d-486">流覽至 c： \\ windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="e4d4d-486">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="e4d4d-487">輸入 dir/o：-g/o：-d >> c： \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="e4d4d-487">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="e4d4d-488">Windows Vista 和 Windows 7：設定為 150% DPI \[ 1。8\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-488">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="e4d4d-489">繼續 [安裝](#3-installation)</span><span class="sxs-lookup"><span data-stu-id="e4d4d-489">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="e4d4d-490">5.3 安裝</span><span class="sxs-lookup"><span data-stu-id="e4d4d-490">5.3 Install</span></span>

1.  <span data-ttu-id="e4d4d-491">以使用者 Jane 登入</span><span class="sxs-lookup"><span data-stu-id="e4d4d-491">Log on as User Jane</span></span>
2.  <span data-ttu-id="e4d4d-492">將遊戲光碟插入 CD/DVD 光碟機中，確認 [安裝/執行] 對話方塊自動出現 \[ 3。7\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-492">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="e4d4d-493">確認遊戲安裝程式會提示使用者 Jane 提升系統管理員認證 \[ 3。2\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-493">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="e4d4d-494">確認遊戲自動執行程式本身不會提示使用者 Jane 透過系統管理員認證3.7 進行提升 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-494">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="e4d4d-495">確認遊戲未顯示超過一份 End-User 授權合約 (EULA) \[ 3。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-495">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="e4d4d-496">確認遊戲顯示預設/簡單和自訂/Advanced 安裝選項 \[ 3。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-496">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="e4d4d-497">確認 [預設/簡單安裝] 選項會略過安裝程式的所有使用者輸入選項， (選取 [安裝資料夾]、[元件選取] 等等。 ) \[ 3。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-497">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="e4d4d-498">確認遊戲安裝程式不會提示 OS 元件安裝 (DirectX 安裝程式、C Run-Time 程式庫等等。 ) \[ 3。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-498">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="e4d4d-499">確認遊戲安裝程式未提示防火牆互動 \[ 3。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-499">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="e4d4d-500">確認遊戲安裝程式未遇到關於 OS 版本 \[ 2.5 \] \[ 4.2 的錯誤\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-500">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="e4d4d-501">確認遊戲安裝程式未顯示未簽署的驅動程式對話方塊 (s) \[ 2。4\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-501">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="e4d4d-502">確認未在安裝程式期間出現任何 Windows 資源保護 (WRP) 對話方塊： \[ 3。4\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-502">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="e4d4d-503">確認在安裝後將光碟重新插入磁片磁碟機，不會再次自動開始安裝</span><span class="sxs-lookup"><span data-stu-id="e4d4d-503">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="e4d4d-504">確認遊戲不需要在安裝3.5 後重新開機系統 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-504">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="e4d4d-505">確認您可以將遊戲安裝為使用者 Jane \[ 3。2\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-505">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="e4d4d-506">確認遊戲會自動執行，或在安裝程式結束時出現啟動器功能表 \[ 3。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-506">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="e4d4d-507">如果遊戲在安裝後自動執行，請跳至[運行](#55-runtime)時間</span><span class="sxs-lookup"><span data-stu-id="e4d4d-507">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="e4d4d-508">如果遊戲離開啟動功能表，或無法卸載，請參閱[安裝後](#54-post-install)的章節</span><span class="sxs-lookup"><span data-stu-id="e4d4d-508">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="e4d4d-509">5.4 安裝後</span><span class="sxs-lookup"><span data-stu-id="e4d4d-509">5.4 Post-Install</span></span>

1.  <span data-ttu-id="e4d4d-510">確認遊戲未在使用者桌面1.1 上放置啟動快捷方式 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-510">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="e4d4d-511">確認遊戲未在 [開始] 功能表1.1 中放置啟動快捷方式 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-511">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="e4d4d-512">確認遊戲圖示顯示在 Windows 遊戲瀏覽器 \[ 1.1 中\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-512">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="e4d4d-513">確認底部的 [發行者]、[開發人員]、[內容類型]、[發行日期]、[版本])  (的中繼資料，以及是否正確 \[ 1。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-513">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="e4d4d-514">確認遊戲圖示顯示 Windows 體驗指數 (Windows 遊戲瀏覽器1.1 中) 資訊的 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-514">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="e4d4d-515">確認適用于中繼資料的遊戲超連結在 Windows 遊戲瀏覽器1.1 中正確運作 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-515">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="e4d4d-516">確認該遊戲在 Windows 遊戲瀏覽器1.1 中顯示精確的家長監護控制項分級 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-516">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="e4d4d-517">建立 System32 的後置安裝快照集</span><span class="sxs-lookup"><span data-stu-id="e4d4d-517">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="e4d4d-518">顯示命令視窗 (啟動-> 執行-> cmd) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-518">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="e4d4d-519">流覽至 c： \\ windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="e4d4d-519">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="e4d4d-520">輸入 dir/o：-g/o：-d >> c： \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="e4d4d-520">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="e4d4d-521">藉由比較 pregame.txt 與 postgame.txt 3.6，確認遊戲未回歸兩份檔中所列檔案的任何檔案版本 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-521">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="e4d4d-522">繼續進行[運行](#55-runtime)時間</span><span class="sxs-lookup"><span data-stu-id="e4d4d-522">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="e4d4d-523">5.5 執行時間</span><span class="sxs-lookup"><span data-stu-id="e4d4d-523">5.5 Runtime</span></span>

1.  <span data-ttu-id="e4d4d-524">執行時間1：如果出現 [啟動] 功能表，請從該處啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-524">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="e4d4d-525">如果在安裝後自動執行遊戲或從遊戲啟動器功能表啟動，請執行下列動作：如果沒有，請跳至執行時間2：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-525">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="e4d4d-526">如果遊戲允許， (建立設定檔) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-526">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="e4d4d-527">開始新的遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-527">Start a new game</span></span>
    3.  <span data-ttu-id="e4d4d-528">儲存遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-528">Save the game</span></span>
    4.  <span data-ttu-id="e4d4d-529">離開遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-529">Exit the game</span></span>
    5.  <span data-ttu-id="e4d4d-530">從遊戲瀏覽器啟動遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-530">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="e4d4d-531">確認遊戲從遊戲瀏覽器圖示 \[ 1.2 啟動\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-531">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="e4d4d-532">確認遊戲不會在啟動1.2 時提示輸入系統管理員認證 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-532">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="e4d4d-533">確認使用者 Jane 帳戶3.2 可存取使用者設定檔和儲存遊戲 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-533">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="e4d4d-534">繼續執行執行時間3</span><span class="sxs-lookup"><span data-stu-id="e4d4d-534">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="e4d4d-535">執行時間2：如果遊戲未從遊戲啟動器功能表自動執行或顯示啟動，這會是3.1 的失敗 \[ \] ; 不過，測試可以正常地繼續：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-535">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="e4d4d-536">從遊戲瀏覽器啟動遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-536">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="e4d4d-537">確認遊戲從遊戲瀏覽器圖示 \[ 1.2 啟動\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-537">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="e4d4d-538">確認遊戲不會在啟動1.2 時提示輸入系統管理員認證 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-538">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="e4d4d-539">繼續執行執行時間3</span><span class="sxs-lookup"><span data-stu-id="e4d4d-539">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="e4d4d-540">執行時間3：如果遊戲支援遊戲台，請確認遊戲可將 Windows Xbox 360 控制器辨識為輸入裝置 \[ 1。4\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-540">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="e4d4d-541">如有需要，請透過 [選項] 功能表啟用控制器</span><span class="sxs-lookup"><span data-stu-id="e4d4d-541">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="e4d4d-542">使用 Xbox 360 名稱確認遊戲參考控制器按鈕和觸發程式</span><span class="sxs-lookup"><span data-stu-id="e4d4d-542">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="e4d4d-543">確認遊戲和功能表系統可控制適用于 Windows 的 Xbox 360 控制器</span><span class="sxs-lookup"><span data-stu-id="e4d4d-543">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="e4d4d-544">確認適用于 Windows 的 Xbox 360 控制器根據接受的標準運作</span><span class="sxs-lookup"><span data-stu-id="e4d4d-544">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="e4d4d-545">將影片設定為 \[ 1.5 \] ：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-545">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="e4d4d-546">確認遊戲以4:3 的外觀比例解析度執行 (800 600 或 1024 768) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-546">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="e4d4d-547">確認遊戲以16:9 的外觀比例解析度執行 (1280 720) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-547">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="e4d4d-548">確認遊戲以16:10 的外觀比例解析度（ (1680 1050、800 480 或 1152 720）執行) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-548">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="e4d4d-549">確認當解決問題時，遊戲提示使用者</span><span class="sxs-lookup"><span data-stu-id="e4d4d-549">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="e4d4d-550">如果您未在15秒內接受，請確認顯示器會還原為先前的設定</span><span class="sxs-lookup"><span data-stu-id="e4d4d-550">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="e4d4d-551">確認遊戲不會延展圖片，而是會顯示更廣大的視圖區域</span><span class="sxs-lookup"><span data-stu-id="e4d4d-551">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="e4d4d-552">確認遊戲未在遊戲播放區域的左邊和右邊新增黑色橫條</span><span class="sxs-lookup"><span data-stu-id="e4d4d-552">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="e4d4d-553">如果影片設定中有提供，請確認遊戲轉譯選項預設為 Direct3D \[ 1.7 \] ; 否則，請繼續進行 [自動化測試](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="e4d4d-553">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="e4d4d-554">如果出現提示或選項可供使用，請建立使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-554">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="e4d4d-555">確認在使用長檔名時，遊戲不會遇到錯誤 \[ 2。7\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-555">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="e4d4d-556">開始新的遊戲、建立遊戲儲存，並確認在處理不支援的檔案系統字元時，遊戲不會遇到錯誤 \[ 2。7\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-556">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="e4d4d-557">確認遊戲正確地將 ALT + Tab 切換至 Windows 桌面 \[ 2。6\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-557">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="e4d4d-558">按一下 [開始-> 切換使用者]，切換執行遊戲的使用者</span><span class="sxs-lookup"><span data-stu-id="e4d4d-558">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="e4d4d-559">以 Toby 登入</span><span class="sxs-lookup"><span data-stu-id="e4d4d-559">Log on as Toby</span></span>
    3.  <span data-ttu-id="e4d4d-560">確認在以使用者 Jane 2.6 的形式執行時，遊戲以使用者 Toby 的形式啟動 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-560">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="e4d4d-561">確認在使用者切換程式期間，此遊戲不會遇到使用者 Toby 或使用者 Jane 的錯誤 \[ 2。6\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-561">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="e4d4d-562">確認您無法聽到原始遊戲會話2.6 的音訊 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-562">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="e4d4d-563">離開遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-563">Exit the game</span></span>
    7.  <span data-ttu-id="e4d4d-564">登出 Toby</span><span class="sxs-lookup"><span data-stu-id="e4d4d-564">Log off Toby</span></span>
    8.  <span data-ttu-id="e4d4d-565">切換回正在執行遊戲的原始使用者</span><span class="sxs-lookup"><span data-stu-id="e4d4d-565">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="e4d4d-566">ALT + TAB 回到遊戲中</span><span class="sxs-lookup"><span data-stu-id="e4d4d-566">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="e4d4d-567">離開遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-567">Exit the game</span></span>
10. <span data-ttu-id="e4d4d-568">繼續進行[後置運行](#56-post-runtime)時間</span><span class="sxs-lookup"><span data-stu-id="e4d4d-568">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="e4d4d-569">5.6 後置執行時間</span><span class="sxs-lookup"><span data-stu-id="e4d4d-569">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="e4d4d-570">確認遊戲未在結束4.3 時產生錯誤 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-570">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="e4d4d-571">確認已將遊戲安裝至 Program Files \[ 3。3\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-571">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="e4d4d-572">繼續進行[家長](/windows)監護</span><span class="sxs-lookup"><span data-stu-id="e4d4d-572">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="e4d4d-573">5.7 家長監護</span><span class="sxs-lookup"><span data-stu-id="e4d4d-573">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="e4d4d-574">在主控台中開啟家長監護</span><span class="sxs-lookup"><span data-stu-id="e4d4d-574">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="e4d4d-575">確認該遊戲在家長監護的遊戲標題下方顯示精確的家長監護，主控台 \[ 1。2\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-575">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="e4d4d-576">請參閱測試案例 \[ 1.2 \] 以進行下列測試：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-576">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="e4d4d-577">將家長監護設定為 [開啟] 之後，請確認遊戲以使用者 Jane 1.2 的這些設定執行。 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-577">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="e4d4d-578">登出並以 Toby 登入</span><span class="sxs-lookup"><span data-stu-id="e4d4d-578">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="e4d4d-579">確認遊戲以這些設定作為使用者 Toby 1.2 來執行 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-579">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="e4d4d-580">登出並以 Jane 登入</span><span class="sxs-lookup"><span data-stu-id="e4d4d-580">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="e4d4d-581">在 [家長監護] 區段中，封鎖使用者 Toby 從您剛剛安裝的遊戲中，讓使用者看得到一個 ESRB 等級以上的遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-581">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="e4d4d-582">範例：如果遊戲的分級為 E，請設定它，讓 Toby 只能播放評為 C 的遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-582">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="e4d4d-583">確認遊戲以使用者 Jane 1.2 的這些設定執行 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-583">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="e4d4d-584">登出並以使用者 Toby 登入</span><span class="sxs-lookup"><span data-stu-id="e4d4d-584">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="e4d4d-585">當使用者 Jane 1.2 封鎖 ESRB 時，確認遊戲未在使用者 Toby 上啟動 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-585">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="e4d4d-586">以使用者 Jane 的形式登出使用者 Toby 及重新登入</span><span class="sxs-lookup"><span data-stu-id="e4d4d-586">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="e4d4d-587">如果之前有變更，請還原 ESRB 設定</span><span class="sxs-lookup"><span data-stu-id="e4d4d-587">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="e4d4d-588">如果沒有任何 ESRB 設定，請選取 [封鎖或允許特定遊戲]，然後依名稱選取遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-588">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="e4d4d-589">以 Jane 的形式登出，並以 Toby</span><span class="sxs-lookup"><span data-stu-id="e4d4d-589">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="e4d4d-590">確認使用者 Jane 1.2 封鎖了 EXE/名稱時，該遊戲未在使用者 Toby 上啟動 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-590">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="e4d4d-591">以 Jane 的形式登出 Toby 和上一頁</span><span class="sxs-lookup"><span data-stu-id="e4d4d-591">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="e4d4d-592">像 Jane 一樣，開啟使用者控制項-> 應用程式限制</span><span class="sxs-lookup"><span data-stu-id="e4d4d-592">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="e4d4d-593">按一下 [Toby 只能使用我允許的程式]，然後按一下 [確定] (即 [不允許 exe]) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-593">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="e4d4d-594">按一下 [全選] 方塊，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-594">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="e4d4d-595">前往使用者控制項 \| 遊戲控制，並允許使用 ESRB 分級的特定遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-595">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="e4d4d-596">以 Jane 的身份登入，並以 Toby 登入，然後嘗試播放遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-596">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="e4d4d-597">確認遊戲未被封鎖，而且 Toby 可以在 [允許沒有 exe] 設定為1.2 時播放 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-597">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="e4d4d-598">以使用者 Jane 的形式登出使用者 Toby 及重新登入</span><span class="sxs-lookup"><span data-stu-id="e4d4d-598">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="e4d4d-599">移至主控台中的 [家長監護]，並移除限制</span><span class="sxs-lookup"><span data-stu-id="e4d4d-599">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="e4d4d-600">確認這兩個使用者現在都可以玩遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-600">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="e4d4d-601">繼續進行 [自動化測試](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="e4d4d-601">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="e4d4d-602">5.8 自動化測試</span><span class="sxs-lookup"><span data-stu-id="e4d4d-602">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="e4d4d-603">確認在應用程式驗證器下執行時，遊戲未產生失敗-請參閱商標測試控管檔 \[ 4。2\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-603">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="e4d4d-604">確認遊戲可執行檔包含資訊清單-請參閱商標測試控管檔 \[ 2。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-604">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="e4d4d-605">確認遊戲可執行檔資訊清單並無 requestedexecutionlevel 為 "AsInvoker"-請參閱商標測試控管檔 \[ 2。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-605">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="e4d4d-606">繼續進行 [其他測試](#59-other-tests)</span><span class="sxs-lookup"><span data-stu-id="e4d4d-606">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="e4d4d-607">5.9 其他測試</span><span class="sxs-lookup"><span data-stu-id="e4d4d-607">5.9 Other Tests</span></span>

1.  <span data-ttu-id="e4d4d-608">確認遊戲可執行檔包含數位簽章 \[ 2。3\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-608">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="e4d4d-609">確認遊戲安裝程式在 Windows Vista 及/或 Windows 7 2.3 的64位版本上正常執行 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-609">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="e4d4d-610">在 Windows Vista 及/或 Windows 7 2.3 的64位版本上執行16位可執行檔時，請確認該遊戲未遇到錯誤 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-610">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="e4d4d-611">在測試時強制應用程式損毀，並確認遊戲顯示 Windows 錯誤報告正確，並收集損毀資料 \[ 4。3\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-611">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="e4d4d-612">確定正確的檔案摘要 \[ 4。3\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-612">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="e4d4d-613">按一下 [開始-> 電腦]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-613">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="e4d4d-614">流覽至遊戲目錄</span><span class="sxs-lookup"><span data-stu-id="e4d4d-614">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="e4d4d-615">在 [搜尋] 視窗中，輸入 \*.dll</span><span class="sxs-lookup"><span data-stu-id="e4d4d-615">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="e4d4d-616">針對每個檔案：以滑鼠右鍵按一下檔案，然後按一下 [屬性]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-616">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="e4d4d-617">在 Windows XP 中：按一下 [版本] 索引標籤。確認已正確填入 [產品名稱]、[公司名稱] 和 [檔案版本] 欄位。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-617">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="e4d4d-618">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-618">\[4.3\]</span></span>
        -   <span data-ttu-id="e4d4d-619">在 Windows Vista 和 Windows 7 中：按一下 [詳細資料] 索引標籤。確認 [產品名稱] 和 [檔案版本] 欄位已正確填入。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-619">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="e4d4d-620">在 Windows Vista 或 Windows 7 屬性頁面4.3 中看不到公司名稱 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-620">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="e4d4d-621">針對 .exe 檔案重複此檢查</span><span class="sxs-lookup"><span data-stu-id="e4d4d-621">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="e4d4d-622">啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-622">Launch the game.</span></span>

    1.  <span data-ttu-id="e4d4d-623">按 CTRL + ALT + DEL</span><span class="sxs-lookup"><span data-stu-id="e4d4d-623">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="e4d4d-624">按一下 [關機選項] 箭號</span><span class="sxs-lookup"><span data-stu-id="e4d4d-624">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="e4d4d-625">按一下 [重新開機]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-625">Click Restart</span></span>
    4.  <span data-ttu-id="e4d4d-626">驗證遊戲不會封鎖關機 \[ 3。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-626">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="e4d4d-627">繼續 [卸載](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="e4d4d-627">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="e4d4d-628">5.10 卸載</span><span class="sxs-lookup"><span data-stu-id="e4d4d-628">5.10 Uninstall</span></span>

-   <span data-ttu-id="e4d4d-629">確認遊戲卸載程式會移除所有已安裝、未轉散發的作業系統元件檔案，並清除所有設定 \[ 3。1\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-629">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="e4d4d-630">在 Windows Vista 或 Windows 7 中確認主控台是移除程式1.1 的唯一方法 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-630">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="e4d4d-631">測試控管注意事項</span><span class="sxs-lookup"><span data-stu-id="e4d4d-631">Test Tool Notes</span></span>

<span data-ttu-id="e4d4d-632">這些是上述測試需求中所列的每個測試控管的附注。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-632">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="e4d4d-633">6.1 Appverifier 4.0 (或更新版本) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-633">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="e4d4d-634">**測試案例：2.5、4。2**</span><span class="sxs-lookup"><span data-stu-id="e4d4d-634">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="e4d4d-635">有些應用程式無法執行，因為禁止複製的 AppVerifier 正在執行中。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-635">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="e4d4d-636">您可以使用遊戲可執行檔的未受保護髮行版來執行，以解決此問題。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-636">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="e4d4d-637">在執行 Windows XP 的電腦上安裝 AppVerifier 4.0 (或更高版本) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-637">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="e4d4d-638">啟動 AppVerifier，然後按一下 [檔案-> 新增應用程式]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-638">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="e4d4d-639">找出遊戲可執行檔、選取它，然後按一下 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-639">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="e4d4d-640">在 [應用程式] 區段中，選取 [遊戲可執行檔]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-640">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="e4d4d-641">在 [基本概念] 區段中，選取下列測試：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-641">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="e4d4d-642">處理</span><span class="sxs-lookup"><span data-stu-id="e4d4d-642">Handles</span></span>
    -   <span data-ttu-id="e4d4d-643">堆積</span><span class="sxs-lookup"><span data-stu-id="e4d4d-643">Heaps</span></span>
    -   <span data-ttu-id="e4d4d-644">鎖定</span><span class="sxs-lookup"><span data-stu-id="e4d4d-644">Locks</span></span>
    -   <span data-ttu-id="e4d4d-645">記憶體</span><span class="sxs-lookup"><span data-stu-id="e4d4d-645">Memory</span></span>
    -   <span data-ttu-id="e4d4d-646">TLS</span><span class="sxs-lookup"><span data-stu-id="e4d4d-646">TLS</span></span>

6.  <span data-ttu-id="e4d4d-647">在 [其他] 區段中，選取下列測試：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-647">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="e4d4d-648">DangerousAPIs</span><span class="sxs-lookup"><span data-stu-id="e4d4d-648">DangerousAPIs</span></span>
    -   <span data-ttu-id="e4d4d-649">DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="e4d4d-649">DirtyStacks</span></span>

7.  <span data-ttu-id="e4d4d-650">確定未選取所有其他測試</span><span class="sxs-lookup"><span data-stu-id="e4d4d-650">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="e4d4d-651">啟動遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-651">Launch the game</span></span>
9.  <span data-ttu-id="e4d4d-652">玩遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-652">Play the game</span></span>
10. <span data-ttu-id="e4d4d-653">關閉遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-653">Close the game</span></span>
11. <span data-ttu-id="e4d4d-654">在 AppVerifier 中選取 View-> 記錄</span><span class="sxs-lookup"><span data-stu-id="e4d4d-654">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="e4d4d-655">在 [應用程式] 區段中，選取應用程式 .exe 檔</span><span class="sxs-lookup"><span data-stu-id="e4d4d-655">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="e4d4d-656">在 [記錄檔] 區段中，選取記錄檔並觀察錯誤計數。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-656">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="e4d4d-657">如果沒有任何錯誤，請結束 AppVerifier 測試。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-657">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="e4d4d-658">如果發生錯誤，請按一下 [流覽] 按鈕</span><span class="sxs-lookup"><span data-stu-id="e4d4d-658">If there are errors, click the View button</span></span>
14. <span data-ttu-id="e4d4d-659">搜尋檔 (CTRL + F) 嚴重性 = "錯誤</span><span class="sxs-lookup"><span data-stu-id="e4d4d-659">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="e4d4d-660">根據失敗的 LayerName = 部分建立 bug</span><span class="sxs-lookup"><span data-stu-id="e4d4d-660">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="e4d4d-661">6.2 資訊清單測試-mt.exe</span><span class="sxs-lookup"><span data-stu-id="e4d4d-661">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="e4d4d-662">**測試案例：1.8、2。1**</span><span class="sxs-lookup"><span data-stu-id="e4d4d-662">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="e4d4d-663">此工具是從 MT.exe 所在的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-663">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="e4d4d-664">範例：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-664">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="e4d4d-665">按一下 [開始-> 執行-> 輸入 cmd，然後按一下 [確定] 按鈕</span><span class="sxs-lookup"><span data-stu-id="e4d4d-665">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="e4d4d-666">執行 mt.exe 工具，為隨遊戲安裝的每個 .exe 檔案產生資訊清單檔</span><span class="sxs-lookup"><span data-stu-id="e4d4d-666">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="e4d4d-667">開啟產生的資訊清單檔案</span><span class="sxs-lookup"><span data-stu-id="e4d4d-667">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="e4d4d-668">確定每個 .exe 檔案都包含下列所要求的 (：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-668">Ensure that each .exe file contains the following (requested:</span></span>

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> <span data-ttu-id="e4d4d-669">每個檔案都應該要有要求的執行層級，而且至少要有遊戲的可執行檔的 DPIAware。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-669">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="e4d4d-670">6.3 執行緒劫匪-threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="e4d4d-670">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="e4d4d-671">此工具是從 threadhijacker.exe 所在的命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-671">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="e4d4d-672">範例：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-672">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="e4d4d-673">其中 str 是program.exe 的 \_ 名稱 \_</span><span class="sxs-lookup"><span data-stu-id="e4d4d-673">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="e4d4d-674">顯示工作管理員，按一下 [處理常式] 索引標籤，然後找出遊戲可執行檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-674">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="e4d4d-675">以系統管理員模式開啟命令提示字元</span><span class="sxs-lookup"><span data-stu-id="e4d4d-675">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="e4d4d-676">流覽至 threadhijacker.exe 所在的目錄</span><span class="sxs-lookup"><span data-stu-id="e4d4d-676">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="e4d4d-677">Type： **threadhijacker.exe/process：** str，其中 str 是您想要叫用之可執行檔的名稱</span><span class="sxs-lookup"><span data-stu-id="e4d4d-677">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="e4d4d-678">6.4 Windows 測試控管的 Microsoft 遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-678">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="e4d4d-679">此工具位於 DirectX SDK 中。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-679">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="e4d4d-680">一旦 SDK 安裝在電腦上，就可以將 Windows 測試控管的安裝程式放置在測試電腦上，然後安裝。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-680">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="e4d4d-681">在安裝 DirectX SDK 的開發電腦上，找出適用于 Windows Test Tool 安裝程式的 Microsoft 遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-681">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="e4d4d-682">依預設，它位於下列位置：</span><span class="sxs-lookup"><span data-stu-id="e4d4d-682">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="e4d4d-683">將安裝程式 (MicrosoftGFWTestTool.msi/setup.exe) 複製到測試電腦。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-683">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="e4d4d-684">執行安裝程式。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-684">Run the installer.</span></span>
3.  <span data-ttu-id="e4d4d-685">啟動 Windows 測試控管的 Microsoft 遊戲。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-685">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="e4d4d-686">在 [ **專案清單** ] 欄位中，將 [ **建立新專案** ] 取代為您的標題名稱， **然後按一下 [新建]**。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-686">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="e4d4d-687">等候基準完成。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-687">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="e4d4d-688">在 [ **遊戲資訊** ] 區段中填寫任何您可能擁有的資訊，然後按一下 [ **更新遊戲資訊**]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-688">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="e4d4d-689">按一下 [ **測試案例** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-689">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="e4d4d-690">從頂端開始，繼續進行測試案例，適當地按一下 [ **通過** ] 或 [ **失敗** ]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-690">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="e4d4d-691">如需有關在報表中包含錯誤的詳細資訊，請參閱本節稍後的「撰寫 Bug」。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-691">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="e4d4d-692">核取 [**報表**] 和 [ **Bug 編輯**] 索引標籤，以在查看報表 (之後返回 [**專案**] 索引標籤) 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-692">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="e4d4d-693">按一下 [ **編譯報告**]。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-693">Click **Compile Report**.</span></span>

    <span data-ttu-id="e4d4d-694">當報表完成編譯時，就會開啟一個視窗。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-694">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="e4d4d-695">您會在這裡找到 .ZIP *的檔案名report.zip 的名稱* \_ 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-695">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="e4d4d-696">此檔案包含在測試階段期間收集的所有記錄和結果。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-696">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="e4d4d-697">撰寫 Bug</span><span class="sxs-lookup"><span data-stu-id="e4d4d-697">Writing a Bug</span></span>

<span data-ttu-id="e4d4d-698">有兩種方式可以撰寫 bug 報告：您可以完成測試案例，然後按一下 [當標題無法測試案例時 **失敗** ]，或者按一下 [ **bug 編輯** ] 索引標籤並手動加入 bug 報表。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-698">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="e4d4d-699">在測試案例上按一下 [失敗]</span><span class="sxs-lookup"><span data-stu-id="e4d4d-699">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="e4d4d-700">當您按一下測試案例的 [ **失敗** ] 時，[ **問題類型** ] 下拉式清單會自動設定為測試案例類型。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-700">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="e4d4d-701">將簡短描述新增至簡要描述問題的 [ **標題** ] 欄位。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-701">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="e4d4d-702">將問題的詳細描述新增至 [觀察到的 **行為** ] 欄位。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-702">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="e4d4d-703">視需要新增預期的 (，而不是 [ **預期行為** ] 欄位) 問題的描述。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-703">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="e4d4d-704">新增如何重現問題至 **重現步驟** 欄位的詳細描述。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-704">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="e4d4d-705">完成時，按一下 [ **儲存** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-705">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="e4d4d-706">手動新增 Bug</span><span class="sxs-lookup"><span data-stu-id="e4d4d-706">Manually Adding a Bug</span></span>

<span data-ttu-id="e4d4d-707">此程式與按一下 [ **失敗**] 相同，但自動填入的下拉式清單除外。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-707">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="e4d4d-708">在此情況下，請選取適當的 TCR 失敗類型，或針對落在 TR 範圍之外但仍應回報的 bug 選取 **\* \* 非 TR 問題 \* \*** 。</span><span class="sxs-lookup"><span data-stu-id="e4d4d-708">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="e4d4d-709">資源</span><span class="sxs-lookup"><span data-stu-id="e4d4d-709">Resources</span></span>

<dl> <dt>

<span data-ttu-id="e4d4d-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>適用于 Windows 的遊戲：技術需求</span><span class="sxs-lookup"><span data-stu-id="e4d4d-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="e4d4d-711">Windows 技術需求的遊戲： Windows XP、Windows Vista 和 Windows 7 遊戲的最佳作法</span><span class="sxs-lookup"><span data-stu-id="e4d4d-711">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="e4d4d-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e4d4d-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="e4d4d-713">Windows Sdk</span><span class="sxs-lookup"><span data-stu-id="e4d4d-713">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="e4d4d-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>使用者帳戶控制指導方針</span><span class="sxs-lookup"><span data-stu-id="e4d4d-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-715">[使用者帳戶控制相容性的 Windows Vista 應用程式開發需求](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e4d4d-715">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="e4d4d-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer 資訊</span><span class="sxs-lookup"><span data-stu-id="e4d4d-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="e4d4d-717">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e4d4d-717">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="e4d4d-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual 開發人員入口網站</span><span class="sxs-lookup"><span data-stu-id="e4d4d-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="e4d4d-719">Windows Quality Online Services (Winqual) </span><span class="sxs-lookup"><span data-stu-id="e4d4d-719">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="e4d4d-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX 開發人員入口網站</span><span class="sxs-lookup"><span data-stu-id="e4d4d-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="e4d4d-721">[DirectX 開發人員中心](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="e4d4d-721">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="e4d4d-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Windows 和 DirectX SDK Blog 的遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="e4d4d-723">適用於 Windows 與 DirectX SDK 的遊戲</span><span class="sxs-lookup"><span data-stu-id="e4d4d-723">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="e4d4d-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>其他 DirectX 文章</span><span class="sxs-lookup"><span data-stu-id="e4d4d-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="e4d4d-725">DirectX 技術文章</span><span class="sxs-lookup"><span data-stu-id="e4d4d-725">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

