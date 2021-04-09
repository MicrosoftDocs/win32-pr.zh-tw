---
description: PKEY \_ Device \_ DeviceDesc 屬性包含端點裝置的裝置描述 (例如 &\# 0034;喇叭&\# 0034; ) 。
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: 'PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846960"
---
# <a name="pkey_device_devicedesc"></a><span data-ttu-id="c8f25-103">PKEY \_ 裝置 \_ DeviceDesc</span><span class="sxs-lookup"><span data-stu-id="c8f25-103">PKEY\_Device\_DeviceDesc</span></span>

<span data-ttu-id="c8f25-104">**PKEY \_ Device \_ DeviceDesc** 屬性包含端點裝置的裝置描述 (例如「喇叭」 ) 。</span><span class="sxs-lookup"><span data-stu-id="c8f25-104">The **PKEY\_Device\_DeviceDesc** property contains the device description of the endpoint device (for example, "Speakers").</span></span>

<span data-ttu-id="c8f25-105">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="c8f25-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="c8f25-106">**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 終止的寬字元字串，其中包含裝置描述。</span><span class="sxs-lookup"><span data-stu-id="c8f25-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the device description.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f25-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8f25-107">Requirements</span></span>



| <span data-ttu-id="c8f25-108">需求</span><span class="sxs-lookup"><span data-stu-id="c8f25-108">Requirement</span></span> | <span data-ttu-id="c8f25-109">值</span><span class="sxs-lookup"><span data-stu-id="c8f25-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f25-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8f25-110">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f25-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8f25-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c8f25-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8f25-112">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f25-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8f25-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="c8f25-114">標頭</span><span class="sxs-lookup"><span data-stu-id="c8f25-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8f25-115"><dt>Functiondiscoverykeys \_ devpkey。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8f25-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f25-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8f25-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f25-117">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="c8f25-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="c8f25-118">裝置內容</span><span class="sxs-lookup"><span data-stu-id="c8f25-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




