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
ms.openlocfilehash: bfc5d73d1b03f22923e6001d65898c05e2bd853e
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/27/2020
ms.locfileid: "104314433"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a><span data-ttu-id="7b53a-112">產生對話方塊來選取特定類型的格式</span><span class="sxs-lookup"><span data-stu-id="7b53a-112">Producing a Dialog Box for Selecting a Specific Type of Format</span></span>

<span data-ttu-id="7b53a-113">您可能會想要讓使用者在對話方塊中，從受限制的格式清單中選取格式。</span><span class="sxs-lookup"><span data-stu-id="7b53a-113">You might want an application to allow the user to select a format from a restricted list of formats in a dialog box.</span></span> <span data-ttu-id="7b53a-114">限制可能會限制通道的數目、取樣率、波形-音訊格式標記，或每個樣本的位數數目。</span><span class="sxs-lookup"><span data-stu-id="7b53a-114">Restrictions might limit the number of channels, the sampling rate, the waveform-audio format tag, or the number of bits per sample.</span></span> <span data-ttu-id="7b53a-115">在上述所有情況下，您都可以使用 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose)函數來產生清單，設定 [**AcmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)結構的 **fdwEnum** 和 **pwfxEnum** 成員。</span><span class="sxs-lookup"><span data-stu-id="7b53a-115">In all of these cases, you can generate the list by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, setting the **fdwEnum** and **pwfxEnum** members of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span> <span data-ttu-id="7b53a-116">下列範例將說明此程序。</span><span class="sxs-lookup"><span data-stu-id="7b53a-116">The following example illustrates this process.</span></span>


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



 

 




