---
description: 本主題說明如何建立新的檔案類型，以及如何將應用程式與您的檔案類型和其他妥善定義的檔案類型產生關聯。
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: 檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973244"
---
# <a name="file-types"></a><span data-ttu-id="a492b-103">檔案類型</span><span class="sxs-lookup"><span data-stu-id="a492b-103">File Types</span></span>

<span data-ttu-id="a492b-104">本主題說明如何建立新的檔案類型，以及如何將應用程式與您的檔案類型和其他妥善定義的檔案類型產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a492b-104">This topic explains how to create new file types and how to associate your app with your file type and other well-defined file types.</span></span> <span data-ttu-id="a492b-105">共用通用副檔名的檔案 ( .doc、.html 等) 屬於相同的 *類型*。</span><span class="sxs-lookup"><span data-stu-id="a492b-105">Files with a shared common file name extension (.doc, .html, and so on) are of the same *type*.</span></span> <span data-ttu-id="a492b-106">例如，如果您建立新的文字編輯器，則可以使用現有的 .txt 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="a492b-106">For example, if you create a new text editor, then you can use the existing .txt file type.</span></span> <span data-ttu-id="a492b-107">在其他情況下，您可能需要建立新的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="a492b-107">In other cases, you might need to create a new file type.</span></span>

<span data-ttu-id="a492b-108">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="a492b-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a492b-109">公用和私用檔案類型</span><span class="sxs-lookup"><span data-stu-id="a492b-109">Public and Private File Types</span></span>](#public-and-private-file-types)
-   [<span data-ttu-id="a492b-110">註冊檔案類型</span><span class="sxs-lookup"><span data-stu-id="a492b-110">Registering a File Type</span></span>](#registering-a-file-type)
    -   [<span data-ttu-id="a492b-111">設定選擇性的子機碼和檔案類型延伸模組屬性</span><span class="sxs-lookup"><span data-stu-id="a492b-111">Setting Optional Subkeys and File Type Extension Attributes</span></span>](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [<span data-ttu-id="a492b-112">卸載期間刪除登錄資訊</span><span class="sxs-lookup"><span data-stu-id="a492b-112">Deleting Registry Information During Uninstallation</span></span>](#deleting-registry-information-during-uninstallation)
-   [<span data-ttu-id="a492b-113">支援開放中繼資料的檔案類型</span><span class="sxs-lookup"><span data-stu-id="a492b-113">File Types That Support Open Metadata</span></span>](#file-types-that-support-open-metadata)
-   [<span data-ttu-id="a492b-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="a492b-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="a492b-115">您可以在下列主題中找到其他資訊：</span><span class="sxs-lookup"><span data-stu-id="a492b-115">Additional information can be found on the following topics:</span></span>

-   [<span data-ttu-id="a492b-116">如何選擇檔案類型延伸模組</span><span class="sxs-lookup"><span data-stu-id="a492b-116">How To Choose a File Type Extension</span></span>](how-to-choose-a-file-type-extension.md)
-   [<span data-ttu-id="a492b-117">如何定義檔案類型屬性</span><span class="sxs-lookup"><span data-stu-id="a492b-117">How To Define File Type Attributes</span></span>](./how-to-define-file-type-attributes.md)
-   <span data-ttu-id="a492b-118">[如何在 [開啟檔案] 對話方塊中加入應用程式](how-to-include-an-application-on-the-open-with-dialog-box.md)</span><span class="sxs-lookup"><span data-stu-id="a492b-118">[How To Include an Application on the Open with Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md)</span></span>
-   [<span data-ttu-id="a492b-119">如何從非關聯檔案類型的開啟檔案對話方塊中排除應用程式</span><span class="sxs-lookup"><span data-stu-id="a492b-119">How To Exclude an Application from the Open with Dialog Box for Unassociated File Types</span></span>](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a><span data-ttu-id="a492b-120">公用和私用檔案類型</span><span class="sxs-lookup"><span data-stu-id="a492b-120">Public and Private File Types</span></span>

<span data-ttu-id="a492b-121">公用檔案類型也稱為熱門或之間爭論類型，因為競爭應用程式可能會想要與這些檔案類型相關聯。</span><span class="sxs-lookup"><span data-stu-id="a492b-121">Public file types are also known as popular or contentious types because competing applications might want to be associated with these file types.</span></span> <span data-ttu-id="a492b-122">公用檔案類型的特性包括：</span><span class="sxs-lookup"><span data-stu-id="a492b-122">Characteristics of public file types include:</span></span>

-   <span data-ttu-id="a492b-123">它們通常是由標準主體所定義，而且/或由其定義組織作為交換格式來升級。</span><span class="sxs-lookup"><span data-stu-id="a492b-123">They are typically defined by standards bodies, and/or are promoted by their defining organizations as interchange formats.</span></span>
-   <span data-ttu-id="a492b-124">它們通常會在電腦和使用者之間進行不同用途的交換。</span><span class="sxs-lookup"><span data-stu-id="a492b-124">They are often exchanged between computers and users for diverse purposes.</span></span>
-   <span data-ttu-id="a492b-125">它們必須在許多不同的平臺上受到支援。</span><span class="sxs-lookup"><span data-stu-id="a492b-125">They need to be supported on many different platforms.</span></span>
-   <span data-ttu-id="a492b-126">來自多個廠商的應用程式很可能會處理它們。</span><span class="sxs-lookup"><span data-stu-id="a492b-126">Applications from multiple vendors are likely to handle them.</span></span>

<span data-ttu-id="a492b-127">以下是一些被視為公用的檔案類型範例：圖像檔案類型 .png、.gif、.jpg 和 .bmp，以及音訊類型 .wav、mp3 和 au。</span><span class="sxs-lookup"><span data-stu-id="a492b-127">Some examples of file types that are considered public are the image file types .png, .gif, .jpg, and .bmp, and the audio types .wav, .mp3, and .au.</span></span>

<span data-ttu-id="a492b-128">與公用檔案類型不同的是，私用或專屬檔案類型的格式通常只有一個應用程式或廠商可執行和瞭解。</span><span class="sxs-lookup"><span data-stu-id="a492b-128">Unlike public file types, private or proprietary file types typically have a format that is implemented and understood by only one application or vendor.</span></span> <span data-ttu-id="a492b-129">因此，私用檔案類型通常不容易發生應用程式之間的衝突。</span><span class="sxs-lookup"><span data-stu-id="a492b-129">As a result, private file types are typically not prone to conflicts between applications.</span></span> <span data-ttu-id="a492b-130">某些檔案類型可以啟動為私用檔案類型，但之後會變成公用檔案類型。</span><span class="sxs-lookup"><span data-stu-id="a492b-130">Some file types can start as private file types but later become public file types.</span></span>

> [!Note]  
> <span data-ttu-id="a492b-131">Windows 不會區分公用和私用檔案類型。</span><span class="sxs-lookup"><span data-stu-id="a492b-131">Windows does not differentiate between public and private file types.</span></span> <span data-ttu-id="a492b-132">差別僅與決定您選擇的檔案類型註冊有關。</span><span class="sxs-lookup"><span data-stu-id="a492b-132">The distinction is relevant only in making decisions about your choice of file type registration.</span></span>

 

## <a name="registering-a-file-type"></a><span data-ttu-id="a492b-133">註冊檔案類型</span><span class="sxs-lookup"><span data-stu-id="a492b-133">Registering a File Type</span></span>

<span data-ttu-id="a492b-134">若要將檔案類型與現有的應用程式產生關聯，請在登錄中找出應用程式 ProgID。</span><span class="sxs-lookup"><span data-stu-id="a492b-134">To associate the file type with an existing application, locate the application ProgID in the registry.</span></span> <span data-ttu-id="a492b-135">若要將檔案類型與新的應用程式產生關聯，請定義應用程式的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="a492b-135">To associate the file type with a new application, define a ProgID for your application.</span></span> <span data-ttu-id="a492b-136">如需定義新 ProgID 的詳細資訊，請參閱程式 [設計識別碼](fa-progids.md)。</span><span class="sxs-lookup"><span data-stu-id="a492b-136">For information about defining a new ProgID, see [Programmatic Identifiers](fa-progids.md).</span></span>

<span data-ttu-id="a492b-137">檔案名延伸子機碼具有下列一般格式：*延伸* = *ProgID*。</span><span class="sxs-lookup"><span data-stu-id="a492b-137">File name extension subkeys have the following general form: *extension*=*ProgID*.</span></span> <span data-ttu-id="a492b-138">副檔名子機碼會儲存在 **HKEY \_ 類別 \_ 根** 子樹中。</span><span class="sxs-lookup"><span data-stu-id="a492b-138">File name extension subkeys are stored in the **HKEY\_CLASSES\_ROOT** subtree.</span></span>

<span data-ttu-id="a492b-139">在登錄中建立檔案類型的子機碼時，請務必包含前置期間 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="a492b-139">It is important to include the leading period (.) when creating file type subkeys in the registry.</span></span> <span data-ttu-id="a492b-140">例如，如果您想要使用名為 Myprogram.exe 的應用程式開啟副檔名為 myp 的檔案類型和長副檔名. myp 檔案，請使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="a492b-140">For example, if you want a file type with the short extension .myp and the long extension .myp-file to be opened with an application called MyProgram, use the following syntax:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

<span data-ttu-id="a492b-141">如上一個範例所示，如果您也 ( 登錄簡短的副檔名) ，您也應該為完整的延伸模組建立子機碼 (. myp-file) 。</span><span class="sxs-lookup"><span data-stu-id="a492b-141">As demonstrated in the preceding example, if you also register a short file name extension (.myp), you should create a subkey for the long extension (.myp-file) as well.</span></span> <span data-ttu-id="a492b-142">如需詳細資訊，請參閱 [檔案類型處理常式](fa-file-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="a492b-142">For more information, see [File Type Handlers](fa-file-extensions.md).</span></span>

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a><span data-ttu-id="a492b-143">設定選擇性的子機碼和檔案類型延伸模組屬性</span><span class="sxs-lookup"><span data-stu-id="a492b-143">Setting Optional Subkeys and File Type Extension Attributes</span></span>

<span data-ttu-id="a492b-144">登錄中的檔案類型延伸模組專案有數個選擇性的子機碼和屬性。</span><span class="sxs-lookup"><span data-stu-id="a492b-144">File type extension entries in the registry have several optional subkeys and attributes.</span></span>

<span data-ttu-id="a492b-145">下表說明檔案關聯所使用的檔案類型延伸模組專案。</span><span class="sxs-lookup"><span data-stu-id="a492b-145">The file type extension entries that are used by file associations are described in the following table.</span></span> <span data-ttu-id="a492b-146">所有值都是 **REG \_ SZ** 型別。</span><span class="sxs-lookup"><span data-stu-id="a492b-146">All values are of the **REG\_SZ** type.</span></span>



| <span data-ttu-id="a492b-147">登錄項目</span><span class="sxs-lookup"><span data-stu-id="a492b-147">Registry entry</span></span>  | <span data-ttu-id="a492b-148">動作</span><span class="sxs-lookup"><span data-stu-id="a492b-148">Action</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a492b-149">預設</span><span class="sxs-lookup"><span data-stu-id="a492b-149">Default</span></span>         | <span data-ttu-id="a492b-150">將擴充子機碼的預設值設定為其所連結的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="a492b-150">Set the default value of the extension subkey to the ProgID to which it is linked.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a492b-151">內容類型</span><span class="sxs-lookup"><span data-stu-id="a492b-151">Content Type</span></span>    | <span data-ttu-id="a492b-152">將內容類型值設定為檔案類型的 MIME 內容類型。</span><span class="sxs-lookup"><span data-stu-id="a492b-152">Set the Content Type value to the file type's MIME content type.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a492b-153">OpenWithList</span><span class="sxs-lookup"><span data-stu-id="a492b-153">OpenWithList</span></span>    | <span data-ttu-id="a492b-154">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="a492b-154">Do not use.</span></span> <span data-ttu-id="a492b-155">這個子機碼包含應用程式的一或多個應用程式子機碼，而這些應用程式會出現在檔案類型的 [ **開啟檔案** ] 對話方塊專案中，而且只適用于 Windows XP 之前作業系統上的 .exe 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a492b-155">This subkey contains one or more application subkeys for applications that appear in the **Open with** dialog box entry for the file type and is intended only for .exe applications on operating systems prior to Windows XP.</span></span> <span data-ttu-id="a492b-156">請改用 OpenWithProgIds。</span><span class="sxs-lookup"><span data-stu-id="a492b-156">Use OpenWithProgIds instead.</span></span>                                                            |
| <span data-ttu-id="a492b-157">OpenWithProgIds</span><span class="sxs-lookup"><span data-stu-id="a492b-157">OpenWithProgIds</span></span> | <span data-ttu-id="a492b-158">此子機碼包含這個檔案類型的替代 Progid 清單。</span><span class="sxs-lookup"><span data-stu-id="a492b-158">This subkey contains a list of alternate ProgIDs for this file type.</span></span> <span data-ttu-id="a492b-159">這些 Progid 的程式會顯示在 [ **開啟檔案** ] 功能表中，並可作為檔案類型的預設 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a492b-159">The programs for these ProgIDs appear in the **Open with** menu and are available as default Windows Store apps for the file type.</span></span> <span data-ttu-id="a492b-160">每當應用程式藉由變更預設值來接管此檔案類型時，也應該在此清單中新增一個專案。</span><span class="sxs-lookup"><span data-stu-id="a492b-160">Whenever an application takes over this file type by changing the default value, it should also add an entry to this list.</span></span> |
| <span data-ttu-id="a492b-161">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="a492b-161">PerceivedType</span></span>   | <span data-ttu-id="a492b-162">將 PerceivedType 值設定為檔案所屬的 PerceivedType （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a492b-162">Set the PerceivedType value to the PerceivedType to which the file belongs, if any.</span></span> <span data-ttu-id="a492b-163">Windows Vista 之前的 Windows 版本不會使用這個字串。</span><span class="sxs-lookup"><span data-stu-id="a492b-163">This string is not used by Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="a492b-164">如需詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="a492b-164">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>                                                                           |



 

<span data-ttu-id="a492b-165">副檔名的一般格式如下所示。</span><span class="sxs-lookup"><span data-stu-id="a492b-165">The general form of a file name extension subkey is as follows.</span></span> <span data-ttu-id="a492b-166">所有專案類型都是 **REG \_ SZ** 型別。</span><span class="sxs-lookup"><span data-stu-id="a492b-166">All entry types are of the **REG\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

<span data-ttu-id="a492b-167">有關檔案類型的重要考慮包括：</span><span class="sxs-lookup"><span data-stu-id="a492b-167">Important considerations about file types include:</span></span>

-   <span data-ttu-id="a492b-168">**HKEY \_ 類別 \_ 根** 子樹是藉由合併 HKEY 的 **\_ 目前 \_ 使用者** \\ **軟體** \\ **類別** 和 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別** 所形成的視圖</span><span class="sxs-lookup"><span data-stu-id="a492b-168">The **HKEY\_CLASSES\_ROOT** subtree is a view formed by merging **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** and **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes**</span></span>
-   <span data-ttu-id="a492b-169">一般情況下， **HKEY \_ 類別 \_ 根目錄** 的目的是要讀取，但不是寫入。</span><span class="sxs-lookup"><span data-stu-id="a492b-169">In general, **HKEY\_CLASSES\_ROOT** is intended to be read from but not written to.</span></span> <span data-ttu-id="a492b-170">如需詳細資訊，請參閱 [HKEY \_ 類別的 \_ 根](../sysinfo/hkey-classes-root-key.md) 文章。</span><span class="sxs-lookup"><span data-stu-id="a492b-170">For more information, see the [HKEY\_CLASSES\_ROOT](../sysinfo/hkey-classes-root-key.md) article.</span></span>
-   <span data-ttu-id="a492b-171">若要在特定電腦上全域註冊檔案類型，請在 [ **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別**] 子機碼中建立檔案類型的專案。</span><span class="sxs-lookup"><span data-stu-id="a492b-171">To register a file type globally on a particular computer, create an entry for the file type in the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="a492b-172">若要讓目前的使用者可以看到檔案類型註冊，請在 [ **HKEY \_ 目前 \_ 使用者** \\ **軟體** \\ **類別**] 子機碼中建立檔案類型的專案。</span><span class="sxs-lookup"><span data-stu-id="a492b-172">To make a file type registration visible to the current user only, create an entry for the file type in the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="a492b-173">應用程式可以提供自己的動詞命令，例如開啟或播放，如下列登錄範例所示。</span><span class="sxs-lookup"><span data-stu-id="a492b-173">An application can provide its own implementation of a verb, such as open or play, as shown in the following registry example.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    <span data-ttu-id="a492b-174">動詞子機碼的子機碼包含命令列和 drop target 方法： **command** 和 **DropTarget**。</span><span class="sxs-lookup"><span data-stu-id="a492b-174">Subkeys of the verb subkey include the command line and the drop target method: **command** and **DropTarget**.</span></span>

-   <span data-ttu-id="a492b-175">當您建立或變更檔案關聯時，請務必通知系統您已進行變更。</span><span class="sxs-lookup"><span data-stu-id="a492b-175">When you create or change a file association, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="a492b-176">若要這麼做，請呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 並指定 **SHCNE \_ ASSOCCHANGED** 事件。</span><span class="sxs-lookup"><span data-stu-id="a492b-176">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) and specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="a492b-177">如果您未呼叫 **SHChangeNotify**，則在重新開機系統之前，可能無法辨識變更。</span><span class="sxs-lookup"><span data-stu-id="a492b-177">If you do not call **SHChangeNotify**, the change may not be recognized until after the system is rebooted.</span></span>
-   <span data-ttu-id="a492b-178">若要取得有關檔案關聯的登錄資訊，請使用 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 介面。</span><span class="sxs-lookup"><span data-stu-id="a492b-178">To retrieve registry information regarding a file association, use the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface.</span></span> <span data-ttu-id="a492b-179">如需示範此程式的案例，請參閱檔案 [關聯範例案例](fa-sample-scenarios.md)。</span><span class="sxs-lookup"><span data-stu-id="a492b-179">For a scenario that illustrates this procedure, see [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

> [!Note]  
> <span data-ttu-id="a492b-180">應用程式 **路徑** 和 **應用程式** 登錄子機碼都是用來代表應用程式註冊和控制系統的行為。</span><span class="sxs-lookup"><span data-stu-id="a492b-180">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="a492b-181">如需此功能的詳細資訊，請參閱 [應用程式註冊](app-registration.md)。</span><span class="sxs-lookup"><span data-stu-id="a492b-181">For more detailed information about this functionality, see [Application Registration](app-registration.md).</span></span>

 

### <a name="deleting-registry-information-during-uninstallation"></a><span data-ttu-id="a492b-182">卸載期間刪除登錄資訊</span><span class="sxs-lookup"><span data-stu-id="a492b-182">Deleting Registry Information During Uninstallation</span></span>

<span data-ttu-id="a492b-183">卸載應用程式時，與該應用程式相關聯的 Progid 和其他大部分的登錄資訊都應該在卸載過程中刪除。</span><span class="sxs-lookup"><span data-stu-id="a492b-183">When uninstalling an application, the ProgIDs and most other registry information associated with that application should be deleted as part of the uninstallation.</span></span> <span data-ttu-id="a492b-184">不過，已取得檔 (類型擁有權的應用程式，會將檔案類型的 **HKEY \_ 類別 \_ 根目錄** 的預設值設定 \\ 為應用程式) 的 ProgID，所以不應該嘗試在卸載時移除該值。</span><span class="sxs-lookup"><span data-stu-id="a492b-184">However, applications that have taken ownership of a file type (by setting the Default value of the file type's **HKEY\_CLASSES\_ROOT**\\ *.extension* subkey to the ProgID of the application) should not attempt to remove that value when uninstalling.</span></span> <span data-ttu-id="a492b-185">將資料保留為預設值，可避免判斷其他應用程式是否已取得檔案類型的擁有權，並在安裝原始應用程式之後覆寫預設值的困難。</span><span class="sxs-lookup"><span data-stu-id="a492b-185">Leaving the data in place for the Default value avoids the difficulty of determining whether another application has taken ownership of the file type and overwritten the Default value after the original application was installed.</span></span> <span data-ttu-id="a492b-186">只有當 ProgID 找到已註冊的 ProgID 時，Windows 才會遵循預設值。</span><span class="sxs-lookup"><span data-stu-id="a492b-186">Windows respects the Default value only if the ProgID found there is a registered ProgID.</span></span> <span data-ttu-id="a492b-187">如果 ProgID 已取消註冊，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="a492b-187">If the ProgID is unregistered, it is ignored.</span></span>

<span data-ttu-id="a492b-188">請注意，其他的檔案類型擁有權資訊會儲存在 [ **HKEY \_ 目前 \_ 使用者**] 子樹中，而且只有在註冊它所參考的應用程式時才會使用。</span><span class="sxs-lookup"><span data-stu-id="a492b-188">Note that other file-type ownership information is stored in the **HKEY\_CURRENT\_USER** subtree and also is used only when the application that it references is registered.</span></span> <span data-ttu-id="a492b-189">因此，在卸載應用程式時，不需要移除這種資料。</span><span class="sxs-lookup"><span data-stu-id="a492b-189">Therefore, this data does not need to be removed when uninstalling an application.</span></span>

<span data-ttu-id="a492b-190">例如，以下顯示在卸載應用程式之前的登錄狀態：</span><span class="sxs-lookup"><span data-stu-id="a492b-190">As an example, the following shows the state of the registry before an application is uninstalled:</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

<span data-ttu-id="a492b-191">以下顯示在卸載應用程式之後，這些登錄專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="a492b-191">The following shows the state of those same registry entries after the application has been uninstalled.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a><span data-ttu-id="a492b-192">支援開放中繼資料的檔案類型</span><span class="sxs-lookup"><span data-stu-id="a492b-192">File Types That Support Open Metadata</span></span>

<span data-ttu-id="a492b-193">在 Windows 7 和更新版本中，下列檔案類型支援開放中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a492b-193">In Windows 7 and later, the following file types support open metadata.</span></span>



| <span data-ttu-id="a492b-194">檔案類型</span><span class="sxs-lookup"><span data-stu-id="a492b-194">File type</span></span>                                                               | <span data-ttu-id="a492b-195">副檔名</span><span class="sxs-lookup"><span data-stu-id="a492b-195">File name extensions</span></span>                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a492b-196">Office 2007 檔</span><span class="sxs-lookup"><span data-stu-id="a492b-196">Office 2007 Documents</span></span>                                                   | <span data-ttu-id="a492b-197">.docx、.xlsx、.pptx</span><span class="sxs-lookup"><span data-stu-id="a492b-197">.docx, .xlsx, .pptx</span></span>                                           |
| <span data-ttu-id="a492b-198">Office 97-2003 檔</span><span class="sxs-lookup"><span data-stu-id="a492b-198">Office 97-2003 Documents</span></span>                                                | <span data-ttu-id="a492b-199">.doc、.xls、.ppt</span><span class="sxs-lookup"><span data-stu-id="a492b-199">.doc, .xls, .ppt</span></span>                                              |
| <span data-ttu-id="a492b-200">已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="a492b-200">Saved Search</span></span>                                                            | <span data-ttu-id="a492b-201">。搜尋-ms</span><span class="sxs-lookup"><span data-stu-id="a492b-201">.search-ms</span></span>                                                    |
| <span data-ttu-id="a492b-202">Windows Media 格式 (Advanced 串流格式 (ASF) 容器) </span><span class="sxs-lookup"><span data-stu-id="a492b-202">Windows Media-based formats (Advanced Streaming Format (ASF) container)</span></span> | <span data-ttu-id="a492b-203">.wmv、.wma</span><span class="sxs-lookup"><span data-stu-id="a492b-203">.wmv, .wma</span></span>                                                    |
| <span data-ttu-id="a492b-204"> (的屬性處理常式) </span><span class="sxs-lookup"><span data-stu-id="a492b-204">MP4 (property handler)</span></span>                                                  | <span data-ttu-id="a492b-205">m4a、. m4v、. mp4v、m4p、m4b、3gp、3gpp、.3gp2、mov</span><span class="sxs-lookup"><span data-stu-id="a492b-205">.mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a492b-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="a492b-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a492b-207">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="a492b-207">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="a492b-208">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="a492b-208">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="a492b-209">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="a492b-209">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="a492b-210">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="a492b-210">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="a492b-211">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="a492b-211">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="a492b-212">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="a492b-212">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="a492b-213">認知類型</span><span class="sxs-lookup"><span data-stu-id="a492b-213">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="a492b-214">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="a492b-214">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
