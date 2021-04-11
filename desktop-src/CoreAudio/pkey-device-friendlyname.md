---
description: PKEY \_ Device \_ FriendlyName 屬性包含端點裝置的易記名稱 (例如，&\# 0034; (XYZ 音訊介面卡) &\# 0034; ) 的喇叭。
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: 'PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab8b8f30e04ae66356fb0910e3767d74b7b697a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846952"
---
# <a name="pkey_device_friendlyname"></a><span data-ttu-id="f18eb-103">PKEY \_ 裝置 \_ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f18eb-103">PKEY\_Device\_FriendlyName</span></span>

<span data-ttu-id="f18eb-104">**PKEY \_ Device \_ FriendlyName** 屬性包含端點裝置的易記名稱 (例如「喇叭 (XYZ 音訊介面卡) 」 ) 。</span><span class="sxs-lookup"><span data-stu-id="f18eb-104">The **PKEY\_Device\_FriendlyName** property contains the friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span>

<span data-ttu-id="f18eb-105">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="f18eb-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="f18eb-106">**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含端點裝置的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="f18eb-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the friendly name of the endpoint device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f18eb-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="f18eb-107">Requirements</span></span>



| <span data-ttu-id="f18eb-108">需求</span><span class="sxs-lookup"><span data-stu-id="f18eb-108">Requirement</span></span> | <span data-ttu-id="f18eb-109">值</span><span class="sxs-lookup"><span data-stu-id="f18eb-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f18eb-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f18eb-110">Minimum supported client</span></span><br/> | <span data-ttu-id="f18eb-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f18eb-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f18eb-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f18eb-112">Minimum supported server</span></span><br/> | <span data-ttu-id="f18eb-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f18eb-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="f18eb-114">標頭</span><span class="sxs-lookup"><span data-stu-id="f18eb-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="f18eb-115"><dt>Functiondiscoverykeys \_ devpkey。h</dt></span><span class="sxs-lookup"><span data-stu-id="f18eb-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f18eb-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f18eb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18eb-117">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="f18eb-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="f18eb-118">裝置內容</span><span class="sxs-lookup"><span data-stu-id="f18eb-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




