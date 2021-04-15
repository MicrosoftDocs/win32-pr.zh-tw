---
title: 播放 WAVE 資源
description: 播放 WAVE 資源
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- 波形音訊，播放 WAVE 資源
- 輔助音訊，播放 WAVE 資源
- 播放 WAVE 資源
- PlaySound 函式，播放 WAVE 資源
- sndPlaySound 函式
- PlaySound 函式，相較于 sndPlaySound 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463120"
---
# <a name="playing-wave-resources"></a><span data-ttu-id="9b639-109">播放 WAVE 資源</span><span class="sxs-lookup"><span data-stu-id="9b639-109">Playing WAVE Resources</span></span>

<span data-ttu-id="9b639-110">您可以使用 [**PlaySound**](/previous-versions//dd743680(v=vs.85)) 函式來播放儲存為資源的音效。</span><span class="sxs-lookup"><span data-stu-id="9b639-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play a sound that is stored as a resource.</span></span> <span data-ttu-id="9b639-111">雖然您也可以使用 [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) 函式來進行這項工作，但是 **sndPlaySound** 需要您尋找、載入、鎖定、解除鎖定和釋放資源; **PlaySound** 會使用一行程式碼來達到上述所有的。</span><span class="sxs-lookup"><span data-stu-id="9b639-111">Although this is also possible using the [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function, **sndPlaySound** requires that you find, load, lock, unlock, and free the resource; **PlaySound** achieves all of this with a single line of code.</span></span>

## <a name="playsound-example"></a><span data-ttu-id="9b639-112">PlaySound 範例</span><span class="sxs-lookup"><span data-stu-id="9b639-112">PlaySound Example</span></span>


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a><span data-ttu-id="9b639-113">sndPlaySound 範例</span><span class="sxs-lookup"><span data-stu-id="9b639-113">sndPlaySound Example</span></span>

<span data-ttu-id="9b639-114">OPERATORS.SND \_ 記憶體旗標表示 *lpszSoundName* 參數是 WAVE 檔案之記憶體中影像的指標。</span><span class="sxs-lookup"><span data-stu-id="9b639-114">The SND\_MEMORY flag indicates that the *lpszSoundName* parameter is a pointer to an in-memory image of the WAVE file.</span></span> <span data-ttu-id="9b639-115">若要將 WAVE 檔案納入為應用程式中的資源，請將下列專案加入至應用程式的資源腳本 (。RC) 檔。</span><span class="sxs-lookup"><span data-stu-id="9b639-115">To include a WAVE file as a resource in an application, add the following entry to the application's resource script (.RC) file.</span></span>


```C++
soundName WAVE c:\sounds\bells.wav 
```



<span data-ttu-id="9b639-116">名稱 *soundName* 是您提供用來參考此 WAVE 資源之名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="9b639-116">The name *soundName* is a placeholder for a name that you supply to refer to this WAVE resource.</span></span> <span data-ttu-id="9b639-117">WAVE 資源的載入和存取方式就像其他應用程式定義的 Windows 資源一樣。</span><span class="sxs-lookup"><span data-stu-id="9b639-117">WAVE resources are loaded and accessed just like other application-defined Windows resources.</span></span> <span data-ttu-id="9b639-118">下列範例中的 PlayResource 函式會播放指定的 WAVE 資源。</span><span class="sxs-lookup"><span data-stu-id="9b639-118">The PlayResource function in the following example plays a specified WAVE resource.</span></span>


```C++
BOOL PlayResource(LPSTR lpName) 
{ 
    BOOL bRtn; 
    LPSTR lpRes; 
    HANDLE hResInfo, hRes; 
 
    // Find the WAVE resource. 
 
    hResInfo = FindResource(hInst, lpName, "WAVE"); 
    if (hResInfo == NULL) 
        return FALSE; 
 
    // Load the WAVE resource. 
 
    hRes = LoadResource(hInst, hResInfo); 
    if (hRes == NULL) 
        return FALSE; 
 
    // Lock the WAVE resource and play it. 
 
    lpRes = LockResource(hRes); 
    if (lpRes != NULL) { 
        bRtn = sndPlaySound(lpRes, SND_MEMORY | SND_SYNC | 
            SND_NODEFAULT); 
        UnlockResource(hRes); 
    } 
    else 
        bRtn = 0; 
 
    // Free the WAVE resource and return success or failure. 
 
    FreeResource(hRes); 
    return bRtn; 
} 
```



<span data-ttu-id="9b639-119">若要使用此函式來播放 WAVE 資源，請將包含資源名稱之字串的指標傳遞至函式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="9b639-119">To play a WAVE resource by using this function, pass to the function a pointer to a string containing the name of the resource, as shown in the following example.</span></span>


```C++
PlayResource("soundName"); 
```



 

 