---
description: 描述在登錄中執行裝置事件處理常式的進程。
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: 如何註冊裝置事件的處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849191"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a><span data-ttu-id="09396-103">如何註冊裝置事件的處理常式</span><span class="sxs-lookup"><span data-stu-id="09396-103">How to Register a Handler for a Device Event</span></span>

<span data-ttu-id="09396-104">處理常式會定義自動播放的軟體部分。</span><span class="sxs-lookup"><span data-stu-id="09396-104">Handlers define the software portion of AutoPlay.</span></span> <span data-ttu-id="09396-105">它們定義軟體的圖示和易記名稱，以及元件物件模型 (COM) 元件具現化，以及如何初始化元件以回應事件。</span><span class="sxs-lookup"><span data-stu-id="09396-105">They define the software's icon and friendly name, as well as the Component Object Model (COM) component to instantiate and how to initialize the component in response to an event.</span></span> <span data-ttu-id="09396-106">特定事件的每個處理常式都會註冊為適當 **EventHandler** 索引鍵下的值。</span><span class="sxs-lookup"><span data-stu-id="09396-106">Each handler for a specific event registers as a value under the appropriate **EventHandler** key.</span></span> <span data-ttu-id="09396-107">當偵測到該事件時，系統會提示使用者從所有針對該事件註冊的處理常式清單中選擇處理常式。</span><span class="sxs-lookup"><span data-stu-id="09396-107">When that event is detected, the user is prompted to choose a handler from a list of all the handlers registered for that event.</span></span>

## <a name="instructions"></a><span data-ttu-id="09396-108">指示</span><span class="sxs-lookup"><span data-stu-id="09396-108">Instructions</span></span>


<span data-ttu-id="09396-109">處理常式及其相關聯的值會定義在 **AutoplayHandlers** \\ **處理常式** 索引鍵下。</span><span class="sxs-lookup"><span data-stu-id="09396-109">Handlers and their associated values are defined under the **AutoplayHandlers**\\**Handlers** key.</span></span> <span data-ttu-id="09396-110">子機碼會因系統是否可以直接讀取裝置內容，或裝置是否透過專屬介面提供內容給系統而有所不同。</span><span class="sxs-lookup"><span data-stu-id="09396-110">Subkeys differ depending on whether the system can read device contents directly or whether the device provides contents to the system through a proprietary interface.</span></span>

<span data-ttu-id="09396-111">下列範例顯示用於裝置的子機碼和值，例如數位攝影機或 mp3 播放程式，可透過專屬介面提供其內容給系統。</span><span class="sxs-lookup"><span data-stu-id="09396-111">The following example shows the subkeys and values that are used for a device, such as a digital video camera or .mp3 player, that provides its contents to the system through a proprietary interface.</span></span> <span data-ttu-id="09396-112">範例處理常式稱為 **MyHandler**。</span><span class="sxs-lookup"><span data-stu-id="09396-112">The example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> <span data-ttu-id="09396-113">雖然此範例顯示 ProgID 和類別識別碼 (CLSID) 值，但實際上這些值是互斥的，因此只會有一個或另一個。</span><span class="sxs-lookup"><span data-stu-id="09396-113">While the example shows both a ProgID and a class identifier (CLSID) value, in practice these values are mutually exclusive so that only one or the other is present.</span></span> <span data-ttu-id="09396-114">首選 ProgID 值。</span><span class="sxs-lookup"><span data-stu-id="09396-114">The ProgID value is preferred.</span></span> <span data-ttu-id="09396-115">無論使用哪種方式，都應該指向實 [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) 介面的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="09396-115">Whichever is used, it should point to a COM component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

 

<span data-ttu-id="09396-116">您可以輸入動作值做為常值（例如，如本範例所示的「播放音樂」），或輸入包含資源字串的檔案名。</span><span class="sxs-lookup"><span data-stu-id="09396-116">You can enter the Action value as a literal value, for example "Play music" as shown in this example, or as a file name with a resource string.</span></span> <span data-ttu-id="09396-117">您也可以輸入提供者值做為常值，或輸入包含資源字串的檔案名。</span><span class="sxs-lookup"><span data-stu-id="09396-117">You can also enter the Provider value as a literal value or as a file name with a resource string.</span></span> <span data-ttu-id="09396-118">自動播放會將動作值和提供者值與 "using" 這個字結合，以建立在 UI 中顯示的易記標題。</span><span class="sxs-lookup"><span data-stu-id="09396-118">AutoPlay combines the Action value and the Provider value with the word "using" to create a friendly caption that displays in the UI.</span></span> <span data-ttu-id="09396-119">在此範例中，產生的標題是「使用 Windows Media Player 播放音樂」。</span><span class="sxs-lookup"><span data-stu-id="09396-119">In the example, the resulting caption is "Play music using Windows Media Player."</span></span>

