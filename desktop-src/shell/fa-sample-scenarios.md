---
description: 在下列範例中，假設軟體發展公司稱為 Litware，Inc.。
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: 檔案關聯範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111752"
---
# <a name="file-association-example"></a><span data-ttu-id="244a7-103">檔案關聯範例</span><span class="sxs-lookup"><span data-stu-id="244a7-103">File Association Example</span></span>

<span data-ttu-id="244a7-104">在下列範例中，名為 Litware，Inc. 的假想軟體發展公司會建立名為 LitwarePlayer 的新音訊播放機。</span><span class="sxs-lookup"><span data-stu-id="244a7-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="244a7-105">Litware 想要設計 LitwarePlayer 與其主要檔案類型之間的檔案關聯，其使用新開發的音訊格式，可讓整個音訊 CD 儲存在 10 kb 以內的記憶體中，且不會失去品質。</span><span class="sxs-lookup"><span data-stu-id="244a7-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="244a7-106">本主題不適用於 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="244a7-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="244a7-107">預設檔案關聯在 Windows 10 中的運作方式有所變更。</span><span class="sxs-lookup"><span data-stu-id="244a7-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="244a7-108">如需詳細資訊，請參閱 [這篇文章](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)中有關 **Windows 10 如何處理預設應用程式的變更** 一節。</span><span class="sxs-lookup"><span data-stu-id="244a7-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="244a7-109">設計新的檔案關聯</span><span class="sxs-lookup"><span data-stu-id="244a7-109">Designing a New File Association</span></span>

<span data-ttu-id="244a7-110">公司應採取下列步驟。</span><span class="sxs-lookup"><span data-stu-id="244a7-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="244a7-111">**決定是否應將新的檔案類型視為公用或私用。**</span><span class="sxs-lookup"><span data-stu-id="244a7-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="244a7-112">這個新的檔案類型是媒體類型。</span><span class="sxs-lookup"><span data-stu-id="244a7-112">This new file type is a media type.</span></span> <span data-ttu-id="244a7-113">由於使用者會跨各種平臺交換媒體檔案，而且可能會有其他需要讀取 LitwarePlayer 格式的應用程式，因此， [公用](fa-file-types.md) 檔案類型是最適當的。</span><span class="sxs-lookup"><span data-stu-id="244a7-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="244a7-114">**判斷是否已定義此檔案類型。**</span><span class="sxs-lookup"><span data-stu-id="244a7-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="244a7-115">檢查網際網路指派的號碼授權單位 (IANA) MIME 資料庫，以及網際網路上的其他公用檔案類型資料庫，判斷沒有定義任何可比較的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="244a7-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="244a7-116">因為這是新的檔案格式，所以您需要定義新的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="244a7-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="244a7-117">**定義新檔案類型的副檔名。**</span><span class="sxs-lookup"><span data-stu-id="244a7-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="244a7-118">開發人員會選擇 `.opa-ltw-audio` ，其中包含其廠商縮寫，以及檔案所包含內容的提示。</span><span class="sxs-lookup"><span data-stu-id="244a7-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="244a7-119">研究判斷此延伸模組未由其他人使用。</span><span class="sxs-lookup"><span data-stu-id="244a7-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="244a7-120">遵循目前的建議，未定義任何簡短的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="244a7-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="244a7-121">**為檔案類型定義 MIME 類型，並向 IANA 註冊。**</span><span class="sxs-lookup"><span data-stu-id="244a7-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="244a7-122">Litware 會將新的 MIME 類型定義為 *音訊/LitwarePlayer* ，並準備 MIME 類型應用程式，並遵循 (RFC) 號碼2045、2046、2047和2048提出的指導方針。</span><span class="sxs-lookup"><span data-stu-id="244a7-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="244a7-123">然後，他們會將應用程式提交至 IANA，以將新的檔案類型新增至已註冊之 MIME 類型的資料庫。</span><span class="sxs-lookup"><span data-stu-id="244a7-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="244a7-124">**判斷檔案類型是否存在 ProgID。**</span><span class="sxs-lookup"><span data-stu-id="244a7-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="244a7-125">因為這是新的檔案類型，所以不會有 [ProgID](fa-progids.md) 。</span><span class="sxs-lookup"><span data-stu-id="244a7-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="244a7-126">針對 LitwarePlayer 設計新 ProgID 的 Litware 集。</span><span class="sxs-lookup"><span data-stu-id="244a7-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="244a7-127">他們會決定易記名稱 "LitwarePlayer Audio Player" (儲存為 LitwarePlayer.exe 檔案) 中的資源，並針對與 LitwarePlayer 相關聯的檔案設計要使用的預設圖示 (也儲存在 LitwarePlayer.exe) 中。</span><span class="sxs-lookup"><span data-stu-id="244a7-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="244a7-128">因為 LitwarePlayer 是新的應用程式，所以這是第1版的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="244a7-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="244a7-129">**註冊 ProgID。**</span><span class="sxs-lookup"><span data-stu-id="244a7-129">**Register the ProgID.**</span></span> <span data-ttu-id="244a7-130">安裝 LitwarePlayer 時，安裝程式會在登錄中建立下列 [ProgID](fa-progids.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="244a7-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    <span data-ttu-id="244a7-131">在命令索引鍵中，會將 %1 傳遞為要播放之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="244a7-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="244a7-132">**註冊檔案類型的副檔名。**</span><span class="sxs-lookup"><span data-stu-id="244a7-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="244a7-133">當安裝 LitwarePlayer 時，安裝程式會在登錄中為其自訂檔案類型延伸建立下列專案。</span><span class="sxs-lookup"><span data-stu-id="244a7-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="244a7-134">每當建立或變更檔案關聯時，就會藉由呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)來指定 SHCNE ASSOCCHANGED 事件，以通知系統已進行變更 \_ 。</span><span class="sxs-lookup"><span data-stu-id="244a7-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="244a7-135">如果未這麼做，Shell 可能無法辨識在系統重新開機之前所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="244a7-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="244a7-136">其他資源</span><span class="sxs-lookup"><span data-stu-id="244a7-136">Additional Resources</span></span>

-   [<span data-ttu-id="244a7-137">檔案關聯簡介</span><span class="sxs-lookup"><span data-stu-id="244a7-137">Introduction to File Associations</span></span>](fa-intro.md)
-   <span data-ttu-id="244a7-138">[如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式](start-menu-reg.md)</span><span class="sxs-lookup"><span data-stu-id="244a7-138">[How to Register an Internet Browser or Email Client With the Windows Start Menu](start-menu-reg.md)</span></span>
-   <span data-ttu-id="244a7-139">[將應用程式註冊至 URI 配置](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="244a7-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="244a7-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="244a7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="244a7-141">檔案關聯的最佳作法</span><span class="sxs-lookup"><span data-stu-id="244a7-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="244a7-142">在 Windows Vista 和更新版本中管理預設應用程式的指導方針</span><span class="sxs-lookup"><span data-stu-id="244a7-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="244a7-143">預設程式</span><span class="sxs-lookup"><span data-stu-id="244a7-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="244a7-144"> (SPAD) 設定程式存取和電腦預設值 </span><span class="sxs-lookup"><span data-stu-id="244a7-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
