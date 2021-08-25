---
title: 產生對話方塊來選取特定類型的格式
description: 產生對話方塊來選取特定類型的格式
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- 音訊壓縮管理員 (的) 、產生對話方塊
- " (音效壓縮管理員) 、產生對話方塊"
- 進行中的範例，產生對話方塊
- 產生對話方塊
- acmFormatChoose 函式
- 音訊壓縮管理員 (的) ，選取格式類型
- " (音效壓縮管理員) ，選取格式類型"
- 進行中的範例，選取格式類型
- 選取格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f25f7b196fcb9462a3b61dd8e351ed75276c7df7bf46cec233dd8eac7deda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037648"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a>產生對話方塊來選取特定類型的格式

您可能會想要讓使用者在對話方塊中，從受限制的格式清單中選取格式。 限制可能會限制通道的數目、取樣率、波形-音訊格式標記，或每個樣本的位數數目。 在上述所有情況下，您都可以使用 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose)函數來產生清單，設定 [**AcmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)結構的 **fdwEnum** 和 **pwfxEnum** 成員。 下列範例將說明此程序。


```C++
MMRESULT            mmr; 
ACMFORMATCHOOSE     afc; 
WAVEFORMATEX        wfxSelection; 
WAVEFORMATEX        wfxEnum; 
 
// Initialize the ACMFORMATCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfx        = &wfxSelection;    // wfx to receive selection 
afc.cbwfx       = sizeof(wfxSelection); 
afc.pszTitle    = TEXT("16 Bit PCM Selection"); 
 
//  Request that all 16-bit PCM formats be displayed for the user 
//  to select from. 
memset(&wfxEnum, 0, sizeof(wfxEnum)); 
wfxEnum.wFormatTag = WAVE_FORMAT_PCM; 
wfxEnum.wBitsPerSample = 16; 
afc.fdwEnum = ACM_FORMATENUMF_WFORMATTAG | 
    ACM_FORMATENUMF_WBITSPERSAMPLE; 
afc.pwfxEnum = &wfxEnum; 
mmr = acmFormatChoose(&afc); 
if ((MMSYSERR_NOERROR != mmr) && (ACMERR_CANCELED != mmr)) 
{ 
    // There was a fatal error in bringing up the list 
    // dialog box (probably invalid input parameters). 
} 
 
```



 

 