<span data-ttu-id="09396-120">DefaultIcon 值指向 .ico 檔案或二進位檔案中的資源。</span><span class="sxs-lookup"><span data-stu-id="09396-120">The DefaultIcon value points to either an .ico file or a resource in a binary file.</span></span> <span data-ttu-id="09396-121">如果二進位檔案名之後的數值是零或大於零，則它是該二進位檔案中圖示的索引值。</span><span class="sxs-lookup"><span data-stu-id="09396-121">If the numeric value that follows the binary file name is zero or greater, then it is the index value of the icon in that binary file.</span></span> <span data-ttu-id="09396-122">如果是負值，則它是圖示資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="09396-122">If it is a negative value, then it is the icon resource ID.</span></span> <span data-ttu-id="09396-123">建議使用負的索引值。</span><span class="sxs-lookup"><span data-stu-id="09396-123">Negative index values are recommended.</span></span> <span data-ttu-id="09396-124">.Ico 檔案的案例中不需要任何值。</span><span class="sxs-lookup"><span data-stu-id="09396-124">No value is necessary in the case of an .ico file.</span></span> <span data-ttu-id="09396-125">建議您在路徑中使用環境變數。</span><span class="sxs-lookup"><span data-stu-id="09396-125">It is recommended that you use environment variables in the path.</span></span>

<span data-ttu-id="09396-126">InitCmdLine 值會在呼叫任何其他方法之前，透過 [**IHWEventHandler：： Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) 方法原封不動地傳遞。</span><span class="sxs-lookup"><span data-stu-id="09396-126">The InitCmdLine value passes unaltered through the [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method before any other methods are called.</span></span>

<span data-ttu-id="09396-127">下列範例顯示可直接讀取的裝置（例如 CD-ROM 光碟機或其他卸載式磁片）所使用的子機碼和值。</span><span class="sxs-lookup"><span data-stu-id="09396-127">The following example shows the subkeys and values that are used for a device that can be read directly, such as a CD-ROM drive or other removable disk.</span></span> <span data-ttu-id="09396-128">同樣地，範例處理常式稱為 **MyHandler**。</span><span class="sxs-lookup"><span data-stu-id="09396-128">Again, the example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

<span data-ttu-id="09396-129">在此範例中，動作和提供者值會顯示為包含資源字串的檔案名，而不是常值，但它們參考的字串會以相同的方式使用。</span><span class="sxs-lookup"><span data-stu-id="09396-129">In this example, the Action and Provider values are shown as a file name with a resource string rather than literal values, but the strings that they reference are used in the same manner.</span></span> <span data-ttu-id="09396-130">它們會與 "using" 這個字結合，以形成易記的標題，如稍早所述。</span><span class="sxs-lookup"><span data-stu-id="09396-130">They are combined with the word "using" to form a friendly caption as explained earlier.</span></span>

<span data-ttu-id="09396-131">InvokeProgID 和 InvokeVerb 值會取代 CLSID、InitCmdLine 和 ProgID。</span><span class="sxs-lookup"><span data-stu-id="09396-131">InvokeProgID and InvokeVerb values replace CLSID, InitCmdLine, and ProgID.</span></span> <span data-ttu-id="09396-132">InvokeProgID 和 InvokeVerb 值符合在 **HKEY \_ 類別 \_ 根目錄** 下找到的索引鍵名稱，如下列登錄專案所示。</span><span class="sxs-lookup"><span data-stu-id="09396-132">The InvokeProgID and InvokeVerb values match key names that are found under **HKEY\_CLASSES\_ROOT**, as shown in the following registry entry.</span></span> <span data-ttu-id="09396-133">這組範例索引鍵會對應至稍早所述的特定處理常式範例。</span><span class="sxs-lookup"><span data-stu-id="09396-133">This set of example keys corresponds to the specific Handler example described earlier.</span></span>

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

<span data-ttu-id="09396-134">[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)函數會使用 CLSID 來執行適當的應用程式。</span><span class="sxs-lookup"><span data-stu-id="09396-134">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function uses the CLSID to implement the appropriate application.</span></span>

<span data-ttu-id="09396-135">在您以這兩種方式之一定義處理常式之後，您需要針對特定事件註冊處理常式。</span><span class="sxs-lookup"><span data-stu-id="09396-135">After you define the handler in either of these two ways, you need to register it for a specific event.</span></span> <span data-ttu-id="09396-136">若要這麼做，請將處理常式名稱提供為 **EventHandlers** 下該事件索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="09396-136">You do this by providing the handler name as a value for that event's key under **EventHandlers**.</span></span> <span data-ttu-id="09396-137">下列範例顯示如何將 **MyHandler** 註冊為 GenericVolumeArrival 事件的處理常式。</span><span class="sxs-lookup"><span data-stu-id="09396-137">The following example shows how to register **MyHandler** as a handler for the GenericVolumeArrival event.</span></span> <span data-ttu-id="09396-138">它沒有指派的資料值。</span><span class="sxs-lookup"><span data-stu-id="09396-138">It has no assigned data value.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a><span data-ttu-id="09396-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="09396-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09396-140">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="09396-140">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[<span data-ttu-id="09396-141">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="09396-141">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
