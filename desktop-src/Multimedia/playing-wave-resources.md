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
ms.openlocfilehash: fd256d3c4cf07d6d2f57ba9c4d85c54b9d0e599f9382a5b8d9d1f3a0ef4705ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136757"
---
# <a name="playing-wave-resources"></a>播放 WAVE 資源

您可以使用 [**PlaySound**](/previous-versions//dd743680(v=vs.85)) 函式來播放儲存為資源的音效。 雖然您也可以使用 [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) 函式來進行這項工作，但是 **sndPlaySound** 需要您尋找、載入、鎖定、解除鎖定和釋放資源; **PlaySound** 會使用一行程式碼來達到上述所有的。

## <a name="playsound-example"></a>PlaySound 範例


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>sndPlaySound 範例

OPERATORS.SND \_ 記憶體旗標表示 *lpszSoundName* 參數是 WAVE 檔案之記憶體中影像的指標。 若要將 WAVE 檔案納入為應用程式中的資源，請將下列專案加入至應用程式的資源腳本 (。RC) 檔。


```C++
soundName WAVE c:\sounds\bells.wav 
```



名稱 *soundName* 是您提供用來參考此 WAVE 資源之名稱的預留位置。 WAVE 資源的載入和存取方式就像其他應用程式定義的 Windows 資源一樣。 下列範例中的 PlayResource 函式會播放指定的 WAVE 資源。


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



若要使用此函式來播放 WAVE 資源，請將包含資源名稱之字串的指標傳遞至函式，如下列範例所示。


```C++
PlayResource("soundName"); 
```



 

 