---
description: 指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: userBasedVirtualLan (singleSignOn) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113616"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a><span data-ttu-id="b2094-103">userBasedVirtualLan (singleSignOn) 元素</span><span class="sxs-lookup"><span data-stu-id="b2094-103">userBasedVirtualLan (singleSignOn) Element</span></span>

<span data-ttu-id="b2094-104">UserBasedVirtualLan (singleSignOn) 元素會指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。</span><span class="sxs-lookup"><span data-stu-id="b2094-104">The userBasedVirtualLan (singleSignOn) element specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="b2094-105">有些網路存取伺服器 (NAS) 裝置會在使用者驗證之後變更 VLAN。</span><span class="sxs-lookup"><span data-stu-id="b2094-105">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="b2094-106">當 userBasedVirtualLan 為 TRUE 時，NAS 可能會在使用者驗證之後變更裝置的 VLAN。</span><span class="sxs-lookup"><span data-stu-id="b2094-106">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span>

<span data-ttu-id="b2094-107">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="b2094-107">This element is optional.</span></span> <span data-ttu-id="b2094-108">當設定檔中未指定 userBasedVirtualLan 時，會使用 FALSE 值。</span><span class="sxs-lookup"><span data-stu-id="b2094-108">When userBasedVirtualLan is not specified in a profile, a value of FALSE is used.</span></span>

<span data-ttu-id="b2094-109">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="b2094-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="b2094-110">**UserBasedVirtualLan** 元素是由 [**singleSignOn**](onexschema-singlesignon-onex-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="b2094-110">The **userBasedVirtualLan** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2094-111">備註</span><span class="sxs-lookup"><span data-stu-id="b2094-111">Remarks</span></span>

<span data-ttu-id="b2094-112">您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。</span><span class="sxs-lookup"><span data-stu-id="b2094-112">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="b2094-113">如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="b2094-113">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2094-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2094-114">Requirements</span></span>



| <span data-ttu-id="b2094-115">需求</span><span class="sxs-lookup"><span data-stu-id="b2094-115">Requirement</span></span> | <span data-ttu-id="b2094-116">值</span><span class="sxs-lookup"><span data-stu-id="b2094-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2094-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2094-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b2094-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2094-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2094-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2094-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b2094-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2094-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2094-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2094-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2094-122">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b2094-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b2094-123">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="b2094-123">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="b2094-124">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b2094-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b2094-125">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="b2094-125">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
