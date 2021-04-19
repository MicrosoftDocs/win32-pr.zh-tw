---
description: PKEY \_ AudioEndpoint \_ Association 屬性會將核心串流 (KS) 釘選類別與音訊端點裝置產生關聯。
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: 'PKEY_AudioEndpoint_Association (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001323"
---
# <a name="pkey_audioendpoint_association"></a><span data-ttu-id="c971c-103">PKEY \_ AudioEndpoint \_ 關聯</span><span class="sxs-lookup"><span data-stu-id="c971c-103">PKEY\_AudioEndpoint\_Association</span></span>

<span data-ttu-id="c971c-104">**PKEY \_ AudioEndpoint \_ Association** 屬性會將核心串流 (KS) 釘選類別與音訊端點裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c971c-104">The **PKEY\_AudioEndpoint\_Association** property associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span> <span data-ttu-id="c971c-105">安裝音訊介面卡的 .inf 檔案會將釘選類別指派給介面卡中的每個 KS pin。</span><span class="sxs-lookup"><span data-stu-id="c971c-105">The .inf file that installs an audio adapter assigns a pin category to each KS pin in the adapter.</span></span> <span data-ttu-id="c971c-106">介面卡裝置上的 KS pin 代表音訊串流進入或離開裝置的時間點。</span><span class="sxs-lookup"><span data-stu-id="c971c-106">A KS pin on an adapter device represents the point at which an audio stream enters or leaves the device.</span></span> <span data-ttu-id="c971c-107">Pin 類別是 GUID，可指定由 KS 釘選執行的函式類型。</span><span class="sxs-lookup"><span data-stu-id="c971c-107">A pin category is a GUID that specifies the type of function performed by a KS pin.</span></span> <span data-ttu-id="c971c-108">例如，標頭檔 Ksmedia 會定義釘選類別 GUID KSNODETYPE 麥克風， \_ 以表示連接至麥克風的 ks pin，以及 KSNODETYPE \_ 耳機以表示連接到耳機的 ks pin。</span><span class="sxs-lookup"><span data-stu-id="c971c-108">For example, header file Ksmedia.h defines pin-category GUID KSNODETYPE\_MICROPHONE to indicate a KS pin that connects to a microphone, and KSNODETYPE\_HEADPHONES to indicate a KS pin that connects to headphones.</span></span> <span data-ttu-id="c971c-109">如需詳細資訊，請參閱 Windows DDK 檔中的 pin 分類屬性說明。</span><span class="sxs-lookup"><span data-stu-id="c971c-109">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="c971c-110">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="c971c-110">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="c971c-111">**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含一個 KS 釘選類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="c971c-111">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a KS pin category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="c971c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c971c-112">Requirements</span></span>



| <span data-ttu-id="c971c-113">需求</span><span class="sxs-lookup"><span data-stu-id="c971c-113">Requirement</span></span> | <span data-ttu-id="c971c-114">值</span><span class="sxs-lookup"><span data-stu-id="c971c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c971c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c971c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c971c-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c971c-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c971c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c971c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c971c-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c971c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c971c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c971c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c971c-120"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c971c-120"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c971c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c971c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c971c-122">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="c971c-122">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="c971c-123">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="c971c-123">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




