---
description: 定義原生 Wifi 自動設定服務所使用的 WLAN 設定檔。
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: WLAN_profile 架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112724"
---
# <a name="wlan_profile-schema"></a><span data-ttu-id="0af0f-103">WLAN \_ 設定檔架構</span><span class="sxs-lookup"><span data-stu-id="0af0f-103">WLAN\_profile Schema</span></span>

<span data-ttu-id="0af0f-104">WLAN \_ 設定檔架構會定義原生 Wifi 自動設定服務所使用的 wlan 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0af0f-104">The WLAN\_profile Schema defines a WLAN profile used by the Native Wifi AutoConfig service.</span></span>

<span data-ttu-id="0af0f-105">自動設定服務會接受來自群組原則代理程式的無線設定檔、指令碼介面 (**netsh**) 、使用者介面，或從 USB flash 設定介面。</span><span class="sxs-lookup"><span data-stu-id="0af0f-105">The AutoConfig service accepts wireless profiles from the Group Policy Agent, the scripting interface (**netsh**), the user interface, or from the USB flash configuration interface.</span></span>

<span data-ttu-id="0af0f-106">從這些系統之一收到的設定檔會對應至 WLAN \_ 設定檔架構，並儲存在設定檔存放區中。</span><span class="sxs-lookup"><span data-stu-id="0af0f-106">A profile received from one of these systems is mapped to the WLAN\_profile schema and stored in the profile store.</span></span> <span data-ttu-id="0af0f-107">您可以使用 netsh 命令或使用 API 元素（例如 [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)），從設定檔存放區匯出設定檔。</span><span class="sxs-lookup"><span data-stu-id="0af0f-107">Profiles can be exported from the profile store using netsh commands or using API elements such as [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span></span>

<span data-ttu-id="0af0f-108">WLAN 設定檔的根項目是 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="0af0f-108">The root element of a WLAN profile is the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span> <span data-ttu-id="0af0f-109">每個設定檔都只會有一個根項目。</span><span class="sxs-lookup"><span data-stu-id="0af0f-109">Each profile will have exactly one root element.</span></span> <span data-ttu-id="0af0f-110">**WLANProfile** 元素位於命名空間中 `https://www.microsoft.com/networking/WLAN/profile/v1` 。</span><span class="sxs-lookup"><span data-stu-id="0af0f-110">The **WLANProfile** element is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

<span data-ttu-id="0af0f-111">若要查看範例 WLAN 設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="0af0f-111">To view sample WLAN profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

-   [<span data-ttu-id="0af0f-112">WLAN \_ 設定檔架構元素</span><span class="sxs-lookup"><span data-stu-id="0af0f-112">WLAN\_profile Schema Elements</span></span>](wlan-profileschema-elements.md)
-   [<span data-ttu-id="0af0f-113">WLAN \_ 設定檔架構簡單類型</span><span class="sxs-lookup"><span data-stu-id="0af0f-113">WLAN\_profile Schema Simple Types</span></span>](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a><span data-ttu-id="0af0f-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="0af0f-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0af0f-115">[無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0af0f-115">[Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span></span>
</dt> </dl>

 

 
