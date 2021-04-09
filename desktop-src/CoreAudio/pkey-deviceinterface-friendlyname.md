---
description: PKEY \_ DeviceInterface \_ FriendlyName 屬性。
ms.assetid: beef2153-489f-4ff5-a161-b4e2cd4ac1fa
title: 'PKEY_DeviceInterface_FriendlyName (Functiondiscoverykeys \_ devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7590e9254e336bf9dbfe0fdeb3349bf19c0b8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110005"
---
# <a name="pkey_deviceinterface_friendlyname"></a><span data-ttu-id="5a1f8-103">PKEY \_ DeviceInterface \_ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5a1f8-103">PKEY\_DeviceInterface\_FriendlyName</span></span>

<span data-ttu-id="5a1f8-104">**PKEY \_ DeviceInterface \_ FriendlyName** 屬性包含端點裝置所連接之音訊介面卡的易記名稱 (例如「XYZ 音訊介面卡」 ) 。</span><span class="sxs-lookup"><span data-stu-id="5a1f8-104">The **PKEY\_DeviceInterface\_FriendlyName** property contains the friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span>

<span data-ttu-id="5a1f8-105">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="5a1f8-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="5a1f8-106">**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5a1f8-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the friendly name.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a1f8-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a1f8-107">Requirements</span></span>



| <span data-ttu-id="5a1f8-108">需求</span><span class="sxs-lookup"><span data-stu-id="5a1f8-108">Requirement</span></span> | <span data-ttu-id="5a1f8-109">值</span><span class="sxs-lookup"><span data-stu-id="5a1f8-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1f8-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a1f8-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1f8-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a1f8-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5a1f8-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a1f8-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1f8-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a1f8-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="5a1f8-114">標頭</span><span class="sxs-lookup"><span data-stu-id="5a1f8-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a1f8-115"><dt>Functiondiscoverykeys \_ devpkey。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a1f8-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a1f8-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a1f8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1f8-117">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="5a1f8-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="5a1f8-118">裝置內容</span><span class="sxs-lookup"><span data-stu-id="5a1f8-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




