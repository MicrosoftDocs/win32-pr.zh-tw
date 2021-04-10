---
description: PKEY \_ AudioEndpoint \_ JackSubType 屬性包含音訊端點裝置的輸出類別 GUID。
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: 'PKEY_AudioEndpoint_JackSubType (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111321"
---
# <a name="pkey_audioendpoint_jacksubtype"></a><span data-ttu-id="f0610-103">PKEY \_ AudioEndpoint \_ JackSubType</span><span class="sxs-lookup"><span data-stu-id="f0610-103">PKEY\_AudioEndpoint\_JackSubType</span></span>

<span data-ttu-id="f0610-104">**PKEY \_ AudioEndpoint \_ JackSubType** 屬性包含音訊端點裝置的輸出類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="f0610-104">The **PKEY\_AudioEndpoint\_JackSubType** property contains an output category GUID for an audio endpoint device.</span></span> <span data-ttu-id="f0610-105">標頭檔 Ksmedia 會定義 Guid;每個 GUID 都會指定連接的類型。</span><span class="sxs-lookup"><span data-stu-id="f0610-105">The header file Ksmedia.h defines the GUIDs; each GUID specifies the type of connection.</span></span> <span data-ttu-id="f0610-106">這些 Guid 也有相關聯的釘選類別。</span><span class="sxs-lookup"><span data-stu-id="f0610-106">These GUIDs also have associated pin categories.</span></span> <span data-ttu-id="f0610-107">例如，標頭檔 Ksmedia 會針對顯示埠定義 GUID **KSNODETYPE \_ DISPLAYPORT \_ 介面** ，此介面會連接到 GUID **PINNAME \_ DISPLAYPORT \_ OUT** 所定義的 KS pin。</span><span class="sxs-lookup"><span data-stu-id="f0610-107">For example, header file Ksmedia.h defines the GUID **KSNODETYPE\_DISPLAYPORT\_INTERFACE** for a display port that connects with the KS pin defined by the GUID **PINNAME\_DISPLAYPORT\_OUT**.</span></span>

<span data-ttu-id="f0610-108">如需詳細資訊，請參閱 Windows DDK 檔中的 pin 分類屬性說明。</span><span class="sxs-lookup"><span data-stu-id="f0610-108">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="f0610-109">**PROPVARIANT** 結構的 **vt** 成員會設定為 **vt \_ LPWSTR**。</span><span class="sxs-lookup"><span data-stu-id="f0610-109">The **vt** member of the **PROPVARIANT** structure is set to **VT\_LPWSTR**.</span></span>

<span data-ttu-id="f0610-110">**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 終止的寬字元字串，其中包含分類 GUID。</span><span class="sxs-lookup"><span data-stu-id="f0610-110">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0610-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0610-111">Requirements</span></span>



| <span data-ttu-id="f0610-112">需求</span><span class="sxs-lookup"><span data-stu-id="f0610-112">Requirement</span></span> | <span data-ttu-id="f0610-113">值</span><span class="sxs-lookup"><span data-stu-id="f0610-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0610-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0610-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f0610-115">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0610-115">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f0610-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0610-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f0610-117">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0610-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0610-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f0610-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0610-119"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0610-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0610-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0610-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0610-121">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="f0610-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="f0610-122">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="f0610-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




