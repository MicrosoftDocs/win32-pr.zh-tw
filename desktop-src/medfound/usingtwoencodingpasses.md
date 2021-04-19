---
description: 雙通編碼可用於常數位元速率 (CBR) 和變數位元速率 (VBR) 編碼與某些 Windows Media 編解碼器。
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: '使用 Two-Pass 編碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969295"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a><span data-ttu-id="751b9-103">使用 Two-Pass 編碼 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="751b9-103">Using Two-Pass Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="751b9-104">雙通編碼可用於常數位元速率 (CBR) 和變數位元速率 (VBR) 編碼與某些 Windows Media 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="751b9-104">Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs.</span></span> <span data-ttu-id="751b9-105">您可以藉由抓取 [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) 屬性，找到編解碼器所支援的最大編碼傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="751b9-105">You can find the maximum number of encoding passes supported by a codec by retrieving the [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) property.</span></span> <span data-ttu-id="751b9-106">所有編解碼器皆不支援兩個以上的傳遞。</span><span class="sxs-lookup"><span data-stu-id="751b9-106">None of the codecs supports more than two passes.</span></span> <span data-ttu-id="751b9-107">將 [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) 屬性設定為2，以將 sql-dmo 設定為使用兩個階段。</span><span class="sxs-lookup"><span data-stu-id="751b9-107">Configure the DMO to use two passes by setting the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2.</span></span>

<span data-ttu-id="751b9-108">您可以一次將範例傳遞給編碼器，就像在單一階段模式中一樣。</span><span class="sxs-lookup"><span data-stu-id="751b9-108">Deliver the samples to the encoder DMO one at a time, as you would in a one-pass mode.</span></span> <span data-ttu-id="751b9-109">當您處理前置處理行程的輸入範例時，對 [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) 或 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 的呼叫會傳回 **\_ FALSE**，表示不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="751b9-109">When you process the input samples for your preprocessing pass, the calls to [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) or [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will return **S\_FALSE**, to indicate that no output is produced.</span></span>

<span data-ttu-id="751b9-110">在第一) 次傳遞 (的最後一個輸入第一次處理之後，您必須設定 [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) 屬性，以通知編解碼器下一個輸入所處理的是第二次的輸入。</span><span class="sxs-lookup"><span data-stu-id="751b9-110">At the end of the first pass (after the last input is processed for the first time), you then must set the [MFPKEY\_ENDOFPASS](mfpkey-endofpassproperty.md) property to notify the codec that the next input processed is the first input of the second pass.</span></span> <span data-ttu-id="751b9-111">這個屬性不需要任何值，因此您應該使用空白的 **VARIANT** 結構。</span><span class="sxs-lookup"><span data-stu-id="751b9-111">No value is required for this property, so you should use an empty **VARIANT** structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="751b9-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="751b9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="751b9-113">Windows Media 轉碼器</span><span class="sxs-lookup"><span data-stu-id="751b9-113">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 
