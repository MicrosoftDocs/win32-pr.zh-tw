---
description: 指定行動寬頻裝置是否會自動連接到網路。
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: AutoConnectOnInternet (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191443"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a><span data-ttu-id="6863a-103">AutoConnectOnInternet (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="6863a-103">AutoConnectOnInternet (MBNProfile) Element</span></span>

<span data-ttu-id="6863a-104">**AutoConnectOnInternet (MBNProfile)** 元素會指定行動寬頻裝置是否會自動連接到網路。</span><span class="sxs-lookup"><span data-stu-id="6863a-104">The **AutoConnectOnInternet (MBNProfile)** element specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="6863a-105">如果設定為 **FALSE**，則如果系統有其他可用的網路連線，就不會使用行動寬頻服務的自動連接邏輯。</span><span class="sxs-lookup"><span data-stu-id="6863a-105">If set to **FALSE**, then the Mobile Broadband service's auto connect logic will not be used if there is any other network connectivity available to the system.</span></span> <span data-ttu-id="6863a-106">如果設定為 **TRUE**，行動寬頻服務會根據 [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) 元素中定義的自動連線設定，嘗試自動將裝置連線到網路。</span><span class="sxs-lookup"><span data-stu-id="6863a-106">If set to **TRUE**, then the Mobile Broadband service will try to automatically connect the device to the network based on the auto connection setting defined in the [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) element.</span></span>

<span data-ttu-id="6863a-107">**Windows 8 和更新版本：** 此元素已被取代。</span><span class="sxs-lookup"><span data-stu-id="6863a-107">**Windows 8 and later:** This element is deprecated.</span></span> <span data-ttu-id="6863a-108">請改用 [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) 方法，將 *property* 參數設定為 [ **wcm \_ global Property 的 \_ \_ 最小化 \_ 原則** ]。</span><span class="sxs-lookup"><span data-stu-id="6863a-108">Use the [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) method with the *Property* parameter set to **wcm\_global\_property\_minimize\_policy** instead.</span></span>

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

<span data-ttu-id="6863a-109">**AutoConnectOnInternet** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="6863a-109">The **AutoConnectOnInternet** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6863a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6863a-110">Requirements</span></span>



| <span data-ttu-id="6863a-111">需求</span><span class="sxs-lookup"><span data-stu-id="6863a-111">Requirement</span></span> | <span data-ttu-id="6863a-112">值</span><span class="sxs-lookup"><span data-stu-id="6863a-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="6863a-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6863a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6863a-114">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6863a-114">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="6863a-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6863a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6863a-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="6863a-116">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="6863a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6863a-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="6863a-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="6863a-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6863a-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="6863a-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="6863a-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="6863a-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6863a-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="6863a-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

